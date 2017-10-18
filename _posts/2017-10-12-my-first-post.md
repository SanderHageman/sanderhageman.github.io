---
layout: post
title: "My First Post"
date: 2017-10-12
thumbnail: "/assets/first.jpg"
subtitle: "Testing subtitle and code snippet"
---


First Post Test


{% highlight cpp linenos %}
// ----------------------------
// ----Internal Includes----
// ----------------------------
#include "SystemClass.h"

#include "InputClass.h"
#include "GraphicsClass.h"

SystemClass::SystemClass(LPCWSTR AppName, HINSTANCE hInst) :
	m_applicationName(AppName),
	m_hInstance(hInst){
	int screenHeight = 0, 
		screenWidth = 0;

	// Initialize win api
	InitializeWindows(screenWidth, screenHeight);


	assert(m_Graphics->Initialize(screenWidth, screenHeight, m_hWnd));
}

int SystemClass::Run() {
	MSG msg{};
	bool done = false, 
		result = false;

	while (!done) {
		if (PeekMessage(&msg, nullptr, 0, 0, PM_REMOVE)) {
			TranslateMessage(&msg);
			DispatchMessage(&msg);
		}

		if (msg.message == WM_QUIT) {
			done = true;
		}
		else {
			result = Frame();
			if (!result) {
				done = true;
			}
		}
	}

	return 0;
}

bool SystemClass::Frame() {
	if (m_Input->IsKeyDown(VK_ESCAPE)) {
		return false;
	}

	if (!m_Graphics->Frame()) {
		return false;
	}

	return true;
}

void SystemClass::InitializeWindows(int& sWidth, int& sHeight) {
	// Get external pointer to me
	ApplicationHandle = this;

	// Setup windows class
	WNDCLASSEX windowClass{};
	windowClass.cbSize = sizeof(WNDCLASSEX);
	windowClass.style = CS_HREDRAW | CS_VREDRAW;
	windowClass.lpfnWndProc = WndProc;
	windowClass.hInstance = m_hInstance;
	windowClass.hCursor = LoadCursor(NULL, IDC_ARROW);
	windowClass.lpszClassName = m_applicationName;
	RegisterClassEx(&windowClass);

	sWidth = 800, sHeight = 600;
	RECT windowRect = { 0,0,sWidth,sHeight };
	AdjustWindowRect(&windowRect, WS_OVERLAPPEDWINDOW, FALSE);

	m_hWnd = CreateWindow(
		windowClass.lpszClassName,
		m_applicationName,
		WS_OVERLAPPEDWINDOW,
		CW_USEDEFAULT,
		CW_USEDEFAULT,
		windowRect.right - windowRect.left,
		windowRect.bottom - windowRect.top,
		nullptr,
		nullptr,
		m_hInstance,
		nullptr
	);

	ShowWindow(m_hWnd, SW_SHOW);

	return;
}

LRESULT CALLBACK WndProc(HWND hwnd, UINT umsg, WPARAM wparam, LPARAM lparam) {
	switch (umsg)
	{
	case WM_DESTROY:
	case WM_CLOSE: {
		PostQuitMessage(0);
		return 0;
	}
	default: {
		return ApplicationHandle->MessageHandler(hwnd, umsg, wparam, lparam);
	}
	}
}

LRESULT CALLBACK SystemClass::MessageHandler(HWND hwnd, UINT umsg, WPARAM wparam, LPARAM lparam) {
	switch (umsg)
	{
	case WM_KEYDOWN: {
		m_Input->KeyDown(static_cast<unsigned int>(wparam));
		return 0;
	}
	case WM_KEYUP: {
		m_Input->KeyUp(static_cast<unsigned int>(wparam));
		return 0;
	}

	default: {
		return DefWindowProc(hwnd, umsg, wparam, lparam);
	}
	}
}
{% endhighlight %}

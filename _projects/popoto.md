---
layout: post
published: false
title: "Popoto Prototype"
subtitle: "Third person hack and slash game made in Unreal Engine 4 for PS4."
info: "Einar is a third person hack and slash game made in Unreal Engine 4. The game is based on Norse mythology and was developed for the PS4 by a team of more than 30 students. In the game the player has to use a multitude of 'god-powers' to deafeat his enemies; the draugr."
date: 2017-09-01
projectDate: "September 2017 - July 2018"
achievement: true
role: Engine- and PS4 Programmer
contributions:
  - name: Playstation 4
    shortdesc: "Compatibility with the PS4"
    desc: "During the development of the game I was responsible for making the game compatible with the PS4, I had to use the PS4 development tools for performance profiling and graphical debugging."
  - name: Unreal Engine 4
    shortdesc: "Editing UE4 source for PS4 support"
    desc: "Although Unreal Engine 4 offers Playstation 4 support out of the box, it's not available out of the box. I had to rebuild the complete engine using the PS4 binaries and public UE4 source. I also enhanced small parts of the UE4 source to make creating builds for the PS4 easier."
  - name: Prototyping
    shortdesc: "Rapid prototyping"
    desc: "At the start of the project I was involved with rapidly prototyping a multitude of mechanics."
---
<div class="galleryOverlay">
  {% include gallery.html prefix="/popotoPics/" %}
</div>

```cpp
/*
  This code snippet is part of my Popoto Prototype project and it is responsible for rendering all the required models to the shadow maps.
*/
void D3DClass::RenderSceneToShadowMap(const ShadowCaster& sc) {
	const auto& shadowMap = sc.shadowMap;

	m_commandList->RSSetViewports(1, &shadowMap->m_viewport);
	m_commandList->RSSetScissorRects(1, &shadowMap->m_scissorRect);

	{
		const auto transitionBarrier = CD3DX12_RESOURCE_BARRIER::Transition(
			shadowMap->Resource().Get(),
			D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE,
			D3D12_RESOURCE_STATE_DEPTH_WRITE
		);

		m_commandList->ResourceBarrier(1, &transitionBarrier);
	}

	const UINT numDSVs = sc.shadowMap->m_cubemap ? 6U : 1U;

	for (UINT i = 0U; i < numDSVs; ++i) {
		m_lightPassConstantBufferData[m_frameIndex][shadowMap->m_id + i] = { sc.projMatrix * sc.transform[i]->GetViewMatrix() };

		const auto lightPassOffset =
			m_lightPassConstantBufferData[m_frameIndex]->GetAlignedOffset(shadowMap->m_id + i);

		const D3D12_GPU_VIRTUAL_ADDRESS mainPassBaseOffset =
			m_mainPassConstantBufferResource[m_frameIndex]->GetGPUVirtualAddress() +
			m_mainPassConstantBufferData[m_frameIndex]->GetAlignedOffset(1);

		m_commandList->SetGraphicsRootConstantBufferView(
			RootParameterIndices::Light,
			mainPassBaseOffset + lightPassOffset);

		const auto dsvCPUDescriptorHandle = shadowMap->GetDSV(i);

		m_commandList->ClearDepthStencilView(dsvCPUDescriptorHandle,
			D3D12_CLEAR_FLAG_DEPTH | D3D12_CLEAR_FLAG_STENCIL,
			1.0f, 0UI8, 0U, nullptr);

		m_commandList->OMSetRenderTargets(0U, NULL, FALSE, &dsvCPUDescriptorHandle);

		RenderAllModels();
	}

	{
		const auto transitionBarrier = CD3DX12_RESOURCE_BARRIER::Transition(
			shadowMap->Resource().Get(),
			D3D12_RESOURCE_STATE_DEPTH_WRITE,
			D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE
		);

		m_commandList->ResourceBarrier(1, &transitionBarrier);
	}
}
```

## Description
{{ page.info }}

{% include contributionItem.md proj=page %}
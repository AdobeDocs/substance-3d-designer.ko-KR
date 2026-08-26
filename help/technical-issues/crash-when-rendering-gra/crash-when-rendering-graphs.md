---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 그래프를 렌더링할 때 발생하는 충돌 문제를 해결하고 이를 방지하기 위한 솔루션을 찾습니다.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 그래프를 렌더링할 때 충돌
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# 그래프를 렌더링할 때 충돌

이 페이지에서는 Substance 3D Designer의 그래프 렌더링 과정에서 발생하는 충돌을 나열하고 각각에 대한 문제 해결 단계를 제공합니다.

## TDR(Windows만 해당)

<b>[![(오류)](../../assets/error.svg)](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) 문제</b>

시스템의 <b>시간 제한 감지 및 복구(TDR)</b> 타이머가 *너무 짧아서* 그래픽 드라이버가 *다시 시작*&#x200B;되기 전에 Substance 3D Designer에서 현재 계산을 마칠 수 없습니다.

Substance 3D Designer에서 수행하는 계산은 매우 복잡할 수 있으며 그래픽 드라이버를 사용하여 운영 체제에서 잠시 동안 *응답하지 않는* 정도까지 사용할 수 있습니다.\
안정성 및 보안 대책으로 운영 체제 *그래픽 드라이버를 다시 시작*&#x200B;하여 계산 시간이 짧아지고 Substance 3D Designer *충돌*&#x200B;이 발생합니다.

<b>![(틱)](../../assets/check.svg) 권장 단계</b>

이러한 충돌을 방지하려면 TDR 타이머 값을 *증가*&#x200B;해야 합니다. Substance 3D Designer에도 적용되는 Substance 3D Painter 설명서의 [이 페이지](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)에 있는 지침을 따르면 이 작업을 수행할 수 있습니다.

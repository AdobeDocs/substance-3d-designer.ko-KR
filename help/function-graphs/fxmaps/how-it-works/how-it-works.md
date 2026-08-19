---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 FXMaps가 함수 그래프를 텍스처에 적용하여 절차적 효과를 얻는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 사용 방법
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# 사용 방법

FX-Map 그래프의 원리를 이해하는 것이 이 강력한 기능을 마스터하는 데 있어 핵심입니다.

FX-Map 그래프는 3가지 FX-Map 노드 유형(사분면, 반복 및 스위치) 중 하나 이상을 포함할 수 있습니다. 이러한 노드 중에서 가장 자주 사용하는 노드는 사분면이며 반복 노드는 1초 정도 걸립니다.

Parameter Set 노드는 FX-Maps 의 Prime Mover 입니다. 핵심 영역 쿼드 트리 그래프 FX-Maps를 사용하지만 하나로 표시되지 않습니다. 시각적으로 쿼드트리 그래프는 마코프 체인의 형태로 나타난다.

FX-맵을 렌더링할 때 단순화된 FX-맵 그래프는 큰 나무 같은 그래프처럼 보이도록 &#39;래핑 해제&#39;됩니다. 엔진은 위쪽에서 아래쪽으로 그리고 왼쪽에서 오른쪽으로 전체 쿼드 트리를 &quot;걷습니다.&quot;

FX-Map 노드는 이미지를 맹목적으로 복사하여 붙여넣지 않습니다. 각 이미지가 렌더링되면 포함된 모든 동적 함수가 실행됩니다. 이러한 기능은 노드가 렌더링한 각 이미지에 영향을 줍니다. 따라서 각 개별 이미지에 무작위 회전, 비율 조정 또는 기타 여러 조정 사항을 적용할 수 있습니다.

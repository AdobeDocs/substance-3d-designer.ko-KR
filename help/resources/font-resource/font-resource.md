---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 글꼴 리소스를 가져와서 사용하여 텍스트에 텍스트와 타이포그래피를 추가할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 글꼴 리소스
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# 글꼴 리소스

글꼴 리소스는 [atomic Text 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)과(와) 함께 사용됩니다. 디스크의 어디에서든 글꼴 파일을 참조하여 시스템에 설치되지 않은 글꼴을 사용할 수 있습니다.

>[!NOTE]
>
> **SBSAR의 글꼴**
> 
> 글꼴은 연결된 리소스에서나 시스템 설치 글꼴을 사용하는 것과 관계없이 항상 SBSAR에 포함됩니다. 이 방법의 장점은 설치할 필요가 없고, 종속성이 있는 SBS 파일을 내보낼 때 글꼴 파일을 함께 가져올 수 있다는 것입니다.

## 사용자 정의 글꼴 리소스 사용

* 패키지를 마우스 오른쪽 단추로 클릭하고 <b>링크 > 글꼴</b>을 선택합니다.
* .otf 또는 .ttf 파일을 선택합니다.
* [그래프](../../compositing-graphs/substance-compositing-graphs.md)에 [텍스트 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)를 배치합니다.
* <b>글꼴 </b> 속성에서 글꼴 리소스는 목록 맨 위에 표시됩니다.

속성이 열려 있는 경우 글꼴 목록이 자동으로 새로 고쳐지지 않습니다. 새로 연결된 글꼴을 보려면 다른 속성 창으로 전환하고 텍스트 노드로 다시 전환해야 합니다.

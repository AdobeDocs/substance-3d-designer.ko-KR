---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: 플러그인을 이전 버전의 Substance Designer에서 현재 Python API로 연결하는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 이전 플러그인 포팅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 이전 플러그인 포팅

Python에 대한 Qt 지원을 위한 변경 사항으로 인해 **이전 플러그인이 더 이상 작동하지 않습니다**.\
특히 다음 사항에 유의하십시오.

## 플러그인 로드 및 언로드

이제 <b>응용 프로그램이 시작</b>될 때 플러그인이 로드되고 <b>종료</b>될 때 플러그인이 언로드됩니다.\
따라서 플러그인이 더 이상 &#39;*sdplugins.Plugin*&#39;에서 상속되는 것은 *필요하지 않습니다*.

자세한 내용은 [플러그인 기본 사항](../../scripting/plugin-basics/plugin-basics.md) 섹션을 확인하십시오.

## 사용자 인터페이스 요소 만들기

더 이상 &#39;*sdplugins.PluginDesc*&#39;을 정의하는 데 *플러그인이 필요하지 않습니다*.\
대신에 플러그인은 <b>새로운 [UI 관리자](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr) 개체</b> 및 <b>Python용 Qt</b>를 사용하여 필요한 사용자 인터페이스 요소를 만들 수 있습니다.

[사용자 인터페이스 요소 만들기](../../scripting/creating-user-interface/creating-user-interface-elements.md) 섹션에서 작은 코드 샘플을 찾을 수 있습니다.

## 위치 컨텍스트 사용을 바꾸는 중

Python API에서 &#39;*SDLocationContext*&#39; 클래스가 *제거*&#x200B;되었습니다.\
플러그인은 <b>[UI 관리자](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr) 개체</b>를 사용하여 현재 활성화된 그래프 및 선택 항목에 액세스할 수 있습니다.

[그래프 및 선택 영역 액세스](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md) 섹션에서 몇 가지 예를 확인할 수 있습니다.

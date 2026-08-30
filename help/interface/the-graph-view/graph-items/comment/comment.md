---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Substance 3D Designer 그래프에 주석을 추가하여 워크플로우를 문서화하고 노드 연결을 설명합니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 주석
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# 주석

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![댓글 아이콘](comment.resources/graphatomic-comment_1.png "댓글 아이콘")

</td>
<td width="100.00%" style="border: 0;" valign="top">

주석은 그래프의 아무 곳에나 배치할 수 있는 자유 부동 텍스트 조각입니다.

그래프의 일부에 주석을 달고 설명하기 위한 것입니다. <b>설명</b> 속성에 표시되는 텍스트가 있습니다.

</td>
</tr>
</table>

>[!NOTE]
>
> 주석에는 그래프에서 발자국을 최소화하는 것을 목표로 하는 자동 줄바꿈이 있습니다.

## 주석 만들기

기본 주석 유형은 그래프의 노드와 독립적으로 배치됩니다.

다음과 같은 방법으로 만들 수 있습니다.

+++노드 메뉴
그래프 보기에서 <b>스페이스바</b>를 눌러 <b>노드 메뉴</b>를 열고 목록에서 &#39;주석&#39; 항목을 선택합니다.

검색 필드에 &#39;comment&#39;를 입력하여 항목을 표시하고 항목을 더 빠르게 찾습니다.

+++

+++단축키
키보드 단축키가 [환경 설정](../../../../interface/preferences-window/preferences-window.md)의 &#39;주석&#39; 항목에 매핑되어 있으면 그래프 보기에 포커스가 있을 때 해당 단축키를 누릅니다.

+++

+++상황별 메뉴
그래프 보기에서 개체 또는 빈 공간에 있는 <b>RMB</b>을 누르고 <b>주석 추가</b> 옵션을 선택합니다.

+++

+++그래프 도구 모음
[그래프 보기] 도구 모음의 <b>노드 팔레트</b>에서 &#39;주석&#39; 단추를 클릭합니다.

+++

+++라이브러리
라이브러리에서 <b>그래프 항목</b> 범주를 선택한 다음 &#39;주석&#39; 항목을 그래프 보기로 드래그하여 놓습니다.

+++

>[!TIP]
>
> 댓글이 작성되면 &#39;설명&#39; 속성에 자동으로 포커스가 추가되므로 해당 댓글의 텍스트를 즉시 편집할 수 있습니다.

## 상위 댓글

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

상위 주석은 그래프에서 *특정 노드에 연결된* 주석으로, 노드를 이동하면 해당 주석이 따라오고, 노드를 삭제하면 해당 주석과 함께 삭제됩니다.

*단일* 노드가 현재 선택되어 있거나 단일 노드의 상황별 메뉴를 통해 만들어진 주석은 해당 노드에 상위가 됩니다.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![댓글: 상위 댓글](comment.resources/graph-comment_parented.gif "댓글: 상위 댓글")

</td>
</tr>
</table>

## HTML 서식

HTML 태그를 사용하여 텍스트 서식을 지정할 수 있습니다. 이 서식은 주석의 <b>설명</b> 속성에서 ![](comment.resources/graph-frames_html-markup-button.png) <b>HTML 태그</b> 단추를 사용하여 전환됩니다.

>[!TIP]
>
> [프레임](../../../../interface/the-graph-view/graph-items/frame/frame.md) 설명서의 <b>설명</b> 섹션에서 이 기능에 대해 자세히 알아보십시오.

![주석: HTML 마크업](comment.resources/graph-comment_html-markup.gif "주석: HTML 마크업")

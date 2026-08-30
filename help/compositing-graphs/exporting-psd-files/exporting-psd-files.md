---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Adobe Photoshop 및 기타 이미지 편집 작업 과정에서 사용할 Substance 합성 그래프를 PSD 파일로 내보내는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PSD 파일 내보내기
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# PSD 파일 내보내기

Substance 3D Designer에서 텍스처를 Adobe Photoshop 문서 또는 PSD 파일로 내보낼 수 있습니다.이 페이지에서는 그래프의 노드를 레이어로 변환하는 데 사용되는 특수 인터페이스에 대해 설명합니다.**이 프로세스는 자동으로 수행되지 않습니다. 많은 제어가 가능하지만 노드와 레이어 간의 정확한 일치를 얻을 수 없는 경우가 많습니다.** 또한 그래프에 대해 명시적으로 설정하지 않는 한 PSD에 그래프와 동일한 출력이 포함된다는 보장은 없습니다. 일반적으로 더 정확하고 올바르게 되고 싶을수록 사용자가 더 많은 노력을 기울여야 합니다. 일반적으로 비파괴적인 방법으로 밀접하게 복제할 수 있는 유일한 방법은 [혼합 노드](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)입니다. 조정 레이어는 지원되지 않으며, 레이어 스타일이나 레이어 혼합 모드 이외의 다른 스타일도 지원되지 않습니다.

[Substance 3D Designer에서 비트맵 파일로 내보낼 수도 있습니다.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## PSD 내보내기 대화 상자

[PSD 내보내기] 대화 상자는 한 가지 방법으로만 열 수 있습니다. PSD으로 내보낼 그래프의 [그래프 보기](../../interface/the-graph-view/the-graph-view.md)에서 ![](exporting-psd-files.resources/image2019-9-17-14-44-17.png) <b>도구</b> 단추를 클릭하고 <b>PSD 내보내기</b>를 선택합니다. 인터페이스가 <b>그래프 보기</b>에 표시됩니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![PSD 내보내기 사용자 인터페이스](exporting-psd-files.resources/psd-dialog.png "PSD 내보내기 사용자 인터페이스")

</td>
<td style="border: 0;" valign="top">

1. <b>파일 이름 및 위치:</b> 여기서 내보낼 폴더 및 파일 이름을 설정합니다. 내보내기 버튼을 눌러 내보내기 프로세스를 수행합니다.
1. <b>그룹 추가:</b> 레이어 그룹을 추가합니다.
1. <b>레이어 추가 드롭다운:</b> 레이어를 추가할 두 가지 방법 중 하나를 선택합니다. *마우스 오른쪽 단추로 노드를 드래그하여* 레이어를 스택으로 추가할 수도 있습니다.
1. <b>레이어 제거 드롭다운:</b> 선택한 레이어 또는 모든 레이어를 제거합니다.
1. <b>Layerstack:</b> 대부분의 설치 작업은 여기서 수행됩니다. Photoshop의 제한된 인터페이스 미러 옵션. 레이어 이름, 혼합 모드 및 불투명도를 설정합니다. 레이어에 두 개의 축소판이 있는 경우 두 번째 축소판은 Alpha 채널을 나타냅니다.

</td>
</tr>
</table>

## 워크플로

Photoshop에서는 다중 출력 재질을 직접 지원하지 않으므로 다양한 방법으로 PSD을 설정할 수 있습니다. 다음은 가장 일반적인 방법의 개요입니다.

* 모든 출력의 폴더 수를 설정합니다. [기본 색상], [표준], [거칠음] 등의 폴더를 한 개 선택합니다.
* 마우스 오른쪽 버튼으로 출력을 적절한 그룹으로 드래그 앤 드롭합니다. 간단하게 하려면 PSD을 여기에만 두면 됩니다.
* PSD을 더 확장하려면 그래프의 적절한 그룹에서 그래프의 중간 단계를 삭제하여 그래프의 왼쪽으로 다시 돌아옵니다. 출력/그룹 간에 레이어를 공유할 수 없습니다.

드문 경우지만 PSD이 더 중요한 출력인 경우 혼합 모드만 사용하도록 그래프를 구축할 수 있습니다. 이 경우 더 편집 가능한 버전의 그래프를 레이어로 구성된 문서로 다시 만들 수 있어야 합니다.

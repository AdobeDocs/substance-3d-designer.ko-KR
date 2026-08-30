---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: 경로 선택 노드 를 사용하여 조건에 따라 경로 목록에서 특정 경로를 선택하고 필터링합니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패스 선택
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# 패스 선택

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![노드 아이콘](paths-select.resources/paths-select-icon.png "노드 아이콘")

<b>인:</b> 스플라인 및 패스 도구 > 패스 도구

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 설명

패스에 포함된 다중 중에서 하나의 패스를 분리합니다.

</td>
</tr>
</table>

<a name="inputs"></a>

## 입력

|  |  |
|:---|:---|
| <b>레이블</b> <i>유형</i> | 인코딩된 세그먼트 경로 목록입니다. 이 입력을 [패스에 마스크](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) 또는 다른 패스 처리 노드에 연결합니다. |

<a name="outputs"></a>

## 출력

|  |  |
|:---|:---|
| <b>경로</b> <i>색상</i> | 패스는 하나의 패스로만 입력됩니다. [패스 미리 보기](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)를 사용하여 결과가 어떻게 나타나는지 파악하거나 다른 패스 처리 노드를 사용하거나 [스플라인으로 패스](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)에 입력하여 스플라인으로 추가로 처리할 수 있습니다. |

<a name="parameters"></a>

## 매개변수

|  |  |
|:---|:---|
| <b>선택 모드</b> <i>정수</i> | 경로를 선택하는 데 사용되는 메서드:<br>*- ID 기준:* 인덱스가 <b>경로 ID</b>;<br>*- 길이 기준:*&#x200B;이(가) <b>대상 길이</b>에 지정된 임계값보다 크거나 작은 경로를 목록에서 선택합니다. |
| <b>경로 ID</b> <i>정수</i>(<b>선택 모드</b>가 *ID별*(으)로 설정된 경우 사용 가능) | 선택한 패스의 인덱스입니다.<br><b>패스 *의 패스 수보다 큰 값을 사용하면 빈 출력이 생성됩니다*</b>. |
| <b>길이가 더 길거나 더 짧습니까?</b> <i>부울</i>(<b>선택 모드</b>가 *길이*(으)로 설정된 경우 사용 가능) | 선택 영역의 길이가 <b>대상 길이</b>보다 크거나 작은지 여부를 제어합니다. |
| <b>대상 길이</b> <i>부동</i>(<b>선택 모드</b>가 *길이*(으)로 설정된 경우 사용 가능) | 스플라인을 선택하는 데 사용되는 길이 임계값입니다. |

## 예

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>이전</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>이후</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

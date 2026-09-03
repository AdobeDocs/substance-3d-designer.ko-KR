---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 출력
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# 출력

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomic node: 출력](output.resources/output-01.png "Atomic node: 출력"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

출력 노드는 Substance 그래프의 <b>결과</b>를 지정하거나 출력 노드가 두 개 이상 있는 경우 결과 중 하나를 지정합니다.

그래프의 출력 노드에 연결된 이미지 또는 값은 이 그래프를 나타내는 [인스턴스 노드](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)에서 출력되며 [그래프 출력으로 내보낼 수 있습니다](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md).

</td>
</tr>
</table>

마찬가지로 [게시된 SBSAR 파일](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)에 이 그래프가 포함되어 있으면 해당 파일은 파일을 사용하는 모든 통합 또는 플러그인에서 해당 이미지를 출력할 수 있습니다.

유형에 관계없이 하나의 입력 슬롯이 있으며, 이는 데이터 유형이 연결된 후에 해당 입력 슬롯이 스스로 입력된다는 것을 의미합니다.

매개 변수가 없고, 오히려 결과물을 적절하게 라벨링하여 의도한 용도에 부여하는 데 매우 중요한 속성을 가지고 있다.

모든 Substance 그래프에는 *하나 이상의* 출력 노드가 있어야 합니다. 출력이 없으면 그래프에서 실제 결과를 반환할 수 없으며 [경고](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md)가 발생합니다.

## 특성

|  |  |
| --- | --- |
| <b>식별자</b> *문자열* | 출력의 고유 식별자입니다. 이 속성은 비워 둘 수 없으며 특수 문자 또는 공백을 포함할 수 없습니다.   이 식별자는 노드의 레이블인 &#39;Label&#39; 속성이 공백으로 남아 있을 때 사용됩니다. [내보낸 텍스처](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)의 이름을 지정하는 데 사용할 수도 있습니다. |
| <b>설명</b> *문자열* | 출력의 도구 설명으로 사용되는 선택적 설명은 Substance 그래프입니다. |
| <b>레이블</b> *문자열* | 출력 노드 및 이 그래프를 나타내는 [인스턴스 노드](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)의 해당 커넥터에 대한 레이블로 사용됩니다. 레이블에는 공백 및 특수 문자가 포함될 수 있습니다. |
| <b>사용자 데이터</b> *문자열* | 특정 필터링 작업에 사용할 수 있는 선택적 메타데이터입니다. [Substance 3D Painter](https://www.adobe.com/kr/products/substance3d/apps/painter.html)에서 이 데이터를 사용하여 [일부 기능을 구동](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/content/creating-custom-effects/user-data)합니다. |
| <b>그룹</b> *문자열* | Designer의 [링크 만들기 모드](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)에 대한 출력을 함께 그룹화하는 데 사용되는 특성입니다.   &#39;Group&#39; 특성이 동일한 출력이 &#39;Compact Material&#39; 링크 생성 모드에서 단일 연결로 표시됩니다. |

## 통합 특성

[게시된 SBSAR 파일](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)에서 그래프를 사용하는 통합/플러그인이 사용하도록 지정된 특성입니다.

따라서 [비트맵 내보내기](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)의 형식에는 영향을 주지 않습니다. 또한 Designer에서는 <b>Usage</b> 특성만 사용됩니다. 자세한 내용은 아래를 참조하세요.

<b>사용</b>

|  |  |
| --- | --- |
| <b>구성 요소</b> *문자열* | AxF 작업 과정에서 일부 텍스처 채널을 적절한 SVBRDF 셰이더 입력에 매핑하는 데 사용됩니다. |
| <b>사용</b> *문자열* | 출력 노드의 유형 및 사용을 정의합니다. 이 속성은 다음을 추진하는 데 중요합니다.<ul data-preserve-html="true"> <li data-preserve-html="true">일부 [Substance 생성 모드](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)를 사용할 때 링크 그래프의 노드 연결 </li> <li data-preserve-html="true">3D 보기의 셰이더에 텍스처 연결(아래 &#39;[3D 보기의 사용 역할 정보](#usages-role-3dview)&#39; 참조)</li> <li data-preserve-html="true">통합/플러그인의 자료에 텍스처 연결</li> </ul> |
| <b>색상 공간</b> *문자열* | 이 출력을 해석해야 하는 색상 공간을 설정합니다. 다른 응용 프로그램의 일부 통합에서 사용되며 Designer에는 영향을 주지 않습니다. |

### 3D 뷰의 사용 역할 정보

그래프 출력이 종종 특정 텍스처 채널에 대한 최종 결과인 경우가 많기 때문에, 출력은 3D 뷰에서 사용되는 셰이더의 적절한 샘플러로 자동으로 전송될 수 있다.

실제로 3D 보기에서 <b>사용</b> 속성이 *샘플러 사용과 일치*&#x200B;하는 출력이 해당 샘플러에 연결됩니다. 예를 들어 `basecolor` 사용이 포함된 출력이 3D 뷰 셰이더의 `basecolor` 샘플러에 연결됩니다. [3D 보기](https://substance3d.adobe.com/documentation/display/draftdesigner/.3d%20view%20vdraftversion) 페이지의 [3D 보기](../../../../interface/3d-view/3d-view.md) 섹션에서 자세히 알아보십시오.

[그래프 보기](../../../../interface/the-graph-view/the-graph-view.md)의 빈 영역에서 RMB를 클릭하고 컨텍스트 메뉴에서 <b>3D 보기에서 출력 보기</b> 옵션을 선택하여 모든 출력을 *일치하는 사용*&#x200B;이 포함된 3D 보기 샘플러에 연결합니다.

>[!IMPORTANT]
>
> 예를 들어 압축된 텍스처의 채널에 사용을 할당하기 위해 여러 사용을 순서대로 설정하면 목록의 *첫 번째 사용*&#x200B;만 3D 보기에 연결됩니다. 알려진 제한 사항입니다.

## 기본 출력

그래프에 출력이 두 개 이상 있는 경우 이러한 출력 중 하나를 해당 그래프의 기본 출력으로 설정할 수 있습니다. 이 옵션은 다음 작업에 사용할 출력을 지정합니다.

* 해당 그래프를 나타내는 인스턴스 노드의 축소판입니다
* 2D 뷰에서 이러한 인스턴스 노드 보기
* 라이브러리에 있는 해당 그래프의 축소판([여기](../../../../interface/preferences-window/project-settings/project-settings.md)에서 내 리소스를 추가하는 방법에 대해 알아보기)

이 기능을 사용하면 그래프가 노드로 시각화되는 방법과는 독립적으로 그래프 출력을 임의의 순서로 정렬할 수 있습니다.

출력 노드를 그래프의 기본 출력으로 설정하려면 다음을 수행합니다.

* 출력 노드를 마우스 오른쪽 버튼으로 클릭하고 컨텍스트 메뉴에서 &#39;기본 출력으로 설정&#39; 작업을 선택합니다.
* 출력 노드의 속성에서 &#39;특성&#39; 섹션의 헤더에 있는 &#39;기본값으로 설정&#39; 버튼을 사용합니다.

다음은 기본 출력을 설정하기 전과 후의 인스턴스 노드 예입니다.

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="output.resources/output-02.png" alt="defaultouput2">
      <br><i>이전</i>
    </td>
    <td style="border: 0">
      <img src="output.resources/output-03.png" alt="defaultouput1">
      <br><i>이후</i>
    </td>
  </tr>
</table>

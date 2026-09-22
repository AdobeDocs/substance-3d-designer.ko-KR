---
name: generate-node-documentation
description: |
  도움말/합성-그래프/노드-참조-for-com/노드-라이브러리/에서 사용되는 표준 레이아웃과 일치하도록 Substance 3D Designer 노드-참조 페이지를 작성하는 방법. 해당 노드 라이브러리 트리 또는 동등한 함수-노드/원자-노드 참조 페이지에서 노드 페이지(노드의 설명, 입력, 출력, 매개변수 또는 예제)를 만들거나 편집할 때마다 이 기술을 사용합니다. 폴더/TOC 규칙, 최소 앞면 문제, 아이콘/설명 테이블, 고정된 입력/출력/매개 변수 테이블 및 예제 갤러리에 대해 설명합니다. 일반적인 Adobe Experience League 마크다운 규칙(콜아웃, 링크, UICONTROL/DNL, 이미지)에는 write-experience-league-markdown 기술이 사용됩니다. 이 기술은 노드 페이지 구조만 다룹니다. 정식 예: help/compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 3%
---

# 노드 설명서 생성

이 리포지토리의 모든 리프 노드 참조 페이지는 하나의 일관된 구조를 따릅니다. 이
스킬이 해당 구조의 사양입니다. 정석적이고 완전히 노력한 예는 다음과 같습니다.
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
의심스러우면 열고 미러링합니다.

이 기술은 노드 페이지 *구조*에만 적용됩니다. 기본 Experience League 마크다운의 경우
(참고/경고 블록, 상대-절대 링크, UICONTROL/DNL, 이미지 쿼리 매개 변수,
린트는 `write-experience-league-markdown` 기술을 따릅니다.

## 노드 페이지가 있는 위치(폴더/목차 규칙)

* 일치하는 범주/하위 범주 경로 아래의 노드당 하나의 폴더
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* 이 폴더의 이름은 kebab-case 노드 제목으로 지정되었으며 **one** `.md` 파일이 포함되어 있습니다.
이름이 동일합니다.
* 페이지의 모든 포함된 미디어(아이콘, 예제 이미지, GIF)는 **형제 페이지에 있습니다.
  `.md` 옆의 `<node-name>.resources/` 폴더&#x200B;**을(를)
  상대 경로(예: `<node-name>.resources/<file>.png`). 노드 페이지를 가리키지 않음
  공유된 `help/assets/` 폴더 — 단계적으로 폐지되는 레거시 패턴이며, 새로운 및
  편집된 페이지는 고유한 `.resources` 폴더를 사용합니다.
* 모든 페이지에는 `help/guide/TOC.md`에 해당 항목이 있습니다. 이미지를 추가하거나 이동할 때
페이지, `TOC.md` 업데이트 및 폴더 레이아웃을 함께 표시(AGENTS.md의 폴더/목차 참조)
규칙).

## 전문

노드 페이지에서 **최소** 블록을 사용합니다. `title` 및 탐색 경로 스타일만 사용
`description`. (이것은 다음에 대한 11개 필드 레거시 블록 AGENTS.md 문서와는 다릅니다.
일반 콘텐츠 페이지

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## 본문 구조

위에서 아래로, 아래 모든 것이 중요함:

### &#x200B;1. H1 제목

단일 `# <Node title>`(페이지당 정확히 하나의 H1).

### &#x200B;2. 아이콘/설명 테이블

HTML 테이블 하나, 행 하나, 셀 두 개 왼쪽 셀(`33.33%`)에 아이콘이 있으면
`In:` 탐색 경로; 오른쪽 셀(`100.00%`)에 `## Description` 및 산문이 있습니다.

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

Description-cell prose 규칙:
* 단락을 `<br><br>`과(와) 분리합니다. 셀 안의 빈 줄은 신뢰할 수 없습니다.
* 인라인 강조는 `<b>…</b>`/`<i>…</i>`입니다.
* 앞줄 바꿈 부분은 문장 시작 부분에 `<i>Note:</i>`/`<i>Tip:</i>`을(를) 사용합니다.
* `In:`행(HTML 안에 있음)의 `>`에 대해 `&gt;`을(를) 사용합니다. 범주 가져오기 /
노드 자체의 하위 범주 이름이므로 작성하지 마십시오.
* 여러 버전(예: 색상/회색 음영/값 또는 번호 매기기 변형)이 있는 노드의 경우
셀 1/셀 2)와 마찬가지로 다른 하나를 참조하는 최종 설명 단락을 추가합니다
한 줄 바꿈으로 구분된 상대 링크가 있는 버전. 예: `See also: [Input
grayscale](../input-grayscale/input-grayscale.md), [Input value](../input-value/input-value.md)`.

### &#x200B;3. 선택적 콜아웃

`>[!INFO]`, `>[!TIP]`, `>[!NOTE]` 등은 아이콘/설명 테이블(아님)을 **다음** 뒤로 이동합니다.
셀 내부). `write-experience-league-markdown` 스킬당 구문

### &#x200B;4. 입력

노드에 입력 핀이 있는 경우에만 포함합니다. 머리글 앞에 앵커를 붙입니다.

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* 두 개의 열, 빈 헤더 행, `|:---|:---|` 정렬입니다.
* 입력당 하나의 행: 왼쪽 셀 `<b>Name</b> <i>Type</i>`, 오른쪽 셀 설명
* 형식 마커가 HTML 이탤릭체 `<i>Type</i>`이며 markdown `*Type*`이(가) 아닙니다.

### &#x200B;5. 출력

`<a name="outputs"></a>` + `## Outputs`을(를) 사용하여 입력과 동일한 모양입니다. 다음 경우에만 포함:
노드 문서 고유 출력(많은 노드에는 단일 암시적 출력이 있고 이 출력은 생략됨)
섹션 — 작성하지 마십시오).

압축된 멀티채널 출력의 경우 `<br>`(으)로 채널을 나누고 들여씁니다.
`&nbsp;`이(가) 있는 하위 포인트(&quot;Splatter UVW&quot;/&quot;스플래터 데이터&quot; 행 참조)
참조):

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. 매개변수

`<a name="parameters"></a>` + `## Parameters`과(와) 동일한 테이블 모양입니다. 전체 생략
노드에 매개 변수가 없는 경우 섹션입니다. 즉, 빈 테이블이나 &quot;매개 변수 없음&quot;을 내보내지 않습니다.
줄).

* **그룹화된 매개 변수**: 다음 시간 앞에 빈 오른쪽 셀이 있는 확장 레이블 행을 내보냅니다.
그룹 행:

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **열거형/다중 옵션 값**: 설명 셀 안에 있는 옵션을 다음과 같이 나열합니다.
  `<br>` 구분된 대시 목록:

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. 예

예제 이미지/GIF이 있는 경우에만 포함합니다. 테두리 없는 고정 레이아웃 HTML 사용
갤러리 테이블, 이미지당 `<td>`개, 3개 이미지 뒤에 새 `<tr>`개로 줄 바꿈. 미디어 경로
페이지의 `.resources` 폴더를 가리킵니다. 다음에 대해 HTML `<img>` 요소 사용
예를 들어, `class="modal-image"`을(를) 사용하면 게시된 이미지가 표준에서 열립니다
이미지 뷰어. 노드 및 예제를 식별하는 의미 있는 `alt` 텍스트를 제공합니다.
번호. 이 갤러리에서 마크다운 이미지 구문을 사용하지 마십시오.

```html
## Examples

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="<node-name>.resources/<file>.gif" class="modal-image" alt="<Node title> - Example 1" />
        </td>
        <td style="border: 0;">
            <img src="<node-name>.resources/<file2>.jpg" class="modal-image" alt="<Node title> - Example 2" />
        </td>
    </tr>
</table>
```

테이블의 `style="table-layout:fixed"`과(와) `style="border: 0;"`
표시된 것과 정확히 같은 특성을 사용할 수 있으며 테두리, 여백 또는 배경 스타일은 추가하지 않습니다.
부분적으로 채워진 최종 행의 후행 셀을 비워 둡니다.
리플로우하지 않고 (`<td style="border: 0;"></td>`). 기존 이미지 사용
순서 및 파일 이름. 페이지에 캡션이 있는 경우 `alt` 텍스트로 유지하십시오.
표시 가능한 캡션 마크업 추가와 동일합니다. 페이지에 가 없는 경우 전체 섹션 생략
예제 미디어.

## 표준 유형 값

노드의 고유한 형식 문구를 다시 사용합니다. 일반적인 값: `Grayscale`, `Color`, `Integer`,
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. 문자를 발명하거나 &quot;표준화&quot;하지 마십시오.
노드는 실제로 사용하지 않습니다.

## 표 셀 규칙

* 표 셀 안에 Raw 새 행이 없습니다. `<br>`(및 `<br><br>` 사이)의 행을 연결하십시오.
단락)을 참조하십시오.
* 셀 내에서 강조되는 부분은 `<b>`/`<i>`이며 형식 표식은 항상 `<i>Type</i>`입니다.
* `&nbsp;`개의 시퀀스로 중첩된 하위 지점을 들여씁니다.

## 규칙 / 금지사항

* 노드에 없는 입력, 출력 또는 매개 변수를 **조작하지 마십시오.**
대신 섹션으로 이동합니다. 기존 기술 내용을 다시 말하거나 요약하거나 삭제하지 마십시오.
다시 포맷하세요.
* **링크를 다른 `.md`페이지에 상대적인 상태로 유지**&#x200B;합니다. 외부 링크는 절대적입니다.
* 이전 페이지를 다음 형식으로 편집할 때 **기존 페이지 삭제**: 난이도 태그
(`**Simple**` / `**Intermediate**` / `**Complex**`), 중복 `## <Title>`
아이콘 셀 내부의 부제목, &quot;연결된 이미지가 없습니다.
이 페이지&quot;와 이전 마이그레이션의 빈 탐색/래퍼 테이블
* 페이지당 **H1** 1개; 섹션은 `##` 및 입력/출력/매개 변수 앵커를 사용합니다.
(`inputs` / `outputs` / `parameters`)이(가) 제목 앞에 와야 페이지를 넘습니다.
  `#inputs`개의 링크가 확인되었습니다.
* 페이지를 추가하거나 이름을 바꾸거나 이동할 때 **동기화 상태로 `TOC.md`을(를) 유지**&#x200B;합니다.

---
name: write-experience-league-markdown
description: |
  Adobe Experience League에 게시된 [마크다운] 콘텐츠를 작성하기 위한 구문 규칙, 사용자 정의 확장 및 개선 사항입니다. 이 레포(또는 다른 Experience League 콘텐츠 레포)에서 도움말/ 제목, 링크, 이미지, 표, 메모/경고 블록, UICONTROL/DNL 태그, 비디오 임베드, 앵커 및 알려진 렌더링 함수와 같은 페이지를 만들거나 편집할 때마다 이 기술을 사용합니다. 출처: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
---

# Experience League 마크다운 작성

Experience League이 사용자 지정 파이프라인을 통해 GitHub 풍의 마크다운을 렌더링합니다.
확장자와 렌더링 기발함으로. 표준 GFM은 대부분 작동하지만
아래 항목은 Experience League 전용입니다. 잘못 입력했거나 내용을 담고 있습니다.
lint/link-check CI가 실패하거나 라이브 사이트에서 잘못 렌더링됩니다.

## 머리글

* `#` - `#####`(수준 1-5). 페이지의 `title` 초기 문제는 다음과 같습니다.
효과적으로 레벨 0; 본문에서 첫 번째 [마크다운] 머리글은
페이지 제목과 일치하는(또는 가깝게 일치하는) 단일 `# Level 1` 머리글입니다.
* 임의로 레벨을 건너뛰지 마십시오. mini-TOC는 머리글에서 생성됩니다.

## 텍스트 서식 지정

* `**bold**`, `*italic*`, `***bold and italic***`.
* 백슬래시(`\*`, `\_` 등)를 사용하여 리터럴 특수 문자를 이스케이프합니다.
* 머리글/제목의 **앰퍼샌드**&#x200B;은(는) 다음과 같이 작성(`and`)하거나 인코딩해야 합니다.
  `&amp;` — 제목의 raw `&`이(가) 구문 분석을 중단할 수 있습니다.
* 리터럴 텍스트(실제 HTML 아님)로 사용된 **꺾쇠 괄호**는 인코딩해야 합니다.
  `<placeholder>` → `&lt;placeholder&gt;`입니다.
* 워드 프로세서에서 붙여넣은 **스마트 따옴표**를 인코딩해야 합니다.
리터럴 곱슬 문자: 왼쪽 이중 `&#8220;`, 오른쪽 이중 `&#8221;`,
아포스트로피/오른쪽 싱글 `&#8217;`.

## 목록

* 번호 매기기 목록: `1.`(또는 `1)`)로 모든 항목 시작 — GitHub/Experience
입력한 리터럴 숫자에 관계없이 리그 자동 번호입니다.
* 글머리 기호 목록: `*`, `-` 또는 `+`을(를) 사용하지만 **글머리 기호 문자를 혼합하지 않습니다.
같은 목록/문서** 내에서
* `TOC.md` 목록 중첩은 `+`을(를) 일관되게 사용합니다. 기존 파일의
다른 스타일을 도입하는 대신 글머리 기호 스타일을 사용합니다.

## 링크

* 내부 상호 참조는 **상대** 마크다운 링크여야 합니다.
대상 `.md` 파일: `[Overview](../../overview.md)`.
* 외부 참조는 **절대** URL이어야 합니다.
* 다른 페이지의 머리글/범위에 연결: `#anchor-id`(예:
  `[Mesh](../../glossary/glossary.md#mesh)`.
* 페이지 내 앵커는 제목으로 선언되거나(자동 슬러그 처리됨)
용어 바로 앞의 명시적 `<span id="anchor-id"></span>`(HTML)/`{: #anchor-id}`(마크다운) —
이 리포지토리 전체에 사용된 패턴은 `help/glossary/glossary.md`을(를) 참조하십시오.
* `TOC.md` 섹션 앵커가 머리글/목록 뒤에 `{#section-id}` 구문을 사용합니다.
레이블(예: `Getting started{#getting-started}`).

## 이미지

가능한 한 마크다운 이미지 구문을 사용합니다.

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* `![...]` 텍스트는 액세스 가능한 대체 텍스트가 필요합니다. 간결하게 하고 하세요
밑줄을 사용하지 않습니다. 대신 공백이나 하이픈을 사용하십시오.
* 이미지 경로는 다음과 같이 마크다운 파일 또는 루트를 기준으로 할 수 있습니다
`/help/assets/shared-image.png`(으)로 내보내기 페이지별 이미지는
형제 `<page-name>.resources/` 폴더(예:
  `<page-name>.resources/image.png`). `help/assets/`은(는) 레거시 공유 폴더입니다.
  여기에 페이지별 이미지를 새로 추가하지 마십시오.
* 선택적 이미지 쿼리 매개 변수는 CDN 처리를 제어할 수 있습니다.
  `?width=750&format=png&optimize=medium`. 이미지에 이러한 매개 변수 유지
  URL, 속성 블록 앞
* `)`을(를) 닫은 후 바로 이미지 속성을 추가합니다.
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width`은(는) 보기 영역의 픽셀 값 또는 백분율입니다. 이미지 비율
비례적으로 지원되는 맞춤 값은 `center` 및 `right`입니다.
  `valign`은(는) 지원되지 않습니다.
* `modal="regular"` 또는 `zoomable="yes"`을(를) 사용하여 이미지를 클릭하여 확대/축소합니다.
  `![Alt text](image.png){width="100" zoomable="yes"}`. 결합하지 않음
  이미지 링크를 사용하여 클릭하여 확대/축소하면 하이퍼링크가 먼저 적용됩니다.
* 다른 페이지에 이미지 링크를 만들려면 이미지를 [마크다운] 링크로 감싸십시오.
  `[![Alt text](image.png)](../target/target.md)`.
* 큰 이미지의 경우 가능하다면 소스 너비를 최소 640픽셀로 제공하십시오.
필요한 경우 제외하고 최대 2,000픽셀을 사용하고 이미지 파일을 아래 위치에 유지
가능한 경우 5MB. 파이프라인은 최대 100MB의 파일을 허용하지만 그 이상의 파일을 허용합니다.
20MB의 유효성 검사 실패 및 아티클은 일반적으로 다음 이하의 용량을 포함해야 합니다.
100개 이미지(이전의 지침에서는 200개로, 더 엄격한 제한을 사용하십시오.)

마크다운에서 다음과 같이 필요한 레이아웃을 표현할 수 없는 경우에만 HTML을 사용합니다.
특수 테이블 또는 사용자 지정 인라인 프레젠테이션 지원되는 HTML 이미지 양식
상태:

```html
<img src="image.png" alt="Alt text" />
```

* 항상 의미 있는 `alt` 특성을 제공하고 상대 또는
루트 상대 `src`이(가) Markdown 이미지와 일치합니다.
* 보존된 인라인 HTML 내의 HTML 이미지에서 다음을 추가합니다.
  `data-preserve-html="true"`을(를) 포함하는 태그에
  주변 마크업. 예:

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* HTML 이미지에 Click-to-Zoom을 사용하려면
  `<img>` 태그의 `class="modal-image"`.
* 지원되지 않는 HTML 특성을 사용하지 않거나 `valign`에 의존합니다. 마크다운을 선호합니다.
폭 및 정렬 속성

## 표

일반적인 표 형식 콘텐츠에 대해 네이티브 마크다운 테이블 선호:

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* 테이블 앞에 빈 줄을 놓아라. 마크다운 테이블에는 적어도 하나 이상이 필요합니다.
머리글 행 및 본문 행 하나, 1행 또는 머리글자에 HTML 테이블 사용
테이블입니다.
* 모든 머리글 구분 기호 셀에서 하이픈을 세 개 이상 사용하고 동일한 하이픈을 유지합니다
모든 행에 있는 파이프 문자 수입니다. 리터럴 파이프를 `\|` 또는
  `&vert;`.
* 필요할 때 구분 기호 행에 맞춤 표시자를 사용합니다.
  왼쪽, 가운데 및 오른쪽 맞춤에 대한 `|---|:---:|---:|`.
* 인라인 HTML은 단락 나누기에 대해 마크다운 표 셀에서 지원되며
기본 목록. 개별 단락에 `<p>`, 줄 바꿈에 `<br>`을(를) 사용하고
  `<ul>`/`<ol>`(목록 항목 `<li>`개 포함). 추가
  `data-preserve-html="true"`에서 필요한 경우 인라인 HTML 요소에 연결합니다.
  주변 저장소 마크업.

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* 매우 넓고 매우 큰 테이블은 피하십시오. 테이블을 탐색하기가 어렵습니다.
긴 코드가 강제로 적용될 수 있으므로 테이블의 인라인 코드에 주의해야 합니다
열 너비가 일치하지 않습니다.
* Markdown 테이블의 테이블 레이아웃을 선택하려면 속성 뒤에
빈 줄로 구분된 테이블:

  ```markdown
  {style="table-layout:fixed"}
  ```

  긴 텍스트 또는 코드를 유연하게 수정해야 하는 경우 `table-layout:auto`(기본값) 사용
  열 너비. 다음을 포함하는 테이블과 같이 균형 잡힌 열에 `fixed`을(를) 사용합니다.
  크기가 비슷합니다.

Markdown에서 다음과 같은 필수 구조를 표현할 수 없는 경우 HTML 테이블을 사용합니다.
헤더 생략, 스팬과 셀 결합, 열 균형 조정 또는 정렬
셀 내용:

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* 지원되는 테이블 요소는 `<table>`, `<tbody>`, `<thead>`, `<tfoot>`,
  `<tr>`, `<th>`, `<td>`, `<col>` 및 `<colgroup>`과(와) 함께 지원됨
`<p>`, `<br>`, `<b>`, `<i>`, `<ul>`, `<ol>` 및
  `<li>`.
* HTML 테이블 내에서 Markdown 구문을 사용하지 마십시오. 예를 들어, Markdown
메모, 이미지 및 링크는 문자 그대로 렌더링될 수 있습니다. 대신 HTML 구문을 사용하십시오.
  `UICONTROL` 및 `DNL` 지역화 태그는 예외입니다.
* 셀에 `align="left"`, `align="center"` 또는 `align="right"`을(를) 사용하는 경우
필요. HTML 테이블에는 중첩 테이블이 포함될 수 없습니다.
* 여는 태그의 HTML 테이블 레이아웃 설정:
  `<table style="table-layout:auto">` 또는
  `<table style="table-layout:fixed">`.
* 테두리 없는 1행 HTML 테이블의 경우
  `<tr style="border: 0;">`.

## 코드

* 인라인 코드: 단일 백틱.
* 펜싱된 블록: 구문용 선택적 언어가 있는 트리플 백틱
강조 표시(` ```python `, ` ```javascript ` 등).

## 메모/경고 블록

사용자 정의 블록 따옴표 구문, 블록당 한 유형, 블록 따옴표 행 사이의 공백
태그와 본문:

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

지원되는 형식: `NOTE`, `TIP`, `IMPORTANT`, `CAUTION`, `WARNING`,
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## 비디오 포함

Experience League이 `[!VIDEO]` 블록에 직접 MP4 또는 YouTube 비디오 임베드를 지원하지 않습니다. 애니메이션 미리 보기가 필요한 경우 페이지의 형제 `.resources` 폴더에 있는 GIF을 대신 사용하고 필요한 경우 인라인 HTML으로 가운데로 맞춥니다.

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

로컬 MP4 파일, 원격 MP4 파일 또는 YouTube URL에 `[!VIDEO]`을(를) 사용하지 마십시오. 게시 파이프라인이 이를 거부하고 CI가 실패합니다.

## UICONTROL 태그

UI 요소 이름(단추 레이블, 메뉴 항목, 필드 이름)을 인라인
로컬라이제이션 파이프라인은 번역된 문자열을 확인할 수 있고 중단됩니다.
영어 레이블로 돌아가기(없는 경우):

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

설명 텍스트(메뉴)에서 참조하는 모든 리터럴 UI 레이블에 사용합니다.
항목, 버튼 이름, 대화 상자 제목, 패널 이름).

## DNL 태그(&quot;현지화 안 함&quot;)

제품 이름, 타사 기능 이름 또는
기계로 번역되지 않음:

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

이 리포지토리에서 `[!DNL Substance 3D Designer]`과(와) 같은 제품 이름에 사용하십시오.
`[!DNL Substance 3D Sampler]`님, 페이지당 첫 번째/눈에 띄는 언급에서,
기존 페이지와 일치합니다.

## 인라인 HTML

Raw HTML이 허용됩니다(이 리포지토리의 `markdownlint_custom.json`은(는) MD033을 비활성화합니다.
특히 이러한 이유 때문에) : 그러나 다음의 과정을 통해서만 안정적으로 보존된다.
태그가 `data-preserve-html="true"`을(를) 포함하는 경우 파이프라인입니다. 인라인 HTML 예약
일반 마크다운에서 표현할 수 없는 경우(표 셀 내부의 이미지/목록)
Markdown의 일반적인 대체물이 아닌 `<span id="...">`개의 앵커)입니다.

## 전문

에서 사용하는 정확한 블록에 대해서는 AGENTS.md의 &quot;Page front matter&quot; 섹션을 참조하십시오.
이 리포지토리의 일반 콘텐츠 페이지와 리포지토리 수준의 `metadata.md`
상속된 필드.
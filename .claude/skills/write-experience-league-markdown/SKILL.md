---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ec58342925d3e608b0180b67a1e20ffaeb1f306a
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 5%

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
* 리터럴 텍스트(실제 HTML 아님)로 사용된 **꺾쇠 괄호**&#x200B;는 인코딩해야 합니다.
  `<placeholder>` → `&lt;placeholder&gt;`입니다.
* 워드 프로세서에서 붙여넣은 **스마트 따옴표**&#x200B;를 인코딩해야 합니다.
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
용어 바로 앞에 `<span id="anchor-id"></span>`을(를) 명시합니다. —
이 리포지토리 전체에 사용된 패턴은 `help/glossary/glossary.md`을(를) 참조하십시오.
* `TOC.md` 섹션 앵커가 머리글/목록 뒤에 `{#section-id}` 구문을 사용합니다.
레이블(예: `Getting started{#getting-started}`).

## 이미지

* `![Alt text](path/to/image.png "Optional hover title")`.
* 선택적 크기 조정/최적화 쿼리 매개 변수가 지원됩니다.
  `![Adobe logo](assets/logo.png?width=750&format=png&optimize=medium)`.
* **대체 텍스트는 밑줄을 포함할 수 없습니다**. 올바르게 렌더링되지 않습니다.
대신 하이픈이나 공백을 사용하십시오.
* `<page-name>.resources/`에 있는 페이지별 이미지, 공유/앱 아이콘
`help/assets/`에 있습니다(CLAUDE.md 참조).

## 표

* 하이픈 헤더 구분 기호가 있는 파이프로 구분:

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* 빈 줄이 표 앞에 와야 합니다. 그렇지 않으면 표로 렌더링되지 않습니다.
* 표에는 여러 단락 또는 복잡한 블록 내용을
셀 — 이 레포에 표 셀 내의 이미지/목록이 필요한 경우(예:
`overview.md`의 비교 테이블), 인라인 HTML으로 돌아갑니다.
(`<div>`, `<b>`, `<ul>`/`<li>`)(각 항목 `data-preserve-html="true"` 포함)
파이프라인이 찢어지지 않도록 태그를 지정합니다. 그 기존 패턴을 따르세요
필요한 경우가 아니면 새 인라인 HTML을 인벤터리할 수 없습니다.

## 코드

* 인라인 코드: 단일 백틱.
* 펜싱된 블록: 구문용 선택적 언어가 있는 트리플 백틱
강조 표시(` `&#x200B;``python `, ` ``&#x200B;`javascript ` 등).

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

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

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

에 사용된 정확한 블록에 대해서는 CLAUDE.md의 &quot;페이지 앞부분&quot; 섹션을 참조하십시오.
이 리포지토리의 일반 콘텐츠 페이지와 리포지토리 수준의 `metadata.md`
상속된 필드.
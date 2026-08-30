---
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---
# CLAUDE.md

이 파일은 이 리포지토리에서 코드를 사용하여 작업할 때 클라우드 코드(claude.ai/code)에 대한 지침을 제공합니다.

&#x200B;# Substance 3D Designer 설명서

이 저장소에는 Substance 3D Designer 설명서가 포함되어 있습니다. 응용 프로그램 코드, 빌드 단계 또는 테스트 도구 모음이 없습니다. 리포지토리는 *is* 콘텐츠를 마크다운으로 작성하고 [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en)에 게시했습니다.

&#x200B;# 저장소 구조

* `help/` - 목차를 미러링하도록 구성된 모든 문서 콘텐츠.
* `help/guide/TOC.md` — 목차. 모든 항목은 페이지의 Markdown 파일에 대한 상대 링크(`/help/...`에 있음)입니다. `TOC.md`은(는) 페이지 트리 메타데이터(`user-guide-title`, `breadcrumb-title`, `nudge`, `{#section-id}`과(와) 같은 섹션 앵커)도 포함합니다.
* `help/assets/` — 레거시 공유 이미지 폴더. 이제 페이지별 미디어가 페이지당 `<md-file-name>.resources/` 형제 폴더에 있습니다(아래 폴더/TOC 규칙 참조). 아무 페이지에서도 참조되지 않은 일부 남아 있는 이미지만 남아 있습니다. 새 이미지를 여기 말고 사용 중인 페이지의 `.resources` 폴더에 넣으십시오.
* `help/glossary/glossary.md` — `#term` 조각을 통한 상호 연결에 사용되는 앵커 범위(`<span id="term"></span>`)를 사용하여 알파벳순으로 구성된 하나의 큰 용어집 페이지입니다.
* `metadata.md` — 리포지토리 수준 프런트 문제(클라우드/솔루션/제품 ID, `git-repo` 등) `TOC.md`마다 상속됩니다. 리포지토리 전체 메타데이터 변경을 위해서만 이 설정을 편집합니다. 페이지별 메타데이터는 해당 페이지의 자체 앞면에 포함됩니다.
* `redirects.csv`, `linkcheckexclude.json`, `markdownlint_custom.json`, `pipeline.opts` - 게시 파이프라인 구성(리디렉션, 링크 확인 예외, 린트 규칙 재정의, 파이프라인 옵션).
* `fix-image-names.py` — `help/assets` 이미지의 이름을 괄호 접미사(예: `foo(1).png` → `foo_1.png`)로 변경하고 일치하도록 모든 마크다운 참조를 다시 쓰는 일회용 유틸리티입니다. 일반 작업 과정에 포함되지 않습니다. 파일 이름이 다시 나타날 때만 수동으로 실행하십시오.

## 폴더/목차 규칙

`help/guide/TOC.md`의 모든 항목에 대해:
* `help/` 아래에 TOC와 같은 중첩 뒤에 해당 폴더가 있습니다.
* 이 폴더에는 kebab-case 버전의 페이지 제목이라는 Markdown 파일이 포함되어 있습니다.
* 페이지가 특정 미디어(이미지, GIF, 비디오)인 경우 해당 페이지는 `<md-file-name>.resources`(이)라는 형제 하위 폴더에 있습니다.

페이지를 추가하거나 이동할 때 `TOC.md`과(와) 폴더 레이아웃을 함께 업데이트하십시오. 동기화가 유지되어야 합니다.

## 노드 참조 페이지

노드 라이브러리 트리(예: `help/compositing-graphs/nodes-reference-for-com/node-library/<category>/<node>/<node>.md`)는 고유한 일관된 레이아웃을 가진 고유한 페이지 유형입니다. 아이콘/설명 HTML 테이블, 뒤에 고정된 `## Inputs` / `## Outputs` / `## Parameters` 테이블(`#inputs`/`#outputs`/`#parameters`) 및 `## Examples` 갤러리가 있습니다. `.../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md`을(를) 모델로 하여 아래의 일반 콘텐츠 페이지 블록이 아닌 **최소** 앞면(`title` + `description`만)을 사용합니다. 포함된 미디어(아이콘, 예제 이미지/GIF)가 상대적으로 참조되는 페이지 옆의 형제 `<node-name>.resources/` 폴더에 있습니다. 전체 작성 템플릿에 `generate-node-documentation` 스킬(있는 경우)을 사용합니다.

## 페이지 앞면 문제

일반 컨텐츠 페이지에서는 다음과 같은 주요 블록을 사용합니다.

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

`description`을(를) 정확하고 간결하게 유지합니다. SEO/검색 스니펫에 사용됩니다.

&#x200B;# 컨텐트 작성 규칙

* 영어는 진리의 원천이다; 다른 모든 언어는 그것으로부터 번역된다.
* 다른 문서 페이지에 대한 모든 링크는 **상대** 링크여야 하고 외부 리소스에 대한 모든 링크는 **절대** 링크여야 합니다.
* 콘텐츠는 Experience League의 사용자 지정 확장/변경 사항이 있는 GitHub 풍의 마크다운에 기록되며 [여기](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown)에 문서화되어 있습니다. 자세한 내용은 `write-experience-league-markdown` 스킬(있는 경우)을 사용하세요.
* 제출된 모든 변경 사항은 CI에서 자동화된 린트 검사 및 링크 유효성 검사를 거칩니다(아래 참조). 규칙이 적용되거나 링크가 수정되어야 한다고 가정하기 전에 `markdownlint_custom.json` 및 `linkcheckexclude.json`을(를) 확인하십시오.

&#x200B;# 검증 / CI

* `.github/workflows/validate-articles.yml`은(는) PR에서 실행되고 `main`에게 푸시하여(그리고 `retest` PR 주석을 통해) 공유된 `Adobe-Enterprise-Docs/workflows` 재사용 가능한 워크플로를 호출하여 마크다운을 lint하고 링크를 확인합니다. 이 문서에는 로컬에 해당하는 스크립트가 없습니다. CI는 합격/불합격의 진원입니다.
* `.github/workflows/mirror.yml`은(는) 푸시 시 공용 리포지토리에 `main`을(를) 미러링합니다. 콘텐츠 변경 내용이 수정될 필요가 없는 인프라입니다.
* `markdownlint_custom.json`은(는) 공유 `markdownlint.json` 규칙 집합을 확장하고 Experience League의 사용자 지정 마크다운 확장(예: 인라인 HTML, 비표준 강조)과 충돌하는 여러 규칙(MD005, MD007, MD018, MD032, MD033, MD034, MD037, MD040)을 사용하지 않도록 설정합니다. 이러한 사용 안 함 규칙을 충족하기 위해 콘텐츠를 &quot;수정&quot;하지 마십시오.
* `linkcheckexclude.json`은(는) 링크 확인기가 건너뛰어야 하는 링크 패턴(현재 `example.com`/`example-end.com`)을 화이트리스트에 나열합니다.

&#x200B;# 작업 규칙

* 릴리스 노트 중심의 설명서입니다. 릴리스 노트는 `help/release-notes/` 아래에 있으며, 버전당 하나의 폴더(예: `version-16-0`)와 `all-changes` 및 `old-versions`개의 집계 페이지를 포함합니다. 새 릴리스를 추가할 때 기존 버전 폴더를 템플릿으로 따르십시오.

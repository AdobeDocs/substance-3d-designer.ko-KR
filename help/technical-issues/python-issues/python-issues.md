---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: 플러그인 및 API 문제를 포함하여 Substance 3D Designer의 Python 스크립팅 문제를 해결합니다.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Python 문제
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Python 문제

이 페이지에는 Python에서 구현된 기능뿐만 아니라 Substance 3D Designer [Python API](../../scripting/scripting.md)와 관련된 기술 문제가 나열되어 있으며 각각에 대한 문제 해결 단계를 제공합니다.

Python에 구현된 기능에는 [탐색기](../../interface/the-explorer-window/the-explorer-window.md)의 도구 모음에 있는 [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[보내기](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) 작업과 그래프에서 사용하지 않는 노드를 제거하는 도구가 포함됩니다.

## &#39;QtForPython&#39; 모듈을 로드하지 못합니다

<b>![(오류)](../../assets/error.svg) 문제</b>

&#39;QtForPython&#39; Python 모듈을 로드하지 못하여 Python에 구현된 기능(예: [탐색기](../../interface/the-explorer-window/the-explorer-window.md)의 도구 모음에서 [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[보내기](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) 작업 및 그래프에서 사용하지 않는 노드를 제거하는 도구)이 누락됩니다.

또한 많은 [Python 플러그인](../../scripting/plugin-basics/plugin-basics.md)이 로드되지 않거나 예상대로 작동하지 않습니다.

<b>![(틱)](../../assets/check.svg) 권장 단계</b>

Designer의 QtForPython 설치 및 해당 종속 항목과 시스템의 기존 설치 항목이 충돌할 수 있습니다.

[QtForPython](https://doc.qt.io/qtforpython-5/index.html)&#x200B;([PySide2](https://pypi.org/project/PySide2/)) 및 [Shiboken2](https://pypi.org/project/shiboken2/)의 다른 시스템 설치를 제거합니다.

또는 QtForPython의 시스템 전체 설치 대신 Python *가상 환경* 또는 [rez](https://github.com/AcademySoftwareFoundation/rez)와 같은 *패키지 관리자*&#x200B;를 사용할 수도 있습니다.

---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Substance 3D Designer의 시스템 요구 사항을 검토하여 컴퓨터가 필요한 사양을 충족하는지 확인하십시오.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 시스템 요구 사항
user-guide-description: ''
user-guide-title: ''
source-git-commit: ec787363bab8318804a71d6cf7c5484fc67a987e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# 지원되는 시스템

다음은 애플리케이션에서 지원하는 하드웨어 및 시스템 목록입니다.

## Windows

|  | 최소 | 권장 | 최적 |
| --- | --- | --- | --- |
| <b>OS</b> | Windows 11 64비트 버전 23H2 | Windows 11 64비트 버전 24H1 | Windows 11 64비트 버전 24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8GB | 16GB | 24GB |
| <b>RAM</b> | 16GB | 32GB | 64GB |
| <b>저장소</b> | 30GB의 사용 가능한 공간이 있는 SSD | 50GB의 사용 가능한 공간이 있는 SSD | 70GB의 사용 가능한 공간이 있는 SSD |

### macos

|  | 최소 | 권장 | 최적 |
| --- | --- | --- | --- |
| <b>OS</b> | macOS 소노마 | macOS 타호 | macOS 타호 |
| <b>CPU</b> | Apple | Apple | Apple M4 Pro |
| <b>GPU</b> | Apple | Apple | Apple M4 Pro |
| <b>RAM</b> | 16GB | 32GB | 64GB |
| <b>저장소</b> | 30GB의 사용 가능한 공간이 있는 SSD | 50GB의 사용 가능한 공간이 있는 SSD | 70GB의 사용 가능한 공간이 있는 SSD |

### 리눅스

| 기업 | 증기 |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## 일반 권장 사항

* 편안한 환경에서 작업하려면 해상도가 1메가픽셀보다 크고 1280픽셀보다 넓은 모니터를 사용하는 것이 좋습니다.
* 대부분의 Substance 앱은 RHEL8/9 호환을 위해 OpenSSL 1.1.1을 사용합니다. 최신 OpenSSL 버전을 사용하는 시스템의 경우 수동으로 제공해야 합니다.
* *<b>MacOS 10.15</b>(Catalina)에서 실행하기 위해* 버전 <b>2019.x</b> 이상만 공증되었습니다.
* OpenGL 3.3 컨텍스트를 사용할 수 있는 경우 <b>원격 데스크톱</b> 연결이 가능합니다. OpenGL 1.4 컨텍스트만 제공하므로 <b>Nvidia Quadro</b>에서는 작동하지만 Nvidia GeForce에서는 *작동 안 함*&#x200B;입니다. 문제가 있는 경우 <b>VNC</b>/<b>Teamviewer</b>와 같은 대체 솔루션을 사용하는 것이 좋습니다.
* <b>Steam</b> 버전 사용자는 Designer의 <b>Steam 오버레이</b>를 *비활성화*&#x200B;해야 합니다. 활성 시 성능 문제가 발생할 수 있습니다.

## 지원되는 GPU

아래는 애플리케이션과 호환되는 GPU 목록입니다 .

* NVIDIA GeForce GTX 1060 이상
* NVIDIA Quadro P2200 이상
* AMD Radeon RX 580 이상
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR(Windows만 해당)**
> 
> 복잡한 그래프 렌더링, 3D 보기에서 렌더링, 3D 보기에서 장면 내보내기 등과 같이 GPU에서 많은 계산을 수행하는 동안 최상의 전반적인 안정성을 위해 <b>시간 초과 감지 및 복구(TDR)</b> 값이 설명서의 [이 페이지](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)의 권장 사항과 일치하는지 확인하는 것이 좋습니다.

## 지원되지 않는 구성

<b>Windows</b>

* 가상 컴퓨터가 지원되지 않습니다.
* Windows Server가 지원되지 않습니다.

<b>macOS</b>

* Intel 기반 macOS 시스템은 지원되지 않습니다.
* 공식 Apple 구성만 지원됩니다.
* eGPU는 현재 지원되지 않으며 안정성 문제가 있을 수 있습니다.

<b>Linux</b>

* Linux의 Mesa 드라이버는 지원되지 않습니다.

<b>모든 플랫폼</b>

* 통합 GPU는 x86-64(Intel, AMD) CPU에서 지원되지 않습니다.
* 그래픽 드라이버에 대한 Designer 호출을 차단하는 서드파티 소프트웨어와 함께 Designer을 사용하는 것은 지원되지 않습니다. 이러한 소프트웨어에는 다음이 포함됩니다.
  * 색 보정, 카메라 효과 등을 적용하는 리셰이더와 같은 후처리 인젝터입니다.
  * 사용자 정의 십자선, GPU 성능 지표, 비디오 스트리밍용 스킨 등의 화면 오버레이...

## 최소 GPU 드라이버 버전

다음은 응용 프로그램을 문제 없이 실행하는 데 필요한 최소 GPU 드라이버 버전 목록입니다. 이 목록은 새 버전 릴리스부터 변경될 수 있습니다.

새 드라이버를 다운로드하려면 [GPU에 오래된 드라이버가 있음](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers)을 참조하십시오.

| OS | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | 지원되지 않음 |

>[!NOTE]
>
> **Mac OS**&#x200B;에서 GPU 드라이버는 운영 체제에서 제공됩니다. 최신 드라이버에 액세스하려면 최신 버전의 OS로 업데이트하십시오.

## 베이킹용 GPU 광선 추적

Optix 또는 DXR을 통해 GPU 광선 추적을 활성화하려면 위에 권장되는 드라이버를 설치해야 합니다.

<b>DXR</b>에는 다음과 같은 최소 구성이 필요합니다.

* <b>Windows 10</b> 버전 1809에서 자세한 내용은 [이 페이지](https://experienceleague.adobe.com/ko/docs/substance-3d/bakers/features/gpu-raytracing)를 참조하세요.
* <b>Pascal 아키텍처의 GPU</b>(Nvidia GeForce 10XX)

>[!TIP]
>
> GPU 광선 추적은 NVIDIA GeForce RTX 또는 NVIDIA Quadro RTX GPU와 같은 전용 광선 추적 하드웨어에서 최적으로 실행됩니다.

## 태블릿 사용

<b>Windows</b>의 태블릿 사용자는 다음 페이지에 설명된 설정을 적용하여 가장 안정적인 경험을 얻어야 합니다. [펜 및 태블릿 구성](https://experienceleague.adobe.com/ko/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

## 언어

소프트웨어 인터페이스는 다음 언어로 제공됩니다.

* 독일어(Deutschland)
* 영어(미국)
* 스페인어(스페인어)
* 프랑스어(프랑스)
* 이탈리아어(이탈리아)
* Português (Brasil)
* 日本語（日本）
* 한국어(한국)
* 简体中文（中国)

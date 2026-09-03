---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: Substance 3D Designer을 시작할 수 없는 문제를 해결하고 응용 프로그램을 시작할 수 있는 솔루션을 찾습니다.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 애플리케이션이 시작되지 않음
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---


# 애플리케이션이 시작되지 않음

이 페이지에서는 Substance 3D Designer이 올바르게 시작되지 않는 일반적인 원인을 나열하고 각 운영 체제에 대한 문제 해결 단계를 제공합니다.

[Designer 15.0 이상](#version-15-0)

[윈도우 /](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[리눅스](#linux)

## Designer 15.0 이상

<b>[(오류)](application-does-not-start.resources/error.svg) 문제</b>

Designer 버전 15.0 이상이 통합 GPU(iGPU) 및 개별 GPU(dGPU)가 모두 있는 시스템에서 시작되지 않습니다.

<b>[(틱)](application-does-not-start.resources/check.svg) 권장 단계</b>

iGPU의 그래픽 드라이버를 업데이트합니다. 다음 위치에서 최신 드라이버를 찾을 수 있습니다. [인텔](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## 윈도우 /

**![(오류)](application-does-not-start.resources/error.svg) 문제**

Windows 10 또는 Windows 11을 사용하는 시스템에서 Substance 3D Designer을 시작할 수 없습니다.

**![(틱)](application-does-not-start.resources/check.svg) 권장 단계**

라이선스 유효성 검사 프로세스에 사용된 *오래된* `libeay32.dll` 라이브러리로 인해 Windows 10 또는 Windows 11에서 이전 버전의 Designer을 시작하지 못할 수 있습니다.

다음 단계에 따라 라이브러리를 [여기](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows)&#x200B;(32비트 Windows용 파일 선택)에 배포된 것과 같은 *업데이트된 버전*(으)로 바꾸려고 할 수 있습니다.

1. Designer 설치 디렉터리에서 `libeay32.dll` 파일 찾기
1. 나중에 복원해야 할 경우 파일을 안전한 위치에 백업하십시오
1. 파일을 업데이트된 버전으로 바꿉니다.
1. Designer 시작

>[!WARNING]
>
> 지원되지 않는 구성
> 
> Windows 10은 지원되지 않습니다. [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md) 페이지에서 자세히 알아볼 수 있습니다.
> 
> 유지 관리 기간이 만료된 Designer 버전은 지원되지 않습니다. OS 업그레이드와 같이 시스템에 중대한 변경이 발생하면 이러한 버전이 더 이상 안정적으로 실행되지 않을 수 있습니다.

## Windows 7/8/8.1

**![(오류)](application-does-not-start.resources/error.svg) 문제**

Substance 3D Designer이 Windows 7, Windows 8 또는 Windows 8.1을 사용하는 시스템에서 시작되지 않습니다.

**![(틱)](application-does-not-start.resources/check.svg) 권장 단계**

버전 **11.3.0** 업데이트의 일부로 Windows 10보다 낮은 Windows 버전에서 *호환성 중단*&#x200B;인 여러 라이브러리, 도구 및 SDK를 업그레이드했습니다.

Microsoft 자체는 더 이상 주류용 Windows의 이전 버전을 지원하지 않으므로 *적극* Windows 10으로 업그레이드하는 것이 좋습니다([여기](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information) 및 [여기](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1) 참조). 따라서 이러한 버전을 계속 사용하면 *보안 문제*&#x200B;가 발생합니다.\
Windows 10으로 업그레이드할 수 없는 경우 *Designer*&#x200B;과거&#x200B;*버전&#x200B;**11.2.2**&#x200B;의 설치를 업데이트하지 마십시오*.

>[!WARNING]
>
> 지원되지 않는 구성
> 
> Windows 7, Windows 8 및 Windows 8.1은 *공식적으로 지원되지 않습니다*. [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md) 페이지에서 자세히 알아볼 수 있습니다.

## 리눅스

<b>[(오류)](application-does-not-start.resources/error.svg) 문제</b>

홈 화면을 닫고 기본 창을 표시할 때 충돌이 발생합니다.

<b>[(틱)](application-does-not-start.resources/check.svg) 권장 단계</b>

Designer에서 Python 구성 요소를 로드할 수 없습니다. 자체 라이브러리가 아닌 시스템의 <b>libffi.so</b> 라이브러리를 로드하기 때문입니다.

Designer에서 자체 라이브러리를 로드하도록 하려면 Designer의 설치 디렉터리에서 이 명령을 사용하여 `%command%`을(를) Designer을 실행하는 명령으로 바꾸십시오.

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


Python 버전 번호는 실행 중인 Designer 버전에 따라 다릅니다.

* 14.0.0 미만: python3.9
* 12.1.0 미만: python3.7

+++Steam 실행 옵션
Steam에서 Designer을 시작하는 Linux 사용자는 아래와 같이 Designer의 실행 옵션에서 LD\_PRELOAD 명령을 설정할 수 있습니다.

이 작업이 완료되면 향후 모든 세션에서 일반적으로 Steam을 통해 Designer을 시작할 수 있습니다.

![Steam 실행 옵션](application-does-not-start.resources/application-does-not-start-01.jpg "Steam 실행 옵션")



+++

**![(오류)](application-does-not-start.resources/error.svg) 문제**

Designer의 Steam 버전이 오류 메시지로 시작되지 않습니다.

**![(틱)](application-does-not-start.resources/check.svg) 권장 단계**

대신 Steam 응용 프로그램을 로그하여 오류 메시지를 얻을 수 있습니다.

[여기](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260)에서 권장하는 대로 Steam을 완전히 닫은 다음 터미널에서 다음 명령을 실행하십시오(또는 이 명령에 대한 바로 가기 만들기).

```
steam 2>&1 | tee /path/to/logfile
```


<b>![(오류)](application-does-not-start.resources/error.svg) Issu</b><b>e</b>

`<b>xcb</b>` 플러그 인을 로드할 수 없습니다. 명령줄에 다음 메시지가 표시됩니다.

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![(틱)](application-does-not-start.resources/check.svg) 권장 단계**

일부 필수 패키지가 누락되었습니다. Designer 설치 디렉터리에서 다음 명령을 실행합니다.

```
ldd libQt5XcbQpa.so.5
```


인쇄된 목록에서 `not found`(으)로 보고된 패키지를 확인한 다음 누락된 각 패키지에 대해 다음 명령을 실행하십시오.

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![(오류)](application-does-not-start.resources/error.svg) 문제</b>

Designer을 시작할 때 다음 오류가 발생합니다.

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Designer에서 로드한 시스템 라이브러리가 Designer의 자체 <b>libcrypto.so.1.1</b> 라이브러리와 호환되지 않습니다.

<b>![(틱)](application-does-not-start.resources/check.svg) 권장 단계</b>

시스템의 라이브러리가 대신 사용되도록 Designer 설치 디렉터리에서 <b>`libcrypto.so.1.1`</b> 라이브러리를 제거하십시오.

>[!NOTE]
>
> 이 해결 방법은 시스템에 자체 libcrypto.so.1 라이브러리가 있는 경우에만 작동합니다. 최근 배포에서는 <b>libxcrypt-compat</b>과(와) 같은 호환성 패키지를 설치해야 할 수 있습니다.

<b>![(오류)](application-does-not-start.resources/error.svg) 문제</b>

Substance 3D Designer이 Linux의 *Arch 기반* 배포를 사용하는 시스템에서 시작되지 않습니다.

**![(틱)](application-does-not-start.resources/check.svg) 권장 단계 *(![(경고)](application-does-not-start.resources/warning.svg) 불안정, AMD GPU만 해당!)***

**progl**([AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO) 드라이버의 일부)을 설치하고 Designer을 시작해 보십시오. 응용 프로그램 실행 명령에서 `progl` 접두사를 사용하여 이 작업을 수행할 수 있습니다.

```
progl <designer-application-path>
```


`progl`이(가) 불안정할 수 있습니다. 따라서 이 작업은 *마지막 수단*&#x200B;으로 시도해야 합니다.

>[!WARNING]
>
> Linux의 Arch 기반 배포판은 *지원되지 않습니다*&#x200B;입니다. [시스템 요구 사항](../../getting-started/system-requirements/system-requirements.md) 페이지에서 자세히 알아볼 수 있습니다.

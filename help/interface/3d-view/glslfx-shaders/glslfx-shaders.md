---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Substance 3D Designer 3D 보기에서 GLSLFX 셰이더를 사용하여 재질 렌더링 및 미리 보기 효과를 사용자 정의할 수 있습니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GLSLFX 셰이더
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# GLSLFX 셰이더

GLSLFX 파일은 응용 프로그램과 glsl 셰이더 파일 간의 브리지를 만듭니다.\
이렇게 하면 코드를 수정하지 않고도 모든 glsl 셰이더를 사용할 수 있습니다.

## 승_File Format

GLSLFX 파일 형식은 XML 파일입니다. 댓글은 지원됩니다.

### 헤더 및 루트 노드

XML 루트 노드 요소의 이름은 <b>glslfx</b>입니다.

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### 본문

#### 기법

기법을 설명하는 XML 요소입니다. 기법은 현재 FX의 변형입니다. GLSLFX에는 여러 기법이 포함될 수 있지만 적어도 하나의 기법이 정의되어야 합니다.

형상은 응용 프로그램에서 정의한 기술 중 하나로 렌더링됩니다.

+++XML 요소 정의
<b>이름:</b> 기법

<b>특성:</b>

* 이름: 기법의 이름을 지정하는 데 사용되는 문자열

+++

XML 요소에는 여러 개의 자식이 있을 수 있습니다. 기법에 정의된 요소는 전역으로 정의된 요소를 재정의합니다.

예를 들어 일부 유니폼 값을 재정의하고 이 기법에 대한 FX 변형을 얻는 데 사용합니다.

#### 렌더링 통과

렌더링 패스를 설명하는 XML 요소 렌더링 패스는 형상의 렌더링을 설명합니다.

한 기법에는 순차적으로 실행되는 여러 렌더링 패스가 포함될 수 있습니다. 렌더링 과정이 없는 기법은 &#39;화면상의&#39; 렌더링 과정이 포함된 기법과 동일합니다.

렌더링 패스에 정의된 요소는 상위 기법에 정의된 요소를 재정의합니다.

+++XML 요소 정의
<b>이름:</b> 통과

<b>특성:</b>

* output

* 오프 스크린: 렌더링이 사용자 정의 렌더링 대상으로 수행됩니다

* 화면: 렌더링이 기본 렌더링 대상으로 수행됩니다

+++

#### 셰이더

각 유형에 대한 GLSL 셰이더 파일을 설정합니다.

XML 요소 정의:

+++XML 요소 정의
<b>이름:</b> 셰이더

<b>특성:</b>

* 유형: GLSL 셰이더 유형;

* filename: glsl 셰이더 파일의 경로입니다. GLSLFX 파일에 대해 절대 또는 상대일 수 있습니다.

* primitiveType: 프리미티브를 렌더링하는 메서드입니다.


| &#39;type&#39; 값 | 설명 |
| --- | --- |
| 꼭지점 | 버텍스 셰이더 |
| 모양 | 지오메트리 셰이더 |
| tess\_control | 테셀레이션 컨트롤 셰이더 |
| tess\_eval | 테셀레이션 평가 셰이더 |
| 파편 | 프래그먼트 셰이더 |



| &#39;primitiveType&#39; 값 | 설명 |
| --- | --- |
| 포인트 | 포인트로 렌더링 |
| 리넬루프 | 선 루프로 렌더링 |
| patch[1..N] | [1..N] 정점을 사용하여 패치로 렌더링 |


+++

#### 속성

OpenGL 상태의 일부를 설정할 수 있습니다.

+++XML 요소 정의
<b>이름:</b> 속성

<b>특성:</b>

* 이름: 설정할 속성의 이름입니다. 이름은 OpenGL 함수 또는 glEnum 이름을 기반으로 합니다.
  * 구문 열거형: 소문자에는 &#39;GL\_&#39; 접두사가 없습니다. 예: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;
  * 함수 구문: &#39;gl&#39; 접두사가 없는 경우에는 소문자로, 모든 단어가 &#39;\_&#39; 문자로 구분됩니다. 예: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* 구문 열거형: 소문자에는 &#39;GL\_&#39; 접두사가 없습니다. 예: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;

* 함수 구문: &#39;gl&#39; 접두사가 없는 경우에는 소문자로, 모든 단어가 &#39;\_&#39; 문자로 구분됩니다. 예: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* 값: 등록 정보의 값입니다.


| &#39;name&#39; 값 | &#39;value&#39; 값 | 설명 |
| --- | --- | --- |
| blend\_enabled | 부울 | 혼합 모드 활성화/비활성화 |
|  | true |  |
|  | 거짓 |  |
| blend\_func | 문자열, 문자열 | 소스 및 대상 혼합 함수 설정 |
|  | 0 | OpenGL 열거형 GL\_ZERO의 경우 |
|  | 1 | OpenGL 열거형 GL\_ONE의 경우 |
|  | src\_color | (OpenGL 열거형 GL\_SRC\_COLOR용) |
|  | one\_minus\_src\_color | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | (OpenGL 열거형 GL\_DST\_COLOR용) |
|  | one\_minus\_dst\_color | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | (OpenGL 열거형 GL\_SRC\_ALPHA) |
|  | one\_minus\_src\_alpha | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alpha | OpenGL 열거형 GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_DST\_ALPHA |
|  | constant\_color | (OpenGL 열거형 GL\_CONSTANT\_COLOR) |
|  | one\_minus\_constant\_color | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | 상수\_알파 | (OpenGL 열거형 GL\_CONSTANT\_ALPHA) |
|  | one\_minus\_constant\_alpha | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | OpenGL 열거형의 경우 GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | (OpenGL 열거형 GL\_SRC1\_COLOR용) |
|  | one\_minus\_src1\_color | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | (OpenGL 열거형 GL\_SRC1\_ALPHA) |
|  | one\_minus\_src1\_alpha | OpenGL 열거형의 경우 GL\_ONE\_MINUS\_SRC1\_ALPHA |
| curl\_face\_enabled | 부울 | 얼굴 컬링 활성화/비활성화 |
|  | true |  |
|  | 거짓 |  |
| 오려내기\_얼굴\_모드 | 문자열 | 얼굴 컬링 모드 설정 |
|  | 맨 앞으로 | (OpenGL 열거형 GL\_FRONT용) |
|  | 뒷면 | (OpenGL 열거형 GL\_BACK의 경우) |
|  | front\_and\_back | OpenGL 열거형의 경우 GL\_FRONT\_AND\_BACK |
| 깊이\_func | 문자열 | 깊이 비교 기능 설정 |
|  | 사용 안 함 | (OpenGL 열거형 GL\_NEVER용) |
|  | 더 적은 | (OpenGL 열거형 GL\_LESS) |
|  | 르쿠알 | (OpenGL 열거형 GL\_LEQUAL용) |
|  | equal | (OpenGL 열거형 GL\_EQUAL의 경우) |
|  | 주목할만 해 | (OpenGL 열거형 GL\_NOTEQUAL용) |
|  | 대담해 | (OpenGL 열거형 GL\_GEQUAL용) |
|  | 큼 | (OpenGL 열거형 GL\_GREATER) |
|  | 항상 | (OpenGL 열거형 GL\_ALWAYS) |


+++

#### 유니폼

전역적으로 또는 상위 기술에서 정의된 일부 유니폼을 재정의할 수 있습니다. 이렇게 하면 이 기술 또는 렌더링 패스에 대한 셰이더 동작을 변경할 수 있습니다.

해당 정의에 대한 자세한 내용은 아래의 <b>유니폼</b> 섹션을 참조하십시오.

+++예


+++

## 렌더링 대상

&#39;오프스크린&#39; 렌더링 패스의 경우 렌더링 패스에 렌더링 대상을 정의해야 합니다.

+++XML 요소 정의
<b>이름:</b> 출력

<b>특성:</b>

* 첨부 파일: OpenGL 이름에서 영감을 받은 OpenGL 첨부 지점:\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
  GL\_깊이\_첨부 파일 => &#39;깊이&#39;

첨부 파일: OpenGL 이름에서 영감을 받은 OpenGL 첨부 지점:\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
GL\_깊이\_첨부 파일 => &#39;깊이&#39;

* 이름: 렌더링 대상의 이름입니다.\
  이 렌더러는 이후 렌더링 패스에서 이 렌더링 대상을 샘플러로 바인딩하는 데 사용할 수 있습니다.

이름: 렌더링 대상의 이름입니다.\
이 렌더러는 이후 렌더링 패스에서 이 렌더링 대상을 샘플러로 바인딩하는 데 사용할 수 있습니다.

* 형식: 렌더링 대상의 내부 형식입니다.

형식: 렌더링 대상의 내부 형식입니다.

* clear: 지우기 값을 정의하는 선택적 속성입니다.\
  이 값이 있는 경우 렌더링 패스가 시작될 때 렌더링 대상이 이 값으로 지워집니다.\
  없으면 렌더링 대상이 이전 내용을 유지합니다.

+++

>[!NOTE]
>
> 색상 렌더링 대상은 &#39;화면상의&#39; 렌더링 패스에서 금지되어 있지만 깊이 렌더링 대상은 모든 렌더링 패스와 공유할 수 있습니다(단, 장면의 여러 재질을 혼합할 때 렌더링이 중단될 수 있음).

<b>형식 정보</b>

깊이 형식의 경우 모든 깊이 전용(스텐실 없음) OpenGL 형식이 지원됩니다.

* GL\_깊이\_COMPONENT16 => &#39;깊이26&#39;
* GL\_깊이\_COMPONENT24 => &#39;깊이34&#39;
* GL\_깊이\_COMPONENT32 => &#39;깊이42&#39;
* GL\_깊이\_COMPONENT32F => &#39;깊이42f&#39;

색상 형식의 경우 이름은 &#39;GL\_&#39; 접두어가 없는 OpenGL 열거형 이름을 기반으로 합니다(소문자 구분).\
세 가지 채널 포맷(RGB)은 지원되지 않으며, 대신 RGBA 포맷을 사용합니다.\
지원되는 채널당 비트 심도 수:

* 정규화된 부호 없는 정수: 8, 16
* 부동 소수점: 16, 32

이러한 규칙에 대한 예외는 지원되는 GL\_R11F\_G11F\_B10F 형식입니다.

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => &quot;rg16&quot;

### 샘플러

전역으로 정의된 일부 샘플러를 재정의하도록 허용합니다. 기술에서는 정의할 수 없습니다. 이렇게 하면 이 렌더링 패스에 대한 샘플러 사용을 정의하거나 이전 렌더링 패스의 렌더링 대상에서 읽을 수 있습니다.

해당 정의에 대한 자세한 내용은 <b>샘플러</b> 섹션을 참조하십시오.

+++예


+++

## 입력 정점 형식

이렇게 하면 꼭짓점 셰이더에 정의된 각 특성의 의미 체계를 정의할 수 있습니다.

<b>XML 요소 정의:</b>

이름: &#39;vertexformat&#39;

특성:

* &#39;name&#39;: 꼭지점 셰이더에 정의된 특성의 이름입니다.
* &#39;semantic&#39;: 특성의 semantic입니다.

| &#39;semantic&#39; 값 | 설명 |
| --- | --- |
| 위치 | 정점 위치(float3) |
| 표준 | 꼭지점 표준(float3) |
| texcoord[0..N] | 정점 텍스처 좌표 버퍼 N(float2) |
| tangent[0..N] | 정점 탄젠트 버퍼 N(float4) |
| 이진[0..N] | 정점 이항 버퍼 N (float4) |

예:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## 샘플러

이렇게 하면 각 샘플러의 사용을 정의할 수 있습니다.\
지정된 샘플러에서 설정할 텍스처를 알고 있는 응용 프로그램에서 사용됩니다.

<b>XML 요소 정의:</b>

이름: &#39;sampler&#39;

특성:

* &#39;name&#39;: 셰이더 파일에 있는 sampler 변수의 이름입니다.
* &#39;사용법&#39;: sampler의 사용량입니다. 그래프의 출력 노드에 지정된 사용량과 일치합니다.

| &#39;usage&#39; 값 | 설명 |
| --- | --- |
| 산만해 | 확산 맵 |
| 불투명도 | 불투명도 맵 |
| 배출 | 발광 지도 |
| 양쪽융기 | 앰비언트 오클루전 맵 |
| 주변 | 앰비언트 맵 |
| 마스크 | 마스크 맵 |
| detailnormal | 세부 사항 표준 맵 |
| 표준 | 일반 맵 |
| 부딪치다 | 범프 맵 |
| Height | Height 맵 |
| 변위 | 변위 맵 |
| 특별 수준 | Specular level 맵 |
| specularcolor | Specular 색상 맵 |
| Specular | Specular 맵 |
| 광택 | 광택 지도 |
| 거칠음 | 거칠음 지도 |
| 비등방성 | Anisothropy 레벨 맵 |
| 비등방성 | 아니소트로피 각도 맵 |
| 투과- | 투과지도 |
| 반사 | 반사 맵 |
| 굴절 | 굴절 맵 |
| 환경 | 환경 맵(큐브 맵) |
| 파노라마 | 파노라마 지도(위도/경도 지도) |
| bluenoisemask | 256x256 디더링 텍스처 |

* 여러 사용이 지원됩니다.
  * 예:

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;: 샘플러가 GUI에 표시되어야 하는지 여부를 나타내는 부울

* 예:

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


흐름 모드:

<table data-preserve-html="true"><tbody><tr><th>이름</th><th>값</th></tr><tr><td rowspan="4">texture_wrap_s, texture_wrap_t, texture_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">반복<br/><br/></td></tr></tbody></table>

텍스처 필터

<table data-preserve-html="true"><tbody><tr><th>이름</th><th>값</th></tr><tr><td rowspan="6">texture_min_filter, texture_mag_filter<br/><br/><br/></td><td>가장 가까우</td></tr><tr><td>선형</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

예:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## 유니폼

이렇게 하면 각 셰이더 유니폼에 대한 추가 정보를 추가할 수 있습니다.

<b>XML 요소 정의:</b>

이름: &#39;uniform&#39;

특성:

&#39;name&#39;: 셰이더 파일에 있는 유니폼의 이름입니다.

| &#39;semantic&#39; 값 | 설명 |
| --- | --- |
| 세계 | 월드 매트릭스(float16) |
| worldinversetranspose | 세계 역전치 행렬(float16) |
| worldviewprojection | World View Projection Matrix(float16) |
| viewinverse | 월드 역행렬(float16) |
| 세계관 | World View Matrix(float16) |
| modelview | 모델 뷰 행렬(float16) |
| 투영 | 투영 행렬(float16) |
| 주변 | 장면 주변 색상(float3) |
| lightposition[0..N] | 장면의 N번째 조명 위치(float3) |
| lightcolor[0..N] | 장면의 N번째 조명 색상(float3) |
| lightintensity[0..N] | 장면의 N번째 조명 강도(부동 소수점) |
| 세계화 시대 | 현재 시간(초)(부동 소수점) |
| 해결 방법 | 뷰포트 해상도 (int2) |
| 쥐 | 마우스 위치(int2) |
| samplespostablesize | 환경 조명(int)을 계산하는 데 사용할 샘플 수입니다. |
| 방사선 암시 | 구형 조화 벡터의 배열(float3[10]) |
| 파노라마미프테이트 | 파노라마 맵(부동 소수점)의 밉맵 레벨 수 |
| panoramarotation | 파노라마 맵의 각도 회전 각도(부동 소수점) |
| panoramaintenance | 파노라마 맵의 강도(부동 소수점) |
| computebinormalinfragmentshader | 이진 파일은 조각당 계산됩니까? (정점당 아님) (bool) |
| isdirectxnormal | 표준 맵 포맷 DirectX이 맞나요? (bool) |
| uvwscale | u, v, w의 비율 값(float3) |
| 렌데루브타일 | UV 타일을 1개만 렌더링하시겠습니까? (bool) |
| 포도주화 | 렌더링할 UV 타일 좌표(int2) |

&#39;semantic&#39;: 유니폼의 의미 체계입니다. 모든 행렬은 float16입니다.

예:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


예:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### 기타 매개 변수

각 유니폼에 다음과 같은 기타 추가 정보를 추가할 수 있습니다.

* 기본값 정의
* 클램프 값
* 응용 프로그램에 유니폼이 표시되는 방식 제어:
* 레이블 설정
* 응용 프로그램에서 값을 편집하는 데 사용되는 위젯 정보를 설정합니다.
* 위젯 이름, 최소, 최대, 증가/감소 단계
* 그룹 위젯의 그룹 유니폼

유니폼은 각 기법에 대해 오버라이드될 수 있으므로 각 기법에 대한 특정 gui 설정을 표시할 수 있습니다.

<b>XML 요소 정의:</b>

이름: &#39;uniform&#39;

특성:

* &#39;name&#39;: 셰이더 파일에 있는 유니폼의 이름입니다.
* &#39;default&#39;: 균일 기본값
* &#39;min&#39;: 유효성 범위의 최소 값입니다.
* &#39;max&#39;: 유효성 범위의 최대값입니다.
* &#39;guiName&#39;: 응용 프로그램의 GUI에 있는 교복의 이름입니다.
* &#39;guiGroup&#39;: 응용 프로그램의 GUI에 유니폼을 넣을 그룹의 이름입니다.
* &#39;guiWidget&#39;: 응용 프로그램의 GUI에서 균일 값을 편집하는 데 사용되는 위젯의 이름입니다.

| &#39;guiWidget&#39; 값 | 설명 |
| --- | --- |
| 슬라이더 | floatN용 슬라이더 위젯 |
| 각도 | Float용 각도 위젯 |
| 색상 | float3, float4 색상에 대한 색상 위젯 |
| 확인란 | bool용 CheckBox 위젯 |

* &#39;guiMin&#39;: 위젯의 최소 값입니다
* &#39;guiMax&#39;: 위젯의 최대 값입니다.

## 예: 테셀레이션/시차

### 시차 꼭지점 셰이더 파일

위치: .\tessellation\_parallax\parallax\vs.glsl

내용:

> #version년

vec4 iVS\_Position; 속성\
속성 vec4 iVS\_Normal;\
속성 vec2 iVS\_UV;\
특성 vec4 iVS\_Tangent;\
속성 vec4 iVS\_Binormal;

varying vec3 iFS\_Normal;\
varying vec2 iFS\_UV;\
varying vec3 iFS\_Tangent;\
varying vec3 iFS\_Binormal;\
varying vec3 iFS\_PointWS;

uniform mat4 worldMatrix;\
uniform mat4 worldViewProjMatrix;

void main()\
&lbrace;\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_Binormal = iVS\_Binormal.xyz;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz;\
&rbrace;

### 테셀레이션 꼭지점 셰이더 파일

위치: .\tessellation\_parallax\tessellation\vs.glsl

내용:

&#x200B;>> 

&#x200B;#version년

vec4 iVS\_Position; 속성\
속성 vec4 iVS\_Normal;\
속성 vec2 iVS\_UV;\
특성 vec4 iVS\_Tangent;\
속성 vec4 iVS\_Binormal;

varying vec4 oVS\_Normal;\
varying vec2 oVS\_UV;\
varying vec4 oVS\_Tangent;\
varying vec4 oVS\_Binormal;

void main()\
&lbrace;\
gl\_Position = iVS\_Position;\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_Tangent = iVS\_Tangent;\
oVS\_Binormal = iVS\_Binormal;\
&rbrace;

### 테셀레이션 제어 셰이더 파일

위치: .\tessellation\_parallax\tessellation\tcs.glsl

내용:

&#x200B;>> 

&#x200B;#version 코어\
&#x200B;#extension GL\_ARB\_tessellation\_shader : 활성화

layout(vertices = 3) out;

in vec4 oVS\_Normal[];\
in vec2 oVS\_UV[];\
in vec4 oVS\_Tangent[];\
in vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

uniform float tessellationFactor;

void main()\
&lbrace;\
gl\_TessLevelOuter[0] = tessellationFactor;\
gl\_TessLevelOuter[1] = tessellationFactor;\
gl\_TessLevelOuter[2] = tessellationFactor;\
gl\_TessLevelInner[0] = tessellationFactor;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_이진[gl\_호출ID] = oVS\_이진[gl\_호출ID];\
&rbrace;

### 테셀레이션 평가 셰이더 파일

위치: .\tessellation\_parallax\tessellation\tcs.glsl

내용:

&#x200B;>> 

&#x200B;#version 코어

layout(triangles, equal\_spacing, ccw) in;

in vec4 oTCS\_Normal[];\
in vec2 oTCS\_UV[];\
in vec4 oTCS\_Tangent[];\
in vec4 oTCS\_Binormal[];

uniform mat4 worldMatrix;\
uniform mat4 worldViewProjMatrix;

uniform sampler2D heightMap;

균일 부동 타일링 = 1.0f;\
uniform float heightMapScale = 1.0f;

out vec3 iFS\_Normal;\
out vec2 iFS\_UV;\
out vec3 iFS\_Tangent;\
out vec3 iFS\_Binormal;\
out vec3 iFS\_PointWS;

vec3 interpolate3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
&lbrace;\
uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2 반환;\
&rbrace;

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
&lbrace;\
uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2 반환;\
&rbrace;

void main()\
&lbrace;\
vec3 uvw = gl\_TessCoord.xyz;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw));\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw));\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTexSample = texture(heightMap, newUV \&#42; tiling).x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTexSample \&#42; heightMapScale;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42; 타일링;\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz;\
&rbrace;

### 조각 셰이더 파일

위치: .\tessellation\_parallax\fs.glsl

내용:

&#x200B;>> 

&#x200B;#version년

// #define ALG\_NORMAL\_DIRECTX\
&#x200B;#define ALG\_NORMAL\_OPENGL

&#x200B;#ifdef ALG\_NORMAL\_DIRECTX\
// #define 뒤집기\_표준\_X\
&#x200B;#define 뒤집기\_표준\_Y\
// #define 뒤집기\_표준\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_DIRECTX

&#x200B;#ifdef ALG\_NORMAL\_OPENGL\
// #define 뒤집기\_표준\_X\
&#x200B;#define 뒤집기\_표준\_Y\
// #define 뒤집기\_표준\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_OPENGL

varying vec3 iFS\_Normal;\
varying vec2 iFS\_UV;\
varying vec3 iFS\_Tangent;\
varying vec3 iFS\_Binormal;\
varying vec3 iFS\_PointWS;

uniform vec3 Lamp0Pos = vec3(0.0f,0.0f,70.0f);\
uniform vec3 Lamp0Color = vec3(1.0f,1.0f,1.0f);\
uniform vec3 Lamp1Pos = vec3(70.0f,0.0f,0.0f);\
uniform vec3 Lamp1Color = vec3(0.198f,0.198f,0.198f);\
uniform bool flipNormal = true;\
uniform float TilingDetail = 3.0f;\
uniform float SpecExpone = 50.0;\
uniform float Ks = 1.0;\
균일 int parallax\_mode = 0;\
uniform float tessellationFactor = 4.0;\
uniform float heightMapScale = 1.0f;\
균일 부동 깊이\_detail = 0.5f;\
uniform float Kr = 0.5f;\
uniform int KF\_on = 1;\
uniform float KFs = 1.0f;\
uniform vec3 AmbiColor = vec3(0.07f,0.07f,0.07f);\
균일 부동 타일링 = 1.0f;\
uniform int enableTilingInFS = 0;

uniform sampler2D heightMap;\
uniform sampler2D normalMap;\
uniform sampler2D detailNormalMap;\
uniform sampler2D emissiveMap;\
uniform sampler2D diffuseMap;\
uniform sampler2D specularMap;\
uniform sampler2D opacityMap;\
uniform samplerCube environmentMap;

uniform mat4 worldMatrix;\
uniform mat4 worldInverseTransposeMatrix;\
uniform mat4 viewInverseMatrix;

vec4 litFct(float NdotL, float NdotH, float specExp)\
&lbrace;\
float ambient = 1.0;\
float diffuse = max(NdotL, 0.0);\
float Specular = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
return vec4(ambient, diffuse, Specular, 1.0);\
&rbrace;

vec3 lerpFct(vec3 v0, vec3 v1, float percent)\
&lbrace;\
return v0 + (v1-v0) \&#42;%;\
&rbrace;

// 퐁 음영\
void phong\_음영(\
(으)로 내보내기\
vec3 normalWS에서,\
vec3 pointToLightDirWS에서\
vec3 pointToCameraDirWS에서\
inout vec3 DiffuseContrib,\
inout vec3 SpecularContrib)\
&lbrace;\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpone);\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
&rbrace;

vec3 fixNormalSample(vec3 v)\
&lbrace;\
vec3 결과 = v - vec3(0.5,0.5,0.5);

&#x200B;#ifdef 뒤집기\_표준\_X\
result.x = -result.x;\
&#x200B;#endif // ifdef 뒤집기\_표준\_X\
&#x200B;#ifdef 뒤집기\_표준\_Y\
result.y = -result.y;\
&#x200B;#endif // ifdef 뒤집기\_표준\_Y\
&#x200B;#ifdef 뒤집기\_표준\_Z\
result.z = -result.z;\
&#x200B;#endif // ifdef 뒤집기\_표준\_Z

반환 결과;\
&rbrace;

vec3 normalVecOSToWS(vec3 normal)\
&lbrace;\
return normal;\
&rbrace;

void main()\
&lbrace;\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalize(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_Tangent);\
vec3 binormalOS = normalize(iFS\_Binormal);

// ------------------------------------------\
// TBN이 정직교화되어 있는지 확인\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 누적NormalOS = normalOS;

// ------------------------------------------\
// UV 업데이트\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0 ? iFS\_UV : (iFS\_UV \&#42; 타일링);\
float Height = texture2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
부동 시차 = 시차\_모드 == 0 ? (tessellationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
uv +=(Height \&#42; s.xy \&#42; 시차) ;

// ------------------------------------------\
// normalMap에서 Normal 추가\
vec3 normalTS = texture2D(normalMap,uv).xyz;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
// 세부 정보 추가 표준 맵\
vec3 normalDetailTS = texture2D(detailNormalMap,uv\&#42;TilingDetail).xyz;\
normalDetailTS = fixNormalSample(normalDetailTS);\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,깊이\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

if (length(normalTS)&lt;0.0001)\
cumulatedNormalOS = normalOS;

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// 확산 및 Specular 계산

// Light 0 기여도\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_음영(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

// Light 1 기여도\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_음영(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffuseColor = texture2D(diffuseMap,uv);

vec3 specularColor = texture2D(specularMap,uv).rgb;\
vec3 R = reflect(pointToCameraDirWS,cumulatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr;

float FallofRefl;

if (KFs >= 0.0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS)),0)\&#42;KF\_on;\
else\
FallofRefl = (1-max((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS))),0)\&#42;KF\_on;

if (KF\_on == 0)\
FallofRefl=1.0;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
vec3 emissive = texture2D(emissiveMap,uv).xyz;

vec3 finalcolor = Ambiant\_final\
&#x200B;+ specularColor\&#42;specContrib\
&#x200B;+ diffuseColor.rgb\&#42;diffContrib\
&#x200B;+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
&#x200B;+ 방출;

// 최종 색상\
vec4 finalColor4 = vec4(finalcolor, texture2D(opacityMap,uv));

gl\_FragColor = finalColor4;\
&rbrace;

### GLSLFX 파일

glslfx 파일은 형상을 렌더링하는 두 가지 기술을 정의합니다.

* 하나는 하드웨어 테셀레이션 기술을 사용합니다
* 다른 하나는 사용자 하드웨어가 테셀레이션을 지원하지 않는 경우 폴백으로 사용될 시차 효과를 기반으로 합니다.

위치: .\tessellation\_parallax\fs.glsl

내용:

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```

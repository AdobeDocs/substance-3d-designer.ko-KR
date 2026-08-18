---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: 호환성과 성능을 위해 Substance 3D Designer 3D 보기에서 셰이더를 OpenGL 코어 프로필로 전환하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 셰이더를 OpenGL 코어 프로필로 전환
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# 셰이더를 OpenGL 코어 프로필로 전환

버전 2018.2.0 이후 3D 뷰포트는 OpenGL 코어 프로필을 사용합니다.\
이 경우 GLSL 버전 120에서 GLSL 버전 330으로 애플리케이션을 제공하는 일부 셰이더를 업데이트했습니다.

새로운 GLSL 기능을 활용하거나 GLSL 코드를 더욱 최신 버전으로 만들기 위해 자신만의 셰이더를 업데이트할 수 있습니다. macOS에서는 이전 셰이더가 더 이상 작동하지 않을 수 있습니다.\
새로운 기능에 대한 전체 개요를 보려면 공식 OpenGL 문서를 검토하는 것이 좋습니다. 예를 들어 [OpenGL 음영 언어 사양 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf)을 살펴볼 수 있습니다.\
그렇지 않은 경우, 다음은 GLSL 3.30에서 GLSL 1.20 셰이더를 변환하는 데 도움이 되는 빠른 안내서입니다.

## 버전 번호 업데이트

먼저 `#version 330`까지 이전 `#version` 지시문을 바꾸거나(아직 없는 경우 파일 상단에 추가합니다).

### &quot;attribute&quot; 및 &quot;varying&quot;을 &quot;in&quot; 또는 &quot;out&quot;으로 바꿉니다.

이제 셰이더 단계에 따라 `attribute` 및 `varying` 변수가 `in` 또는 `out`(으)로 명시적으로 선언됩니다.

꼭지점 셰이더에서 꼭지점의 `attribute`은(는) `in`(으)로 선언되고 조각 셰이더로 전달될 `varying`은(는) `out`(으)로 선언됩니다.\
예:

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


은(는)

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


마찬가지로 조각 셰이더에서 varying이 사용됩니다. 또한 더 이상 빌드가 아닌 gl\_FrameColor를 대체할 out 변수를 선언해야 합니다.

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


은(는)

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### 새 텍스처 조회 함수 사용

새로운 버전의 음영 언어를 사용하여 텍스처 조회 API가 단순화되고 확장되었습니다.

`texture1D()`, `texture2D()`, `texture3D()` 및 `textureCube()` 함수는 모두 `texture()`의 오버로드가 됩니다.\
마찬가지로 `texture2DLod()`은(는) `textureLod()`이(가) 되고 `texture2DGrad()`은(는) `textureGrad()`이(가) 됩니다.

이제 `textureSize()`(텍셀로 샘플러 크기를 쿼리하기 위해), `textureOffset()`(대상 위치의 인접 샘플 샘플링), `textureFetch()`(픽셀 단위의 샘플 위치 제공) 등과 같은 유용한 함수에도 액세스할 수 있습니다.

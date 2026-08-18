---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: 향상된 재질 미리 보기 및 시각화를 위해 3D 보기 카메라에 후처리 효과를 적용합니다.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 후처리 효과
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# 후처리 효과

![포스트 효과](../../../../assets/postEffects.png "포스트 효과"){zoomable="yes"}

카메라 속성에서 포스트 효과를 활성화하여 렌더링을 개선하거나 특정 재질 속성을 확인할 수 있습니다.

이러한 효과는 자체 개발되었으며 래스터라이저와 GPU 패스트레이서 [렌더러](../../../../interface/3d-view/3d-renderers/3d-renderers.md)에서만 사용할 수 있습니다.

[3D 장면 리소스](../../../../resources/3d-scene-resource/3d-scene-resource.md) 또는 [장면 상태 파일](../../../../working-with-3d-scenes/working-with-3d-scenes.md)을 저장할 때 활성화된 모든 게시물 효과는 장면 상태의 일부로 저장됩니다.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 톤 매핑

</td>
<td style="border: 0;" valign="top">

### 빛　번짐효과

</td>
<td style="border: 0;" valign="top">

### 필드 심도

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## 톤 매핑

특정 알고리즘 및/또는 조회 테이블(LUT)에 따라 렌더링 색상을 다시 매핑합니다.

이렇게 하면 애플리케이션 간의 색상 일관성을 향상시킬 수 있습니다. 예를 들어 AgX 톤 매퍼도 Blender에서 사용할 수 있습니다.

+++라인하르트


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++로그


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++에이스


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++헤일


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++중립


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr 중립


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## 빛　번짐효과

매우 밝은 영역에서 빛이 적게 들어오는 영역으로 빛이 밖으로 번지는 언저리의 카메라 내 효과를 시뮬레이션합니다.

그 효과는 장면의 조명, 카메라 노출 및 방출 재료들에 의해 영향을 받는다.

+++임계값
이 값을 초과하는 꽃이 피는 경우 표시되는 광도 값입니다.

*왼쪽: 1.0 / 오른쪽: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++밝기 감소
값이 낮을수록 개화 반경이 짧아지는 개화 감쇠 램프.

*왼쪽: 1.0 / 오른쪽: 0.6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++레벨
꽃의 강렬함입니다. 값이 높을수록 더 밝고 뚜렷한 빛 무늬가 생깁니다.

*왼쪽: 8.0 / 오른쪽: 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++색상 이동
개화의 영향을 받는 영역의 색조를 더 따뜻한 색상으로 상쇄합니다.

*왼쪽: 0.0 / 오른쪽: 0.8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## 필드 심도

초점 거리보다 먼 거리가 먼 물체가 뿌옇게 보이는 카메라 렌즈에 의한 광학 현상을 시뮬레이션합니다.

이 효과는 카메라의 &#39;F-스톱&#39; 및 &#39;초점 거리&#39; 매개 변수에 따라 모두 영향을 받습니다.

>[!TIP]
>
> 카메라 초점을 빠르게 조정하려면 초점을 맞출 장면의 위치에 커서를 놓고 Ctrl+LMB(Windows) 또는 Cmd+LMB(macOS)를 눌러 해당 위치에 대한 초점 거리를 자동으로 설정합니다.

+++최대 반경
흐림 효과의 최대 반경

*왼쪽: 32.0 / 오른쪽: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++합성 강도
바깥쪽의 포커스 거리로부터의 흐림 효과의 크기입니다.

*왼쪽: 0.2 / 오른쪽: 0.05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++종방향 수차
초점 거리에서 떨어진 위치에서 발생하는 수차의 강도입니다.

수차는 빛의 파장이 약간 다른 초점 거리를 갖는 방법을 시뮬레이션하여, 색상이 상쇄된 것처럼 보이고 초점이 약간 다르게 나타납니다.

*왼쪽: 0.0/오른쪽: 1.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongituonalAberration0">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongituonalAberrical1">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![depthOfFieldLongteralAberricalAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongteralAberration0")

![depthOfFieldLongteralAberricalAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongteralAberration1")

+++

+++무색 수차
색수차가 무색이어야 하는지 여부를 지정합니다. 즉, 일부 색상이나 모든 색상의 초점 거리가 같아야 합니다.

이로 인해 흐림 효과가 보다 균등하게 분포하는 것으로 보인다.

*왼쪽: 참/오른쪽: 거짓*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++고양이 눈
비스듬한 각도로 들어오는 빛이 디스크에 들어가지 않고 고르지 않은 타원형을 이루어 왜곡을 일으키는 방법을 시뮬레이션하는 장면에서 고양이의 눈 효과를 사용할 수 있습니다.

이 효과는 더 높은 개구, 즉 더 낮은 F-스톱 값에서 더 두드러지게 나타난다.

*왼쪽: 참/오른쪽: 거짓*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>이전</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>이후</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++

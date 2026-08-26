---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/using-spot-colors.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 스크립팅에서 별색을 사용하여 특수화된 색상 작업 과정을 만드는 방법을 살펴보세요.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using spot colors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 별색 사용
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 별색 사용

<b>SDAapplication</b> 클래스에서 액세스할 수 있는 <b> SDSpotColorLibrary </b>클래스에는 Designer에 포함된 별색 라이브러리에 대한 정보가 포함되어 있습니다.

이 클래스를 사용하면 색상 책과 별색을 나열하고 특정 별색 또는 지정된 RGB 색상과 가장 가까운 별색을 찾을 수 있습니다.

<b>OpenColorIO</b>를 사용할 때 Designer에서 별색을 *사용할 수 없음*&#x200B;합니다. 이 경우 app.getSpotColorLibrary()는 <b>없음</b>을 반환합니다.

>[!IMPORTANT]
>
> <b>OpenColorIO</b>를 사용할 때 Designer에서 별색을 *사용할 수 없음*&#x200B;합니다. 이 경우 app.getSpotColorLibrary()는 <b>없음</b>을 반환합니다.

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

spotLib = app.getSpotColorLibrary() 

 

## Find a color by color book and color name.

col = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

 

print(col) 

print(col.get()) 

 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col)) 

 

## Find the closest spot color in a specific book, to an RGB color.

## The RGB color is specified in the working color space currently used by Designer.

col = spotLib.findClosestSpotColor( 

    spotColorBookName="PANTONE+ Solid Coated", 

    r=88 / 255.0, 

    g=132 / 255.0, 

    b=167 / 255.0 

) 

 

print(col) 

print(col.get()) 

print(spotLib.getSpotColorBookName(col)) 

print(spotLib.getSpotColorName(col))
```


별색을 노드 속성에서 불러와 설정할 수 있습니다.

```
import sd 

from sd.api.sdbasetypes import * 

from sd.api.sdvaluecolorrgba import SDValueColorRGBA 

from sd.api.sdvaluespotcolor import SDValueSpotColor 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getUIMgr() 

spotLib = app.getSpotColorLibrary() 

 

node = uiMgr.getCurrentGraphSelection()[0] 

 

## Set RGBA color in node property.

rgbaColor = SDValueColorRGBA.sNew(ColorRGBA(0.7, 0.5, 0.2, 1)) 

node.setInputPropertyValueFromId("outputcolor", rgbaColor) 

 

## Set spot color in node property.

spotColor = spotLib.findSpotColorByName( 

    spotColorBookName="PANTONE+ Solid Coated", 

    spotColorName="PANTONE Yellow 012 C" 

) 

node.setInputPropertyValueFromId("outputcolor", spotColor) 

 

## Get color from node property (could be a SDValueColorRGBA or a SDValueSpotColor)

anyColor = node.getInputPropertyValueFromId("outputcolor") 

 

## Print the RGBA components of the color.

print(anyColor.get()) 

 

## Check if the color is a spot color.

if isinstance(anyColor, SDValueSpotColor): 

## Print the spot color information of the color.

    print(spotLib.getSpotColorBookName(anyColor)) 

    print(spotLib.getSpotColorName(anyColor)) 

 
```

---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Substance 3D Designer Python 스크립팅에서 색상 관리 기능을 사용하여 정확한 색상을 만드는 방법을 살펴보세요.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 색상 관리 사용
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# 색상 관리 사용

<b>SDApplication</b> 클래스에서 액세스할 수 있는 <b> SDColorManagementEngine </b>클래스에는 *현재 색상 관리 설정*&#x200B;에 대한 정보가 포함되어 있습니다.

## 색상 관리 엔진 액세스 및 쿼리

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


또한 Python에서 비트맵 리소스에 *색상 공간을 할당*&#x200B;할 수 있습니다.

### 비트맵 리소스의 색상 공간 설정

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## 색상 공간 변환을 사용하여 SDTextures 작성

**SDTexture** 클래스의 **save** 메서드가 이제 선택적 **outputColorSpace** 매개 변수를 허용합니다. 지정된 경우 이미지를 저장하기 전에 *색상 공간 변환이 적용됩니다*.

색상 관리 모드에서 포함된 ICC 프로필 *및*&#x200B;을(를) 지원하는 경우 대상 파일 형식에서도 이를 지원하므로 색상 공간 ICC 프로필이 *결과 이미지 파일에 포함됩니다*.

---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: 효율적인 개발을 위해 Visual Studio 코드를 사용하여 Substance 3D Designer Python 플러그인을 디버깅하는 방법에 대해 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visual Studio 코드를 사용하여 플러그인 디버깅
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Visual Studio 코드를 사용하여 플러그인 디버깅

많은 개발자를 위한 워크플로 표준으로 **Visual Studio 코드 IDE**&#x200B;를 사용하여 Python 플러그인을 디버깅할 수 있습니다.

>[!WARNING]
>
> <b>debugpy.listen()</b> 메서드를 사용하면 지정된 포트에 연결할 수 있는 모든 사용자가 디버깅 프로세스 내에서 임의 코드를 실행할 수 있습니다.
> 
> 따라서 디버깅은 *<b>전용</b>*&#x200B;을(를) 설정하여 *보안 네트워크*&#x200B;에서 수행해야 합니다.

Visual Studio 코드와 Substance 3D Designer 간의 시너지를 설정하려면 다음 단계를 따르십시오.

1. **[Visual Studio 코드](https://code.visualstudio.com/)** 및 **[Python 확장](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**&#x200B;을 설치합니다.
1. **[디버깅 Python 모듈](https://github.com/microsoft/debugpy)**&#x200B;을 설치합니다.

   >[!NOTE]
   >
   > Designer의 Python 인터프리터가 &#39;*debugpy*&#39; 모듈을 찾을 수 있는지 확인하십시오. 가장 쉬운 방법은 &#39;*debug*&#39; 모듈이 있는 디렉터리를 **PYTHONPATH** 환경 변수에 추가하는 것입니다. 스크립트에서 sys.path를 수정하여 debugpy 모듈에 경로를 추가할 수도 있습니다.
1. 응용 프로그램을 실행하고 Python 편집기를 연 다음 **다음 코드를 실행합니다**.

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. Visual Studio 코드에서 프로젝트를 열고 **launch.json** 파일을 만듭니다. 파일에 다음을 추가합니다.

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. <b>디버그</b> 아이콘을 클릭하고 필요한 경우 디버거 구성을 만들거나 편집합니다.
1. **Python: Designer에 연결** 구성을 선택하고 **디버깅 시작**&#x200B;을 클릭합니다.

   이제 중단점을 설정하고 코드를 단계별로 실행하고 Visual Studio 코드 디버거의 다른 모든 기능을 사용할 수 있습니다.

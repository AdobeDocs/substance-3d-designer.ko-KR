---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/package-metadata.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 체계적인 에셋 라이브러리를 위한 패키지 메타데이터를 만들고 관리하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Package Metadata
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 패키지 메타데이터
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---


# 패키지 메타데이터

패키지 메타데이터 는 패키지 수준에서 정의된 텍스트(문자열) 값의 사전입니다. 게시 시 SBSAR에 포함되며, python 스크립팅에서 사용하기 위한 범용 스토리지입니다.

## Designer 인터페이스를 통한 메타데이터 표시 및 편집

Python 플러그인을 개발하는 경우 테스트 및 디버깅을 위해 메타데이터를 수동으로 편집할 수 있습니다. 방법은 다음과 같습니다.

1. 탐색기에서 패키지를 두 번 클릭하면 이 패키지의 속성 패널이 열립니다.

   ![패키지 메타데이터](../assets/empty.png "패키지 메타데이터")
1. 전용 섹션인 &quot;메타데이터&quot;가 있습니다. 위의 캡처와 같이 사용자의 경우 비어 있을 수 있습니다.

   &quot;더하기&quot; 단추를 사용하여 새 메타데이터를 추가할 수 있습니다.

   ![메타데이터 추가 단추](../assets/hoveradd.png "메타데이터 추가 단추")
1. 새 항목이 섹션에 나타납니다.

   ![새 메타데이터](../assets/newitem-1.png "새 메타데이터")
1. &quot;키&quot; 필드와 &quot;값&quot; 필드가 있습니다. 둘 다 필요에 맞는 설정으로 설정할 수 있습니다. &quot;키&quot; 필드는 목록 전체에서 고유한 값을 가져야 합니다.

   ![새 메타데이터 값](../assets/newitemfilled.png "새 메타데이터 값")
1. 항목의 &quot;유형&quot;을 선택할 수도 있습니다. 현재 &quot;String&quot; 또는 &quot;URL&quot;일 수 있습니다.

   ![메타데이터 형식 변경](../assets/typecombo.png "메타데이터 형식 변경")
1. 여기서 &#39;URL&#39;은 패키지에 포함된 리소스에 대한 참조를 의미합니다. 이렇게 하려면 하드 드라이브에서 파일을 선택하고 탐색기의 패키지에 끌어다 놓습니다. 이미지와 같은 일반 리소스이거나 텍스트 파일과 같은 다른 파일일 수 있습니다.

   ![패키지의 일반 리소스](../assets/resourceinpackage.png "패키지의 일반 리소스")
1. 파일이 패키지에 새 리소스로 표시됩니다.

   이제 패키지 속성 패널로 돌아가서 새 메타데이터를 만들고 적절한 키를 지정한 다음 유형으로 &quot;URL&quot;을 선택합니다. 그런 다음 &quot;...&quot; 아이콘을 선택합니다. &quot;값&quot; 필드에 있는 단추를 클릭하고 &quot;자원에서&quot;를 선택합니다. 마지막으로, 방금 전에 포함시킨 파일을 선택하고 다음을 확인합니다.

   ![URL 메타데이터](../assets/urlmetadata.gif "URL 메타데이터")
1. 이제 &quot;값&quot; 필드에 리소스의 &quot;URL&quot;이 저장되어 있는지 확인할 수 있습니다.

   항목 오른쪽의 &quot;X&quot; 버튼을 사용하여 메타데이터를 삭제할 수도 있습니다.

   ![메타데이터 삭제](../assets/hoverdelete.png "메타데이터 삭제")

>[!NOTE]
>
> 메타데이터 항목 이동 또는 재정렬이 비활성화됨: 순서가 중요하지 않으며 패키지를 게시할 때 유지되지 않습니다.

## 게시된 SBSAR 파일의 메타데이터

일부 시나리오에서는 일치하는 게시된 SBSAR의 패키지에서 정의한 메타데이터를 검색할 수 있습니다. 아래에서는 메타데이터가 어떻게 변환되고 아카이브에 저장되는지, 그리고 메타데이터를 활용하는 적절한 방법을 확인할 수 있습니다.

메타데이터는 /assemblies/content/0000/metadata.json 이라는 파일에 JSON 포맷에 따라 저장됩니다(경로는 .sbsar 아카이브의 루트에 상대적입니다).

일반(문자열) 메타데이터는 그대로 저장됩니다(예: &quot;key&quot;: &quot;stringValue&quot;, 줄당 하나). 다시, 다양한 키의 원래 순서는 유지되지 않으며, 구현이 정의된다. 일반 파이썬 딕트처럼, 주문에만 의존하지 마세요!

URL 메타데이터의 목적은 사용자 및 플러그인이 .sbsar 아카이브에 외부 파일을 포함하도록 허용하는 것이므로 특정 변형의 적용을 받습니다. 먼저 저장된 URL과 일치하는 리소스 파일이 이 파일만 포함하는 구현 정의 위치(일반적으로 번호가 매겨진 하위 폴더)의 아카이브에 복사됩니다. 중요한 것은 이름 충돌을 방지하는 것입니다.) 파일은 원래 이름을 유지합니다(이때 리소스 이름이 무시됩니다). 그런 다음 metadata.json의 원본 URL 대신 metadata.json과 관련된 아카이브의 복사된 파일 경로가 기록됩니다.

이전 섹션에서 생성한 예제 패키지를 내보내면(일부 출력을 사용하여 하나 이상의 그래프를 생성한 후) 다음과 같은 아카이브 컨텐츠가 표시됩니다.

```
myPackage.sbsar

|-- assemblies

        |-- content

            |-- 0000

                |-- New_Graph.sbsasm

                |-- New_Graph.xml

                |-- metadata.json

                |-- resources

                    |-- 0

                        |-- TEXT.txt
```


Metadata.json 콘텐츠는 다음과 같습니다.

```
{

    "myResource": "resources/0/TEXT.txt",

    "myText": "This is a text"

}
```


현재로서는 아카이브에 저장된 메타데이터와 리소스에 액세스할 수 있는 특정 도구가 제공되지 않습니다. 권장 방법은 선택한 LZMA 디코더를 사용하여 아카이브를 열고 일반 JSON 파서로 metadata.json을 구문 분석하는 것입니다(키 또는 값 문자열에 일부 팬시 문자가 포함된 경우 JSON 방식으로 이스케이프 처리됨).

>[!NOTE]
>
> 각각의 메타데이터가 단순한 문자열인지 URL인지에 대한 정보는 남아있지 않으므로 읽고자 하는 각각의 키가 무엇을 의미하는지 알아야 한다.

---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: 플러그인 개발을 위해 전체 Substance 3D Designer Python 스크립팅 API 참조에 액세스합니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스크립팅 API 참조
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# 스크립팅 API 참조

이 페이지에서는 API의 주요 개념에 대해 설명합니다.

자세한 내용은 <b>도움말 > Python API 설명서...</b>에서 액세스할 수 있는 응용 프로그램과 함께 제공되는 설명서를 참조하십시오. 이 설명서에서 모듈 이름(아래 괄호 안)에 대해 <b>빠른 검색</b>을 수행하여 해당 정의를 쉽게 찾을 수 있습니다.

## 컨텍스트

컨텍스트(*Context*) 개체가 <b>API</b>의 주 진입점입니다. 사용자가 &#39;*sd*&#39; 모듈에서 &#39;<b>*getContext()*</b>&#39; 메서드를 사용하여 처음 가져올 때 만들어집니다.

이 개체는 기본적으로 <b>응용 프로그램을 검색</b>(*SDApplication*) 개체를 검색할 수 있습니다.

## 응용 프로그램(SDApplication)

응용 프로그램(*SDApplication*)은 다음과 같이 <b>기본 API 관리자</b>에 대한 액세스를 허용하는 개체입니다.

* 응용 프로그램의 모든 <b>패키지</b>를 관리하는 <b>패키지 </b>관리자(*SDPackageMgr*);
* 응용 프로그램의 모든 <b>모듈</b>을(를) 관리하는 <b>모듈 </b>관리자(*SDModuleMgr*);
* 응용 프로그램 창에서 <b>메뉴 및 도킹</b>을(를) 만들 수 있는 <b>UI </b>관리자(*SDUIMgr*).

특정 이벤트가 발생할 때 호출되는 응용 프로그램에 <b>콜백</b>을 등록할 수 있습니다.

## 패키지 관리자(SDPackageMgr)

이 개체는 모든 응용 프로그램의 <b>패키지</b>를 관리합니다. 패키지가 &#39;<b>*탐색기*</b>&#39; 구성 요소에 표시됩니다.

이를 통해 다음을 수행할 수 있습니다.

* 새 패키지 <b>만들기</b>;
* 패키지를 <b>로드/언로드</b>;
* 패키지를 <b>저장</b>;
* 패키지를 <b>찾기</b>.

## 패키지(SDPackage)

패키지(*SDPackage*)는 <b>리소스 컬렉션</b>(*SDResource*)입니다.

패키지의 콘텐츠는 &#39;*SDPackageMgr*&#39; 개체를 통해 <b>.sbs</b> 확장명을 가진 파일에 <b>저장</b>할 수 있습니다. 이 개체를 사용하면 <b>특정 리소스를 </b>검색할 수 있습니다.

특정 리소스를 <b>만들기</b>하려면 관련 개체 정적 메서드(예: &#39;*SDSBSCompGraph.sNew()*&#39;)를 참조하십시오.

패키지에는 메타데이터 사전(SDMetadataDict)도 포함되어 있습니다. 메타데이터 [여기](../../package-metadata/package-metadata.md)에서 추가 정보를 찾을 수 있습니다.

## 리소스(SDResource)

리소스(*SDResource*)는 다른 리소스에서 <b>참조</b>할 수 있는 개체입니다.

<b>형식</b> 리소스가 여러 개 있습니다.

* 폴더(*SDResourceFolder*);
* 그래프(*SDGraph*);
* 비트맵(*SDResourceBitmap*);
* SVG 이미지(*SDResourceSVG*);
* 글꼴(*SDResourceFont*);
* 장면(*SDResourceScene*);
* BSDF 측정(*SDResourceBSDFMevaluation*);
* 조명 프로필(*SDResourceLightProfile*).

다음 아래에 있는 정적 메서드 &#39;*sNew()*&#39;에서 리소스를 <b>만들기</b>할 수 있습니다.

* 패키지;
* 폴더.

리소스에는 여러 <b>속성</b>(*SDPproperty*)이 있을 수 있습니다.

## UI 관리자 (SDUIMgr)

UI 관리자를 사용하면 <b>메뉴</b>, <b>도킹</b>과 같은 Substance Designer의 기본 창에서 <b>사용자 인터페이스 요소</b>를 만들 수 있으며, 사용자 인터페이스 관련 이벤트가 발생할 때 <b>콜백</b>을 등록할 수 있습니다.

또한 UI 관리자는 <b>현재 활성 그래프</b> 및 활성 그래프의 <b>선택</b>에 액세스할 수 있습니다.

## 그래프 (SDGraph)

그래프(*SDGraph*)는 다음을 포함하는 개체입니다.

* <b>노드 </b>(*SDNode*);
* <b>그래프 개체</b>(*SDGraphObjects*);
* <b>속성 </b>(*SDPproperty*).

다음과 같은 4가지 그래프 유형이 있습니다.

* Substance 그래프(*SDSBSCompGraph*)
* Substance 함수 그래프(*SDSBSFunctionGraph*)
* Substance FXMap 그래프(*SDSBSFxMapGraph*)

그래프에는 하나 이상의 <b>출력</b> 노드가 있을 수 있습니다. 출력 노드는 그래프의 <b>결과</b>를 나타냅니다.

&#39;*getNodeDefinitions()*&#39; 메서드를 사용하여 그래프에 사용할 수 있는 모든 노드를 <b>검색</b>할 수 있습니다.

&#39;*newNode()*&#39; 메서드를 사용하여 새 노드를 <b>만들기</b>할 수 있습니다.

&#39;*newInstanceNode()*&#39; 메서드를 사용하여 리소스(*SDResource*)에서 새 <b>인스턴스</b> 노드를 만들 수 있습니다.

## 노드(SDNode)

노드(*SDNode*)는 개체에 대해 수행되는 <b>작업</b>을 나타냅니다.

다음에서 만들 수 있습니다.

* <b>정의</b>(*SDDefinition*)(&#39;*SDGraph.newNode()&#39;* 참조);
* <b>리소스</b>(*SDResource*)(&#39;*SDGraph.newInstanceNode()&#39;* 참조).

노드에는 여러 <b>속성</b>이 있을 수 있습니다.

노드의 <b>형식</b>이 여러 개 있습니다.

* *<b>SDSBSCompNode</b>*: Substance 그래프의 노드(*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>*: Substance 함수 그래프의 노드(*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>*: Substance FXMap 그래프의 노드(*SDSBSFxMapGraph*);

## 그래프 개체(SDGraphObjects)

그래프 개체(*SDGraphObject*)는 그래프에 <b>추가 정보를 추가</b>하는 개체이지만 그래프 평가 과정에서 <b>*고려되지 않은* 개체입니다.</b>

그래프 개체의 <b>3개 유형</b>이 있습니다.

* <b>핀</b>(*SDGraphObjectPin*)
* <b>댓글</b>(*SDGraphObjectComment*)
* <b>프레임</b> (*SDGraphObjectFrame*)

<b>생성</b> 방법에 대한 자세한 내용은 이러한 개체의 정적 메서드 &#39;*sNew()*&#39;을(를) 참조하십시오.

## 등록 정보(SDPproperty)

속성(*SDPproperty*)은 <b>다른 개체</b>(그래프, 노드, 리소스 등)의 속성을 <b>설명</b>하는 개체입니다.

특정 <b>범주</b>에 속합니다(*SDPropertyCategory*).

* <b>입력</b>: 개체의 입력 속성을 분류합니다. 일반적으로 <b>은(는) 현재 개체에서 수행하는 작업</b>에 영향을 줍니다.
  * 예: Substance 그래프에서 Uniform Color 노드의 &#39;*color*&#39; 속성은 입력 속성입니다.
* <b>출력</b>: 개체의 출력 속성을 분류합니다. 개체의 <b>결과</b>를 식별하는 데 사용됩니다.
* <b>주석</b>: 개체에서 수행하는 <b>*작업에 영향을 주지* 않는</b> 속성을 분류합니다.
  * 예: 그래프의 &#39;*label*&#39;은(는) 그래프 계산에 영향을 주지 않으므로 주석 속성입니다.

다음 <b>구성원</b>이 포함되어 있습니다.

* <b>ID</b>: 해당 범주의 컨텍스트에 있는 속성의 식별자입니다.
* <b>형식</b>: 현재 속성에서 지원하는 형식입니다. 일부 속성은 *여러* 형식(&#39;*int*&#39;, &#39;*float*&#39; 등)을 지원할 수 있습니다.
  * 예: &#39;*sbs::function::add*&#39; 노드의 입력 속성은 다른 형식을 지원할 수 있습니다. &#39;*int&#39;*, &#39;*int2&#39;*, &#39;*int3&#39;*, &#39;*int4&#39;*, &#39;*float&#39;*, &#39;*float2&#39;*, &#39;*float3&#39;*, &#39;*float4&#39; 등;*
* <b>범주</b>: 속성이 속한 범주(입력, 출력, 주석);
* <b>레이블</b>: 속성의 레이블로, *표시 전용*;
* <b>설명</b>: 속성에 대한 설명입니다.
* <b>DefaultValue</b>: 기본값;
* <b>IsConnectable</b>: 이 속성에서 연결(*SDConnection*) *할 수*&#x200B;가 있는지 여부를 나타냅니다.
* <b>isReadyOnly</b>: 속성이 읽기 전용인지 여부를 나타냅니다. true이면 연결된 값을 수정할 수 *없습니다*.
* <b>isVariadic</b>: true인 경우 이 속성은 개체에서 *multiple* 속성으로 표시됩니다.
* <b>isPrimary</b>: 지정한 속성이 다른 속성을 제어하는 *principal* 속성인지 여부를 나타냅니다. *참고:* 이것은 Substance *합성* 노드(*SDSBSCompNode*)에만 해당합니다.

예:

* &#39;*sbs::compositing::input*&#39; 노드의 속성:

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::입력</th></tr><tr><td style="text-align: left;"><strong>입력</strong></td><td style="text-align: left;"><strong>주석</strong></td><td style="text-align: left;"><strong>출력</strong></td></tr><tr><td>$outputsize</td><td>레이블</td><td><p>unique_filter_output(연결 가능)</p></td></tr><tr><td>$format</td><td>설명</td><td><br/></td></tr><tr><td>$pixelsize</td><td>식별자</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$tiling</td><td>그룹</td><td><br/></td></tr><tr><td>$randomseed</td><td>visibleif</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>용도</td><td><br/></td></tr></tbody></table>

* &#39;*sbs::compositing::blend*&#39; 노드의 속성:

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::블렌드</th></tr><tr><td style="text-align: left;"><strong>입력</strong></td><td style="text-align: left;"><strong>주석</strong></td><td style="text-align: left;"><strong>출력</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output(연결 가능)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$tiling</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.connector(연결 가능)</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connector(연결 가능)</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector (연결 가능)</td><td><br/></td><td><br/></td></tr><tr><td>opacitymult</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">혼합 모드</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">색상 혼합</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">직사각형 마스크</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## 유형(SDType)

형식(*SDType*)에는 다음과 같은 값 <b>type</b>의 정보가 포함됩니다.

* <b>ID</b>: 형식의 식별자입니다.
* <b>한정자</b>: &#39;*SDTypeModifier&#39;* <b>열거형</b> 값 중 하나일 수 있는 형식 한정자:
  * *자동*;
  * *균일*: 값이 작업당 *한 번* 평가됩니다.
  * *가변*: 값은 작업당 *여러 번* 평가됩니다(예: 각 텍셀에 대해).

다음과 같이 여러 유형이 정의됩니다.

* <b>열거형</b>(*SDTypeEnum*): 모든 속성과 함께 <b>열거형</b> 형식을 설명합니다.
* <b>구조체</b>(*SDTypeStruct*): 모든 속성이 포함된 <b>구조체</b> 형식을 설명합니다.
* <b>배열</b>(*SDTypeArray*): <b>배열</b>을(를) 설명합니다.
* 등

전체 목록은 Substance Designer의 *Python API 설명서*&#x200B;를 참조하십시오.

## 값(SDValue)

값(*SDValue*)은 *기본 형식* 값으로 <b>캡슐화</b>하는 개체입니다.

예를 들면 다음과 같습니다.

* &#39;<b>*SDValueInt*</b>&#39; 개체는 &#39;*int*&#39; 값을 캡슐화합니다.
* &#39;<b>*SDValueFloat4*</b>&#39; 개체는 &#39;*float4*&#39; 값을 캡슐화합니다.
* 등

기본 형식 값은 일반적으로 &#39;<b>get()</b>&#39; 메서드를 사용하여 <b>검색</b>할 수 있지만, 이는 반환된 &#39;*SDValue&#39;*&#x200B;의 *형식*&#x200B;에 따라 달라질 수 있습니다.

## 연결(SDConnection)

연결(*SDConnection*)은 서로 다른 두 <b>노드</b>의 서로 다른 두 <b> 속성</b> 간의 <b>링크</b>를 나타냅니다.

여기에는 다음이 포함됩니다.

* <b>대상 노드</b>;
* 대상 노드의 <b>대상 속성</b>;

모든 <b>연결 작업</b>이 노드에서 수행됩니다.

* <b>새 연결을 만드는 중</b>, &#39;*SDNode.newPropertyConnection()*&#39; 참조
* <b>기존 연결을 삭제</b>하려면 &#39;*SDNode.deletePropertyConnection()*&#39;을(를) 참조하십시오.
* 속성의 연결을 <b>검색</b>하려면 &#39;*SDNode.getPropertyConnections()*&#39;을(를) 참조하십시오.

## 모듈(SDModule)

모듈은 <b>정의 및 형식의 컬렉션</b>입니다.

열거형과 구조뿐 아니라 만들 수 있는 노드의 모든 정보를 쉽게 검색할 수 있습니다.

여기에는 다음이 포함됩니다.

* 모듈 관리자(*SDModuleMgr*)의 컨텍스트에서 고유한 <b>식별자</b>(*ID*);
* <b>정의</b> 목록(*정의*);
* <b>형식</b>(*SDType*)의 목록입니다.

## 정의(정의)

정의(*SDDefinition*) 개체에는 <b>속성</b>(&#39;*SDNode&#39;* 등)에 기반한 특정 <b>개체</b>의 정의에 대한 정보가 포함되어 있습니다.

여기에는 다음이 포함됩니다.

* <b>ID</b>: 정의 식별자,
* <b>레이블</b>: 정의의 레이블;
* <b>설명</b>: 정의에 대한 설명입니다.
* <b>속성</b>: 사용 가능한 모든 속성 *범주*(*SDPropertyCategory*)의 속성입니다.

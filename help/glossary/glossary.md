---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/glossary.html"
breadcrumb-title: ''
description: Substance 3D Designer 용어집에 액세스하여 용어, 개념 및 기술 용어에 대한 정의를 찾습니다.
helpx_creative_field: ""
helpx_description: Designer > Glossary
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 용어집
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '4459'
ht-degree: 0%

---


# Designer에서 사용되는 용어 및 개념에 대해 알아봅니다.

## #

|  |  |
| --- | --- |
| <b><span id="three-d-scene"></span>3D 장면</b> | 3D 공간의 시각화를 표현하고 애니메이션을 적용하는 데 관련된 개체 및 데이터 컬렉션입니다.<ul data-preserve-html="true"> <li data-preserve-html="true">[망](#mesh)</li> <li data-preserve-html="true">[재질](#material)</li> <li data-preserve-html="true">카메라</li> <li data-preserve-html="true">조명</li> <li data-preserve-html="true">애니메이션</li> <li data-preserve-html="true">시뮬레이션</li> <li data-preserve-html="true">...</li> </ul>3D 장면을 저장하기 위해 [많이 사용되는 파일 형식](https://www.adobe.com/products/substance3d/discover/3d-files-formats.html)으로는 Pixar의 [USD](#usd)과 Autodesk의 FBX가 있습니다. 모든 파일 형식은 이러한 구성 요소를 지원하지 않습니다 |

## A

|  |  |
| --- | --- |
| <b><span id="alpha"></span>Alpha 채널</b> | 불투명도를 설명하는 데 주로 사용되는 색상 이미지의 네 번째 채널입니다. |
| <b><span id="ambient-occlusion"></span>주변 오클루전</b> | 노출이 적기 때문에 도달하기 어려운 표면에서의 주변 광의 감쇠입니다. |
| <b><span id="anisotropy"></span>비등방성</b> | 방향에 종속되는 속성입니다. 다른 말로, 다른 축에서 측정되거나 관찰될 때 다른 결과를 제공하는 것이다.   이방성 물질은 어디를 바라보느냐에 따라 외관이 다르고, 이방성 필터가 모든 방향으로 균일하게 적용되지 않는다. |
| <b><span id="api"></span>API</b> | API(응용 프로그래밍 인터페이스)는 사용자가 다른 프로그램 응용 프로그램의 함수 및 절차에 액세스할 수 있도록 하는 함수 및 절차의 모음입니다.   API는 사용자와 프로그램 간에 제어되고 안전한 계층을 제공합니다. 그것은 또한 그 프로그램을 더 쉽게 상호 작용하고 더 널리 접근할 수 있게 하기 위해 다른 프로그래밍 언어를 사용할 수 있다.   Designer은 데이터를 조작하고 사용자 정의 도구를 빌드하고 작업 과정을 가속화하기 위한 다양한 기능에 쉽게 액세스할 수 있는 [Python API](../scripting/scripting.md)를 제공합니다. |
| <b><span id="atomic-node"></span>Atomic node</b> | 그래프의 기본 구성 요소입니다. 모든 [인스턴스 노드](#instance-node)를 원자 노드의 그래프로 나눌 수 있습니다. 각 그래프 유형에는 고유한 원자 노드 세트가 있습니다. |

## B

|  |  |
| --- | --- |
| <b><span id="baking"></span>굽기</b> | 3D 모델에서 정보를 계산하고 결과를 [텍스처](#texture)에 저장하는 프로세스입니다. 데이터는 모델의 [UV](#uv)에 따라 텍스처에 배치됩니다. |
| <b><span id="base-color"></span>기본 색상</b>(알베도) | PBR 금속 거칠기 [음영](#shader) 모델을 사용하여 정의된 [재질](#material)의 채널입니다. [기준 색상]은 조명 정보가 없는 표면의 색상을 지정합니다.   [확산](#diffuse)과 혼동해서는 안 됩니다. |
| <b><span id="base-parameter"></span>기본 매개 변수</b> | [비트맵](#bitmap)을 계산하는 Substance 그래프의 모든 노드에 공통적인 매개 변수입니다.   여기에는 해상도([출력 크기](#output-size)) 및 [비트 심도](#bit-depth)(출력 형식) 또는 [타일링](#tiling) 모드와 같은 비트맵 계산 방법과 같은 비트맵의 핵심 측면이 포함됩니다.   기본 매개 변수는 일반적으로 노드를 호스팅하는 그래프나 업스트림된 다른 노드에서 [상속](#inheritance)됩니다. |
| <b><span id="bilinear-filtering"></span>쌍선형 필터링</b> | [텍스처 샘플](#texture-sampling)이(가) 픽셀의 중심에서 정확하게 수행되지 않은 경우 컴퓨터 이미징에 사용되는 보간 프로세스입니다.   예를 들어, 이는 이미지를 확대했을 때 발생할 수 있다. |
| <b><span id="bit-depth"></span>비트 심도</b> | 텍스처에 픽셀 값을 저장하는 데 사용되는 비트 수입니다. 비트 심도가 높을수록 더 많은 값을 인코딩할 수 있으므로 그라디언트가 더 부드러워집니다.   값의 유형에 따라 서로 다른 비트 심도를 사용할 수 있습니다. - 8비트(0 ~ 255) 또는 16비트(0 ~ 65,535)를 사용하여 정수 값을 인코딩할 수 있습니다. - 부동 소수점 값은 16비트(+32767.9999부터 -32768.0까지) 또는 32비트(-3.4E+38부터 +3.4E+38까지)로 인코딩할 수 있습니다. 낮은 동적 범위 이미지는 정수 값을 사용하여 0에서 1까지의 단계를 인코딩합니다. High Dynamic Range 이미지는 부동 소수점 값을 사용하여 원시 숫자 값을 인코딩합니다.   Substance 그래프에서 비트 심도는 출력 형식 매개 변수로 제어됩니다. |
| <b><span id="bitmap"></span>비트맵</b> | 디지털 이미지입니다. 두 가지 유형의 이미지가 가장 일반적입니다.<ul data-preserve-html="true"> <li data-preserve-html="true">회색 음영 이미지에는 광도(L),</li> <li data-preserve-html="true">색상 이미지에는 빨강, 녹색 및 파랑(RGB)의 세 가지 채널이 있습니다. 네 번째 것이 있을 수 있습니다: 불투명도에 자주 사용되는 알파(A). Designer의 색상 이미지는 항상 RGBA입니다.</li> </ul>  비트맵은 값의 그리드(grid)로 간주될 수 있습니다. 그리드의 각 셀은 픽셀이며, 이것은 &#39;그림 요소&#39;의 약어입니다. 픽셀은 채널당 하나의 값을 저장합니다. 해당 값의 유형은 비트맵의 [비트 심도](#bit-depth)에 따라 달라집니다. |

## C

|  |  |
| --- | --- |
| <b><span id="cache"></span>캐시</b>(메모리) | 데이터 모음 - 예: 노드의 [기본 매개 변수](#base-parameter) 및 출력 이미지 - 재사용할 메모리에 저장됩니다.   캐시는 [Substance 엔진](#substance-engine)에서 변경된 그래프의 부분만 다시 계산하도록 하여 그래프 계산 속도를 크게 높입니다. 노드 연결 및 매개 변수를 변경할 때 앞에 있는 모든 노드는 이러한 변경 내용의 영향을 받지 않으므로 그래프를 업데이트하기 위해 [평가](#evaluation)를 다시 수행할 필요가 없습니다. 대신 캐시가 사용됩니다.   큰 그래프에서 고해상도 및 비트 심도를 사용하여 작업할 때 캐시의 메모리 풋프린트가 상당할 수 있습니다. |
| <b><span id="channel-packing"></span>채널 패킹</b> | 개별 이미지가 단일 색상 이미지의 RGB(A) 채널에 팩킹되는 최적화 기술입니다.   예를 들어, RMA 텍스처는 거칠기 맵 (R), 금속성 맵 (M) 및 주변 오클루전 맵 (A)가 모두 단일 색상 텍스처로 압축된 것입니다.   또 다른 일반적인 기법은 회색 음영 텍스처를 표준 맵의 파란색 채널에 패킹 하는 것입니다. 이는 표준 벡터의 &#39;위&#39; 구성 요소인 파란색 채널이 런타임에 다시 계산될 수 있기 때문입니다.   [RGBA 병합](../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) 노드는 이 기술을 구현하는 데 유용합니다. |
| <b><span id="color-space"></span>색상 공간</b> | 색상 범위의 표시 방법에 대한 정의입니다. 특정 색상을 디지털 방식으로 인코딩 및 디코딩하려면 사용되는 숫자를 이해하기 위해 이러한 정의가 필요합니다.   이미지 파일에는 지정된 색상 공간을 사용하는 색상 값이 저장되므로 이러한 색상은 해당 색상 공간을 지원하는 디스플레이에서 충실하게 재현할 수 있습니다. 디스플레이는 주어진 컬러 공간을 완전히 또는 부분적으로 지원할 수 있게 하는 특정 컬러 재생 능력들을 갖는다.   원시 데이터 - 예: 표준 맵 - 이러한 색상은 시각화되지 않으며 해당 데이터에 변환을 적용해서는 안 되기 때문에 항상 선형 색상 공간에서 인코딩 및 디코딩됩니다.   sRGB는 널리 지원되는 색상 공간입니다. 그 밖에 인기 있는 색상 공간으로는 Adobe RGB, Rec. 2100 및 ProPhoto RGB. |
| <b><span id="cooking"></span>요리 </b>(<span id="compilation"></span>컴파일) | 데이터를 다른 언어로 번역하여 신속하고 효율적으로 실행할 수 있는 과정이다. Substance 그래프의 결과를 계산하려면 먼저 그래프를 컴파일해야 합니다. 컴파일이 그래프 [평가](#evaluation) 프로세스의 일부입니다.   이 컴파일은 병합 그래프에서 수행됩니다. 즉, 모든 [인스턴스 노드](#instance-node)이(가) 소스 그래프로 &#39;대체&#39;되어 하나의 더 큰 그래프가 남고 해당 그래프가 컴파일됩니다.   컴파일된 그래프는 편집할 수 없습니다. [정적](#static-parameter) 매개 변수가 잠기고 숨겨진 상태에서 [동적](#dynamic-parameter)인 경우 노출된 매개 변수는 계속 사용할 수 있습니다. |
| <b><span id="culling"></span>컬링</b> | 3D 장면 렌더링을 위한 최적화 기법으로, 표시되지 않을 때 렌더링 계산에서 형상을 제거합니다.   여기에는 카메라의 절두체(*절두체 컬링*) 외부의 개체 또는 다각형이 포함될 수 있으며, 카메라에서 반대 방향으로 향하거나(*백페이스 컬링*) 다른 불투명 개체에 의해 완전히 숨겨집니다(*오클루전 컬링*). |

## D

|  |  |
| --- | --- |
| <b><span id="dependency"></span>종속성</b> | 파일 A가 없는 경우 파일 B가 의도한 대로 작동하지 않는 방식으로 다른 파일 B에서 사용되는 파일 A입니다.   [패키지](#package)의 종속성은 내부 그래프, 이미지 파일, 글꼴 등을 참조하므로 다른 패키지가 될 수 있습니다. 패키지는 해당 종속성에 대한 경로를 저장하고 해당 경로에서 종속성을 찾을 수 없으면 경고가 발생합니다. 종속성 누락으로 인해 그래프에서 [고스트 인스턴스 노드](#ghost-instance-node)가 발생할 수도 있습니다. |
| <b><span id="diffuse"></span>확산</b> | PBR Specular 광택 [음영](#shader) 모델을 사용하여 정의된 [재질](../glossary/glossary.md)의 채널입니다. 확산 은 켜져 있을 때 표면의 색상을 지정합니다.   [기본 색상(알베도)](#base-color)과 혼동해서는 안 됩니다. |
| <b><span id="directx"></span>DirectX</b> | 멀티미디어 컨텐츠를 처리하기 위한 API 컬렉션입니다. 3D API인 Direct3D는 비디오 게임 개발 및 기타 3D 산업에서 널리 사용됩니다.   Direct3D는 텍스처의 원점(즉, (0, 0) 좌표)을 *왼쪽 위*(Y-down)에 놓고, [OpenGL](#opengl) API는 *왼쪽 아래*(Y-up)에 둡니다.   즉, OpenGL과 비교하여 DirectX 표준 맵에 *반전된 녹색 채널*&#x200B;이 있습니다. 실제로, 초록색 채널은 법선벡터의 Y좌표를 호스팅한다. |
| <b><span id="displacement"></span>변위</b> | 3D 모델의 [정점](#vertex)을(를) [표준](#normal)을 따라 이동하는 프로세스입니다.   변위는 [테셀레이션](#tessellation) 및 [표준 맵](#normal-map)과 함께 사용되어 표면에 세밀한 디테일을 모델링하는 경우가 많습니다. |
| <b><span id="dynamic-parameter"></span>동적 매개 변수</b> | 값이 변경될 수 있는 매개 변수입니다. 즉, 값이 상수가 아닌 매개 변수는 모두 동적입니다.    여기에는 노출된 매개 변수, 노출된 매개 변수의 영향을 받는 모든 매개 변수 및 [텍스처의 샘플링](#texture-sampling)의 영향을 받는 모든 매개 변수 값이 포함됩니다.   반대로 [정적 매개 변수](#static-parameter)의 경우 그래프를 SBSAR 파일로 컴파일한 후 동적 매개 변수 값을 즉시 조정할 수 있습니다. |

## E

|  |  |
| --- | --- |
| <b><span id="evaluation"></span>평가</b> | 그래프에서 데이터 및 매개 변수의 전달을 확인하는 프로세스입니다. 평가는 그래프와 해당 연결의 유효성을 확인하고 [상속](#inheritance)을 적용하고 그래프를 [요리사](#cooking)합니다.   그래프 뷰에서 연결을 평가하지 않으면 연결이 점선으로 표시됩니다. 평가하면 연결이 실선으로 바뀝니다.    그래프에서 매개 변수를 조정할 때마다 이 매개 변수를 호스팅하는 노드와 다운스트림 모든 노드는 [무효화](#invalidation)되며 [렌더링](#rendering)되기 전에 다시 평가해야 합니다. |

## F

|  |  |
| --- | --- |
| <b><span id="filter"></span>필터</b>(노드) | 이미지에 변형(예를 들어, 변형)을 적용하거나 그로부터 정보(예를 들어, 마스크)를 추출하는 노드이다. |

## G

|  |  |
| --- | --- |
| <b><span id="ghost-instance-node"></span>고스트 인스턴스 노드</b> | 찾을 수 없는 하위 그래프(예: 누락된 [종속성](#dependency))을 참조하는 [인스턴스 노드](#instance-node)가 고스트 인스턴스 노드로 로드되었습니다.   누락된 종속성을 확인하고 [패키지](#package)를 다시 로드하면 고스트 인스턴스 노드가 원하는 상태로 복원됩니다. |
| <b><span id="glossiness"></span>광택</b> | PBR Specular 광택 [음영](../glossary/glossary.md) 모델을 사용하여 정의된 [재질](../glossary/glossary.md)의 채널입니다. 광택은 표면의 거칠음(예: *미세 면*&#x200B;이라고도 하는 Height의 미세 변형)을 지정합니다.   높은 광택은 부드러운 느낌을 만드는 반면 낮은 광택은 거칠고 매트한 느낌을 줍니다.   [거칠음](#roughness)의 역입니다. |

## H

|  |  |
| --- | --- |
| <b><span id="histogram"></span>막대 그래프(이미지)</b> | 이미지의 컨텍스트에서 히스토그램은 주어진 범위(종종 [0, 1])에 있는 값의 모집단을 나타냅니다.   이 모집단은 세로 막대를 사용하여 시각화되며, 이미지에 더 많은 값이 존재하면 해당 값에 대한 막대가 더 높아집니다. 막대는 낮은 값(어두운 영역)부터 높은 값(밝은 영역)까지 수평으로 분포됩니다.   색상 이미지의 막대 그래프는 일반적으로 각 채널의 막대 그래프(일반적으로 R, G, B)와 겹칩니다. |

## I

|  |  |
| --- | --- |
| <b><span id="inheritance"></span>상속</b> | Substance 그래프의 컨텍스트에서 상속은 업스트림 노드 또는 상위 그래프에서 매개변수 값을 얻는 노드의 속성을 설명합니다.   상속된 매개 변수에는 [해상도](#resolution)([출력 크기](#output-size)), [비트 심도](#bit-depth)([출력 형식](#output-format)) 및 [타일링](#tiling) 모드가 포함됩니다.   이 [전용 페이지](../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)의 상속에 대해 자세히 알아보세요. |
| <b><span id="instance-node"></span>인스턴스 노드</b> | 인스턴스 노드는 그래프 A를 다른 그래프 B로 나타낸다. 이 경우, 그래프 A는 그래프 B의 [하위 그래프](#subgraph)로 불릴 수 있다. 그래프 A의 모든 변경 내용은 이를 나타내는 모든 인스턴스 노드에 전파됩니다.   인스턴스 노드는 그래프 B의 컨텍스트에서 그래프 A의 입력 매개변수에 대해 고유한 값 세트를 적용합니다. 그러한 의미에서, 그래프 B는 모든 것이 그래프 A를 참조하지만 각각 상이한 값 또는 텍스처를 입력으로서 그래프 A에 전달하는 다중 인스턴스 노드를 호스팅할 수 있다.   [atomic nodes](#atomic-node)가 아닌 Designer 라이브러리의 모든 노드는 인스턴스 노드입니다. |
| <b><span id="invalidation"></span>무효화</b> | 노드의 결과가 오래된 것으로 선언하는 프로세스입니다.   매개 변수를 조정하면 이 매개 변수를 호스팅하는 노드와 다운스트림 모든 노드가 무효화되므로 다시 [평가](#evaluation) 및 [렌더링](#rendering)해야 합니다. |

## M

|  |  |
| --- | --- |
| <b><span id="material"></span>재질</b> | 표면과 부피를 포함하는 공간의 물질 성질과 거동의 집합이다. 3D 공간에서 엔티티의 모양은 해당 재질에 의해 정의됩니다.   물질은 다양한 방식으로 정의될 수 있으며, 모든 정의는 굴절, 비등방성 또는 광택과 같은 모든 특성을 지지하지 않는다. [셰이더](#shader)는 재료 정의의 특정 구현입니다.   <b>중요:</b> &#39;물질&#39;이라는 용어는 다음을 비롯한 다양한 항목을 참조하는 데 사용되는 *우산 용어*&#x200B;입니다.<ul data-preserve-html="true"> <li data-preserve-html="true">표면이나 볼륨의 모양을 계산하는 데 사용되는 [셰이더](#shader);</li> <li data-preserve-html="true">셰이더에 제공된 [텍스처](#texture) 집합;</li> <li data-preserve-html="true">재질 ID는 서로 다른 재질을 사용하는 부분을 구분하는 데 사용되는 3D 프리미티브 요소의 속성입니다.</li> </ul> |
| <b><span id="mesh"></span>메시</b> | 모서리로 연결되어 삼각형과 같은 다각형을 형성하는 [정점](#vertex)으로 구성된 3D 개체가 서피스로 어셈블됩니다. 이러한 표면은 열려 있거나 닫혀 있을 수 있습니다.   이러한 서피스의 모양은 지정된 [재질](#material)에 의해 정의됩니다. 메시의 세부 수준도 [polycount](#polycount)에 크게 종속됩니다. |
| <b><span id="metadata"></span>메타데이터</b> | 파일 자체, 파일 환경 또는 파일 데이터와 관련된 모든 사항에 대한 정보를 제공하는 데이터입니다.   일반적인 메타데이터에는 파일 작성자, 작성 및 수정 날짜, 저작권 및 커버 아트가 포함됩니다.   Designer에서는 [패키지](#package)의 콘텐츠에 메타데이터도 포함할 수 있습니다. 예를 들어, 직물 재료를 생성하는 Substance 그래프는 직물의 물리적 특성에 대한 메타데이터를 가질 수 있다. |
| <b><span id="mipmap"></span>밉맵</b> | 자동으로 계산되는 더 작은 버전의 텍스처입니다.   텍스처에는 더 작은 버전의 피라미드가 있을 수 있으며, 이 피라미드는 최적의 품질과 성능을 위해 가장 적합한 크기가 사용되도록 런타임에 상호 교환 가능합니다.   예를 들어, 높은 빈도의 세부 묘사가 더 작은 크기로 표시되는 텍스처에서는 *모아레* 아티팩트가 생성될 수 있습니다. 또한 텍스처가 클수록 더 많은 [텍스처 샘플](#texture-sampling)이 포함될 수 있습니다.   &#39;mipmap&#39;이라는 용어는 MIP 매핑 기법에서 유래했습니다. 여기서 MIP는 &#39;작은 장소에 있는 많은 것들&#39;을 의미하는 라틴어 &#39;*parvo*&#39;을 의미합니다. |

## N

|  |  |
| --- | --- |
| <b><span id="node"></span>노드</b> | 계산을 수행하고 하나 이상의 결과를 출력하는 그래프의 개체   입력 매개 변수를 사용하여 결과를 제어합니다. 이러한 매개 변수는 속성 도크에서 컨트롤로 나열되거나 노드 자체에서 입력 커넥터로 나열될 수 있습니다.   노드에는 두 가지 기본 범주가 있습니다. [atomic nodes](#atomic-node)와 인스턴스 노드입니다. |
| <b><span id="noise"></span>노이즈</b> | 모양과 색상의 무작위 또는 의사 무작위 분포를 나타내는 비구상 이미지입니다. 노이즈는 종종 표면이나 변형에 변형을 추가하는 데 사용됩니다.   Designer의 노드 라이브러리에는 [BnW 스팟](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md), [구름](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md), [펄린 노이즈](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/perlin-noise/perlin-noise.md) 또는 [보로노이](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/voronoi/voronoi.md)와 같은 많은 노이즈 생성기가 포함되어 있습니다. |
| <b><span id="normal"></span>표준</b> | 3D 컴퓨팅에서 표면의 법선은 해당 표면에서 바깥쪽으로 향하는 표면에 수직인 [정규화](#normalization) 벡터이다.   이 벡터는 3D 공간에서 표면의 방향을 나타내며 장면의 조명 및 카메라 원근감에 따라 해당 표면을 [음영](#shader)하는 데 사용됩니다.   [표준 맵](#normal-map) 텍스처를 표면에 적용하여 표준을 수정하고 세부 정보를 추가할 수 있습니다. |
| <b><span id="normal-map"></span>표준 맵</b> | 수직을 수정하기 위해 서피스에 적용된 텍스처입니다.   모형의 기하학에 포함시키기에는 비효율적일 수 있는 디테일을 위조하는 데 가장 자주 사용됩니다. 이러한 맵을 사용하면 정점별 수직 외에 텍셀별 수직을 가질 수 있으므로 표면 정보가 더 많아져 표면 세부 정보가 더 많아집니다.   법선 벡터의 X, Y, Z 좌표는 각각 맵의 빨강, 초록, 파랑 채널로 부호화된다. 대상 그래픽 API([DirectX](#directx) 또는 [OpenGL](#opengl))에 따라 녹색 채널이 반전될 수 있습니다. |
| <b><span id="normalization"></span>정규화</b> | 값 범위를 [0, 1] 범위로 다시 매핑하는 프로세스입니다. 여기서 가장 높은 입력 값은 1.0으로 다시 매핑되고 가장 낮은 입력 값은 0.0으로 다시 매핑됩니다.   벡터의 경우 정규화는 벡터의 길이(또는 &#39;크기&#39;)를 1.0의 값으로 조정하는 것입니다. |

## O

|  |  |
| --- | --- |
| <b><span id="opengl"></span>OpenGL</b> | 비디오 게임 개발 및 기타 3D 산업에서 널리 사용되는 3D 그래픽 API입니다.   OpenGL은 텍스처의 원점(즉, (0, 0) 좌표)을 *왼쪽 아래*(Y축 방향)에 배치하는 반면 [DirectX](#directx) API는 *왼쪽 위*(Y축 방향)에 배치합니다.   즉, OpenGL 표준 맵에 DirectX과 비교하여 *반전된 녹색 채널*&#x200B;이 있습니다. 실제로, 초록색 채널은 법선벡터의 Y좌표를 호스팅한다. |
| <b><span id="openusd"></span>OpenUSD</b> | [USD](#usd)을(를) 참조하십시오. |
| <b><span id="output-format"></span>출력 형식</b> | 노드의 [비트 심도](#bit-depth)을(를) 설명하는 Substance 그래프에 있는 노드의 [기본 매개 변수](#base-parameter)입니다. |
| <b><span id="output-size"></span>출력 크기</b> | 노드의 [해상도](#resolution)를 설명하는 Substance 그래프에 있는 노드의 [기본 매개 변수](#base-parameter)입니다.   이 [전용 페이지](../compositing-graphs/output-size/output-size.md)의 출력 크기에 대해 자세히 알아보세요. |

## P

|  |  |
| --- | --- |
| <b><span id="package"></span>패키지</b> | Substance 3D 파일([SBS](#sbs-file))은 그래프, [비트맵](#bitmap), [3D 장면](#three-d-scene) 등의 리소스에 대한 컨테이너라는 점에서 패키지라고 합니다. 패키지는 [메타데이터](#metadata)뿐만 아니라 [종속성](#dependency)에 대한 경로도 저장합니다. |
| <b><span id="pattern"></span>패턴</b> | 다른 이미지를 생성하기 위한 모델 또는 참조로 사용해야 하는 이미지입니다.   대부분의 경우에, 패턴은 반복되도록 의도된 이미지(예를 들어, 타일링되거나, 무작위로 흩어지거나 또는 일부 세트의 규칙에 따라 배열됨)이다. |
| <b><span id="pixel-ratio"></span>픽셀 비율</b> | 이 [기본 매개 변수](#base-parameter)는 픽셀 수준에서 이미지의 종횡비 보상을 제어합니다. 다시 말해, 정사각형이 아닌 이미지에서 정방형 비율을 보전하기 위해 픽셀 크기를 보정해야 하는지 여부이다.   이 매개 변수는 비 로컬 필터, 즉 인접 픽셀의 값을 사용하여 픽셀의 값을 계산하는 필터에 의해 사용됩니다. |
| <b><span id="pixel-size"></span>픽셀 크기</b> | 이 기본 매개 변수는 픽셀의 가로 및 세로 크기를 정의합니다.   이는 비-로컬 필터, 즉 인접 픽셀의 값을 사용하여 픽셀의 값을 계산하는 필터에 대한 승수의 역할을 합니다. |
| <b><span id="polycount"></span>Polycount</b> | 3D [메시](#mesh)의 다각형의 양입니다. 실제로 polycount는 &#39;polygon count&#39;에 비해 짧습니다.   더 많은 다각형을 사용하여 더 세밀한 세부 묘사를 모델링할 수 있습니다. 폴리카운트가 낮은 메시를 &#39;낮은 폴리&#39;라고 하며, 폴리카운트가 높은 메시를 &#39;높은 폴리&#39;라고 합니다. |
| <b><span id="primary-input"></span>기본 입력</b> | 해당 노드가 [기본 매개 변수](#base-parameter) 값을 상속하는 [인스턴스 노드](#instance-node)의 입력 커넥터입니다.   기본 입력은 해당 커넥터에 작은 점으로 표시되고 레이블에 &#39;(기본) 접미사가 표시됩니다.   둘 이상의 입력이 있는 노드를 사용할 때는 해당 입력 중 어느 것이 기본 입력이고 그래프 전체에서 [상속](#inheritance)에 어떤 영향을 미치는지 유의하는 것이 *적극*&#x200B;입니다. |
| <b><span id="procedural"></span>절차</b> | 수동으로 만드는 것이 아니라 컴퓨터 알고리즘을 따라 만들 데이터 또는 아티팩트의 특성입니다.   Designer에서는 알고리즘이 노드 그래프로 디자인되는 절차 워크플로우를 사용합니다.     절차 워크플로를 사용하면 알고리즘과 해당 매개 변수를 수정하여 변경 및 조정을 빠르게 생성할 수 있으므로 더 빠른 반복이 가능합니다.   알고리즘으로 결과가 완전히 생성되면 그 결과는 구어적으로 &#39;100% 절차&#39;라고 일컬어진다. 절차 생성이 &#39;proc-gen&#39;으로 단축되는 경우가 있습니다.   Designer 노드 라이브러리의 대부분의 생성기는 결과를 생성하기 위해 입력 이미지가 필요하지 않다는 점에서 100% 절차적입니다. |
| <b><span id="publishing"></span>게시(SBSAR)</b> | Designer에서 게시란 [패키지](#package)를 SBSAR 보관 파일로 내보내는 것을 말하며, 여기에는 [컴파일된](#compilation) 버전의 그래프, 해당 리소스([비트맵](#bitmap), 글꼴 등), 해당 사전 설정과 [메타데이터](#metadata)가 포함됩니다.   그런 다음 결과 SBSAR 파일이 [Substance 3D 플러그인](https://substance3d.adobe.com/plugins/)을 통해 다른 Substance 3D 응용 프로그램 또는 서드파티 응용 프로그램에서 배포되고 사용될 수 있습니다. |

## R

|  |  |
| --- | --- |
| <b><span id="renderer"></span>렌더러</b> | 조명, 메시, 재질과 같은 3D 정보를 처리하여 2D 이미지를 만드는 프로그램입니다. |
| <b><span id="rendering"></span></b> 렌더링 중(3D 보기) | [렌더러](#renderer)와 같은 프로그램을 사용하여 입력 데이터에 따라 이미지를 계산하는 프로세스입니다. |
| <b><span id="resolution"></span>해상도</b> | [비트맵](#bitmap)을 형성하는 가로 및 세로 픽셀 양입니다. 더 많은 픽셀을 사용하여 더 세밀한 세부 사항을 표현할 수 있습니다.   Substance 그래프에서 [노드](#node)에 의해 계산되는 비트맵의 해상도는 노드의 &#39;[출력 크기](#output-size)&#39; [기본 매개 변수](#base-parameter)에 의해 제어됩니다. |
| <b><span id="roughness"></span>거칠음</b> | PBR 금속 거칠기 [음영](../glossary/glossary.md) 모델을 사용하여 정의된 [재질](../glossary/glossary.md)의 채널입니다. 거칠기는 표면의 거칠기, 즉 *미세 면*&#x200B;이라고도 하는 Height의 미세 변형을 지정합니다.   높은 거칠기는 매트한 느낌을 주는 반면 낮은 거칠기는 매끄럽고 광택이 나는 느낌을 줍니다.   [광택](#glossiness)의 역입니다. |

## S

|                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>샘플링</b>(샘플) | 특정 지점에서 이미지 또는 함수의 값을 가져옵니다.   [텍스처 샘플링](#texture-sampling)을 참조하세요. |
| <b><span id="sbs-file"></span>SBS 파일</b> | SBS는 &#39;Substance 3D 파일&#39;을 의미합니다. 이 파일은 Substance 3D Designer 프로젝트를 저장하는 데 사용됩니다. 해당 데이터는 [XML](#xml) 형식을 사용합니다. [패키지](#package)를 참조하세요. |
| <b><span id="sbsar-file"></span>SBSAR 파일</b> | SBSAR는 &#39;Substance 3D ARchive&#39;를 나타냅니다. 이 보관 파일은 컴파일된 Substance 3D Designer 그래프와 이 그래프에 필요한 리소스([비트맵](#bitmap), 글꼴 등)를 저장하는 데 사용됩니다.   SBSAR은 다른 Substance 3D 응용 프로그램과 Substance 3D 플러그인에서 사용할 수 있는 Substance 그래프를 배포하는 데 사용되는 기본 파일 형식입니다.   SBSAR 파일에 저장된 그래프는 컴파일되므로 Substance 3D Designer에서 로드 및 편집할 수 없습니다. 그러나 [7Zip](https://www.7-zip.org/)을 사용하여 SBSAR 파일을 열어 포함된 [XML](#xml) 파일에서 매개 변수, 사전 설정 및 메타데이터를 검색할 수 있습니다. |
| <span id="sdf"></span><b>SDF</b> | [서명된 거리 필드](#signed-distance-field)를 참조하세요. |
| <b><span id="shader"></span>셰이더</b> | [재질](#material) 속성, 들어오는 빛 및 보고 있는 위치에 따라 표면이나 볼륨의 모양을 계산하는 프로그램입니다. 셰이더는 재료 정의의 특정 구현입니다.   텍스처는 그것의 비헤이비어를 구동하기 위해 셰이더에 제공될 수 있다. Raw 값도 사용할 수 있습니다. [3D 보기](../interface/3d-view/3d-view.md)에서 &#39;재질&#39; 메뉴로 이동하여 현재 장면의 재질에서 사용 중인 셰이더를 확인합니다. 또한 이 메뉴를 통해 [셰이더 속성](../interface/3d-view/3d-view.md)과 셰이더에서 현재 사용 중인 텍스처 및 값에 액세스할 수 있습니다.   &#39;Shader&#39;는 때때로 &#39;[Material](#material)&#39;과(와) 혼용되어 사용됩니다. |
| <span id="sheen"></span><b>광택</b> | 직물의 광택이나 광택이 나는 측면.   이 용어는 섬유 업계에서 미세한 색상 명도를 추가하는 반사 특성을 설명하는 데 널리 사용됩니다. |
| <b><span id="signed-distance-field"></span>SDF(서명된 거리 필드)</b> | <p>부호 있는 거리 필드는 공간의 임의의 점에서 서피스의 가장 가까운 점까지의 거리를 계산하여 3D 공간의 서피스를 정의하는 수학 함수입니다.</p><p>개념 및 Designer에서 사용하는 방법에 대한 자세한 내용은 [SDF 함수 작업](../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#what-is-an-sdf-function)을 참조하세요.</p> |
| <b><span id="spline"></span>스플라인</b> | 일반적으로 수학 함수를 사용하여 모델링한 곡선으로, 모든 해상도에서 깔끔하고 매끄러운 모양을 그릴 수 있습니다. Designer에서는 사용자 정의 데이터 형식을 사용하여 텍스처로 인코딩된 손실 근사치를 사용합니다.   스플라인은 길이 및 궤적에 대한 직관적인 컨트롤을 제공하며, Thickness 및 Height과 같은 다른 데이터를 포함하고, 이를 따라 임의의 지점에서 거리 및 방향에 쉽게 액세스할 수 있도록 합니다.   이러한 특성으로 인해 드로잉과 텍스처링에는 강력한 도구가 됩니다. |
| <b><span id="static-parameter"></span>정적 매개 변수</b> | 값을 변경할 수 없는 매개 변수입니다.   [동적 매개 변수](#dynamic-parameter)와 반대로 그래프를 SBSAR 파일로 컴파일하면 정적 매개 변수를 즉시 변경할 수 없습니다. 그래프가 작성되는 동안에만 Designer에서 노출하고 수정할 수 있습니다.   미리 보기 모드는 게시된 SBSAR 파일의 동작을 최대한 가깝게 일치시키기 위해 설정되므로 경우에 따라 이러한 매개 변수를 숨깁니다.   정적 매개 변수 목록은 [여기](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)에서 사용할 수 있습니다. |
| <b><span id="subgraph"></span>하위 그래프</b> | 다른 그래프에서 [인스턴스 노드](#instance-node)로 사용되는 그래프입니다. |
| <b><span id="substance-engine"></span>Substance 엔진</b> | Substance 3D 팀이 개발한 독자적인 기술로, 입력 이미지에 대해 다량의 변형, 효과 및 합성을 매우 효율적으로 수행하여 이미지를 컴퓨팅하는 역할을 담당합니다.   Substance 엔진은 Designer의 [atomic nodes](#atomic-node)를 구현하고 계산합니다.   엔진은 CPU, GPU 및 운영 체제에서 실행되는 플랫폼에 따라 다른 백엔드를 통해 구현됩니다. Designer에서는 [도구 > 엔진 전환](../interface/the-main-toolbar/the-main-toolbar.md)으로 이동하여 백엔드를 전환할 수 있습니다.   일부 백엔드는 다른 백엔드보다 훨씬 뛰어난 성능을 제공합니다(예: GPU 백엔드가 CPU보다 훨씬 빠름). 결과는 백엔드에서 약간 다를 수 있습니다. |
| <b><span id="substance-graph"></span></b><b>Substance 그래프</b>(또는 Substance 합성 그래프) | 하나 이상의 [비트맵](#bitmap)을 출력하는 그래프입니다.   Substance 그래프는 다양한 용도로 사용할 수 있습니다. - 재질을 설명하는 텍스처인 비트맵 세트를 생성합니다. - 하나 이상의 비트맵 입력에 대해 필터로 이미지 처리를 수행합니다. - 노이즈, 패턴 또는 원시 데이터를 생성기로 생성합니다. |

## T

|  |  |
| --- | --- |
| <b><span id="tessellation"></span>테셀레이션</b> | 컴퓨터 그래픽에서 테셀레이션이란 표면을 더 많은 다각형, 흔히 삼각형으로 세분화하는 과정이다.   이 프로세스는 런타임에 수행되어 3D 모델의 다각형의 양을 동적으로 늘릴 수 있으며, 종종 [변위](#displacement) 및 [표준 맵](#normal-map)과 함께 추가되어 추가된 다각형을 사용하여 더 미세한 세부 사항을 모델링합니다. |
| <b><span id="texel"></span>텍스트</b> | 픽셀이 사진의 정보 단위인 것과 비슷한 [텍스처](#texture)의 정보 단위입니다. |
| <b><span id="texture"></span>텍스처</b> | 그래픽을 나타내고, [셰이더](#shader)에 값을 제공하여 표면의 [재질](#material) 속성을 설명하고, 원본 데이터를 [텍셀](#texel)로 인코딩하는 데 사용되는 이미지입니다.   텍스처는 GPU에 의해 매우 효율적으로 압축을 풀고 조작할 수 있는 개체입니다. 대부분의 경우 이 효율성에는 텍스처가 1024x1024, 4096x4096, 512x256 등의 두 가지 해상도의 성능을 사용해야 합니다. |
| <b><span id="texture-sampling"></span>텍스처 샘플링</b> | 특정 위치에서 [텍스처](#texture) 값을 가져옵니다.   일부 알고리즘은 값들을 비교하거나, 그것들의 평균화, 또는 다른 연산들을 위해 많은 샘플들이 수행될 것을 요구한다.   픽셀의 정확히 중심에서 샘플을 수행하지 않는 경우 Designer에는 다음과 같은 두 가지 획득 값 옵션이 있습니다.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>가장 가까운 픽셀:</b> 중심에 따른 가장 가까운 픽셀 값</li> <li data-preserve-html="true"><b>쌍선형 필터링:</b> 인접한 픽셀이 더 가까운 픽셀에 더 많은 가중치가 있는 수평과 수직 사이의 보간 값입니다.</li> </ul> |
| <b><span id="tiling"></span>타일링</b> | 가시적인 이음새 또는 시각적 불연속 없이 이미지를 가로, 세로 또는 양방향으로 반복하는 것입니다.   Designer은 해당 타일에 [잡음](#noise) 또는 [패턴](#pattern)을 생성하는 [노드](#node)를 많이 제공합니다. 마찬가지로 많은 [필터](#filter) 노드는 타일링을 유지하면서 이미지를 처리하도록 설계되었습니다. |

## U

|  |  |
| --- | --- |
| <b><span id="usage"></span>사용(출력)</b> | Substance 그래프에서 용도는 응용 프로그램이 [텍스처](#texture)를 [3D 보기](../interface/3d-view/3d-view.md)의 [셰이더](#shader)에 연결하는 방법을 알리는 데 사용되는 [출력](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드의 특성입니다.   3D 뷰에 Substance 그래프를 적용하는 경우 모든 출력이 일치하는 사용에 따라 셰이더에 연결됩니다. 즉, &#39;basecolor&#39;에서 &#39;basecolor&#39;로, &#39;roughness&#39;에서 &#39;roughness&#39;로 구분됩니다.   &#39;재질&#39; 및 &#39;컴팩트 재질&#39; [링크 만들기 모드](../interface/the-graph-view/link-creation-modes/link-creation-modes.md)를 사용할 때 커넥터를 일치시키는 데 사용도 사용됩니다. |
| <b><span id="udim"></span>UDIM</b>(UV 타일) | [UV](#uv) 공간을 고유한 숫자 식별자를 가진 타일로 분할하는 표준으로, 이를 통해 각 타일에 서로 다른 텍스처를 할당할 수 있습니다.   UDIM 워크플로우는 충실도가 높은 에셋에 많은 디테일이 필요하기 때문에 고해상도 텍스처가 여러 개 필요한 VFX 파이프라인에서 흔히 볼 수 있습니다. 이 경우 에셋의 [UV](#uv)이(가) 여러 UDIM(또는 UV 타일)에 걸쳐 정렬됩니다.   Designer은 UDIM 워크플로우를 지원하며 UDIM마다 다른 Substance 그래프를 할당할 수 있습니다. |
| <b><span id="usd"></span>USD</b>(또는 OpenUSD) | [Universal Scene Description](https://openusd.org/release/index.html)&#x200B;(USD)는 Pixar에서 구축한 3D 장면 설명 형식으로, 응용 프로그램과 플랫폼 간의 상호 운용성과 데이터 교환을 위해 작성되었습니다.   USD 파일에는 장면에 사용된 데이터의 정의와 해당 장면의 구성, 그리고 모든 관련: 모델, 재료, 카메라, 애니메이션, 시뮬레이션 등 USD 파일이 포함됩니다. 응용 프로그램이 해당 데이터를 올바르게 읽고 사용할 수 있도록 USD 플러그인에 액세스할 수 있는 경우 USD 파일에는 모든 유형의 데이터가 포함될 수 있습니다.   Adobe은 형식 개발 및 표준화에 적극적으로 기여하는 3D 업계 전문가의 컨소시엄인 [Alliance for OpenUSD](https://blog.adobe.com/en/publish/2023/08/01/powering-3d-interoperability-continued-collaboration-through-openusd)에 참여하고 있습니다. |
| <b><span id="uv"></span>UV</b> | UV는 2D 공간에서 3D 모델을 나타냅니다. 2D 공간에서 2D 이미지를 3D 공간의 모델 표면에 매핑하는 데 사용됩니다.   UV를 만드는 과정은 종종 솔기를 펼쳐 납작하게 만드는 것으로 묘사됩니다. |

## V

|  |  |
| --- | --- |
| <b><span id="vertex"></span>정점</b> | 두 개 이상의 선이 만나는 고유한 공간입니다. |

## X

|  |  |
| --- | --- |
| <b><span id="xml"></span>XML</b> | XML(eXtensible Markup Language)은 사람이 읽을 수 있는 형식으로 데이터를 저장하는 형식입니다.   태그와 유사하게 HTML(&lt;>)와 값을 사용하여 정의된 데이터는 태그 안에 포함됩니다.   [SBS](#sbs-file) 파일 형식은 XML을 사용하여 데이터를 정렬하고 저장합니다. |

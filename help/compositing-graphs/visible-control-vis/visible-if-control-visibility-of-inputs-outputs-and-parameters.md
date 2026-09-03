---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: Substance 3D Designer에서 표현식이 조건에 따라 매개 변수 표시 여부를 제어하는 경우 표시되는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 표현식이 있는 경우 표시
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# 표현식이 있는 경우 표시

&#39;Visible if&#39; 식을 사용하면 그래프에서 입력, 출력 및 매개 변수의 <b>가시성을 제어할 수 있습니다</b>.

[매개 변수를 노출](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)할 때 다른 매개 변수의 상태에 따라 매개 변수 또는 노드 커넥터를 숨기거나 표시할 수 있습니다. 예를 들어, 슬라이더는 부울 매개 변수 단추가 `true`(으)로 설정된 경우에만 표시되는데, 이는 그렇지 않은 경우 아무런 영향을 주지 않고 사용자에게 혼동을 줄 수 있기 때문입니다.

이를 위해 다음 항목의 <b>보이는 경우</b> 속성에 *논리 식*&#x200B;을 입력할 수 있습니다.

* 그래프의 [입력 매개 변수](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md);
* 그래프의 [입력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) 노드;
* 그래프의 [출력](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) 노드입니다.

![입력 매개 변수 표시 여부 전환](visible-if-control-visibility-of-inputs-outputs-and-parameters.resources/visible-if-control-visibility-of-inputs-outputs-and-parameters-01.gif "입력 매개 변수 표시 여부 전환"){width="512px"}

논리 식이 `true`(으)로 평가되면 매개 변수, 입력 또는 출력이 현재 그래프를 나타내는 모든 [인스턴스 노드](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)에 표시됩니다. 그렇지 않으면 *숨김*&#x200B;이 됩니다.

이러한 조건을 명시하는 논리식이 유효하다면 복잡한 조건이 가능하다.

>[!NOTE]
>
> 주의 사항
> 
> * 이 기능 *전용*&#x200B;은 매개 변수 또는 커넥터가 사용자 인터페이스에 표시되는지 여부에 영향을 주며, 그래프의 계산 및 결과에 *영향을 주지 않습니다*.
> * &#39;Visible if&#39; 문에 사용된 매개 변수에 함수를 표시하거나 적용하는 경우 해당 문은 *무시되고* 기본값이 &#39;true&#39;로 설정됩니다.

>[!IMPORTANT]
>
> 이 기능은 Substance 3D 에코시스템 내에서 작동하지만 일부 통합에서는 지원하지 않을 수 있습니다. 지원되지 않는 경우 표시 조건 기본값은 `true`입니다.

## &#39;보이는 경우&#39; 표현식 쓰기

### 입력 매개 변수 액세스

모든 표시 표현식에서 적어도 하나의 입력을 사용해야 하는 경우 다음 구문을 통해 수행할 수 있습니다.

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> **식별자**&#x200B;는 기존 입력 매개 변수의 **식별자** 속성의 *정확한* 이름이어야 하며 *대/소문자를 구분*&#x200B;해야 합니다. *해당 레이블로 매개 변수를 참조할 수 없습니다*.\
>  참조된 매개 변수가 없거나 논리 식이 잘못된 경우 *경고*&#x200B;가 **보이는 경우** 속성에 표시됩니다.

### 사용 가능한 연산자

&quot;표시되는 경우&quot; 필드에는 다음과 같은 매개 변수가 허용됩니다.

* 부울, 부동 및 정수 입력입니다.
* `true` 및 `false` 값(대/소문자 구분, 대문자 없음)
* `.x` : 하위 매개 변수에 액세스합니다.
* `&&`<b> </b>: 및
* `||`<b> </b>: 또는
* `!`<b> </b>: 아님
* `<`<b>, </b>`>`<b>, </b>`<=`<b>, </b>`>=`<b>, </b>`==`<b>, </b>`!=` : 비교
* `()` : 대괄호

### 항상 부울로 평가해야 함

Visible If 식이 &quot;IF&quot; 문의 조건으로 사용되므로 항상 `true` 또는 `false`이(가) 생성되어야 합니다.

* 부울 값은 조건으로 직접 평가할 수 있습니다. 부울 값이 있는 단순 단추는 이 이상 필요하지 않습니다. 아래 예제, 첫 번째 사례 참조
* 비 부울 매개 변수에는 일반적으로 *비교* 작업이 필요합니다. 비교 연산자는 위, 예제는 아래를 참조하십시오.
* 일부 비부울 값은 *truthy* 또는 *falsy*&#x200B;일 수 있습니다. 즉, `false`의 `true`(으)로 평가할 수 있습니다. `0`의 정수 값이 false로 평가됩니다.

## 예

| 조건(&quot;If&quot;) | 수식 | 메모 |
| --- | --- | --- |
| True | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input은 부울 값입니다. |
| False | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input은 부울 값입니다. |
| 보다 낮음 | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input은 정수 값입니다. |
| Equal | ` input["param1"] == 2   input.param1 == 2 ` | param1은 부동 소수점 또는 정수 값입니다. |
| 보다 낮음 | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input은 float 또는 하나 이상의 구성 요소(예: float2(x, y), integer3(x, y, z))가 있는 정수 값입니다. |
| Or | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1 및 param2는 부울 값입니다 |
| And | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1 및 param2는 부동 소수점 또는 정수 값입니다 |

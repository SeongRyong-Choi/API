---
description: 지도 설정 및 제어를 위한  API를 제공합니다.
---

# JSMap

## addHeatMaps\([CJSVec3Array](CJSVec3Array.md) pointArray\)
> 히트맵 좌표 리스트 배열을 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| pointArray | [CJSVec3Array](CJSVec3Array.md) | 히트맵 좌표 리스트 배열 |
* Detail
  * pointArray : ([JSVector3D](JSVector3D.md), [JSVector3D](JSVector3D.md), ...) 히트맵 좌표 리스트 배열
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=effect_heatmap
{% endtab %}
{% endtabs %}

## clearHeatMap\(\)
> 히트맵을 초기화 합니다.
{% tabs %}
{% tab title="Parameter" %}
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=effect_heatmap
{% endtab %}
{% endtabs %}

## clearInputPoint\(\)
> 입력된 좌표 리스트를 초기화 합니다.
{% tabs %}
{% tab title="Parameter" %}
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=object_polygon_height
{% endtab %}
{% endtabs %}

## clearSelectObj\(\)
> 오브젝트 선택 상태를 해제합니다.
{% tabs %}
{% tab title="Parameter" %}
* Code
  * Module.getMap().clearSelectObj();
{% endtab %}
{% endtabs %}

## clearSnowfallArea\(\)
> 적설 효과를 초기화 합니다.
{% tabs %}
{% tab title="Parameter" %}
* Code
  * Module.getMap().clearSnowfallArea();
{% endtab %}
{% endtabs %}

## getInputPoints\(\) → [CJSVec3Array](CJSVec3Array.md)
> 입력된 좌표 리스트를 반환합니다.
{% tabs %}
{% tab title="Parameter" %}
* Detail
  * [CJSVec3Array](CJSVec3Array.md) : 입력된 좌표 리스트
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=analysis_terrain_edit
{% endtab %}
{% endtabs %}

## getInputPointList\(\) → [CJSCollection](CJSCollection.md)
> 입력된 좌표 리스트를 반환합니다.
{% tabs %}
{% tab title="Parameter" %}
* Detail
  * [CJSCollection](CJSCollection.md) : 입력된 좌표 리스트
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=object_pipe
{% endtab %}
{% endtabs %}
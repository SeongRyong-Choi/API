---
description: 2D 그리드 객체를 위한 API를 제공합니다.
---

# JSColorGrid

Module createColorGrid API로 생성할 수 있습니다.

```javascript
var colorGrid = Module.createColorGrid("COLOR_GRID_2D");
```

## SetGridPosition([CJSVector2D](CJSVector2D.md) leftTop, [CJSVector2D](CJSVector2D.md) rightTop, [CJSVector2D](CJSVector2D.md) rightBottom, [CJSVector2D](CJSVector2D.md) leftBottom, number altitude, number rowNum, number colNum) → number

> 3D 그리드 객체를 생성합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter   | Type                          | Contents   |
| ----------- | ----------------------------- | ---------- |
| leftTop     | [CJSVector2D](CJSVector2D.md) | 좌상단 경위도 좌표 |
| rightTop    | [CJSVector2D](CJSVector2D.md) | 우상단 경위도 좌표 |
| rightBottom | [CJSVector2D](CJSVector2D.md) | 우하단 경위도 좌표 |
| leftBottom  | [CJSVector2D](CJSVector2D.md) | 좌하단 경위도 좌표 |
| altitude    | number                        | 객체 높이      |
| rowNum      | number                        | 가로 그리드 개수  |
| colNum      | number                        | 세로 그리드 개수  |
{% endtab %}

{% tab title="Detail" %}
```
var colorGrid3D = Module.createColorGrid3D("COLOR_GRID_3D");
var gridCellNum = colorGrid3D.SetGridPosition(
	new Module.JSVector2D(124.2, 39), 	// 그리드 좌상단
	new Module.JSVector2D(130.5, 39), 	// 그리드 우상단
	new Module.JSVector2D(130.5, 34.5), 	// 그리드 우하단
	new Module.JSVector2D(124.2, 34.5), 	// 그리드 좌하단
	100000.0, 				// 그리드 바닥면 고도
	rowNum, 				// 그리드 가로 셀 갯수
	colNum					// 그리드 세로 셀 갯수
);
```

* Return
  * 총 그리드 개수
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=object\_grid\_3d
{% endtab %}
{% endtabs %}

## SetGridCellDefaultColor([CJSColor](CJSColor.md) color) → boolean

> 초기 그리드 색상값을 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type                    | Contents |
| --------- | ----------------------- | -------- |
| color     | [CJSColor](CJSColor.md) | 그리드 색상값  |
{% endtab %}

{% tab title="Detail" %}
```
var colorGrid3D = Module.createColorGrid3D("COLOR_GRID_3D");
colorGrid3D.SetGridCellDefaultColor(new Module.JSColor(255, 255, 255, 0));
```

* Return
  * 설정 성공 (true) 혹은 실패 (false)
  * 다음의 경우 API는 false 을 반환합니다.\
    1\) 엔진이 정상적으로 로드되지 않았을 경우
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=object\_grid\_3d
{% endtab %}
{% endtabs %}
---
description: 지도 내 카메라 설정 API를 제공합니다.
---

# JSCamera

## getTilt\(\)

> 카메라의 Tilt를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 카메라의 Tilt

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let tilt = camera.getTilt();
```
{% endtab %}
{% endtabs %}

## setTilt\(double \_tilt\)

> 카메라의 Tilt를 설정합니다.

{% tabs %}
{% tab title="Return" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _tilt | double | 카메라 Tilt

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let tilt = 45;
camera.setTilt(tilt);
```
{% endtab %}
{% endtabs %}

## getDirect\(\)

> 카메라가 바라보는 각도를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 카메라의 방향 각도
* 반환 정보
  * 0도 : 북쪽
  * 90도 : 동쪽
  * 180도 : 남쪽
  * -180도 : 남쪽
  * -90도 : 서쪽
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let direct = camera.getDirect();
```
{% endtab %}
{% endtabs %}

## getAltitude\(\)

> 카메라의 고도를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 카메라의 고도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let alt = camera.getAltitude();
```
{% endtab %}
{% endtabs %}

## getFov\(\)

> 카메라의 FOV 각도를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 카메라의 FOV

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let fov = camera.getFov();
```
{% endtab %}
{% endtabs %}

## getCenterPoint\(\)

> 화면 중심의 지도 좌표를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| CJSVector3D | 화면 중심의 지도 좌표

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let center = camera.getCenterPoint();
console.log(center.Longitude);		// 경도
console.log(center.Latitude);		// 위도
console.log(center.Altitude);		// 고도
```
{% endtab %}
{% endtabs %}

## getLocation\(\)

> 카메라의 위치를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| CJSVector3D | 카메라 위치

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let position = camera.getLocation();
console.log(position.Longitude);	// 경도
console.log(position.Latitude);		// 위도
console.log(position.Altitude);		// 고도
```
{% endtab %}
{% endtabs %}

## removeAtIndex\(number \_index\)

> 레이어 오브젝트 리스트에서 인덱스 번호에 해당되는 오브젝트 삭제

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_index | number | 삭제 오브젝트 인덱 |

* 반환 정보
  * boolean
    * TRUE : 오브젝트 삭제 성공
    * FALSE : 오브젝트 삭제 실패
{% endtab %}

{% tab title="Code" %}
```javascript
let layername = "objectlayer"
let layerList = new Module.JSLayerList(true);
let    layerList.createLayer(layername );

// object 생성 과정

layer.addObject(object, 0);
layer.removeAtIndex(0);
```
{% endtab %}
{% endtabs %}


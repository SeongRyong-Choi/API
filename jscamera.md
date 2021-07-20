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
| _tilt | double | 입력 카메라 Tilt

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

## setDirect\(double \_direct\)

> 카메라의 방향 각도를 설정합니다.

{% tabs %}
{% tab title="Return" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _direct | double | 입력 카메라 방향 각도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let direct = 45;
camera.setDirect(direct);
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

## setAltitude\(double \_alt\)

> 카메라의 고도를 설정합니다.

{% tabs %}
{% tab title="Return" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _alt | double | 입력 카메라 고도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let alt = 2000;
camera.setAltitude(alt);
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

## setFov\(double \_fov\)

> 카메라의 FOV를 설정합니다.

{% tabs %}
{% tab title="Return" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _fov | double | 입력 카메라 FOV

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let fov = 2000;
camera.setFov(fov);
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

## setLocation\(CJSVector3D \_position\)

> 카메라의 위치를 설정합니다.

{% tabs %}
{% tab title="Return" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _position | CJSVector3D | 입력 카메라 위치

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let position = new Module.JSVector3D(126.92836647767662, 37.52439503321471, 1000.0);
camera.setLocation(position);
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


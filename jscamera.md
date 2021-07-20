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
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _tilt | double | 입력 카메라 Tilt

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let tilt = 45.0;
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
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _direct | double | 입력 카메라 방향 각도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let direct = 45.0;
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
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _alt | double | 입력 카메라 고도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let alt = 2000.0;
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
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _fov | double | 입력 카메라 FOV

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let fov = 2000.0;
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
{% tab title="Parameter" %}
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

## getMoveMode\(\)

> 카메라의 회전모드를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| bool | 카메라 회전모드
* 반환 정보
  * true : 1인칭 시점 회전
  * false : 3인칭 시점 회전
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let mode = camera.getMoveMode();
```
{% endtab %}
{% endtabs %}

## setMoveMode\(bool \_mode\)

> 카메라의 회전모드를 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _mode | bool | 카메라 회전모드
* Parameter 정보
  * true : 1인칭 시점 회전
  * false : 3인칭 시점 회전
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
camera.setMoveMode(false);
```
{% endtab %}
{% endtabs %}

## getDistance\(\)

> 카메라의 시점 ~ 위치 거리를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 시점 ~ 위치 거리(m 단위)

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let distance = camera.getDistance();
```
{% endtab %}
{% endtabs %}

## setDistance\(double \_distance\)

> 카메라의 시점 ~ 위치 거리를 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _distance | double | 시점 ~ 위치 거리 (m 단위)
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let distance = 2000.0;
camera.setDistance(distance);
```
{% endtab %}
{% endtabs %}

## getLimitTilt\(\)

> 카메라의 제한된 최소 Tilt값을 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 제한된 최소 Tilt

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let tilt = camera.getLimitTilt();
```
{% endtab %}
{% endtabs %}

## setLimitTilt\(double \_tilt\)

> 카메라의 시점 ~ 위치 거리를 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _tilt | double | 제한할 최소 Tilt
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let tilt = 30.0;
camera.setLimitTilt(tilt);
```
{% endtab %}
{% endtabs %}

## getLimitAltitude\(\)

> 카메라의 제한된 최소 고도값을 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 제한된 최소 고도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let alt = camera.getLimitAltitude();
```
{% endtab %}
{% endtabs %}

## setLimitAltitude\(double \_alt\)

> 카메라의 제한된 최소 고도값을 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _alt | double | 제한할 최소 고도
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let alt = 3000.0;
camera.setLimitAltitude(alt);
```
{% endtab %}
{% endtabs %}

## getAnimationSpeed\(\)

> 마우스에 의한 카메라의 이동 속도를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| double | 이동 속도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let speed = camera.getAnimationSpeed();
```
{% endtab %}
{% endtabs %}

## setAnimationSpeed\(double \_speed\)

> 마우스에 의한 카메라의 이동 속도를 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _speed | double | 이동 속도
* Parameter 정보
  * 1.0 ~ 10.0 사이 값으로 설정 가능
  * 값이 클 수록 속도가 빨라집니다.
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let speed = 5.0;
camera.setAnimationSpeed(speed);
```
{% endtab %}
{% endtabs %}

## getCameraSpeed\(\)

> API에 의한 카메라의 이동 속도를 반환합니다.

{% tabs %}
{% tab title="Return" %}
| Type | Contents |
| :--- | :--- |
| int | 이동 속도

{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let speed = camera.getCameraSpeed();
```
{% endtab %}
{% endtabs %}

## setCameraSpeed\(double \_speed\)

> API에 의한 카메라의 이동 속도를 설정합니다.

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| _speed | int | 이동 속도
* Parameter 정보
  * 1 ~ 10 사이 값으로 설정 가능
  * 값이 클 수록 속도가 빨라집니다.
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let speed = 5.0;
camera.setCameraSpeed(speed);
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


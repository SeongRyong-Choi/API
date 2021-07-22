---
description: 지도 내 카메라 설정 API를 제공합니다.
---

# JSCamera

## getTilt\(\)

> 카메라 Tilt 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라 현재 Tilt 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let tilt = camera.getTilt();
```
{% endtab %}
{% endtabs %}

## setTilt\(number \_tilt\)

> 카메라 Tilt 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_tilt | number | 설정할 Tilt값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let tilt = 45.0;
camera.setTilt(tilt);
```
{% endtab %}
{% endtabs %}

## getDirect\(\)

> 카메라 방향 각도 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 0도 : 북쪽
    * 90도 : 동쪽
    * 180도 : 남쪽
    * -180도 : 남쪽
    * -90도 : 서쪽
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let direct = camera.getDirect();
```
{% endtab %}
{% endtabs %}

## setDirect\(number \_direct\)

> 카메라 방향 각도 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_direct | number | 설정할 카메라 방향 각도값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let direct = 45.0;
camera.setDirect(direct);
```
{% endtab %}
{% endtabs %}

## getAltitude\(\)

> 카메라 고도 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라 현재 고도 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let alt = camera.getAltitude();
```
{% endtab %}
{% endtabs %}

## setAltitude\(number \_alt\)

> 카메라 고도 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_alt | number | 설정할 카메라 고도값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let alt = 2000.0;
camera.setAltitude(alt);
```
{% endtab %}
{% endtabs %}

## getFov\(\)

> 카메라 FOV 각도 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라 현재 FOV 각도 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let fov = camera.getFov();
```
{% endtab %}
{% endtabs %}

## setFov\(number \_fov\)

> 카메라 FOV 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_fov | number | 설정할 카메라 FOV값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let fov = 2000.0;
camera.setFov(fov);
```
{% endtab %}
{% endtabs %}

## getLocation\(\)

> 카메라 위치 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * CJSVector3D Type
    * 카메라 현재 위치 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let position = camera.getLocation();
console.log(position.Longitude);    // 경도
console.log(position.Latitude);        // 위도
console.log(position.Altitude);        // 고도
```
{% endtab %}
{% endtabs %}

## setLocation\(CJSVector3D \_position\)

> 카메라 위치 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_position | CJSVector3D | 설정할 카메라 위치값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let position = new Module.JSVector3D(126.92836647767662, 37.52439503321471, 1000.0);
camera.setLocation(position);
```
{% endtab %}
{% endtabs %}

## getMoveMode\(\)

> 카메라 회전모드 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * boolean Type
    * true : 1인칭 시점 회전
    * false : 3인칭 시점 회전
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let mode = camera.getMoveMode();
```
{% endtab %}
{% endtabs %}

## setMoveMode\(boolean \_mode\)

> 카메라 회전모드 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_mode | boolean | 설정할 카메라 회전모드값 |

* Parameter 정보
  * true : 1인칭 시점 회전
  * false : 3인칭 시점 회전
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
camera.setMoveMode(false);
```
{% endtab %}
{% endtabs %}

## getDistance\(\)

> 카메라 시점 ~ 위치 거리 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라의 시점 ~ 위치 사이 거리\(m 단위\) 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let distance = camera.getDistance();
```
{% endtab %}
{% endtabs %}

## setDistance\(number \_distance\)

> 카메라 시점 ~ 위치 거리 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_distance | number | 시점 ~ 위치 거리 \(m 단위\) |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let distance = 2000.0;
camera.setDistance(distance);
```
{% endtab %}
{% endtabs %}

## getLimitTilt\(\)

> 카메라 제한된 최소 Tilt값 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라의 제한된 최소 Tilt 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let tilt = camera.getLimitTilt();
```
{% endtab %}
{% endtabs %}

## setLimitTilt\(number \_tilt\)

> 카메라 제한할 최소 Tilt 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_tilt | number | 제한할 최소 Tilt값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let tilt = 30.0;
camera.setLimitTilt(tilt);
```
{% endtab %}
{% endtabs %}

## getLimitAltitude\(\)

> 카메라 제한된 최소 고도값 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라의 제한된 최소 고도 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let alt = camera.getLimitAltitude();
```
{% endtab %}
{% endtabs %}

## setLimitAltitude\(number \_alt\)

> 카메라 제한할 최소 고도값 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_alt | number | 제한할 최소 고도값 |
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let alt = 3000.0;
camera.setLimitAltitude(alt);
```
{% endtab %}
{% endtabs %}

## getAnimationSpeed\(\)

> 마우스에 의한 카메라 이동 속도 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 마우스에 의한 카메라 이동속도 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let speed = camera.getAnimationSpeed();
```
{% endtab %}
{% endtabs %}

## setAnimationSpeed\(number \_speed\)

> 마우스에 의한 카메라 이동 속도 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_speed | number | 이동 속도 |

* Parameter 정보
  * 1.0 ~ 10.0 사이 값으로 설정 가능
  * 값이 클 수록 속도가 빨라집니다.
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let speed = 5.0;
camera.setAnimationSpeed(speed);
```
{% endtab %}
{% endtabs %}

## getCameraSpeed\(\)

> API에 의한 카메라 이동 속도 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * API에 의한 카메라 이동속도 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let speed = camera.getCameraSpeed();
```
{% endtab %}
{% endtabs %}

## setCameraSpeed\(number \_speed\)

> API에 의한 카메라 이동 속도 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_speed | number | 이동 속도 |

* Parameter 정보
  * 1 ~ 10 사이 값으로 설정 가능
  * 값이 클 수록 속도가 빨라집니다.
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let speed = 5.0;
camera.setCameraSpeed(speed);
camera.setLocation(new Module.JSVector3D(129.130626, 35.171523, 1000.0));
```
{% endtab %}
{% endtabs %}

## getCenterPoint\(\)

> 화면 중심의 지도 좌표 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * CJSVector3D Type
    * 화면 중심의 지도 좌표 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let center = camera.getCenterPoint();
console.log(center.Longitude);        // 경도
console.log(center.Latitude);        // 위도
console.log(center.Altitude);        // 고도
```
{% endtab %}
{% endtabs %}

## getMapZoomLevel\(\)

> 카메라 현재 Zoom 레벨 반환

{% tabs %}
{% tab title="Parameter" %}
* 반환 정보
  * number Type
    * 카메라 현재 Zoom 레벨 반환
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
let zoomLevel = camera.getMapZoomLevel();
```
{% endtab %}
{% endtabs %}

## setViewAt\(number \_lon, number \_lat, number \_alt, number \_angle, number \_heading\)

> 카메라 상세 위치 설정

{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| \_lon | number | 카메라 위치 경도 |
| \_lat | number | 카메라 위치 위도 |
| \_alt | number | 카메라 위치 고도 |
| \_angle | number | 카메라 각도 |
| \_heading | number | 카메라 방향 각도 |

* Parameter 정보
  * _heading
    * 0도 : 북쪽
    * 90도 : 동쪽
    * 180도 : 남쪽
    * -180도 : 남쪽
    * -90도 : 서쪽
{% endtab %}

{% tab title="Code" %}
```javascript
let camera = Module.getViewCamera();
camera.setViewAt(129.130626, 35.171523, 500.0, 45, 90);
```
{% endtab %}
{% endtabs %}


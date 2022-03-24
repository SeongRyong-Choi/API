---
description: 지도 내 카메라 설정 API를 제공합니다.
---

# JSCamera

Module getViewCamera API로 생성할 수 있습니다.

```javascript
var camera = Module.getViewCamera();
```

## look\([JSVector3D](JSVector3D.md) from, [JSVector3D](JSVector3D.md) to\) → boolean
> from, to 두 점을 이용해 카메라를 이동합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| from | [JSVector3D](JSVector3D.md) | 카메라 위치 |
| to | [JSVector3D](JSVector3D.md) | 카메라가 바라보는 위치 |
{% endtab %}

{% tab title="Detail" %}
* [JSVector3D](JSVector3D.md) : (경도, 위도, 고도)

* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * Module.getViewCamera().look(new Module.JSVector3D(129.128265, 35.171834, 500.0), new Module.JSVector3D(129.128265, 35.161834, 10.0));
{% endtab %}
{% endtabs %}

## move\([JSVector3D](JSVector3D.md) VecLocation, number tilt, number direct, number speed\)
> 카메라를 원하는 위치로 이동 후 Tilt, direct를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| VecLocation | [JSVector3D](JSVector3D.md) | 카메라 위치 |
| tilt | number | 카메라 tilt |
| direct | number | 카메라 direct |
| ~~speed~~ | ~~number~~ | ~~카메라 speed~~ |
{% endtab %}

{% tab title="Detail" %}
* [JSVector3D](JSVector3D.md) : (경도, 위도, 고도)
* tilt : 카메라 heading 각도
* direct : 카메라가 바라보는 방향 각도
  * 0도 : 북쪽
  * 90도 : 동쪽
  * 180도 : 남쪽
  * -180도 : 남쪽
  * -90도 : 서쪽
* speed : 카메라 이동 속도

* Code
  * Module.getViewCamera().move(new Module.JSVector3D(129.128265, 35.171834, 500.0), 70, 0, 0);
{% endtab %}
{% endtabs %}

## moveLonLatBoundarybyJson\(val parameter\) → string
> min, max boundary를 이용하여 카메라를 이동합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| parameter | val | 카메라 min, max boundary |
{% endtab %}

{% tab title="Detail" %}
```
let json = {
	boundary: {														// 카메라 이동 위치
		min: new Module.JSVector2D(area_min_lon, area_min_lat),		// 좌하단
		max: new Module.JSVector2D(area_max_lon, area_max_lat)		// 우상단
	},																
	complete: complete,												// 이동완료 후 발생하는 CallBack
};
```

* Return
  * 설정 성공 (success) 혹은 실패 (fail)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_set_viewrect
{% endtab %}
{% endtabs %}

## moveLonLatAlt\(number Longitude, number Latitude, number Altitude, boolean smooth\)
> 카메라를 지정한 고도, 경위도 위치로 이동합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| Longitude | number | 카메라 경도 |
| Latitude | number | 카메라 위도 |
| Altitude | number | 카메라 고도 |
| smooth | boolean | 카메라 이동 애니메이션 적용 여부 |
{% endtab %}

{% tab title="Detail" %}
* smooth : 카메라가 바라보는 방향 각도
  * True : 카메라 이동 애니메이션 적용
  * False : 카메라 이동 애니메이션 없이 바로 위치 이동
  
* Code
  * Module.getViewCamera().moveLonLatAlt(127.0273188, 37.4977981, 500.0, true);
{% endtab %}
{% endtabs %}

## moveOval\([JSVector3D](JSVector3D.md) VecLocation, number tilt, number direct, number speed\)
> 카메라를 지정한 고도, 경위도 위치로 이동합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| VecLocation | [JSVector3D](JSVector3D.md) | 카메라 위치 |
| tilt | number | 카메라 tilt |
| direct | number | 카메라 direct |
| speed | number | 카메라 speed |
{% endtab %}

{% tab title="Detail" %}
* [JSVector3D](JSVector3D.md) : (경도, 위도, 고도)
* tilt : 카메라 heading 각도
* direct : 카메라가 바라보는 방향 각도
  * 0도 : 북쪽
  * 90도 : 동쪽
  * 180도 : 남쪽
  * -180도 : 남쪽
  * -90도 : 서쪽
* speed : 카메라 이동 속도

* Code
  * Module.getViewCamera().moveOval(new Module.JSVector3D(129.128265, 35.171834, 500.0), 70, 0, 1);
{% endtab %}
{% endtabs %}

## setLocation\([JSVector3D](JSVector3D.md) VecLocation\) → boolean
> 카메라의 위치를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| VecLocation | [JSVector3D](JSVector3D.md) | 카메라 위치 |
{% endtab %}

{% tab title="Detail" %}
* [JSVector3D](JSVector3D.md) : (경도, 위도, 고도)

* Return
  * 설정 성공 (success) 혹은 실패 (fail)
* Code
  * Module.getViewCamera().setLocation(new Module.JSVector3D(129.128265, 35.171834, 500.0));
{% endtab %}
{% endtabs %}

## setLimitTilt\(number tilt\)
> 카메라의 제한 tilt 각도를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| tilt | number | 제한하고자하는 tilt 각도 |
{% endtab %}

{% tab title="Detail" %}
* tilt : 카메라 heading 각도

* Code
  * Module.getViewCamera().setLimitTilt(80);
{% endtab %}
{% endtabs %}

## setTilt\(number tilt\)
> 카메라의 tilt 각도를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| tilt | number | 카메라 tilt |
{% endtab %}

{% tab title="Detail" %}
* tilt : 카메라 heading 각도

* Code
  * Module.getViewCamera().setTilt(80);
{% endtab %}
{% endtabs %}

## setDirect\(number direct\)
> 카메라의 방향 각도를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| direct | number | 카메라 direct |
{% endtab %}

{% tab title="Detail" %}
* direct : 카메라가 바라보는 방향 각도
  * 0도 : 북쪽
  * 90도 : 동쪽
  * 180도 : 남쪽
  * -180도 : 남쪽
  * -90도 : 서쪽
  
* Code
  * Module.getViewCamera().setDirect(0);
{% endtab %}
{% endtabs %}

## setAltitude\(number alt\)
> 카메라의 고도를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| alt | number | 카메라 고도 |
{% endtab %}

{% tab title="Detail" %}
* alt : 카메라 고도

* Code
  * Module.getViewCamera().setAltitude(1000);
{% endtab %}
{% endtabs %}

## setFov\(number fov\)
> 카메라의 FOV를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| fov | number | 카메라 fov |
{% endtab %}

{% tab title="Detail" %}
* fov : 카메라 화각

* Code
  * Module.getViewCamera().setFov(50);
{% endtab %}
{% endtabs %}

## setMoveMode\(boolean mode\)
> 카메라의 회전 모드를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| mode | boolean | 카메라 시점 |
{% endtab %}

{% tab title="Detail" %}
* mode : 설정하고자 하는 카메라 회전 모드
  * true : 1인칭 시점 회전 모드
  * false : 3인칭 시점 회전 모드
  
* Code
  * Module.getViewCamera().setMoveMode(true);
{% endtab %}
{% endtabs %}

## setLimitAltitude\(number alt\)
> 카메라의 제한 고도 값을 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| alt | number | 제한하고자하는 고도(m 단위) |
{% endtab %}

{% tab title="Detail" %}
* alt : 카메라 고도

* Code
  * Module.getViewCamera().setLimitAltitude(3000);
{% endtab %}
{% endtabs %}

## setAnimationSpeed\(number speed\)
> 마우스에 의한 카메라 이동 속도 설정
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| speed | number | 카메라 이동 속도 |
{% endtab %}

{% tab title="Detail" %}
* speed : 1.0 ~ 10.0 사이 값으로 설정 가능
* 값이 클 수록 속도가 빨라집니다.

* Code
  * Module.getViewCamera().setAnimationSpeed(5);
{% endtab %}
{% endtabs %}

## setAutoMovePosition\([CJSVec3Array](CJSVec3Array.md) positionList\) → boolean
> 카메라의 자동이동을 실행할 좌표 리스트를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| positionList | [CJSVec3Array](CJSVec3Array.md) | 자동이동 경로 좌표 리스트 |
{% endtab %}

{% tab title="Detail" %}
* positionList : ([JSVector3D](JSVector3D.md), [JSVector3D](JSVector3D.md), ...) 자동이동 경로 좌표 리스트

* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_move_path
{% endtab %}
{% endtabs %}

## setAutoMoveWaitFrame\(number speed\) → boolean
> 카메라의 자동이동 위치를 갱신할 프레임 수를 지정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| speed | number | 카메라 위치 갱신 프레임 수 |
{% endtab %}

{% tab title="Detail" %}
* speed : n번의 화면 렌더링 당 한 번씩 카메라가 이동. 값이 클 수록 카메라 이동 속도가 느려진다

* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_move_path
{% endtab %}
{% endtabs %}

## setAutoMoveRoundPositions\([CJSVector3D](CJSVector3D.md) center, number distanceFromCenter, number cameraAltitude, number roundStartAngle, number roundEndAngle, boolean clockWise\) → boolean
> 카메라의 원형 경로 이동을 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| center | [CJSVector3D](CJSVector3D.md) | 카메라가 바라보는 지점 |
| distanceFromCenter | number | 중심점과 카메라의 거리 |
| cameraAltitude | number | 카메라 고도 |
| roundStartAngle | number | 시작 방향 |
| roundEndAngle | number | 종료 방향 |
| clockWise | boolean | 방향 설정 |
{% endtab %}

{% tab title="Detail" %}
* [JSVector3D](JSVector3D.md) : (경도, 위도, 고도)
* distanceFromCenter : 카메라가 바라보는 지점에서 카메라 사이 거리
* cameraAltitude : 카메라 고도
* roundStartAngle : 카메라 이동 시작 방향
  * 0도 : 북쪽
  * 90도 : 동쪽
  * 180도 : 남쪽
  * -180도 : 남쪽
  * -90도 : 서쪽
* roundEndAngle : 카메라 이동 종료 방향
  * 0도 : 북쪽
  * 90도 : 동쪽
  * 180도 : 남쪽
  * -180도 : 남쪽
  * -90도 : 서쪽
* clockWise : 카메라 이동 방향 설정
  * true : 반시계방향
  * false : 시계방향
  
* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_move_round_path
{% endtab %}
{% endtabs %}

## SetCameraShakeEffect\(boolean set\) → boolean
> 카메라 흔들림 효과를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| set | boolean | 카메라 흔들림 효과 설정 |
{% endtab %}

{% tab title="Detail" %}
* set : 카메라 흔들림 효과 설정
  * true : 카메라 흔들림 효과 실행
  * false : 카메라 흔들림 효과 종료
  
* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_quake
{% endtab %}
{% endtabs %}

## SetCameraShakeStrength\(number strength\) → boolean
> 카메라 흔들림 효과 강도를 설정합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| strength | number | 카메라 흔들림 효과 강도 설정 |
{% endtab %}

{% tab title="Detail" %}
* strength : 카메라 흔들림 효과 강도

* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_quake
{% endtab %}
{% endtabs %}

## setPermitUnderGround\(boolean permit\)
> 카메라가 지형 아래로 내려가는 것을 허용합니다.
{% tabs %}
{% tab title="Parameter" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| permit | boolean | 카메라 지형 아래 위치 허용 여부 |
{% endtab %}

{% tab title="Detail" %}
* permit : 카메라 지형 아래 위치 허용 여부
  * true : 카메라가 지형 아래로 내려가도록 허용
  * false : 카메라가 지형 아래로 내려가도록 허용하지 않음
 
* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * Module.getViewCamera().setPermitUnderGround(true);
{% endtab %}
{% endtabs %}

## startAutoMove\(\) → boolean
> 카메라 자동이동을 실행합니다.
{% tabs %}
{% tab title="Information" %}
* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_move_path
{% endtab %}
{% endtabs %}

## stopAutoMove\(\) → boolean
> 카메라 자동이동을 종료합니다.
{% tabs %}
{% tab title="Information" %}
* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_move_path
{% endtab %}
{% endtabs %}

## pauseAutoMove\(\) → boolean
> 카메라 자동이동을 일시정지합니다.
{% tabs %}
{% tab title="Information" %}
* Return
  * 설정 성공 (true) 혹은 실패 (false)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_move_path
{% endtab %}
{% endtabs %}
---
description: 지도 내 카메라 설정 API를 제공합니다.
---

# JSCamera

## look\([JSVector3D](JSVector3D.md) from, [JSVector3D](JSVector3D.md) to\) → boolean
> from, to 두 점을 이용해 카메라를 이동합니다.
{% tabs %}
{% tab title="Information" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| from | [JSVector3D](JSVector3D.md) | 카메라 위치 |
| to | [JSVector3D](JSVector3D.md) | 카메라가 바라보는 위치 |
* Detail
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
{% tab title="Information" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| VecLocation | [JSVector3D](JSVector3D.md) | 카메라 위치 |
| tilt | number | 카메라 Tilt |
| direct | number | 카메라 direct |
| ~~speed~~ | ~~number~~ | ~~카메라 speed~~ |
* Detail
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
{% tab title="Information" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| parameter | val | 카메라 min, max boundary |
* Detail
  let json = {
	boundary: {														// 카메라 이동 위치
		min: new Module.JSVector2D(area_min_lon, area_min_lat),		// 좌하단
		max: new Module.JSVector2D(area_max_lon, area_max_lat)		// 우상단
	},																
	complete: complete,												// 이동완료 후 발생하는 CallBack
  };
* Return
  * 설정 성공 (success) 혹은 실패 (fail)
* Code
  * http://sandbox.dtwincloud.com/code/main.do?id=camera_set_viewrect
{% endtab %}
{% endtabs %}

## moveLonLatAlt\(number Longitude, number Latitude, number Altitude, boolean smooth\)
> 카메라를 지정한 고도, 경위도 위치로 이동합니다.
{% tabs %}
{% tab title="Information" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| Longitude | number | 카메라 경도 |
| Latitude | number | 카메라 위도 |
| Altitude | number | 카메라 고도 |
| smooth | boolean | 카메라 이동 애니메이션 적용 여부 |
* Detail
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
{% tab title="Information" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| Longitude | number | 카메라 경도 |
| Latitude | number | 카메라 위도 |
| Altitude | number | 카메라 고도 |
| smooth | boolean | 카메라 이동 애니메이션 적용 여부 |
* Detail
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
{% tab title="Information" %}
| Parameter | Type | Contents |
| :--- | :--- | :--- |
| VecLocation | [JSVector3D](JSVector3D.md) | 카메라 위치 |
* Detail
  * [JSVector3D](JSVector3D.md) : (경도, 위도, 고도)
* Return
  * 설정 성공 (success) 혹은 실패 (fail)
* Code
  * Module.getViewCamera().setLocation(new Module.JSVector3D(129.128265, 35.171834, 500.0));
{% endtab %}
{% endtabs %}
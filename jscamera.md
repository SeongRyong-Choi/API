---
description: 지도 내 카메라 설정 API를 제공합니다.
---

# JSCamera

## look\([JSVector3D](JSVector3D.md) from, [JSVector3D](JSVector3D.md) to\) → boolean
> from, to 두 점으로 카메라를 이동합니다.
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
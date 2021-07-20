---
description: 지도 내 카메라 설정 API를 제공합니다.
---

# JSCamera

## getTilt\(\)

> 해당 레이어 오브젝트 추

{% tabs %}
{% tab title="Return" %}
| Return | Type | Contents |
| :--- | :--- | :--- |
|  | double | 카메라의 현재 Tilt를 반환합니다. |

* 반환 정
  * 없
{% endtab %}

{% tab title="Code" %}
```javascript
let camera= Module.getViewCamera();
let tilt = camera.getTilt();
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


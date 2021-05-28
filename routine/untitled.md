---
description: '루틴 관리 - 생성, 수정, 삭제'
---

# Management

{% api-method method="post" host="http://mytin.com" path="/routine" %}
{% api-method-summary %}
 Routine Create  
{% endapi-method-summary %}

{% api-method-description %}
 루틴 생성  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
 Authentication 토큰  
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="img" type="string" required=false %}
  사진  
{% endapi-method-parameter %}

{% api-method-parameter name="materials" type="string" required=false %}
  루틴 준비물  
{% endapi-method-parameter %}

{% api-method-parameter name="breakTime" type="number" required=true %}
  쉬는시간  
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
  루틴 유형  
{% endapi-method-parameter %}

{% api-method-parameter name="motions" type="array" required=true %}
  루틴에 포함되는 동작 리스트  
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
  루틴 설명  
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
  루틴 이름  
{% endapi-method-parameter %}

{% api-method-parameter name="difficulty" type="string" required=true %}
  루틴 난이도  
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
 루틴 생성 성공  
{% endapi-method-response-example-description %}

```
{
    "message": "routine create successful",
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
 요청 형식에 문제가 있음 
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
 생성 권한이 존재하지 않음  
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}
  이미 생성되어있는 루틴임  
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



#### motions example

```text
motions: [
    {
        "motion_id": 28,
        "motion_time": 5,
        "numOfMotion": 7, 
    }
    ...
]
```

{% api-method method="put" host="http://mytin.com" path="/routine" %}
{% api-method-summary %}
Routine Update  
{% endapi-method-summary %}

{% api-method-description %}
 루틴 수정   
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
 수정할 루틴의 id 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
 Authentication 토큰  
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="img" type="string" required=false %}
  루틴 이미지  
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
  루틴 이름  
{% endapi-method-parameter %}

{% api-method-parameter name="materials" type="string" required=false %}
  루틴 준비물  
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
  루틴 설명  
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}
  유형  
{% endapi-method-parameter %}

{% api-method-parameter name="difficulty" type="string" required=false %}
  루틴 난이도  
{% endapi-method-parameter %}

{% api-method-parameter name="breakTime" type="string" required=false %}
  쉬는 시간
{% endapi-method-parameter %}

{% api-method-parameter name="motions" type="array" required=false %}
  루틴에 포함되는 동작 리스트  
{% endapi-method-parameter %}

{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 루틴 수정 성공   
{% endapi-method-response-example-description %}

```
{
    "message": "routine update successful",
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
 요청 형식에 문제가 있음  
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
 루틴을 수정할 권한이 없음 
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
  수정할 루틴이 존재하지 않음  
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="delete" host="http://mytin.com" path="/routine" %}
{% api-method-summary %}
 Routine Delete 
{% endapi-method-summary %}

{% api-method-description %}
 루틴 삭제  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
 Authentication 토큰  
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="id " type="string" required=true %}
 삭제할 루틴 id  
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 루틴 삭제 성공  
{% endapi-method-response-example-description %}

```
{
    "message": "motion delete successful"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
 요청 형식에 문제가 있음  
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
 루틴을 삭제할 권한이 없음  
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
 삭제할 루틴이 존재하지 않음 
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


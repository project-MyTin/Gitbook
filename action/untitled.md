---
description: '동작 관리 - 생성, 수정, 삭제'
---

# Management

{% api-method method="post" host="http://mytin.com" path="/motion" %}
{% api-method-summary %}
Create
{% endapi-method-summary %}

{% api-method-description %}
 루틴 생성  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="file" type="object" required=true %}
 이미지, GIF, mp4
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="difficulty" type="string" required=true %}
 동작 난이도  
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
 동작 이름  
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
 동작 설명  
{% endapi-method-parameter %}

{% api-method-parameter name="time" type="string" required=true %}
 동작 시간  
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="array" required=true %}
 동작 유형  
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=false %}
 동작 URL
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10000",
    "message": "motion registration successful",
    "data": {}
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "Already exists",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}





{% api-method method="put" host="http://mytin.com" path="/motion/:id" %}
{% api-method-summary %}
Update
{% endapi-method-summary %}

{% api-method-description %}
 루틴 수정  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
 수정할 id  
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="file" type="object" required=true %}
 이미지, GIF, mp4
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
 동작 이름  
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
 동작 설명  
{% endapi-method-parameter %}

{% api-method-parameter name="time" type="string" required=true %}
 동작 시간  
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="array" required=true %}
 동작 유형  
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=false %}
 동작 URL  
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10000",
    "message": "motion update successful",
    "data": {}
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "",
    "data": {}
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "motion not found",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}







{% api-method method="delete" host="http://mytin.com" path="/motion" %}
{% api-method-summary %}
Delete
{% endapi-method-summary %}

{% api-method-description %}
루틴 삭제  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
 동작 아이  
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10000",
    "message": "motion delete successful",
    "data": {}
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "bad request",
    "data": {}
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "motion not found",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}






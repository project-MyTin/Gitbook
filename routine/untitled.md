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

{% api-method-body-parameters %}
{% api-method-parameter name="type" type="array" required=true %}
 루틴 유형  
{% endapi-method-parameter %}

{% api-method-parameter name="difficulty" type="string" required=true %}
 루틴 난이도  
{% endapi-method-parameter %}

{% api-method-parameter name="totalTime" type="string" required=true %}
 총 시간   
{% endapi-method-parameter %}

{% api-method-parameter name="motion" type="array" required=true %}
 루틴에 포함되는 동작 리스트   
{% endapi-method-parameter %}

{% api-method-parameter name="materials" type="string" required=false %}
 루틴 준비물 
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
 루틴 설명  
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
 루틴 이름
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
    "statusCode": StatusCode,
    "message": "routine create successful",
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
    "statusCode": StatusCode,
    "message": "ppap",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="put" host="http://mytin.com" path="/routine" %}
{% api-method-summary %}
Routine Update  
{% endapi-method-summary %}

{% api-method-description %}
 루틴 수정   
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
 Authentication 토큰  
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="type" type="array" required=true %}
 루틴 유형  
{% endapi-method-parameter %}

{% api-method-parameter name="difficulty" type="string" required=true %}
 루틴 난이도  
{% endapi-method-parameter %}

{% api-method-parameter name="totalTime" type="string" required=true %}
 총 시간   
{% endapi-method-parameter %}

{% api-method-parameter name="motion" type="array" required=true %}
 루틴에 포함되는 동작 리스트   
{% endapi-method-parameter %}

{% api-method-parameter name="materials" type="string" required=false %}
 루틴 준비물  
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
 루틴 설명   
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
 루틴 이름 
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
    "statusCode": StatusCode,
    "message": "routine update successful",
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
    "statusCode": StatusCode,
    "message": "ppap",
    "data": {}
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

{% endapi-method-response-example-description %}

```
{
    "statusCode": StatusCode,
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
    "statusCode": StatusCode,
    "message": "ppap",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


---
description: '루틴 조회 with 필터, 정렬'
---

# Search

{% api-method method="get" host="http://mytin.com" path="/routine" %}
{% api-method-summary %}
Routine Detail  
{% endapi-method-summary %}

{% api-method-description %}
  루틴 상세 정보 보기    
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
 루틴 id  
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
  루틴 상세 정보 보기 성공  
{% endapi-method-response-example-description %}

```
{
    "message": "routine read successful",
    "data": {
        name:'',
        description:'',
        time:'',
        type:'',
        url:''
    }
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

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
 조회할 루틴을 찾을 수 없음  
{% endapi-method-response-example-description %}

```
{
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="get" host="http://mytin.com" path="/routine/list" %}
{% api-method-summary %}
Routine Search
{% endapi-method-summary %}

{% api-method-description %}
  루틴 검색 \(필터 + 정렬 기능\)  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="filter" type="string" required=false %}
 필터 값  
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="string" required=false %}
 정렬 값 
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 루틴 검색 성공  
{% endapi-method-response-example-description %}

```
{
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


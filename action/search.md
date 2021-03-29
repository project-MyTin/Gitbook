---
description: 동작 검색
---

# Search

{% api-method method="get" host="http://mytin.com" path="/motion" %}
{% api-method-summary %}
Search
{% endapi-method-summary %}

{% api-method-description %}
 동작 검색  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="filter" type="string" %}
  필터
{% endapi-method-parameter %}

{% api-method-parameter name="sort" type="boolean" %}
 정렬값  
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10000",
    "message": "search sucess",
    "data": {
        id:'',
        name:'',
        Difficulty:'',
        parts:[
            '','',''
        ],
        image:''
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "An invalid format",
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
    "message": "not found motions",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% api-method method="get" host="http://mytin.com" path="/motion/detail/:id" %}
{% api-method-summary %}
detail
{% endapi-method-summary %}

{% api-method-description %}
 루틴 검색  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
 자세히 볼 동작 아이디 
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "statusCode": "10000",
    "message": "load motion detail sucess",
    "data": {
        image: '동작 이미지',
        name: '동작 이름',
        type: '동작 유형',
        Difficulty: '동작 난이도',
        time: '동작 시간',
        description: '동작 설명',
        writer: '동작 작성자',
        url: '동작 참고자료 URL'
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "message": "An invalid format",
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
    "message": "not found motions",
    "data": {}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




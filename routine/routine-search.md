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
    "_id": "루틴 아이디",
    "name": "루틴 이름",
    "description": "루틴 설명",
    "publisher": "작성자",
    "materials": "준비물",
    "motions": [ "동작 아이디 1", "동작 아이디 2"],
    "time": "총 소요 시간",
    "authority": "루틴 권한",
    "difficulty": "루틴 난이도",
    "type": "루틴 유형",
    "createdTime": "생성 시간",
    "updatedTime": "수정 시간",
    "image": "루틴 이미지"
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
{% api-method-parameter name="q" type="string" required=false %}
  검색 값  
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
    "_id": "루틴 아이디",
    "name": "루틴 이름",
    "description": "루틴 설명",
    // "time": "총 소요 시간",
    // "authority": "루틴 권한",
    "difficulty": "루틴 난이도",
    "type": "루틴 유형",
    "image": "루틴 이미지"
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




---
description: 일 상세
---

# Day detail

{% api-method method="get" host="http://mytin.com" path="/calendar/detail" %}
{% api-method-summary %}
Day detail
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="y" type="string" required=false %}
  연도  
{% endapi-method-parameter %}

{% api-method-parameter name="m" type="string" required=false %}
  달  
{% endapi-method-parameter %}

{% api-method-parameter name="d" type="string" required=false %}
  일  
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10000",
    "message": "Success",
    "data": {
        "routine_total_time": 300,
        "exp": 57,
        "routine_num": 3,
        "motion_num": 3,
        "motion_list": [
            {
                "_id": "60b4eed15073205508132278",
                "motion_id": 51,
                "motion_name": "열정!",
                "motion_file": "upload/1622293292823_image_picker4043935270632905498.jpg",
                "motion_time": 10
            },
            ...
        ],
        "routine_list": [
            {
                "_id": "60b4eed15073205508132277",
                "routine_id": 31,
                "routine_name": "안",
                "routine_file": "upload/1622470344477_image_picker3264685267009013454.jpg",
                "routine_time": 20
            },
            
        ]
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
공사중
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "statusCode": "10001",
    "error": "It doesn't exist"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


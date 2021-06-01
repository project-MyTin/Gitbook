---
description: 캘린더 일 단위
---

# Day

{% api-method method="get" host="http://mytin.com" path="/calendar" %}
{% api-method-summary %}
Calendar day
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="y" type="string" required=true %}
  연도  
{% endapi-method-parameter %}

{% api-method-parameter name="m" type="string" required=true %}
    달  
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
        "result": {
            "total_list": [
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                0,
                100
            ],
            "max": 100
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}




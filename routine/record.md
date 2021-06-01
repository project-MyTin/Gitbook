---
description: 루틴 기록
---

# Record

{% api-method method="post" host="http://mytin.com" path="/routine/record" %}
{% api-method-summary %}
Routine record
{% endapi-method-summary %}

{% api-method-description %}
  루틴 성공 시 완료요청    
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
  routine 아이디  
{% endapi-method-parameter %}

{% api-method-parameter name="total\_time" type="number" required=true %}
  routine 총 시간  
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


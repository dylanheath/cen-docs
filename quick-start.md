# 🛻 Quick Start

{% hint style="info" %}
**Downtime:** please be aware of unexpected downtime due to updates/upgrades in our services over the course of development
{% endhint %}

## Setup

The best way to interact with our Api's endpoints

{% tabs %}
{% tab title="Node" %}
```
# Endpoint
mainnet.cen.network/.netlify/functions/api/
```
{% endtab %}

{% tab title="Python" %}
```
# Endpoint
mainnet.cen.network/.netlify/functions/api/
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Important:**  Client usage is restricted to Authorised Entities as all requests must abide by the CORS policy
{% endhint %}

## Make your first request

Make your first request, try getting recent transactions

{% swagger baseUrl="mainnet.cen.network/.netlify/functions/api" method="get" path="/transactions/getall" summary="Get recent transactions" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200" description="transactions received" %}
```javascript
{
    "amount"=0,
    "senderdata": {
        "name": "",
        "address": "",
        "cid": "",
        "email": "",
    }
    "receiverdata": {
        "name": "",
        "address": "",
        "cid": "",
        "email": "",
    }
    "receiver": "",
    "sender": "",
    "date": "",
    "link": "",
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description=":(" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
**Important:** Expect slower response time in early development, Nodes may not stay hot (cached)
{% endhint %}

Take a look on how to send a request in your environment&#x20;

{% tabs %}
{% tab title="curl" %}
```
curl https://mainnet.cen.network/.netlify/functions/api/  
```
{% endtab %}

{% tab title="Node" %}
```javascript
# You do not need to use axios 
axios.get('https://mainnet.cen.network/.netlify/functions/api/')
```
{% endtab %}
{% endtabs %}

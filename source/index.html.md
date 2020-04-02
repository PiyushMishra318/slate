---
title: API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>


search: true
---

# Introduction

Welcome to the Greasy Monkey  API! You can use our API to access Greasy Monkey API endpoints, which can help you to build and integrate frontend and backend efficiently.

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

#CUSTOMER
##General
##Signup

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/user/create"
payload = "{\"email\":{\"address\":\"emailid@email.com\"},\n\"username\":\"user1\",\n\"password\":\"password\",\n\"mobile\":\"1234567890\",\n\"user_type\":\"customer\"\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "80ce7eee-2b64-89da-08b4-565124529e8c"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)
```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/user/create")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '2cc44f82-125c-d094-d2a5-9099e88eff6f'
request.body = "{\"email\":{\"address\":\"emailid@email.com\"},\n\"username\":\"user1\",\n\"password\":\"password\",\n\"mobile\":\"1234567890\",\n\"user_type\":\"customer\"\n}"
response = http.request(request)
puts response.read_body
```
```javascript
var data = JSON.stringify({
  "email": {
    "address": "emailid@email.com"
  },
  "username": "user1",
  "password": "password",
  "mobile": "1234567890",
  "user_type": "customer"
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/user/create");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "4ff2a68d-d0dc-742b-f7e2-f85a64e0c141");
xhr.send(data);
```
```shell
curl --request POST \
  --url http://52.77.255.121:3004/admin/user/create \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 8719af9e-af6d-68f7-2b2f-83a3b23ebf41' \
  --data '{"email":{"address":"emailid@email.com"},\n"username":"user1",\n"password":"password",\n"mobile":"1234567890",\n"user_type":"customer"\n}'

```
>Below is a sample response

```json
{
    "auth": true,
    "user": {
        "email": {
            "verficationStatus": {
                "isVerified": false
            },
            "address": " emailid@provider.com "
        },
        "username": "user_name",
        "mobile": 1234567890,
        "user_type": "customer",
        "personal_details": {
            "_id": "5e84a786bfd0c32be46fa2b1",
            "mobile_nos": [],
            "emails": []
        },
        "_id": "5e84a78618ad3431e0f0fe98",
        "createdAt": "2020-04-01T14:39:02.196Z",
        "updatedAt": "2020-04-01T14:39:02.196Z",
        "__v": 0,
        "bank_accounts": []
    }
}

```
This API is used to signup users to our portal.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/user/create`</p>



##Login

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3001/auth/login/coot/start"
payload = "{\"type\":\"email\",\n\"email\":\"emailid@email.com\",\n\"password\":\"password\"\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "6e51f45f-48f5-12f2-fe02-80553f827d17"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3001/auth/login/coot/start")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '6a3f4c68-c19e-5edd-b8bd-220879b93129'
```
```javascript
var data = JSON.stringify({
  "type": "email",
  "email": "emailid@email.com",
  "password": "password"
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3001/auth/login/coot/start");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "4a3f2924-3750-c443-bc6c-86f925a9230a");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3001/auth/login/coot/start \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 69defc5f-2335-1129-b04d-fbd5a69eee9a' \
  -d '{"type":"email",
"email":"emailid@email.com",
"password":"password"
}'


```
>Below is a sample response

>"cookie set"

This API is used to allow users to login to our portal.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3001/auth/login/coot/start</p>

##Login Verify

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/user/verify"
payload = "{\"user_type\":\"customer\"}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "e4a0d895-1906-d302-6464-ef3b084291fd"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)


```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/user/verify")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '3c3844fe-8358-b22e-157b-6417e5fb1488'
request.body = "{\"user_type\":\"customer\"}"
response = http.request(request)
puts response.read_body

```
```javascript
var data = JSON.stringify({
  "user_type": "customer"
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/user/verify");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "cc887de5-2f8f-880b-6b07-b902792dd7e9");
xhr.send(data);


```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/user/verify \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 2172a537-c26f-5e8b-0ece-68afc3b711c0' \
  -d '{"user_type":"customer"}'



```
>Below is a sample response

```json
{
    "auth": true,
    "user": {
        "user_type": "customer",
        "email": {
            "verficationStatus": {
                "isVerified": false
            },
            "address": "emailid@email.com"
        },
        "personal_details": {
            "_id": "5e84aee8c0277b3163e409fb",
            "mobile_nos": [],
            "emails": [
                {
                    "verficationStatus": {
                        "isVerified": false
                    },
                    "_id": "5e84aee31fc621316c541ac2",
                    "address": "emailid@email.com"
                }
            ]
        },
        "_id": "5e84aee31fc621316c541ac1",
        "username": "emailid@email.com",
        "createdAt": "2020-04-01T15:10:27.404Z",
        "updatedAt": "2020-04-01T15:10:27.404Z",
        "__v": 0,
        "bank_accounts": []
    }
}

```

This API is used to verify the loggedin user.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/user/verify</p>


##Car
for all apis related to car
##Document
for all apis related to documents
##Service request
for all apis related to services
#ADMIN

##Camp
for all apis related to camps
##Brand
for all apis related to brands
##Product&Service
for all apis related to products and services
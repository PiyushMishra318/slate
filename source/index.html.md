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
This section explains about all the apis used in the user login of Greasy Monkey.
##General
This section contains documentation for all the general apis used to build the Greasy Monkey platform.
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
<p>`POST : http://52.77.255.121:3001/auth/login/coot/start`</p>

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
<p>`POST : http://52.77.255.121:3004/admin/user/verify`</p>

##Logout

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3001/auth/logout"
headers = {
    'cache-control': "no-cache",
    'postman-token': "9727c1ab-d038-d2e9-aed8-75f9c2a72a5e"
    }
response = requests.request("GET", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3001/auth/logout")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Get.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = '6f402703-bbd6-d373-8a49-0801960eefed'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("GET", "http://52.77.255.121:3001/auth/logout");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "f02b6550-cfc3-0e3c-231d-666baba407eb");
xhr.send(data);


```
```shell
curl -X GET \
  http://52.77.255.121:3001/auth/logout \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 50f36d08-c0ee-6e4e-7889-e2b0fc84620b'


```
>Below is a sample response

>Logout

This API is used to logout user.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3001/auth/logout`</p>


##Car
This section contains documentation for all the apis that handle Car data on the Greasy Monkey platform.
##Document
This section contains documentation for all the apis that handle documents uploaded on the Greasy Monkey platform.
##Service request
This section contains documentation for all the apis that handle service requests on the Greasy Monkey platform.
#ADMIN
This section explains about all the apis used in the admin login of Greasy Monkey.
##Camp
This section contains documentation for all the apis that handle camp data on the Greasy Monkey platform.
##Add Camp

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/camp/create"
payload = "{\r\n    \"location\": \"#3,13th main road,shivaji nagar,delhi 20\",\r\n    \"status\": \"OPEN\",\r\n    \"date\":\"2020-04-02\",\r\n\t\"start_time\":\"2020-04-02\",\r\n\t\"end_time\":\"2020-04-02\"\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "3398c148-556f-a2da-70d6-02673c91f767"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/camp/create")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '6a0ff31a-cefa-599f-e684-813559cd67ba'
request.body = "{\r\n    \"location\": \"#3,13th main road,shivaji nagar,delhi 20\",\r\n    \"status\": \"OPEN\",\r\n    \"date\":\"2020-04-02\",\r\n\t\"start_time\":\"2020-04-02\",\r\n\t\"end_time\":\"2020-04-02\"\r\n}"
response = http.request(request)
puts response.read_body

```
```javascript
var data = JSON.stringify({
  "location": "#3,13th main road,shivaji nagar,delhi 20",
  "status": "OPEN",
  "date": "2020-04-02",
  "start_time": "2020-04-02",
  "end_time": "2020-04-02"
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/camp/create");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "22265417-a8f5-2b3a-da73-1460fb1192d3");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/camp/create \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 906ccc67-9076-84e0-82d9-a95fd8d2da46' \
  -d '{
    "location": "#3,13th main road,shivaji nagar,delhi 20",
    "status": "OPEN",
    "date":"2020-04-02",
	"start_time":"2020-04-02",
	"end_time":"2020-04-02"
}'

```
>Below is a sample response

```json
{
    "total_revenue": 0,
    "existing_customer_interactions": 0,
    "new_customer_added": 0,
    "_id": "5e85b50fdaf2b743d096632c",
    "location": "#3,13th main road,shivaji nagar,delhi 20",
    "status": "OPEN",
    "date": "2020-04-02T00:00:00.000Z",
    "start_time": "2020-04-02T00:00:00.000Z",
    "end_time": "2020-04-02T00:00:00.000Z",
    "registered_customers": [],
    "createdAt": "2020-04-02T09:49:03.275Z",
    "updatedAt": "2020-04-02T09:49:03.275Z",
    "__v": 0
}

```

This API is used to add a camp.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/camp/create`</p>
<aside class="notice">
Camps are temporary locations where companies set up their equipment for service and people can register themselves for attending these camps.
</aside>

##Brand
This section contains documentation for all the apis that handle brand data on the Greasy Monkey platform.
##Add Brand

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/brand/create/"
payload = "{\r\n    \"brand_name\": \"Maruti Suzuki\",\r\n    \"models\": [\r\n        {\r\n            \"name\": \"Swift\",\r\n            \"variants\": [\r\n                \"lxi\",\r\n                \"ldi\",\r\n                \"vxi\"\r\n            ],\r\n            \"years\": [\r\n                2018,\r\n                2019,\r\n                2020\r\n            ]\r\n        }\r\n    ]\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "8d0c84e3-7278-d6b6-e9be-70ffb2044246"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/brand/create/")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '014eaebc-d6d0-19b4-0a16-277c4eedff51'
request.body = "{\r\n    \"brand_name\": \"Maruti Suzuki\",\r\n    \"models\": [\r\n        {\r\n            \"name\": \"Swift\",\r\n            \"variants\": [\r\n                \"lxi\",\r\n                \"ldi\",\r\n                \"vxi\"\r\n            ],\r\n            \"years\": [\r\n                2018,\r\n                2019,\r\n                2020\r\n            ]\r\n        }\r\n    ]\r\n}"
response = http.request(request)
puts response.read_body


```
```javascript
var data = JSON.stringify({
  "brand_name": "Maruti Suzuki",
  "models": [
    {
      "name": "Swift",
      "variants": [
        "lxi",
        "ldi",
        "vxi"
      ],
      "years": [
        2018,
        2019,
        2020
      ]
    }
  ]
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/brand/create/");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "9ab8982d-a5b0-b5fc-35c6-6b60c40cc790");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/brand/create/ \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: e9289e75-2674-3b82-5f0e-52a976de974d' \
  -d '{
    "brand_name": "Maruti Suzuki",
    "models": [
        {
            "name": "Swift",
            "variants": [
                "lxi",
                "ldi",
                "vxi"
            ],
            "years": [
                2018,
                2019,
                2020
            ]
        }
    ]
}'

```
>Below is a sample response

```json
{
    "_id": "5e858b46c0277b3163e40a00",
    "brand_name": "Maruti Suzuki",
    "models": [
        {
            "variants": [
                "lxi",
                "ldi",
                "vxi"
            ],
            "years": [
                "2018",
                "2019",
                "2020"
            ],
            "_id": "5e858b46c0277b3163e40a01",
            "name": "Swift"
        }
    ],
    "createdAt": "2020-04-02T06:50:46.547Z",
    "updatedAt": "2020-04-02T06:50:46.547Z",
    "__v": 0
}
```

This API is used to add a brand.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/brand/create/`</p>

##View all Brands

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/brand/all/read"
headers = {
    'cache-control': "no-cache",
    'postman-token': "41c0358d-b867-a096-4fab-46cfa27bf95c"
    }
response = requests.request("POST", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/brand/all/read")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = 'b9279938-8cc5-e9dc-6786-7693b09d4c28'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/brand/all/read");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "133dc108-5ea1-d417-e61a-05de0443c3de");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/brand/all/read \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 0bc9e09f-e8a3-d06d-93fb-65c77c9c1f07'

```
>Below is a sample response

```json
[
    {
        "_id": "5e858b46c0277b3163e40a00",
        "brand_name": "Maruti Suzuki",
        "models": [
            {
                "variants": [
                    "lxi",
                    "ldi",
                    "vxi"
                ],
                "years": [
                    "2018",
                    "2019",
                    "2020"
                ],
                "_id": "5e858b46c0277b3163e40a01",
                "name": "Swift"
            }
        ],
        "createdAt": "2020-04-02T06:50:46.547Z",
        "updatedAt": "2020-04-02T06:50:46.547Z",
        "__v": 0
    }
]

```

This API is used to view all brands.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/brand/all/read/`</p>


##View individual Brand information

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/brand/read/5e858b46c0277b3163e40a00"
headers = {
    'cache-control': "no-cache",
    'postman-token': "10d30b31-ec06-ea76-f890-11c37d27a981"
    }
response = requests.request("GET", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/brand/read/5e858b46c0277b3163e40a00")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Get.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = '0dcb7c54-a6c9-8fd7-9975-04bd71908382'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("GET", "http://52.77.255.121:3004/admin/brand/read/5e858b46c0277b3163e40a00");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "4beede58-bab1-c77a-2f58-81530da67c28");
xhr.send(data);

```
```shell
curl -X GET \
  http://52.77.255.121:3004/admin/brand/read/5e858b46c0277b3163e40a00 \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 2fffa260-5a47-8899-dea6-ef140f5f0e4b'

```
>Below is a sample response

```json
{
    "_id": "5e858b46c0277b3163e40a00",
    "brand_name": "Maruti Suzuki",
    "models": [
        {
            "variants": [
                "lxi",
                "ldi",
                "vxi"
            ],
            "years": [
                "2018",
                "2019",
                "2020"
            ],
            "_id": "5e858b46c0277b3163e40a01",
            "name": "Swift"
        }
    ],
    "createdAt": "2020-04-02T06:50:46.547Z",
    "updatedAt": "2020-04-02T06:50:46.547Z",
    "__v": 0
}


```

This API is used to view information about a single brand.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3004/admin/brand/read/<BrandID>`</p>

##Update Brand data

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/update/brand/5e858b46c0277b3163e40a00"
payload = "{\r\n    \"brand_name\": \"Maruti Suzuki\",\r\n    \"models\": [\r\n        {\r\n            \"name\": \"Swift\",\r\n            \"variants\": [\r\n                \"lxi\",\r\n                \"ldi\",\r\n                \"vxi\",\r\n                \"vdi\"\r\n            ],\r\n            \"years\": [\r\n            \t2017,\r\n                2018,\r\n                2019,\r\n                2020\r\n            ]\r\n        }\r\n    ]\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "9587b413-bbdd-e0eb-1b44-fc26330032d0"
    }
response = requests.request("PUT", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/update/brand/5e858b46c0277b3163e40a00")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Put.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = 'ce54023c-dee2-ddfc-6a81-49f399114173'
request.body = "{\r\n    \"brand_name\": \"Maruti Suzuki\",\r\n    \"models\": [\r\n        {\r\n            \"name\": \"Swift\",\r\n            \"variants\": [\r\n                \"lxi\",\r\n                \"ldi\",\r\n                \"vxi\",\r\n                \"vdi\"\r\n            ],\r\n            \"years\": [\r\n            \t2017,\r\n                2018,\r\n                2019,\r\n                2020\r\n            ]\r\n        }\r\n    ]\r\n}"
response = http.request(request)
puts response.read_body


```
```javascript
var data = JSON.stringify({
  "brand_name": "Maruti Suzuki",
  "models": [
    {
      "name": "Swift",
      "variants": [
        "lxi",
        "ldi",
        "vxi",
        "vdi"
      ],
      "years": [
        2017,
        2018,
        2019,
        2020
      ]
    }
  ]
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("PUT", "http://52.77.255.121:3004/admin/update/brand/5e858b46c0277b3163e40a00");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "b82844a9-396c-876b-3132-2521e747da0f");
xhr.send(data);


```
```shell
curl -X PUT \
  http://52.77.255.121:3004/admin/update/brand/5e858b46c0277b3163e40a00 \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: a84abb4b-146c-61d9-26ba-0bfde775751e' \
  -d '{
    "brand_name": "Maruti Suzuki",
    "models": [
        {
            "name": "Swift",
            "variants": [
                "lxi",
                "ldi",
                "vxi",
                "vdi"
            ],
            "years": [
            	2017,
                2018,
                2019,
                2020
            ]
        }
    ]
}'

```
>Below is a sample response

```json
{
    "_id": "5e858b46c0277b3163e40a00",
    "brand_name": "Maruti Suzuki",
    "models": [
        {
            "variants": [
                "lxi",
                "ldi",
                "vxi",
                "vdi"
            ],
            "years": [
                "2017",
                "2018",
                "2019",
                "2020"
            ],
            "_id": "5e8591e7c0277b3163e40a02",
            "name": "Swift"
        }
    ],
    "createdAt": "2020-04-02T06:50:46.547Z",
    "updatedAt": "2020-04-02T07:19:03.152Z",
    "__v": 0
}


```

This API is used to update a particular brands information.
<br>
<h3>Http request</h5>
<p>`PUT :  http://52.77.255.121:3004/admin/update/brand/<BrandID>`</p>
<aside class="notice">
You must replace \<BrandID> with the ID of the brand you want to update.
</aside>

##Delete Brand data

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/brand/delete/5e858b46c0277b3163e40a00"
headers = {
    'cache-control': "no-cache",
    'postman-token': "64653f05-0a78-16cf-d63a-6c162181952a"
    }
response = requests.request("DELETE", url, headers=headers)
print(response.text)


```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/brand/delete/5e858b46c0277b3163e40a00")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Delete.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = '506104a2-4780-8b1b-aac4-b150cf68be38'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("DELETE", "http://52.77.255.121:3004/admin/brand/delete/5e858b46c0277b3163e40a00");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "16e044ec-5405-707b-5215-fd004bacd0f5");
xhr.send(data);

```
```shell
curl -X DELETE \
  http://52.77.255.121:3004/admin/brand/delete/5e858b46c0277b3163e40a00 \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 2683f5de-6cda-1f2c-fc01-2340cd98044d'

```
>Below is a sample response

```json
{
    "_id": "5e858b46c0277b3163e40a00",
    "brand_name": "Maruti Suzuki",
    "models": [
        {
            "variants": [
                "lxi",
                "ldi",
                "vxi",
                "vdi"
            ],
            "years": [
                "2017",
                "2018",
                "2019",
                "2020"
            ],
            "_id": "5e8591e7c0277b3163e40a02",
            "name": "Swift"
        }
    ],
    "createdAt": "2020-04-02T06:50:46.547Z",
    "updatedAt": "2020-04-02T07:19:03.152Z",
    "__v": 0
}


```

This API is used to remove a particular brand.
<br>
<h3>Http request</h5>
<p>`PUT :  http://52.77.255.121:3004/admin/brand/delete/<BrandID>`</p>
<aside class="notice">
You must replace \<BrandID> with the ID of the brand you want to remove.
</aside>


##Product&Service
This section contains documentation for all the apis that handle Product/Service information on the Greasy Monkey platform.
##Add Product

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/service/create/"
payload = "{ \"typeOf\":\"PRODUCT\",\r\n\"image\": \"engineoil.png\",\r\n\"name\": \"Engine Oil\",\r\n\"description\": \"This is engine oil\",\r\n\"cost\": 100,\r\n\"stock\": 5,\r\n\"qty_unit\": \"Bottles\",\r\n\"inclusions\": [],\r\n\"add_on\": [],\r\n\"keywords\": [\"Oil\",\"Engine\",\"Smooth\"]\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "e6fb7bf0-6c78-b3c3-13a9-1de0a27e930a"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/service/create/")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = 'dc383eb2-136a-d29b-c7a0-b7b3cd214b6a'
request.body = "{ \"typeOf\":\"PRODUCT\",\r\n\"image\": \"engineoil.png\",\r\n\"name\": \"Engine Oil\",\r\n\"description\": \"This is engine oil\",\r\n\"cost\": 100,\r\n\"stock\": 5,\r\n\"qty_unit\": \"Bottles\",\r\n\"inclusions\": [],\r\n\"add_on\": [],\r\n\"keywords\": [\"Oil\",\"Engine\",\"Smooth\"]\r\n}"
response = http.request(request)
puts response.read_body

```
```javascript
var data = JSON.stringify({
  "typeOf": "PRODUCT",
  "image": "engineoil.png",
  "name": "Engine Oil",
  "description": "This is engine oil",
  "cost": 100,
  "stock": 5,
  "qty_unit": "Bottles",
  "inclusions": [],
  "add_on": [],
  "keywords": [
    "Oil",
    "Engine",
    "Smooth"
  ]
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/service/create/");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "b6a424ce-e7ac-2dd2-bdac-af039199c97a");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/service/create/ \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 6ac61c32-0dfa-1b41-b379-9d626567db9a' \
  -d '{ "typeOf":"PRODUCT",
"image": "engineoil.png",
"name": "Engine Oil",
"description": "This is engine oil",
"cost": 100,
"stock": 5,
"qty_unit": "Bottles",
"inclusions": [],
"add_on": [],
"keywords": ["Oil","Engine","Smooth"]
}'

```
>Below is a sample response

```json
{
    "stock": 5,
    "inclusions": [],
    "add_on": [],
    "direct_booking": false,
    "recommended_service": false,
    "keywords": [
        "Oil",
        "Engine",
        "Smooth"
    ],
    "_id": "5e8584bac0277b3163e409fe",
    "typeOf": "PRODUCT",
    "image": "engineoil.png",
    "name": "Engine Oil",
    "description": "This is engine oil",
    "cost": 100,
    "qty_unit": "Bottles",
    "createdAt": "2020-04-02T06:22:50.520Z",
    "updatedAt": "2020-04-02T06:22:50.520Z",
    "__v": 0
}

```

This API is used to add a product.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/service/create/`</p>


##Add Service

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/service/create/"
payload = "{ \"typeOf\":\"SERVICE\",\r\n\"image\": \"Quicck_service.png\",\r\n\"name\": \"Quick Service\",\r\n\"description\": \"Service your car in one day with excellant quality asurance\",\r\n\"cost\": 2000,\r\n\"inclusions\": [\"5e8584bac0277b3163e409fe\"],\r\n\"add_on\": [\"5e8584bac0277b3163e409fe\"],\r\n\"keywords\": [\"quick\",\"service\",\"fast\",\"one-day\"]\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "b3e1d4b7-0a75-6fbb-4596-3132d801f27d"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)


```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/service/create/")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '04c5c896-65fa-b3fc-b21c-f80fd1938f99'
request.body = "{ \"typeOf\":\"SERVICE\",\r\n\"image\": \"Quicck_service.png\",\r\n\"name\": \"Quick Service\",\r\n\"description\": \"Service your car in one day with excellant quality asurance\",\r\n\"cost\": 2000,\r\n\"inclusions\": [\"5e8584bac0277b3163e409fe\"],\r\n\"add_on\": [\"5e8584bac0277b3163e409fe\"],\r\n\"keywords\": [\"quick\",\"service\",\"fast\",\"one-day\"]\r\n}"
response = http.request(request)
puts response.read_body


```
```javascript
var data = JSON.stringify({
  "typeOf": "SERVICE",
  "image": "Quicck_service.png",
  "name": "Quick Service",
  "description": "Service your car in one day with excellant quality asurance",
  "cost": 2000,
  "inclusions": [
    "5e8584bac0277b3163e409fe"
  ],
  "add_on": [
    "5e8584bac0277b3163e409fe"
  ],
  "keywords": [
    "quick",
    "service",
    "fast",
    "one-day"
  ]
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/service/create/");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "b8083035-cc78-0fee-db69-ea0b59aa0eba");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/service/create/ \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: beedb573-3f71-e7c2-de03-2980d378d354' \
  -d '{ "typeOf":"SERVICE",
"image": "Quicck_service.png",
"name": "Quick Service",
"description": "Service your car in one day with excellant quality asurance",
"cost": 2000,
"inclusions": ["5e8584bac0277b3163e409fe"],
"add_on": ["5e8584bac0277b3163e409fe"],
"keywords": ["quick","service","fast","one-day"]
}'

```
>Below is a sample response

```json
{
    "stock": 0,
    "inclusions": [
        "5e8584bac0277b3163e409fe"
    ],
    "add_on": [
        "5e8584bac0277b3163e409fe"
    ],
    "direct_booking": false,
    "recommended_service": false,
    "keywords": [
        "quick",
        "service",
        "fast",
        "one-day"
    ],
    "_id": "5e8586c6c0277b3163e409ff",
    "typeOf": "SERVICE",
    "image": "Quicck_service.png",
    "name": "Quick Service",
    "description": "Service your car in one day with excellant quality asurance",
    "cost": 2000,
    "createdAt": "2020-04-02T06:31:34.360Z",
    "updatedAt": "2020-04-02T06:31:34.360Z",
    "__v": 0
}

```

This API is used to add a service.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/service/create/`</p>


##View all services and products

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/service/all/read/"
headers = {
    'cache-control': "no-cache",
    'postman-token': "48364019-a48b-5911-b234-b049fcce5d41"
    }
response = requests.request("POST", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/service/all/read/")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = '374c9182-bc1c-cefc-5a54-fc66bd8accdf'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3004/admin/service/all/read/");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "db3d0019-347e-d311-c209-94e62c894f87");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/service/all/read/ \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 1c30168b-b0c3-58ef-5bcb-c4b2d645825f'
```
>Below is a sample response

```json
[
    {
        "stock": 5,
        "inclusions": [],
        "add_on": [],
        "direct_booking": false,
        "recommended_service": false,
        "keywords": [
            "Oil",
            "Engine",
            "Smooth"
        ],
        "_id": "5e8584bac0277b3163e409fe",
        "typeOf": "PRODUCT",
        "image": "engineoil.png",
        "name": "Engine Oil",
        "description": "This is engine oil",
        "cost": 100,
        "qty_unit": "Bottles",
        "createdAt": "2020-04-02T06:22:50.520Z",
        "updatedAt": "2020-04-02T06:22:50.520Z",
        "__v": 0
    },
    {
        "stock": 0,
        "inclusions": [
            "5e8584bac0277b3163e409fe"
        ],
        "add_on": [
            "5e8584bac0277b3163e409fe"
        ],
        "direct_booking": false,
        "recommended_service": false,
        "keywords": [
            "quick",
            "service",
            "fast",
            "one-day"
        ],
        "_id": "5e8586c6c0277b3163e409ff",
        "typeOf": "SERVICE",
        "image": "Quicck_service.png",
        "name": "Quick Service",
        "description": "Service your car in one day with excellant quality asurance",
        "cost": 2000,
        "createdAt": "2020-04-02T06:31:34.360Z",
        "updatedAt": "2020-04-02T06:31:34.360Z",
        "__v": 0
    }
]

```

This API is used to viewl all services and products.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/service/all/read/`</p>

##View a single service/product

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/service/read/5e8586c6c0277b3163e409ff"
headers = {
    'cache-control': "no-cache",
    'postman-token': "53f5dcce-f89f-c206-5a23-3963f50b279c"
    }
response = requests.request("GET", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/service/read/5e8586c6c0277b3163e409ff")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Get.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = 'ae5486eb-4ab5-3ad1-4fb2-91f6299ff8bf'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("GET", "http://52.77.255.121:3004/admin/service/read/5e8586c6c0277b3163e409ff");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "9cee61d1-fb5c-530d-18a5-ac285fc3bbb6");
xhr.send(data);

```
```shell
curl -X GET \
  http://52.77.255.121:3004/admin/service/read/5e8586c6c0277b3163e409ff \
  -H 'cache-control: no-cache' \
  -H 'postman-token: a1d219b4-6b17-e02e-6095-acd1f213d9e7'
```
>Below is a sample response

```json
{
    "stock": 0,
    "inclusions": [
        "5e8584bac0277b3163e409fe"
    ],
    "add_on": [
        "5e8584bac0277b3163e409fe"
    ],
    "direct_booking": false,
    "recommended_service": false,
    "keywords": [
        "quick",
        "service",
        "fast",
        "one-day"
    ],
    "_id": "5e8586c6c0277b3163e409ff",
    "typeOf": "SERVICE",
    "image": "Quicck_service.png",
    "name": "Quick Service",
    "description": "Service your car in one day with excellant quality asurance",
    "cost": 2000,
    "createdAt": "2020-04-02T06:31:34.360Z",
    "updatedAt": "2020-04-02T06:31:34.360Z",
    "__v": 0
} 

```

This API is used to view a single service/product.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3004/admin/service/read/<ServiceID>`</p>
<aside class="notice">
Dont forget to replace \<ServiceId> with the service id of the product/service.
</aside>


##Remove a single service/product

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/service/delete/5e8584bac0277b3163e409fe"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "28740626-c5ef-53d2-3be9-4defd43b4668"
    }
response = requests.request("DELETE", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/service/delete/5e8584bac0277b3163e409fe")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Delete.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = 'f32ea5fa-0fc4-2a9a-7f37-963d76da6096'
response = http.request(request)
puts response.read_body

```
```javascript
var data = null;
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("DELETE", "http://52.77.255.121:3004/admin/service/delete/5e8584bac0277b3163e409fe");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "3d243704-6048-9094-8dea-953572175151");
xhr.send(data);

```
```shell
curl -X DELETE \
  http://52.77.255.121:3004/admin/service/delete/5e8584bac0277b3163e409fe \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 5d4cdcc6-1aee-1d72-a52f-9035ab7d9e58'

```
>Below is a sample response

```json
{
    "stock": 5,
    "inclusions": [],
    "add_on": [],
    "direct_booking": false,
    "recommended_service": false,
    "keywords": [
        "Oil",
        "Engine",
        "Smooth"
    ],
    "_id": "5e8584bac0277b3163e409fe",
    "typeOf": "PRODUCT",
    "image": "engineoil.png",
    "name": "Engine Oil",
    "description": "This is engine oil",
    "cost": 100,
    "qty_unit": "Bottles",
    "createdAt": "2020-04-02T06:22:50.520Z",
    "updatedAt": "2020-04-02T06:22:50.520Z",
    "__v": 0
}

```

This API is used to delete a single product/service.
<br>
<h3>Http request</h5>
<p>`DELETE : http://52.77.255.121:3004/admin/service/delete/<ServiceID/ProductID>`</p>
<aside class="notice">
Dont forget to replace \<ServiceId> with the service id of the product/service.
</aside>
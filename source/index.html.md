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
#Authorization
##Signup

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/user/create"
payload = "{\"email\":{\"address\":\"emailid@provider.com\"},\n\"username\":\"user1\",\n\"password\":\"password\",\n\"mobile\":\"1234567890\",\n\"user_type\":\"customer\"\n}"
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
request.body = "{\"email\":{\"address\":\"emailid@provider.com\"},\n\"username\":\"user1\",\n\"password\":\"password\",\n\"mobile\":\"1234567890\",\n\"user_type\":\"customer\"\n}"
response = http.request(request)
puts response.read_body
```
```javascript
var data = JSON.stringify({
  "email": {
    "address": "emailid@provider.com"
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
  --data '{"email":{"address":"emailid@provider.com"},\n"username":"user1",\n"password":"password",\n"mobile":"1234567890",\n"user_type":"customer"\n}'

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
A signup is the first and foremost thing needed for any modern day application,this section will guide you through using the signup API to seamlessly integrate your frontend and backend.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/user/create`</p>
<h3>Request headers</h3>
<table>
<tr><th>Key</th><th>Value</th>
<tr><td>Content-Type</td><td>application/json</td></tr>
<tr><td>Access-Control-Allow-Credentials</td><td>true</td></tr>
</table>
<h3>Data parameters</h3>
<table>
<tr><th>Parameter</th><th>Description</th><th>Type</th></tr>
<tr><td>email</td><td>This parameter is to forward the email address of the user being signed up</td><td>required</td></tr>
<tr><td>username</td><td>This parameter is to forward the username of the user being signed up</td><td>required</td></tr>
<tr><td>password</td><td>This parameter is to forward the password of the user being signed up</td><td>required</td></tr>
<tr><td>mobile</td><td>This parameter is to forward the mobile no. of the user being signed up</td><td>required</td></tr>
<tr><td>user_type</td><td>This parameter is to forward the type of the user being signed up it can take values like
<ul>
<li>Ground staff</li>
<li>Customer</li>
<li>Admin</li>
</td><td>required</td></tr>
</table>
<h3>Response Types</h3>
<table>
<tr><th>Status Code</th><th>Description</th></tr>
<tr><td>200</td><td>Everything went well</td></tr>
<tr><td>404</td><td>We might be on a service break,please try later</td></tr>
<tr><td>400</td><td>Please refer the code samples to make a proper request</td></tr>
<tr><td>500</td><td>Internal server error!!</td></td>
</table>
##Login

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3001/auth/login/coot/start"
payload = "{\"type\":\"email\",\n\"email\":\"emailid@provider.com\",\n\"password\":\"password\"\n}"
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
  "email": "emailid@provider.com",
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
"email":"emailid@provider.com",
"password":"password"
}'


```
>Below is a sample response

>"cookie set"

After signing up a user the next step would be to prompt the user to login and get started with your application.This API helps you to login the user to use the services provided.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3001/auth/login/coot/start`</p>

<h3>Request headers</h3>
<table>
<tr><th>Key</th><th>Value</th>
<tr><td>Content-Type</td><td>application/json</td></tr>
<tr><td>Access-Control-Allow-Credentials</td><td>true</td></tr>
</table>
<h3>Data parameters</h3>
<table>
<tr><th>Parameter</th><th>Description</th><th>Type</th></tr>
<tr><td>Type</td><td>This parameter is to forward the type of authentication the user being logged is trying to use ,it can take values like
<ul>
<li>email</li>
<li>username</li>
<li>mobile</li></ul>
</td><td>required</td></tr>
<tr><td>email/mobile/username</td><td>This parameter is to forward the authentication types value of the user being logged in</td><td>required</td></tr>
<tr><td>password</td><td>This parameter is to forward the password of the user being logged in</td><td>required</td></tr>
</table>
<h3>Response Types</h3>
<table>
<tr><th>Status Code</th><th>Description</th></tr>
<tr><td>200</td><td>Everything went well</td></tr>
<tr><td>404</td><td>We might be on a service break,please try later</td></tr>
<tr><td>400</td><td>Please refer the code samples to make a proper request</td></tr>
<tr><td>500</td><td>Internal Server Error</td></tr>
</table>
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
            "address": "emailid@provider.com"
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
                    "address": "emailid@provider.com"
                }
            ]
        },
        "_id": "5e84aee31fc621316c541ac1",
        "username": "emailid@provider.com",
        "createdAt": "2020-04-01T15:10:27.404Z",
        "updatedAt": "2020-04-01T15:10:27.404Z",
        "__v": 0,
        "bank_accounts": []
    }
}

```

Once logged in the next step would be to verify your users authenticity,this section helps you to achieve the same objective.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3004/admin/user/verify`</p>
<aside class="success">
Note:It is important to verify users immediately after login to continue using any other api's.
</aside>
<h3>Request headers</h3>
<table>
<tr><th>Key</th><th>Value</th>
<tr><td>Content-Type</td><td>application/json</td></tr>
<tr><td>Access-Control-Allow-Credentials</td><td>true</td></tr>
</table>
<h3>Data parameters</h3>
<table>
<tr><th>Parameter</th><th>Description</th><th>Type</th></tr>
<tr><td>user_type</td><td>This parameter is to forward the type of the user being verified it can take values like
<ul>
<li>Ground staff</li>
<li>Customer</li>
<li>Admin</li></ul>
</td><td>required</td></tr>
</table>
<h3>Response Types</h3>
<table>
<tr><th>Status Code</th><th>Description</th></tr>
<tr><td>200</td><td>Everything went well</td></tr>
<tr><td>404</td><td>We might be on a service break,please try later</td></tr>
<tr><td>400</td><td>Please refer the code samples to make a proper request</td></tr>
<tr><td>500</td><td>Internal Server Error</td></tr>
</table>
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

You don't want your user to ever stop using your platform but if they want to access your services from a public system you need to allow them to logout.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3001/auth/logout`</p>

<h3>Request headers</h3>
<table>
<tr><th>Key</th><th>Value</th>
<tr><td>Content-Type</td><td>application/json</td></tr>
<tr><td>Access-Control-Allow-Credentials</td><td>true</td></tr>
</table>
<h3>Response Types</h3>
<table>
<tr><th>Status Code</th><th>Description</th></tr>
<tr><td>200</td><td>Everything went well</td></tr>
<tr><td>404</td><td>We might be on a service break,please try later</td></tr>
<tr><td>400</td><td>Please refer the code samples to make a proper request</td></tr>
<tr><td>500</td><td>Internal Server Error</td></tr>
</table>

#CUSTOMER
This section explains about all the apis used in the user login of Greasy Monkey.
##Car
This section contains documentation for all the apis that handle Car data on the Greasy Monkey platform.
##Add Car

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3003/customer/car/create/"
payload = "{\r\n    \"brand\": \"Maruti Suzuki\",\r\n    \"model_name\": \"Swift\",\r\n    \"model_variant\": \"ldi\",\r\n    \"model_year\": \"2019\"\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "342007ec-ae0c-827f-6168-a2bac918ed6d"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3003/customer/car/create/")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = 'f8cbace9-c0fc-49cc-f2ae-1f8b07f3f5fc'
request.body = "{\r\n    \"brand\": \"Maruti Suzuki\",\r\n    \"model_name\": \"Swift\",\r\n    \"model_variant\": \"ldi\",\r\n    \"model_year\": \"2019\"\r\n}"
response = http.request(request)
puts response.read_body

```
```javascript
var data = JSON.stringify({
  "brand": "Maruti Suzuki",
  "model_name": "Swift",
  "model_variant": "ldi",
  "model_year": "2019"
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3003/customer/car/create/");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "61c56d19-ecc0-dba7-c8d9-38d5e4a7e423");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3003/customer/car/create/ \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: a7cca1a2-8f6c-0dec-798a-04502181eec3' \
  -d '{
    "brand": "Maruti Suzuki",
    "model_name": "Swift",
    "model_variant": "ldi",
    "model_year": "2019"
}'

```
>Below is a sample response

```json
{
    "overview": {
        "engine_oil": true,
        "tier": true,
        "suspension": true,
        "brakes": true,
        "electrical_checkup": true,
        "air_conditioner": true
    },
    "_id": "5e859a3e377c0c3168f1b4b0",
    "brand": "Maruti Suzuki",
    "model_name": "Swift",
    "model_variant": "ldi",
    "model_year": "2019",
    "createdAt": "2020-04-02T07:54:38.331Z",
    "updatedAt": "2020-04-02T07:54:38.331Z",
    "__v": 0
}


```

This API is used to add a car.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3003/customer/car/create/`</p>

##View all Cars

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3003/customer/car/all/get"
headers = {
    'cache-control': "no-cache",
    'postman-token': "cb1d8808-7e40-9b2e-fcdd-db0991d3dae0"
    }
response = requests.request("POST", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3003/customer/car/all/get")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = 'ace9beb3-891b-23a2-ea51-824cfe1fb86f'
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
xhr.open("POST", "http://52.77.255.121:3003/customer/car/all/get");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "c3ecfa6e-d2e5-657b-eeaa-49572d8ad0ff");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3003/customer/car/all/get \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 93d24eb5-fffc-873a-ec7c-39b287528db0'

```
>Below is a sample response

```json
[
    {
        "overview": {
            "engine_oil": true,
            "tier": true,
            "suspension": true,
            "brakes": true,
            "electrical_checkup": true,
            "air_conditioner": true
        },
        "_id": "5e859a3e377c0c3168f1b4b0",
        "brand": "Maruti Suzuki",
        "model_name": "Swift",
        "model_variant": "ldi",
        "model_year": "2019",
        "createdAt": "2020-04-02T07:54:38.331Z",
        "updatedAt": "2020-04-02T07:54:38.331Z",
        "__v": 0
    },
    {
        "overview": {
            "engine_oil": true,
            "tier": true,
            "suspension": true,
            "brakes": true,
            "electrical_checkup": true,
            "air_conditioner": true
        },
        "_id": "5e859a3e377c0c3168f1b4b1",
        "brand": "Maruti Suzuki",
        "model_name": "Swift Dzire",
        "model_variant": "ldi",
        "model_year": "2019",
        "createdAt": "2020-04-02T07:54:38.331Z",
        "updatedAt": "2020-04-02T07:54:38.331Z",
        "__v": 0
    }
]

```

This API is used to view all cars of a customer.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3003/customer/car/all/get`</p>

##View specific Car

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3003/customer/car/read/5e859a3e377c0c3168f1b4b0"
headers = {
    'cache-control': "no-cache",
    'postman-token': "29239a7b-99e4-2a73-f8a8-5faf6f0e1002"
    }
response = requests.request("GET", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3003/customer/car/read/5e859a3e377c0c3168f1b4b0")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Get.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = '8bb225d0-0e32-f1a3-14c7-7b4a45247162'
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
xhr.open("GET", "http://52.77.255.121:3003/customer/car/read/5e859a3e377c0c3168f1b4b0");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "4db331c1-d540-c8c3-d681-e4a5540e9e79");
xhr.send(data);

```
```shell
curl -X GET \
  http://52.77.255.121:3003/customer/car/read/5e859a3e377c0c3168f1b4b0 \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 32728b8f-c0b1-7f9e-7b88-e37c1f6ba914'

```
>Below is a sample response

```json
{
    "overview": {
        "engine_oil": true,
        "tier": true,
        "suspension": true,
        "brakes": true,
        "electrical_checkup": true,
        "air_conditioner": true
    },
    "_id": "5e859a3e377c0c3168f1b4b0",
    "brand": "Maruti Suzuki",
    "model_name": "Swift",
    "model_variant": "ldi",
    "model_year": "2019",
    "createdAt": "2020-04-02T07:54:38.331Z",
    "updatedAt": "2020-04-02T07:54:38.331Z",
    "__v": 0
}

```

This API is used to view a specific car.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3003/customer/car/read/<CarId>`</p>
<aside class="notice">
Dont forget to replace \<CarId> with the id of the car you would like to view.
</aside>

##Document
This section contains documentation for all the apis that handle documents uploaded on the Greasy Monkey platform.
##Service request
This section contains documentation for all the apis that handle service requests made by users on the Greasy Monkey platform.

##Make service request

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3003/customer/service_request/create"
payload = "{\r\n  \"car\": \"5e859a3e377c0c3168f1b4b0\",\r\n  \"service\": \"5e8586c6c0277b3163e409ff\",\r\n  \"date\": \"2020-02-29T10:14:11.830Z\",\r\n  \"location\": \"testAddress\"\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "274f0e01-4bdc-00e4-04b5-566cfc7dade2"
    }
response = requests.request("POST", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3003/customer/service_request/create")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '322db753-89c2-8a03-fea1-6f0758c7f2ed'
request.body = "{\r\n  \"car\": \"5e859a3e377c0c3168f1b4b0\",\r\n  \"service\": \"5e8586c6c0277b3163e409ff\",\r\n  \"date\": \"2020-02-29T10:14:11.830Z\",\r\n  \"location\": \"testAddress\"\r\n}"
response = http.request(request)
puts response.read_body

```
```javascript
var data = JSON.stringify({
  "car": "5e859a3e377c0c3168f1b4b0",
  "service": "5e8586c6c0277b3163e409ff",
  "date": "2020-02-29T10:14:11.830Z",
  "location": "testAddress"
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("POST", "http://52.77.255.121:3003/customer/service_request/create");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "5f1e44e7-81c7-30d5-65c5-2f07f8db10be");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3003/customer/service_request/create \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 87661af2-2512-bd1f-a7b2-de5e84381071' \
  -d '{
  "car": "5e859a3e377c0c3168f1b4b0",
  "service": "5e8586c6c0277b3163e409ff",
  "date": "2020-02-29T10:14:11.830Z",
  "location": "testAddress"
}'

```
>Below is a sample response

```json
{
    "payment": {
        "done": false
    },
    "status": "BOOKED",
    "_id": "5e85ac3fb981e543d6fa5729",
    "car": {
        "overview": {
            "engine_oil": true,
            "tier": true,
            "suspension": true,
            "brakes": true,
            "electrical_checkup": true,
            "air_conditioner": true
        },
        "_id": "5e859a3e377c0c3168f1b4b0",
        "brand": "Maruti Suzuki",
        "model_name": "Swift",
        "model_variant": "ldi",
        "model_year": "2019",
        "createdAt": "2020-04-02T07:54:38.331Z",
        "updatedAt": "2020-04-02T07:54:38.331Z",
        "__v": 0
    },
    "service": {
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
    },
    "date": "2020-02-29T10:14:11.830Z",
    "location": "testAddress",
    "add_ons": [],
    "createdAt": "2020-04-02T09:11:27.967Z",
    "updatedAt": "2020-04-02T09:11:27.967Z",
    "__v": 0
}

```

This API is used to make a new request for a service.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3003/customer/service_request/create`</p>

##View all service requests

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3003/customer/service_request/all/get"
headers = {
    'cache-control': "no-cache",
    'postman-token': "30dc523c-a10e-5360-7f4b-39ffafca0b7f"
    }
response = requests.request("POST", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3003/customer/service_request/all/get")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = 'd88f27c7-6460-d9a8-4d9c-2527f31aff7f'
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
xhr.open("POST", "http://52.77.255.121:3003/customer/service_request/all/get");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "046fa740-447d-1869-9f21-a528cca252b1");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3003/customer/service_request/all/get \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 0aeb4200-0579-435e-c376-5bb13f325f6c'

```
>Below is a sample response

```json
[
    {
        "payment": {
            "done": false
        },
        "status": "BOOKED",
        "_id": "5e85ac3fb981e543d6fa5729",
        "car": {
            "overview": {
                "engine_oil": true,
                "tier": true,
                "suspension": true,
                "brakes": true,
                "electrical_checkup": true,
                "air_conditioner": true
            },
            "_id": "5e859a3e377c0c3168f1b4b0",
            "brand": "Maruti Suzuki",
            "model_name": "Swift",
            "model_variant": "ldi",
            "model_year": "2019",
            "createdAt": "2020-04-02T07:54:38.331Z",
            "updatedAt": "2020-04-02T07:54:38.331Z",
            "__v": 0
        },
        "service": {
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
        },
        "date": "2020-02-29T10:14:11.830Z",
        "location": "testAddress",
        "add_ons": [],
        "createdAt": "2020-04-02T09:11:27.967Z",
        "updatedAt": "2020-04-02T09:11:27.967Z",
        "__v": 0
    }
]

```

This API is used to view all service requests made by a user.
<br>
<h3>Http request</h5>
<p>`POST : http://52.77.255.121:3003/customer/service_request/all/get`</p>

##View specific service request

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3003/customer/service_request/read/5e85ac3fb981e543d6fa5729"
headers = {
    'cache-control': "no-cache",
    'postman-token': "549de7d7-b38c-05c6-8d1a-7e0656e2d6fb"
    }
response = requests.request("GET", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3003/customer/service_request/read/5e85ac3fb981e543d6fa5729")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Get.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = 'd9b35814-7e36-7228-90c7-043460c7aef2'
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
xhr.open("GET", "http://52.77.255.121:3003/customer/service_request/read/5e85ac3fb981e543d6fa5729");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "48aaa899-c932-9f7c-a047-55da3d003557");
xhr.send(data);

```
```shell
curl -X GET \
  http://52.77.255.121:3003/customer/service_request/read/5e85ac3fb981e543d6fa5729 \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 13151321-8835-3b24-7b32-c15e50d3ac9f'

```
>Below is a sample response

```json
{
    "payment": {
        "done": false
    },
    "status": "BOOKED",
    "_id": "5e85ac3fb981e543d6fa5729",
    "car": {
        "overview": {
            "engine_oil": true,
            "tier": true,
            "suspension": true,
            "brakes": true,
            "electrical_checkup": true,
            "air_conditioner": true
        },
        "_id": "5e859a3e377c0c3168f1b4b0",
        "brand": "Maruti Suzuki",
        "model_name": "Swift",
        "model_variant": "ldi",
        "model_year": "2019",
        "createdAt": "2020-04-02T07:54:38.331Z",
        "updatedAt": "2020-04-02T07:54:38.331Z",
        "__v": 0
    },
    "service": {
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
    },
    "date": "2020-02-29T10:14:11.830Z",
    "location": "testAddress",
    "add_ons": [],
    "createdAt": "2020-04-02T09:11:27.967Z",
    "updatedAt": "2020-04-02T09:11:27.967Z",
    "__v": 0
}

```

This API is used to view a specific service request made by a user.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3003/customer/service_request/read/<RequestID>`</p>
<aside class="notice">
Dont forget to replace \<RequestID> with the id of the service request you want to view.
</aside>


#ADMIN
This section explains about all the apis used in the admin login of Greasy Monkey.
##Camp
This section contains documentation for all the apis that handle camp data on the Greasy Monkey platform.
<aside class="notice">
Camps are temporary locations where companies set up their equipment for service and people can register themselves for attending these camps.
</aside>
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

##View all Camps

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/camp/all/read"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "90ddccf7-d9cc-e89f-4a31-2f2c35a57c68"
    }
response = requests.request("POST", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/camp/all/read")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Post.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '2fae8b81-a29b-abd8-5e7e-0867f5e0f6fe'
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
xhr.open("POST", "http://52.77.255.121:3004/admin/camp/all/read");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "b0130254-d396-5e43-3f53-9de7d83775ad");
xhr.send(data);

```
```shell
curl -X POST \
  http://52.77.255.121:3004/admin/camp/all/read \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: c7854106-2f59-e61f-3431-ec107c4dd089'

```
>Below is a sample response

```json
[
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
]

```

This API is used to view all camps.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3004/admin/camp/all/read`</p>


##View specific Camp

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/camp/read/5e85b50fdaf2b743d096632c"
headers = {
    'cache-control': "no-cache",
    'postman-token': "9470eb05-13dc-03ec-c884-dc92e0e5040c"
    }
response = requests.request("GET", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/camp/read/5e85b50fdaf2b743d096632c")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Get.new(url)
request["cache-control"] = 'no-cache'
request["postman-token"] = '37ccacf6-ba4e-29c0-868e-b697a01333da'
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
xhr.open("GET", "http://52.77.255.121:3004/admin/camp/read/5e85b50fdaf2b743d096632c");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "fe0383c6-f1a8-8b2b-d81d-96151505bba0");
xhr.send(data);

```
```shell
curl -X GET \
  http://52.77.255.121:3004/admin/camp/read/5e85b50fdaf2b743d096632c \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 0a220b8b-4a41-cb4c-a2c8-cf87684cdf52'

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

This API is used to view a specific camp.
<br>
<h3>Http request</h5>
<p>`GET : http://52.77.255.121:3004/admin/camp/read/<CampId>`</p>
<aside class="notice">
Dont forget to replace \<CampId> with the id of the specific camp you want to view.
</aside>

##Update Camp data

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/update/camp/5e85b50fdaf2b743d096632c"
payload = "{\r\n    \"update\":{\"location\": \"address-latest\",\r\n\"status\": \"Close\",\r\n\"date\": \"2020-04-01T14:39:02.196Z\",\r\n\"start_time\": \"2020-04-01T14:39:02.196Z\",\r\n\"End_time\":\"2020-04-01T14:39:02.196Z\"\r\n}\r\n}"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "7c85c83e-dd9b-50a3-f547-c4a5a1daf917"
    }
response = requests.request("PUT", url, data=payload, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/update/camp/5e85b50fdaf2b743d096632c")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Put.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = 'f64c1265-d399-dbe4-2746-002e5f36a55d'
request.body = "{\r\n    \"update\":{\"location\": \"address-latest\",\r\n\"status\": \"Close\",\r\n\"date\": \"2020-04-01T14:39:02.196Z\",\r\n\"start_time\": \"2020-04-01T14:39:02.196Z\",\r\n\"End_time\":\"2020-04-01T14:39:02.196Z\"\r\n}\r\n}"
response = http.request(request)
puts response.read_body


```
```javascript
var data = JSON.stringify({
  "update": {
    "location": "address-latest",
    "status": "Close",
    "date": "2020-04-01T14:39:02.196Z",
    "start_time": "2020-04-01T14:39:02.196Z",
    "End_time": "2020-04-01T14:39:02.196Z"
  }
});
var xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === 4) {
    console.log(this.responseText);
  }
});
xhr.open("PUT", "http://52.77.255.121:3004/admin/update/camp/5e85b50fdaf2b743d096632c");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "12602c8e-f0b6-fc86-b78f-6b786b5e558c");
xhr.send(data);


```
```shell
curl -X PUT \
  http://52.77.255.121:3004/admin/update/camp/5e85b50fdaf2b743d096632c \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 0e596dc7-2ed0-17a1-d830-f7309d2827e6' \
  -d '{
    "update":{"location": "address-latest",
"status": "Close",
"date": "2020-04-01T14:39:02.196Z",
"start_time": "2020-04-01T14:39:02.196Z",
"End_time":"2020-04-01T14:39:02.196Z"
}
}'

```
>Below is a sample response

```json
{
    "total_revenue": 0,
    "existing_customer_interactions": 0,
    "new_customer_added": 0,
    "_id": "5e85b50fdaf2b743d096632c",
    "location": "address-latest",
    "status": "Close",
    "date": "2020-04-01T14:39:02.196Z",
    "start_time": "2020-04-01T14:39:02.196Z",
    "end_time": "2020-04-02T00:00:00.000Z",
    "registered_customers": [],
    "createdAt": "2020-04-02T09:49:03.275Z",
    "updatedAt": "2020-04-03T10:27:09.449Z",
    "__v": 0
}

```

This API is used to update a particular camps information.
<br>
<h3>Http request</h5>
<p>`PUT :  http://52.77.255.121:3004/admin/update/camp/<CampID>`</p>
<aside class="notice">
You must replace \<CampID> with the ID of the camp you want to update.
</aside>


##Remove Camp

>The below code sample shows you how to use this api

```python
import requests
url = "http://52.77.255.121:3004/admin/camp/delete/5e85b50fdaf2b743d096632c"
headers = {
    'content-type': "application/json",
    'cache-control': "no-cache",
    'postman-token': "3a35f01e-579e-0f5b-f168-4a452b32dcd6"
    }
response = requests.request("DELETE", url, headers=headers)
print(response.text)

```
```ruby
require 'uri'
require 'net/http'
url = URI("http://52.77.255.121:3004/admin/camp/delete/5e85b50fdaf2b743d096632c")
http = Net::HTTP.new(url.host, url.port)
request = Net::HTTP::Delete.new(url)
request["content-type"] = 'application/json'
request["cache-control"] = 'no-cache'
request["postman-token"] = '853abc8d-4fc5-5881-b21f-f2ff6b4ccc40'
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
xhr.open("DELETE", "http://52.77.255.121:3004/admin/camp/delete/5e85b50fdaf2b743d096632c");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("cache-control", "no-cache");
xhr.setRequestHeader("postman-token", "34503d4b-c41c-1251-9421-b17105d7af08");
xhr.send(data);

```
```shell
curl -X DELETE \
  http://52.77.255.121:3004/admin/camp/delete/5e85b50fdaf2b743d096632c \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 91187456-012f-845a-7a01-11097c6284d1'

```
>Below is a sample response

```json
{
    "total_revenue": 0,
    "existing_customer_interactions": 0,
    "new_customer_added": 0,
    "_id": "5e85b50fdaf2b743d096632c",
    "location": "address-latest",
    "status": "Close",
    "date": "2020-04-01T14:39:02.196Z",
    "start_time": "2020-04-01T14:39:02.196Z",
    "end_time": "2020-04-02T00:00:00.000Z",
    "registered_customers": [],
    "createdAt": "2020-04-02T09:49:03.275Z",
    "updatedAt": "2020-04-03T10:27:09.449Z",
    "__v": 0
}

```

This API is used to remove a particular camp.
<br>
<h3>Http request</h5>
<p>`DELETE :  http://52.77.255.121:3004/admin/camp/delete/<CampID>`</p>
<aside class="notice">
You must replace \<CampID> with the ID of the camp you want to update.
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
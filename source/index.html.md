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
###Signup

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
This API is used to signup users to our portal.
ENDPOINT&METHOD
`POST http://52.77.255.121:3004/admin/user/create`
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
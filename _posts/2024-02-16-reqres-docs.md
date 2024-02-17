---
layout: post
title:  "Reqres API"
---

## Resource Endpoint
If you execute this command in your terminal:

[comment]: # (test start {"id": "Test 1", "description": "Test if the endpoint is working at all."})

```sh
curl -X 'GET' \
  'https://reqres.in/api/{resource}' \
  -H 'accept: application/json'
```

[comment]: # (step {"action": "httpRequest", "url": "https://reqres.in/api/{resource}"})

The API will return a list of resources.

[comment]: # (test end)

## Creating Users
If you execute this command in your terminal:

[comment]: # (test start {"id": "Test 2", "description": "Test the user creation endpoint"})

```sh
curl --request POST \
  --url https://reqres.in/api/users \
  --header 'Content-Type: application/json' \
  --header 'accept: application/json' \
  --data '{
"name": "Doc Brown",
"job": "Test master"
}'
```

[comment]: # (step { "action": "httpRequest", "url": "https://reqres.in/api/users", "method": "post", "requestData": { "name": "Doc Brown", "job": "Test master" }, "responseData": { "name": "Doc Brown" }, "statusCodes": [200, 201] })

The API will return confirmation that the request created a new user and will list the fields on that user.

[comment]: # (test end)
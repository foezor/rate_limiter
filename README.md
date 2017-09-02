--- 

title: Rate limiting plugin 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

This is a tools to help applicationsmanage their quotas  without any further implementation 

**Version:** 1.0.0 

[Find out more about Swagger](http://swagger.io) 

# Authentication 

|oauth2|*OAuth 2.0*|
|---|---| 

|apiKey|*API Key*|
|---|---| 

# /RATE
## ***POST*** 

**Summary:** Add a new hit

**Description:** Add a new hit to your application counter, if maximum rate are not already reached. Otherwise an exception is raise.

### HTTP Request 
`***POST*** /rate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| Hit | body | new hit to increase the application | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 401 | Unauthorized grant for this application. |
| 404 | Application not found. |
| 405 | Invalid input. |
| 429 | Too many calls performs, Rate limit exceeded. |

# /RATE/{KEY}
## ***GET*** 

**Summary:** find a specific rate according to a status

**Description:** Multiple keys values can be provided with comma separated strings

### HTTP Request 
`***GET*** /rate/{key}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| key | path | key to be considered for filter | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid key value |
| 401 | Unauthorized grant for this application. |
| 404 | Application not found. |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->

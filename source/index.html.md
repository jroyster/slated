---
title: IPM.ai Alerts API v0.6.2
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="ipm-ai-alerts-api">IPM.ai Alerts API v0.6.2</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

IPM.ai Alerts API

Base URLs:

* <a href="https://api.alerts.ipm.w2odev.com/v1">https://api.alerts.ipm.w2odev.com/v1</a>

* <a href="https://api.alerts.ipm.w2otest.com/v1">https://api.alerts.ipm.w2otest.com/v1</a>

* <a href="https://api.alerts.ipm.w2ostag.com/v1">https://api.alerts.ipm.w2ostag.com/v1</a>

* <a href="https://api.alerts.ipm.w2oanalytics.com/v1">https://api.alerts.ipm.w2oanalytics.com/v1</a>

Email: <a href="mailto:aboothe@w2ogroup.com">Support</a> 

# Authentication

* API Key (api_key)
    - Parameter Name: **session**, in: cookie. 

<h1 id="ipm-ai-alerts-api-user">user</h1>

## getCurrentUser

<a id="opIdgetCurrentUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/users/me \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/users/me HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/users/me',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/users/me',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/users/me', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/users/me', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/users/me");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/users/me", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/me`

*Get the current user*

> Example responses

> 200 Response

```json
{
  "id": "string",
  "email": "string",
  "name": "string",
  "role": "HomeOffice"
}
```

<h3 id="getcurrentuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[User](#schemauser)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## getUser

<a id="opIdgetUser"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/users/{userId} \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/users/{userId} HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/users/{userId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/users/{userId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/users/{userId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/users/{userId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/users/{userId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/users/{userId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/{userId}`

*Get user by ID*

<h3 id="getuser-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userId|path|string(UserId)|true|none|

> Example responses

> 200 Response

```json
{
  "id": "string",
  "email": "string",
  "name": "string",
  "role": "HomeOffice"
}
```

<h3 id="getuser-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[User](#schemauser)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-administration">administration</h1>

## uploadZipTerrFile

<a id="opIduploadZipTerrFile"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile \
  -H 'Content-Type: application/csv' \
  -H 'Accept: application/json'

```

```http
POST https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Content-Type: application/csv
Accept: application/json

```

```javascript
const inputBody = 'string';
const headers = {
  'Content-Type':'application/csv',
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/csv',
  'Accept' => 'application/json'
}

result = RestClient.post 'https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/csv',
  'Accept': 'application/json'
}

r = requests.post('https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/csv',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/csv"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.alerts.ipm.w2odev.com/v1/administration/zipTerrFile", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /administration/zipTerrFile`

*Replace the current zip-to-territory mapping file*

> Body parameter

<h3 id="uploadzipterrfile-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|string(bytes)|true|none|

> Example responses

> 400 Response

```json
{
  "code": 0,
  "error": "string",
  "message": "string"
}
```

<h3 id="uploadzipterrfile-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Successful operation|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|The Zip/Terr file was not acceptable|[ErrorMessage](#schemaerrormessage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to upload a Zip/Terr file|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-trigger-file">trigger file</h1>

Endpoints to explore trigger files

## listTriggerFiles

<a id="opIdlistTriggerFiles"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/triggerFiles \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/triggerFiles HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/triggerFiles',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/triggerFiles',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/triggerFiles', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/triggerFiles', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/triggerFiles");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/triggerFiles", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /triggerFiles`

*List trigger files*

<h3 id="listtriggerfiles-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(TriggerFileCursor)|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "id": "string",
      "name": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listtriggerfiles-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[TriggerFilePage](#schematriggerfilepage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-alert-type">alert type</h1>

Endpoints to explore alert types

## listAlertTypes

<a id="opIdlistAlertTypes"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/alertTypes \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/alertTypes HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/alertTypes',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/alertTypes',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/alertTypes', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/alertTypes', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/alertTypes");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/alertTypes", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /alertTypes`

*List alert types*

<h3 id="listalerttypes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(AlertTypeCursor)|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "id": "string",
      "name": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listalerttypes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[AlertTypePage](#schemaalerttypepage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-provider-specialty">provider specialty</h1>

Endpoints to explore provider specialties

## listProviderSpecialties

<a id="opIdlistProviderSpecialties"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/providerSpecialties \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/providerSpecialties HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/providerSpecialties',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/providerSpecialties',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/providerSpecialties', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/providerSpecialties', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/providerSpecialties");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/providerSpecialties", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /providerSpecialties`

*List provider specialties*

<h3 id="listproviderspecialties-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(ProviderSpecialtyCursor)|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "id": "string",
      "name": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listproviderspecialties-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[ProviderSpecialtyPage](#schemaproviderspecialtypage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-alerts">alerts</h1>

Endpoints to explore alerts

## analyzeNationAlerts

<a id="opIdanalyzeNationAlerts"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}/alerts/analysis", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /nations/{nationId}/alerts/analysis`

*Analyze all alerts in the nation*

<h3 id="analyzenationalerts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(AlertsAnalysisCursor)|false|none|
|dimension1|query|[AlertDimension](#schemaalertdimension)|false|none|
|ordering1|query|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|
|dimension2|query|[AlertDimension](#schemaalertdimension)|false|none|
|ordering2|query|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|
|period|query|string(Period)|false|none|
|geography|query|array[string]|false|none|
|state|query|array[string]|false|none|
|triggerFile|query|array[string]|false|none|
|alertType|query|array[string]|false|none|
|providerSpecialty|query|array[string]|false|none|
|targeting|query|array[string]|false|none|
|nationId|path|string(NationId)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|dimension1|geography|
|dimension1|triggerFile|
|dimension1|alertType|
|dimension1|providerSpecialty|
|dimension1|targeting|
|ordering1|value|
|ordering1|count|
|dimension2|geography|
|dimension2|triggerFile|
|dimension2|alertType|
|dimension2|providerSpecialty|
|dimension2|targeting|
|ordering2|value|
|ordering2|count|
|targeting|target|
|targeting|nonTarget|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "value": "string",
      "count": 0,
      "items": [
        {}
      ]
    }
  ],
  "dimension1": "geography",
  "ordering1": "value",
  "dimension2": "geography",
  "ordering2": "value",
  "period": {
    "since": "2019-08-24",
    "until": "2019-08-24"
  },
  "triggerFiles": [
    "string"
  ],
  "alertTypes": [
    "string"
  ],
  "providerSpecialties": [
    "string"
  ],
  "targetings": [
    "target"
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="analyzenationalerts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[AlertAnalysisPage](#schemaalertanalysispage)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|There was a problem with the user's request|[ErrorMessage](#schemaerrormessage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view alerts data at the national level|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## analyzeRegionAlerts

<a id="opIdanalyzeRegionAlerts"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}/alerts/analysis", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /regions/{regionId}/alerts/analysis`

*Analyze the alerts in a region*

<h3 id="analyzeregionalerts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(AlertsAnalysisCursor)|false|none|
|dimension1|query|[AlertDimension](#schemaalertdimension)|false|none|
|ordering1|query|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|
|dimension2|query|[AlertDimension](#schemaalertdimension)|false|none|
|ordering2|query|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|
|period|query|string(Period)|false|none|
|geography|query|array[string]|false|none|
|state|query|array[string]|false|none|
|triggerFile|query|array[string]|false|none|
|alertType|query|array[string]|false|none|
|providerSpecialty|query|array[string]|false|none|
|targeting|query|array[string]|false|none|
|regionId|path|string(RegionId)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|dimension1|geography|
|dimension1|triggerFile|
|dimension1|alertType|
|dimension1|providerSpecialty|
|dimension1|targeting|
|ordering1|value|
|ordering1|count|
|dimension2|geography|
|dimension2|triggerFile|
|dimension2|alertType|
|dimension2|providerSpecialty|
|dimension2|targeting|
|ordering2|value|
|ordering2|count|
|targeting|target|
|targeting|nonTarget|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "value": "string",
      "count": 0,
      "items": [
        {}
      ]
    }
  ],
  "dimension1": "geography",
  "ordering1": "value",
  "dimension2": "geography",
  "ordering2": "value",
  "period": {
    "since": "2019-08-24",
    "until": "2019-08-24"
  },
  "triggerFiles": [
    "string"
  ],
  "alertTypes": [
    "string"
  ],
  "providerSpecialties": [
    "string"
  ],
  "targetings": [
    "target"
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="analyzeregionalerts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[AlertAnalysisPage](#schemaalertanalysispage)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|There was a problem with the user's request|[ErrorMessage](#schemaerrormessage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view alerts data in the given region|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## analyzeTerritoryAlerts

<a id="opIdanalyzeTerritoryAlerts"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts/analysis", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /territories/{territoryId}/alerts/analysis`

*Analyze the alerts in a territory*

<h3 id="analyzeterritoryalerts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(AlertsCursor)|false|none|
|dimension1|query|[AlertDimension](#schemaalertdimension)|false|none|
|ordering1|query|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|
|dimension2|query|[AlertDimension](#schemaalertdimension)|false|none|
|ordering2|query|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|
|period|query|string(Period)|false|none|
|state|query|array[string]|false|none|
|triggerFile|query|array[string]|false|none|
|alertType|query|array[string]|false|none|
|providerSpecialty|query|array[string]|false|none|
|targeting|query|array[string]|false|none|
|territoryId|path|string(TerritoryId)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|dimension1|geography|
|dimension1|triggerFile|
|dimension1|alertType|
|dimension1|providerSpecialty|
|dimension1|targeting|
|ordering1|value|
|ordering1|count|
|dimension2|geography|
|dimension2|triggerFile|
|dimension2|alertType|
|dimension2|providerSpecialty|
|dimension2|targeting|
|ordering2|value|
|ordering2|count|
|targeting|target|
|targeting|nonTarget|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "id": "string",
      "date": "2019-08-24",
      "location": {
        "latitude": -180,
        "longitude": -180
      },
      "triggerFile": "string",
      "alertType": "string",
      "providerSpecialty": "string",
      "targeting": "target",
      "npi": "string"
    }
  ],
  "period": {
    "since": "2019-08-24",
    "until": "2019-08-24"
  },
  "area": {
    "left": -180,
    "top": -180,
    "right": -180,
    "bottom": -180
  },
  "triggerFiles": [
    "string"
  ],
  "alertTypes": [
    "string"
  ],
  "providerSpecialties": [
    "string"
  ],
  "targetings": [
    "target"
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="analyzeterritoryalerts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[AlertPage](#schemaalertpage)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|There was a problem with the user's request|[ErrorMessage](#schemaerrormessage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view alerts in the given territory|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## listTerritoryAlerts

<a id="opIdlistTerritoryAlerts"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}/alerts", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /territories/{territoryId}/alerts`

*List the alerts in a territory*

<h3 id="listterritoryalerts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(AlertsAnalysisCursor)|false|none|
|area|query|string(BoundingBox)|false|none|
|period|query|string(Period)|false|none|
|state|query|array[string]|false|none|
|triggerFile|query|array[string]|false|none|
|alertType|query|array[string]|false|none|
|providerSpecialty|query|array[string]|false|none|
|targeting|query|array[string]|false|none|
|territoryId|path|string(TerritoryId)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|targeting|target|
|targeting|nonTarget|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "value": "string",
      "count": 0,
      "items": [
        {}
      ]
    }
  ],
  "dimension1": "geography",
  "ordering1": "value",
  "dimension2": "geography",
  "ordering2": "value",
  "period": {
    "since": "2019-08-24",
    "until": "2019-08-24"
  },
  "triggerFiles": [
    "string"
  ],
  "alertTypes": [
    "string"
  ],
  "providerSpecialties": [
    "string"
  ],
  "targetings": [
    "target"
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listterritoryalerts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[AlertAnalysisPage](#schemaalertanalysispage)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|There was a problem with the user's request|[ErrorMessage](#schemaerrormessage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view alerts in the given territory|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-nation">nation</h1>

Endpoints to explore data at the national scope

## listNations

<a id="opIdlistNations"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/nations \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/nations HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/nations',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/nations',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/nations', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/nations', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/nations");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/nations", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /nations`

*List nations*

<h3 id="listnations-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(GeographyCursor)|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "type": "nation",
      "id": "string",
      "parent": "string",
      "owner": "string",
      "name": "string",
      "boundary": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listnations-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[GeographyPage](#schemageographypage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view the given region|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## getNation

<a id="opIdgetNation"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/nations/{nationId} \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/nations/{nationId} HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/nations/{nationId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /nations/{nationId}`

*Get metadata about the given region*

<h3 id="getnation-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|nationId|path|string(NationId)|true|none|

> Example responses

> 200 Response

```json
{
  "type": "nation",
  "id": "string",
  "parent": "string",
  "owner": "string",
  "name": "string",
  "boundary": "string"
}
```

<h3 id="getnation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[Geography](#schemageography)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view the given region|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-region">region</h1>

Endpoints to explore data at the regional scope

## listRegions

<a id="opIdlistRegions"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/regions \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/regions HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/regions',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/regions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/regions', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/regions', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/regions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/regions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /regions`

*List regions*

<h3 id="listregions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(GeographyCursor)|false|none|
|parent|query|string(NationId)|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "type": "nation",
      "id": "string",
      "parent": "string",
      "owner": "string",
      "name": "string",
      "boundary": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listregions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[GeographyPage](#schemageographypage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view region data|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## getRegion

<a id="opIdgetRegion"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/regions/{regionId} \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/regions/{regionId} HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/regions/{regionId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /regions/{regionId}`

*Get metadata about the given region*

<h3 id="getregion-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|regionId|path|string(RegionId)|true|none|

> Example responses

> 200 Response

```json
{
  "type": "nation",
  "id": "string",
  "parent": "string",
  "owner": "string",
  "name": "string",
  "boundary": "string"
}
```

<h3 id="getregion-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[Geography](#schemageography)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view the given region|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-state">state</h1>

Endpoints to explore data at the state scope

## listStates

<a id="opIdlistStates"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/states \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/states HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/states',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/states',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/states', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/states', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/states");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/states", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /states`

*List states*

<h3 id="liststates-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(GeographyCursor)|false|none|
|parent|query|string(NationId)|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "type": "nation",
      "id": "string",
      "parent": "string",
      "owner": "string",
      "name": "string",
      "boundary": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="liststates-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[GeographyPage](#schemageographypage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view state data|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## getState

<a id="opIdgetState"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/states/{stateId} \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/states/{stateId} HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/states/{stateId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/states/{stateId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/states/{stateId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/states/{stateId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/states/{stateId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/states/{stateId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /states/{stateId}`

*Get metadata about the given state*

<h3 id="getstate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|stateId|path|string(RegionId)|true|none|

> Example responses

> 200 Response

```json
{
  "type": "nation",
  "id": "string",
  "parent": "string",
  "owner": "string",
  "name": "string",
  "boundary": "string"
}
```

<h3 id="getstate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[Geography](#schemageography)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view the given state|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-territory">territory</h1>

Endpoints to explore data at the territory scope

## listTerritories

<a id="opIdlistTerritories"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/territories \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/territories HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/territories',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/territories',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/territories', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/territories', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/territories");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/territories", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /territories`

*List territories*

<h3 id="listterritories-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer|false|The max number of items to return per page|
|cursor|query|string(GeographyCursor)|false|none|
|parent|query|array[string]|false|none|

> Example responses

> 200 Response

```json
{
  "items": [
    {
      "type": "nation",
      "id": "string",
      "parent": "string",
      "owner": "string",
      "name": "string",
      "boundary": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}
```

<h3 id="listterritories-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[GeographyPage](#schemageographypage)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view territory data|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

## getTerritory

<a id="opIdgetTerritory"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId} \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId} HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/territories/{territoryId}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /territories/{territoryId}`

*Get metadata about the given territory*

<h3 id="getterritory-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|territoryId|path|string(TerritoryId)|true|none|

> Example responses

> 200 Response

```json
{
  "type": "nation",
  "id": "string",
  "parent": "string",
  "owner": "string",
  "name": "string",
  "boundary": "string"
}
```

<h3 id="getterritory-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[Geography](#schemageography)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|The current user is not allowed to view the given territory|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

<h1 id="ipm-ai-alerts-api-hcp">hcp</h1>

Endpoints to explore health care practitioners

## getHcp

<a id="opIdgetHcp"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://api.alerts.ipm.w2odev.com/v1/hcps/{npi} \
  -H 'Accept: application/json'

```

```http
GET https://api.alerts.ipm.w2odev.com/v1/hcps/{npi} HTTP/1.1
Host: api.alerts.ipm.w2odev.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.alerts.ipm.w2odev.com/v1/hcps/{npi}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.alerts.ipm.w2odev.com/v1/hcps/{npi}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.alerts.ipm.w2odev.com/v1/hcps/{npi}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.alerts.ipm.w2odev.com/v1/hcps/{npi}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("https://api.alerts.ipm.w2odev.com/v1/hcps/{npi}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.alerts.ipm.w2odev.com/v1/hcps/{npi}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /hcps/{npi}`

*Get metadata about HCP by NPI*

<h3 id="gethcp-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|npi|path|string(Npi)|true|none|

> Example responses

> 200 Response

```json
{
  "npi": "string",
  "name": "string"
}
```

<h3 id="gethcp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful operation|[HealthCarePractitioner](#schemahealthcarepractitioner)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|The user's credentials were not valid|[ErrorMessage](#schemaerrormessage)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
api_key
</aside>

# Schemas

<h2 id="tocS_Role">Role</h2>
<!-- backwards compatibility -->
<a id="schemarole"></a>
<a id="schema_Role"></a>
<a id="tocSrole"></a>
<a id="tocsrole"></a>

```json
"HomeOffice"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|HomeOffice|
|*anonymous*|Manager|
|*anonymous*|Rep|

<h2 id="tocS_User">User</h2>
<!-- backwards compatibility -->
<a id="schemauser"></a>
<a id="schema_User"></a>
<a id="tocSuser"></a>
<a id="tocsuser"></a>

```json
{
  "id": "string",
  "email": "string",
  "name": "string",
  "role": "HomeOffice"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(UserId)|false|none|none|
|email|string(Email)|false|none|none|
|name|string|false|none|none|
|role|[Role](#schemarole)|false|none|none|

<h2 id="tocS_AlertDimension">AlertDimension</h2>
<!-- backwards compatibility -->
<a id="schemaalertdimension"></a>
<a id="schema_AlertDimension"></a>
<a id="tocSalertdimension"></a>
<a id="tocsalertdimension"></a>

```json
"geography"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|geography|
|*anonymous*|triggerFile|
|*anonymous*|alertType|
|*anonymous*|providerSpecialty|
|*anonymous*|targeting|

<h2 id="tocS_Targeting">Targeting</h2>
<!-- backwards compatibility -->
<a id="schematargeting"></a>
<a id="schema_Targeting"></a>
<a id="tocStargeting"></a>
<a id="tocstargeting"></a>

```json
"target"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|target|
|*anonymous*|nonTarget|

<h2 id="tocS_Coordinates">Coordinates</h2>
<!-- backwards compatibility -->
<a id="schemacoordinates"></a>
<a id="schema_Coordinates"></a>
<a id="tocScoordinates"></a>
<a id="tocscoordinates"></a>

```json
{
  "latitude": -180,
  "longitude": -180
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|latitude|number(double)|false|none|none|
|longitude|number(double)|false|none|none|

<h2 id="tocS_BoundingBox">BoundingBox</h2>
<!-- backwards compatibility -->
<a id="schemaboundingbox"></a>
<a id="schema_BoundingBox"></a>
<a id="tocSboundingbox"></a>
<a id="tocsboundingbox"></a>

```json
{
  "left": -180,
  "top": -180,
  "right": -180,
  "bottom": -180
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|left|number(double)|false|none|none|
|top|number(double)|false|none|none|
|right|number(double)|false|none|none|
|bottom|number(double)|false|none|none|

<h2 id="tocS_ErrorMessage">ErrorMessage</h2>
<!-- backwards compatibility -->
<a id="schemaerrormessage"></a>
<a id="schema_ErrorMessage"></a>
<a id="tocSerrormessage"></a>
<a id="tocserrormessage"></a>

```json
{
  "code": 0,
  "error": "string",
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|true|none|HTTP status code|
|error|string|true|none|A machine-readable error message|
|message|string|true|none|A human-readable error message|

<h2 id="tocS_Period">Period</h2>
<!-- backwards compatibility -->
<a id="schemaperiod"></a>
<a id="schema_Period"></a>
<a id="tocSperiod"></a>
<a id="tocsperiod"></a>

```json
{
  "since": "2019-08-24",
  "until": "2019-08-24"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|since|string(date)|true|none|none|
|until|string(date)|true|none|none|

<h2 id="tocS_TriggerFile">TriggerFile</h2>
<!-- backwards compatibility -->
<a id="schematriggerfile"></a>
<a id="schema_TriggerFile"></a>
<a id="tocStriggerfile"></a>
<a id="tocstriggerfile"></a>

```json
{
  "id": "string",
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(TriggerFileId)|true|none|none|
|name|string|true|none|none|

<h2 id="tocS_TriggerFilePage">TriggerFilePage</h2>
<!-- backwards compatibility -->
<a id="schematriggerfilepage"></a>
<a id="schema_TriggerFilePage"></a>
<a id="tocStriggerfilepage"></a>
<a id="tocstriggerfilepage"></a>

```json
{
  "items": [
    {
      "id": "string",
      "name": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|items|[[TriggerFile](#schematriggerfile)]|false|none|none|
|limit|integer(int32)|false|none|none|
|cursor|string(TriggerFileCursor)|false|none|none|

<h2 id="tocS_AlertType">AlertType</h2>
<!-- backwards compatibility -->
<a id="schemaalerttype"></a>
<a id="schema_AlertType"></a>
<a id="tocSalerttype"></a>
<a id="tocsalerttype"></a>

```json
{
  "id": "string",
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(AlertTypeId)|true|none|none|
|name|string|true|none|none|

<h2 id="tocS_AlertTypePage">AlertTypePage</h2>
<!-- backwards compatibility -->
<a id="schemaalerttypepage"></a>
<a id="schema_AlertTypePage"></a>
<a id="tocSalerttypepage"></a>
<a id="tocsalerttypepage"></a>

```json
{
  "items": [
    {
      "id": "string",
      "name": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|items|[[AlertType](#schemaalerttype)]|false|none|none|
|limit|integer(int32)|false|none|none|
|cursor|string(AlertTypeCursor)|false|none|none|

<h2 id="tocS_ProviderSpecialty">ProviderSpecialty</h2>
<!-- backwards compatibility -->
<a id="schemaproviderspecialty"></a>
<a id="schema_ProviderSpecialty"></a>
<a id="tocSproviderspecialty"></a>
<a id="tocsproviderspecialty"></a>

```json
{
  "id": "string",
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(ProviderSpecialtyId)|true|none|none|
|name|string|true|none|none|

<h2 id="tocS_ProviderSpecialtyPage">ProviderSpecialtyPage</h2>
<!-- backwards compatibility -->
<a id="schemaproviderspecialtypage"></a>
<a id="schema_ProviderSpecialtyPage"></a>
<a id="tocSproviderspecialtypage"></a>
<a id="tocsproviderspecialtypage"></a>

```json
{
  "items": [
    {
      "id": "string",
      "name": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|items|[[ProviderSpecialty](#schemaproviderspecialty)]|false|none|none|
|limit|integer(int32)|false|none|none|
|cursor|string(ProviderSpecialtyCursor)|false|none|none|

<h2 id="tocS_AlertAnalysisOrdering">AlertAnalysisOrdering</h2>
<!-- backwards compatibility -->
<a id="schemaalertanalysisordering"></a>
<a id="schema_AlertAnalysisOrdering"></a>
<a id="tocSalertanalysisordering"></a>
<a id="tocsalertanalysisordering"></a>

```json
"value"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|value|
|*anonymous*|count|

<h2 id="tocS_AlertAnalysisEntry">AlertAnalysisEntry</h2>
<!-- backwards compatibility -->
<a id="schemaalertanalysisentry"></a>
<a id="schema_AlertAnalysisEntry"></a>
<a id="tocSalertanalysisentry"></a>
<a id="tocsalertanalysisentry"></a>

```json
{
  "value": "string",
  "count": 0,
  "items": [
    {
      "value": "string",
      "count": 0,
      "items": []
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|value|string|true|none|none|
|count|integer(int32)|true|none|none|
|items|[[AlertAnalysisEntry](#schemaalertanalysisentry)]|false|none|none|

<h2 id="tocS_AlertAnalysisPage">AlertAnalysisPage</h2>
<!-- backwards compatibility -->
<a id="schemaalertanalysispage"></a>
<a id="schema_AlertAnalysisPage"></a>
<a id="tocSalertanalysispage"></a>
<a id="tocsalertanalysispage"></a>

```json
{
  "items": [
    {
      "value": "string",
      "count": 0,
      "items": [
        {}
      ]
    }
  ],
  "dimension1": "geography",
  "ordering1": "value",
  "dimension2": "geography",
  "ordering2": "value",
  "period": {
    "since": "2019-08-24",
    "until": "2019-08-24"
  },
  "triggerFiles": [
    "string"
  ],
  "alertTypes": [
    "string"
  ],
  "providerSpecialties": [
    "string"
  ],
  "targetings": [
    "target"
  ],
  "limit": 0,
  "cursor": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|items|[[AlertAnalysisEntry](#schemaalertanalysisentry)]|false|none|none|
|dimension1|[AlertDimension](#schemaalertdimension)|false|none|none|
|ordering1|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|none|
|dimension2|[AlertDimension](#schemaalertdimension)|false|none|none|
|ordering2|[AlertAnalysisOrdering](#schemaalertanalysisordering)|false|none|none|
|period|[Period](#schemaperiod)|false|none|none|
|triggerFiles|[string]|false|none|none|
|alertTypes|[string]|false|none|none|
|providerSpecialties|[string]|false|none|none|
|targetings|[[Targeting](#schematargeting)]|false|none|none|
|limit|integer(int32)|false|none|none|
|cursor|string(AlertAnalysisCursor)|false|none|none|

<h2 id="tocS_Alert">Alert</h2>
<!-- backwards compatibility -->
<a id="schemaalert"></a>
<a id="schema_Alert"></a>
<a id="tocSalert"></a>
<a id="tocsalert"></a>

```json
{
  "id": "string",
  "date": "2019-08-24",
  "location": {
    "latitude": -180,
    "longitude": -180
  },
  "triggerFile": "string",
  "alertType": "string",
  "providerSpecialty": "string",
  "targeting": "target",
  "npi": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string(AlertId)|false|none|none|
|date|string(date)|false|none|none|
|location|[Coordinates](#schemacoordinates)|false|none|none|
|triggerFile|string(TriggerFileId)|false|none|none|
|alertType|string(AlertTypeId)|false|none|none|
|providerSpecialty|string(ProviderSpecialtyId)|false|none|none|
|targeting|[Targeting](#schematargeting)|false|none|none|
|npi|string(Npi)|false|none|none|

<h2 id="tocS_AlertPage">AlertPage</h2>
<!-- backwards compatibility -->
<a id="schemaalertpage"></a>
<a id="schema_AlertPage"></a>
<a id="tocSalertpage"></a>
<a id="tocsalertpage"></a>

```json
{
  "items": [
    {
      "id": "string",
      "date": "2019-08-24",
      "location": {
        "latitude": -180,
        "longitude": -180
      },
      "triggerFile": "string",
      "alertType": "string",
      "providerSpecialty": "string",
      "targeting": "target",
      "npi": "string"
    }
  ],
  "period": {
    "since": "2019-08-24",
    "until": "2019-08-24"
  },
  "area": {
    "left": -180,
    "top": -180,
    "right": -180,
    "bottom": -180
  },
  "triggerFiles": [
    "string"
  ],
  "alertTypes": [
    "string"
  ],
  "providerSpecialties": [
    "string"
  ],
  "targetings": [
    "target"
  ],
  "limit": 0,
  "cursor": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|items|[[Alert](#schemaalert)]|false|none|none|
|period|[Period](#schemaperiod)|false|none|none|
|area|[BoundingBox](#schemaboundingbox)|false|none|none|
|triggerFiles|[string]|false|none|none|
|alertTypes|[string]|false|none|none|
|providerSpecialties|[string]|false|none|none|
|targetings|[[Targeting](#schematargeting)]|false|none|none|
|limit|integer(int32)|false|none|none|
|cursor|string(AlertCursor)|false|none|none|

<h2 id="tocS_GeographyType">GeographyType</h2>
<!-- backwards compatibility -->
<a id="schemageographytype"></a>
<a id="schema_GeographyType"></a>
<a id="tocSgeographytype"></a>
<a id="tocsgeographytype"></a>

```json
"nation"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|*anonymous*|nation|
|*anonymous*|region|
|*anonymous*|state|
|*anonymous*|territory|

<h2 id="tocS_Geography">Geography</h2>
<!-- backwards compatibility -->
<a id="schemageography"></a>
<a id="schema_Geography"></a>
<a id="tocSgeography"></a>
<a id="tocsgeography"></a>

```json
{
  "type": "nation",
  "id": "string",
  "parent": "string",
  "owner": "string",
  "name": "string",
  "boundary": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|[GeographyType](#schemageographytype)|false|none|none|
|id|string|false|none|none|
|parent|string|false|none|none|
|owner|string(UserId)|false|none|none|
|name|string|false|none|none|
|boundary|string(geojson)|false|none|none|

<h2 id="tocS_GeographyPage">GeographyPage</h2>
<!-- backwards compatibility -->
<a id="schemageographypage"></a>
<a id="schema_GeographyPage"></a>
<a id="tocSgeographypage"></a>
<a id="tocsgeographypage"></a>

```json
{
  "items": [
    {
      "type": "nation",
      "id": "string",
      "parent": "string",
      "owner": "string",
      "name": "string",
      "boundary": "string"
    }
  ],
  "limit": 0,
  "cursor": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|items|[[Geography](#schemageography)]|false|none|none|
|limit|integer(int32)|false|none|none|
|cursor|string(GeographyCursor)|false|none|none|

<h2 id="tocS_HealthCarePractitioner">HealthCarePractitioner</h2>
<!-- backwards compatibility -->
<a id="schemahealthcarepractitioner"></a>
<a id="schema_HealthCarePractitioner"></a>
<a id="tocShealthcarepractitioner"></a>
<a id="tocshealthcarepractitioner"></a>

```json
{
  "npi": "string",
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|npi|string(npi)|false|none|none|
|name|string|false|none|none|


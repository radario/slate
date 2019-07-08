---
title: Radario.Api v1
language_tabs:
  - shell: Shell
  - http: HTTP
  - html: JavaScript
  - javascript: Node.JS
  - python: Python
  - ruby: Ruby
  - java: Java
toc_footers: []
includes: []
search: true
highlight_theme: darkula
---

# Radario.Api v1



Base URL = https://api.radario.ru/

The only one accepted Content-Type is 'application/json' (See code examples)  
Messages charset is set to UTF-8



# Categories

## /v1/categories

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/categories
````

````http
GET https://api.radario.ru/v1/categories HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/categories',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/categories', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/categories', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/categories', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/categories");
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
````

`GET /v1/categories`

Get events categories

> Response model

````json
{
  "success": "bool",
  "data": [
	{
	  "id": "int",
      "name": "string"
	}
  ],
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK


### Attributes

Attribute|Description
---|---|---|
id|Category id
name|Category name

# Cities

## /v1/cities

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/cities
````

````http
GET https://api.radario.ru/v1/cities HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/cities',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/cities', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/cities', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/cities', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/cities");
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
````

`GET /v1/cities`

Get cities

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
limit|query|integer|false|Specifies the number of items to return (default 30)
offset|query|integer|false|Specifies the number of items to skip

> Response model

````json
{
  "success": "bool",
  "data": [
	{
		"id": "int",
        "name": "string",
        "latitude": "double",
        "longitude": "double",
        "gmtOffset": "int"
	}
  ],
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK


### Attributes

Attribute|Description
---|---|---|
id|City id
name|City name
latitude|City latitude
longitude|City longitude
gmtOffset|City GMT offset

# Company

## /v1/hosts/{id}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/hosts/{id}
````

````http
GET https://api.radario.ru/v1/hosts/{id} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/hosts/{id}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/hosts/{id}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/hosts/{id}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/hosts/{id}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/hosts/{id}");
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
````

`GET /v1/hosts/{id}`

Get company by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description

> Response model

````json
{
  "success": "bool",
  "data": {
		"id": "int",
		"title": "string",
		"logoUri": "string",
		"requisiteName": "string",
		"requisiteINN": "string",
		"requisiteAddress": "string",
		"supportEmail": "string",
		"supportPhone": "string",
		"visitingRules": "string",
		"refundRules": "string"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK


### Attributes

Attribute|Description
---|---|---|
id|Company id
title|Company title
logoUri|Company logo URI
requisiteName|Company requisite name
requisiteINN|Company requisite INN
requisiteAddress|Company requisite address
supportEmail|Company support email
supportPhone|Company support phone
visitingRules|Company visiting rules
refundRules|Company refund phone

# Events

## /v1/events

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/events
````

````http
GET https://api.radario.ru/v1/events HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/events',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/events', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/events', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/events', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/events");
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
````

`GET /v1/events`

Get events by query

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
onlyActual|query|bool|false|Flag for actual events only
cityId|query|integer|false|Id of city where event take place
placeId|query|integer|false|Id of place where event take place
companyId|query|integer|false|Id of company that organize event
superTagId|query|integer|false|Event type id (e.g concert, perfomance, party, etc.)
limit|query|integer|false|Specifies the number of items to return (default 20)
offset|query|integer|false|Specifies the number of items to skip
groupId|query|integer|false|Id of event group
onlyWithOrderCreationAvailableViaApi|query|bool|false|Should specify true to return events with permission to create
endDate|query|string|false|Get events with end date great or equal than specific in parameter. ISO 8601 format. If endDate is empty and eventDateFrom, eventDateTo are not specified, then current date assign to endDate 
eventDateFrom|query|string|false|If endDate is not specified, then events filtered by eventDateFrom and eventDateTo. So you can fetch all events, that  active in this range. ISO 8601 format.
eventDateTo|query|string|false|If endDate is not specified, then events filtered by eventDateFrom and eventDateTo. So you can fetch all events, that  active in this range. ISO 8601 format.

> Response model

````json
{
  "success": "bool",
  "data": {
	"items": [
		{
			"id": "int",
			"title": "string",
			"description": "string",
			"age": "int",
			"beginDate": "datetime",
			"endDate": "datetime",
			"salesStopped": "bool",
			"videoUrl": "string",
			"images": "string",
			"category": "string",
			"placeId": "int",
			"placeTitle": "string",
			"placeAddress": "string",
			"companyId": "int",
			"companyTitle": "string",
			"eventProviderId": "int",
			"eventProviderName": "string",
			"minPrice": "int",
			"maxPrice": "int",
			"cityId": "int",
			"cityName": "string",
			"placeSchemeId": "int",
			"groupId": "int",
			"currency": "string",
			"ticketCount": "int",
			"gmtOffset": "int"
		}
	],
	"totalCount": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Event id
title|Event title
description|Event description
age|Allowable age
beginDate|Event begining date
endDate|Event ending date
salesStopped|Should specify to return events whose sales stopped
videoUrl|Event video URL
images|Event images
category|Event category
placeId|Id of place where event take place
placeTitle|Title of place where event take place
placeAddress|Address of place where event take place
companyId|Id of company that organize event
companyTitle|Title of company that organize event
eventProviderId|Id of event provider that organize event
eventProviderName|Name of event provider that organize event
minPrice|Minimum price of tickets on event
maxPrice|Maximum price of tickets on event
cityId|Id of city where event take place
cityName|Name of city where event take place
placeSchemeId|Id of event place schema
groupId|Id of event group
currency|Payment currency
ticketCount|Count of event tickets
gmtOffset|GMT offset of city where event take place
totalCount|Total count of items

<aside class="notice">
In case if you passed authorization credentials you get only events available for you as an agent
</aside>

## /v1/events/{eventId}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/events/{eventId}
````

````http
GET https://api.radario.ru/v1/events/{eventId} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/events/{eventId}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/events/{eventId}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/events/{eventId}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/events/{eventId}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/events/{eventId}");
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
````

`GET /v1/events/{eventId}`

Get event by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
eventId|path|integer|true|Event id


> Response model

````json
{
  "success": "bool",
  "data": {
	"id": "int",
	"title": "string",
	"description": "string",
	"age": "int",
	"beginDate": "datetime",
	"endDate": "datetime",
	"salesStopped": "bool",
	"videoUrl": "string",
	"images": "string",
	"category": "string",
	"placeId": "int",
	"placeTitle": "string",
	"placeAddress": "string",
	"companyId": "int",
	"companyTitle": "string",
	"eventProviderId": "int",
	"eventProviderName": "string",
	"minPrice": "int",
	"maxPrice": "int",
	"cityId": "int",
	"cityName": "string",
	"placeSchemeId": "int",
	"groupId": "int",
	"currency": "string",
	"ticketCount": "int",
	"gmtOffset": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Event id
title|Event title
description|Event description
age|Allowable age
beginDate|Event begining date
endDate|Event ending date
salesStopped|Should specify to return events whose sales stopped
videoUrl|Event video URL
images|Event images
category|Event category
placeId|Id of place where event take place
placeTitle|Title of place where event take place
placeAddress|Address of place where event take place
companyId|Id of company that organize event
companyTitle|Title of company that organize event
eventProviderId|Id of event provider that organize event
eventProviderName|Name of event provider that organize event
minPrice|Minimum price of tickets on event
maxPrice|Maximum price of tickets on event
cityId|Id of city where event take place
cityName|Name of city where event take place
placeSchemeId|Id of event place schema
groupId|Id of event group
currency|Payment currency
ticketCount|Count of event tickets
gmtOffset|GMT offset of city where event take place
totalCount|Total count of items

## /v1/events/{eventId}/ticket_types

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/events/{eventId}/ticket_types
````

````http
GET https://api.radario.ru/v1/events/{eventId}/ticket_types HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/events/{eventId}/ticket_types',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/events/{eventId}/ticket_types', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/events/{eventId}/ticket_types', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/events/{eventId}/ticket_types', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/events/{eventId}/ticket_types");
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
````

`GET /v1/events/{eventId}/ticket_types`

Get event TicketType item

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
eventId|path|integer|true|Event id
onlyWithOrderCreationAvailableViaApi|query|bool|false|true to return only TicketTypes, that provide places available to buy
limit|query|integer|false|Specifies the number of items to return (default 30)
offset|query|integer|false|Specifies the number of items to skip

> Response model

````json
{
  "success": "bool",
  "data": {
    "items": [
      {
        "id": "int",
        "title": "string",
        "price": "decimal",
        "ticketCount": "int",
        "soldTicketCount": "int",
        "withSeats": "bool",
        "series": "string",
        "seatBeginNumber": "int",
        "seatEndNumber": "int",
        "zoneId": "int",
		"participantNameRequired": "bool",
        "seats": [
			{
				"isOccupied": "bool",
				"number": "int",
				"rowName": "string",
				"seatName": "string",
				"exists": "bool"
			}
		],
		"baseTicketTypeId": "int"
      }
    ],
    "totalCount": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|TicketType id
title|TicketType title
price|Ticket price
ticket|Ticket amount
soldTicketCount|Sold ticket amount
withSeats|Indicate if tickets of TicketType with seat
series|Series of tickets
seatBeginNumber|Indicate seat number range (from)
seatEndNumber|Indicate seat number range (to)
participantNameRequired|Requires participant name on ticket
zoneId|Id of seats zone
seats|List of seat
seats[i].IsOccupied|Indicate if seat is occupied
seats[i].Number|Number of seat
seats[i].RowName|Name of seat row
seats[i].SeatName|Name of seat
seats[i].Exists|Indicate if seat is exist on grid
baseTicketTypeId|Base TicketType Id

<aside class="notice">
In case if you passed authorization credentials you get only ticket types available for you as an agent
</aside>

## /v1/events/{eventId}/tickets

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/events/{eventId}/tickets
````

````http
GET https://api.radario.ru/v1/events/{eventId}/tickets HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/events/{eventId}/tickets',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/events/{eventId}/tickets', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/events/{eventId}/tickets', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/events/{eventId}/tickets', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/events/{eventId}/tickets");
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
````

`GET /v1/events/{eventId}/tickets`

Get tickets (only bought or booked) by event id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
eventId|path|integer|true|Event id
limit|query|integer|false|Specifies the number of items to return (default 30)
offset|query|integer|false|Specifies the number of items to skip

> Response model

````json
{
  "success": "bool",
  "data": {
	"items": [
	{
		"id": "int",
		"ticketTypeId": "int",
		"userOrderId": "int",
		"ticketTypeTitle": "string",
		"ticketTypeZoneId": "int",
		"number": "string",
		"price": "double",
		"discount": "double",
		"isUsed": "bool",
		"barcodeKey": "string",
		"seatNumber": "string",
		"seatName": "string",
		"rowName": "string",
		"participantName": "string",
		"seatInfo": "string"
	}],
	"totalCount": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Ticket id
ticketTypeId|TicketType id
userOrderId|UserOrder id
ticketTypeTitle|TicketType title
ticketTypeZoneId|TicketType zone id
number|Ticket number
price|Ticket price
discount|Ticket price discount
isUsed|Indicate if ticket is used
barcodeKey|Ticket barcode key
seatNumber|Ticket seat number
seatName|Ticket seat name
rowName|Ticket row name
participantName|Ticket participant name
seatInfo|Ticket customer name


<aside class="notice">
This operation require authentication
</aside>

## /v1/events/{eventId}/orders

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/events/{eventId}/orders
````

````http
GET https://api.radario.ru/v1/events/{eventId}/orders HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/events/{eventId}/orders',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/events/{eventId}/orders', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/events/{eventId}/orders', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/events/{eventId}/orders', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/events/{eventId}/orders");
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
````

`GET /v1/events/{eventId}/orders`

Get orders by event id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
eventId|path|integer|true|Event id
limit|query|integer|false|Specifies the number of items to return (default 30)
offset|query|integer|false|Specifies the number of items to skip

> Response model

````json
{
  "success": "bool",
  "data": {
	"items": [
		{
			"id": "int",
			"isPaid": "bool",
			"eventId": "int",
			"creationDate": "datetime",
			"ticketCount": "int",
			"baseAmount": "double",
			"amount": "double",
			"tickets": [
			{
				"id": "int",
				"ticketTypeId": "int",
				"userOrderId": "int",
				"ticketTypeTitle": "string",
				"ticketTypeZoneId": "int",
				"number": "string",
				"price": "double",
				"discount": "double",
				"isUsed": "bool",
				"barcodeKey": "string",
				"seatNumber": "string",
				"seatName": "string",
				"rowName": "string",
				"participantName": "string",
				"seatInfo": "string"
			}],
			"orderNumber": "string",
			"distributionType": "string",
			"paymentType": "int"
		}
	],
	"totalCount": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Order id
isPaid|Indicate if order is paid
eventId|Order event id
creationDate|Order creation datetime
ticketCount|Order ticket amount
baseAmount|Summarу tickets price
amount|Order amount (with considering debit from user cash)
orderNumber|Order number
distributionType|Order DistributionType
paymentType|Order PaymentType
tickets|List of tickets
tickets[i].id|Ticket id
tickets[i].ticketTypeId|TicketType id
tickets[i].userOrderId|UserOrder id
tickets[i].ticketTypeTitle|TicketType title
tickets[i].ticketTypeZoneId|TicketType zone id
tickets[i].number|Ticket number
tickets[i].price|Ticket price
tickets[i].discount|Ticket price discount
tickets[i].isUsed|Indicate if ticket is used
tickets[i].barcodeKey|Ticket barcode key
tickets[i].seatNumber|Ticket seat number
tickets[i].seatName|Ticket seat name
tickets[i].rowName|Ticket row name
tickets[i].participantName|Ticket participant name
tickets[i].seatInfo|Ticket customer name

<aside class="notice">
This operation require authentication
</aside>

# EventProviders

## v1/event-providers/{eventProviderId}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/event-providers/{eventProviderId}
````

````http
GET https://api.radario.ru/v1/event-providers/{eventProviderId} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/event-providers/{eventProviderId}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/event-providers/{eventProviderId}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/event-providers/{eventProviderId}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/event-providers/{eventProviderId}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/event-providers/{eventProviderId}");
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
````

`GET /v1/event-providers/{eventProviderId}`

Get event provider by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description

> Response model

````json
{
  "success": "bool",
  "data": {
		"id": "int",
		"companyId": "int",
		"cityId": "int",
		"Name": "string",
		"Description": "string",
		"Email": "string",
		"AdditionalEmails": "string",
		"Phone": "string",
		"INN": "string",
		"AllowSendSoldTicketReportForPrevDay": "bool"
		"AllowSendSoldTicketReportForAllTime": "bool",
		"CreationdDate": "datetime",
		"UpdateDate": "datetime",
		"Deleted": "bool",
		"CommissionFeePercent": "decimal",
		"Address": "string",
		"ContractNumber": "string",
		"ContractDate": "datetime"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK


### Attributes

Attribute|Description
---|---|---|
id|Event provider id
companyId|Company id
cityId|City id
name|Event provider name
description|Description
email|Email
additionalEmails|Additional emails
phone|Phone
INN|INN
AllowSendSoldTicketReportForPrevDay|Flag to send reports to event provider
AllowSendSoldTicketReportForAllTime|Flag to send reports to event provider
CreationdDate|Creation Date
UpdateDate|Update Date
Deleted|Deleted
CommissionFeePercent|Event provider percent 
Address|Adress
ContractNumber| Contract number
ContractDate|Contract date

## v1/company/{companyId}/event-providers

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/company/{companyId}/event-providers
````

````http
GET https://api.radario.ru/v1/company/{companyId}/event-providers HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/company/{companyId}/event-providers',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/company/{companyId}/event-providers', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/company/{companyId}/event-providers', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/company/{companyId}/event-providers', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/company/{companyId}/event-providers");
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
````

`GET /v1/company/{companyId}/event-providers`

Get event providers by company id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|No description

> Response model

````json
{
  "success": "bool",
  "data": [
	{
		"id": "int",
		"companyId": "int",
		"cityId": "int",
		"Name": "string",
		"Description": "string",
		"Email": "string",
		"AdditionalEmails": "string",
		"Phone": "string",
		"INN": "string",
		"AllowSendSoldTicketReportForPrevDay": "bool"
		"AllowSendSoldTicketReportForAllTime": "bool",
		"CreationdDate": "datetime",
		"UpdateDate": "datetime",
		"Deleted": "bool",
		"CommissionFeePercent": "decimal",
		"Address": "string",
		"ContractNumber": "string",
		"ContractDate": "datetime"
	}
  ]
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK


### Attributes

Attribute|Description
---|---|---|
id|Event provider id
companyId|Company id
cityId|City id
name|Event provider name
description|Description
email|Email
additionalEmails|Additional emails
phone|Phone
INN|INN
AllowSendSoldTicketReportForPrevDay|Flag to send reports to event provider
AllowSendSoldTicketReportForAllTime|Flag to send reports to event provider
CreationdDate|Creation Date
UpdateDate|Update Date
Deleted|Deleted
CommissionFeePercent|Event provider percent 
Address|Adress
ContractNumber| Contract number
ContractDate|Contract date

# Group

## /v1/hosts/{hostId}/groups

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/hosts/{hostId}/groups
````

````http
GET https://api.radario.ru/v1/hosts/{hostId}/groups HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/hosts/{hostId}/groups',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/hosts/{hostId}/groups', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/hosts/{hostId}/groups', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/hosts/{hostId}/groups', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/hosts/{hostId}/groups");
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
````

`GET /v1/hosts/{hostId}/groups`

Get events groups by company id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
hostId|path|integer|true|Company id
limit|query|string|false|Specifies the number of items to return (default 100)
offset|query|string|false|Specifies the number of items to skip

> Response model

````json
{
  "success": "bool",
  "data": {
	"items": [
		{
			"id": "int",
			"name": "string",
			"hostId": "int",
			"ticketCount": "int"
		}
	],
	"totalCount": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Event group id
name|Event group name
hostId|Company id
ticketCount|Total ticket amount of events group

# Orders

## /v1/orders/reserve

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/reserve
````

````http
POST https://api.radario.ru/v1/orders/reserve HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/reserve',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/reserve', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/reserve', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/reserve', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/reserve");
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
````

`POST /v1/orders/reserve`

Reserve seat to pay order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|ReserveOrderRequest|true|Request object

> Body parameter

````json
{
  "EventId": "int",
  "Tickets": [
  {
	"TicketTypeId": "int",
	"SeatNumber": "int",
	"ParticipantName": "string"
  }],
  "Email": "string",
  "PartnerId": "int",
  "Promocode": "string",
  "UtmData": {
    "UtmSource": "string",
    "UtmMedium": "string",
    "UtmTerm": "string",
    "UtmContent": "string",
    "UtmCampaign": "string",
    "UtmUserId": "string"
  }
}
````

### Attributes

Attribute|Description
---|---|---|
eventId|Event id
email|Customer email
tickets|List of seat info
tickets[i].TicketTypeId|TicketType id
tickets[i].SeatNumber|(Optional for tickets without seats) Seat number
tickets[i].ParticipantName|(Optional) Participant name
PartnerId|(Optional) Partner ID
Promocode|(Optional) Promocode to apply on userOrder
UtmData|(Optional) List of UTM Tracking tags.
UtmData.UtmSource|(Required if UtmData is present) utm-source of request
UtmData.UtmMedium|utm-medium of request
UtmData.UtmTerm|utm-term of request
UtmData.UtmContent|utm-content of request
UtmData.UtmCampaign|utm-campaign of request
UtmData.UtmUserId|utm-userid of requester

> Response model

````json
{
  "success": "bool",
  "data": {
	"order": {
		"id": "int",
		"isPaid": "bool",
		"eventId": "int",
		"creationDate": "datetime",
		"ticketCount": "int",
		"baseAmount": "double",
		"amount": "double",
		"tickets": [
		{
			"id": "int",
			"ticketTypeId": "int",
			"userOrderId": "int",
			"ticketTypeTitle": "string",
			"ticketTypeZoneId": "int",
			"number": "string",
			"price": "double",
			"discount": "double",
			"isUsed": "bool",
			"barcodeKey": "string",
			"seatNumber": "string",
			"seatName": "string",
			"rowName": "string",
			"participantName": "string",
			"seatInfo": "string"
		}],
		"orderNumber": "string",
		"distributionType": "string",
		"paymentType": "int"
	}
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
order|Order info
order.Id|Order id
order.IsPaid|Indicate if order is paid
order.EventId|Order event id
order.CreationDate|Order creation datetime
order.TicketCount|Order ticket amount
order.BaseAmount|Summarу tickets price
order.Amount|Order amount (with considering debit from user cash)
order.OrderNumber|Order number
order.DistributionType|Order DistributionType
order.PaymentType|Order PaymentType
order.Tickets|List of tickets
order.Tickets[i].id|Ticket id
order.Tickets[i].ticketTypeId|TicketType id
order.Tickets[i].userOrderId|UserOrder id
order.Tickets[i].ticketTypeTitle|TicketType title
order.Tickets[i].ticketTypeZoneId|TicketType zone id
order.Tickets[i].number|Ticket number
order.Tickets[i].price|Ticket price
order.Tickets[i].discount|Ticket price discount
order.Tickets[i].isUsed|Indicate if ticket is used
order.Tickets[i].barcodeKey|Ticket barcode key
order.Tickets[i].seatNumber|Ticket seat number
order.Tickets[i].seatName|Ticket seat name
order.Tickets[i].rowName|Ticket row name
order.Tickets[i].participantName|Ticket participant name
order.Tickets[i].seatInfo|Ticket customer name

<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/add_pre_reserved_seat

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/add_pre_reserved_seat
````

````http
POST https://api.radario.ru/v1/orders/add_pre_reserved_seat HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/add_pre_reserved_seat',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/add_pre_reserved_seat', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/add_pre_reserved_seat', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/add_pre_reserved_seat', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/add_pre_reserved_seat");
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
````

`POST /v1/orders/add_pre_reserved_seat`

Reserve seat to pay order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|ReserveOrderRequest|true|Request object

> Body parameter

````json
{
  "EventId": "int",
  "TicketTypeId": "int",
  "SeatNumber": "int",
  "TimeToLive": "int"
}
````

### Attributes

Attribute|Required|Description
---|---|---|---|
eventId|true|Event id
ticketTypeId|true|TicketType id
seatNumber|true|Seat number
timeToLive|false|Reservation lifetime in minutes. Default value - 15min

> Response model

````json
{
  "success": "bool",
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/remove_pre_reserved_seat

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/remove_pre_reserved_seat
````

````http
POST https://api.radario.ru/v1/orders/remove_pre_reserved_seat HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/remove_pre_reserved_seat',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/remove_pre_reserved_seat', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/remove_pre_reserved_seat', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/remove_pre_reserved_seat', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/remove_pre_reserved_seat");
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
````

`POST /v1/orders/remove_pre_reserved_seat`

Reserve seat to pay order

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|ReserveOrderRequest|true|Request object

> Body parameter

````json
{
  "EventId": "int",
  "TicketTypeId": "int",
  "SeatNumber": "int"
}
````

### Attributes

Attribute|Required|Description
---|---|---|---|
eventId|true|Event id
ticketTypeId|true|TicketType id
seatNumber|true|Seat number

> Response model

````json
{
  "success": "bool",
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/approve

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/approve
````

````http
POST https://api.radario.ru/v1/orders/approve HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/approve',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/approve', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/approve', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/approve', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/approve");
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
````

`POST /v1/orders/approve`

Approve order payment

> Body parameter

````json
{
  "orderId": "int"
}
````

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|OrderApproveRequest|true|Request object

### Attributes

Attribute|Description
---|---|---|
orderId|Order Id

> Response model

````json
{
  "success": "bool",
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/update

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/update
````

````http
POST https://api.radario.ru/v1/orders/update HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/update',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/update', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/update', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/update', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/update");
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
````

`POST /v1/orders/update`

> Body parameter

````json
{
  "orderId": "int",
  "email": "string"
}
````
### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|OrderUpdateRequest|true|Request object

### Attributes

Attribute|Description
---|---|---|
orderId|Order Id
email|Customer email

> Response model

````json
{
  "success": "bool",
  "data": 
	{
		"id": "int",
		"isPaid": "bool",
		"eventId": "int",
		"creationDate": "datetime",
		"ticketCount": "int",
		"baseAmount": "double",
		"amount": "double",
		"tickets": [
		{
			"id": "int",
			"ticketTypeId": "int",
			"userOrderId": "int",
			"ticketTypeTitle": "string",
			"ticketTypeZoneId": "int",
			"number": "string",
			"price": "double",
			"discount": "double",
			"isUsed": "bool",
			"barcodeKey": "string",
			"seatNumber": "string",
			"seatName": "string",
			"rowName": "string",
			"participantName": "string",
			"seatInfo": "string"
		}],
		"orderNumber": "string",
		"distributionType": "string",
		"paymentType": "int"
	},
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK
### Attributes

Attribute|Description
---|---|---|
id|Order id
isPaid|Indicate if order is paid
eventId|Order event id
creationDate|Order creation datetime
ticketCount|Order ticket amount
baseAmount|Summarу tickets price
amount|Order amount (with considering debit from user cash)
orderNumber|Order number
distributionType|Order DistributionType
paymentType|Order PaymentType
tickets|List of tickets
tickets[i].id|Ticket id
tickets[i].ticketTypeId|TicketType id
tickets[i].userOrderId|UserOrder id
tickets[i].ticketTypeTitle|TicketType title
tickets[i].ticketTypeZoneId|TicketType zone id
tickets[i].number|Ticket number
tickets[i].price|Ticket price
tickets[i].discount|Ticket price discount
tickets[i].isUsed|Indicate if ticket is used
tickets[i].barcodeKey|Ticket barcode key
tickets[i].seatNumber|Ticket seat number
tickets[i].seatName|Ticket seat name
tickets[i].rowName|Ticket row name
tickets[i].participantName|Ticket participant name
tickets[i].seatInfo|Ticket customer name

<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/cancel

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/cancel
````

````http
POST https://api.radario.ru/v1/orders/cancel HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/cancel',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/cancel', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/cancel', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/cancel', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/cancel");
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
````

`POST /v1/orders/cancel`

Cancel order

> Body parameter

````json
{
  "orderId": "int"
}
````
### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|OrderCancelRequest|true|Request object

Attribute|Description
---|---|---|
orderId|Order id

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

> Response model

````json
{
  "success": "bool",
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/send

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/send
````

````http
POST https://api.radario.ru/v1/orders/send HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/send',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/send', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/send', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/send', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/send");
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
````

`POST /v1/orders/send`

Send order to customer's email

> Body parameter

````json
{
  "orderId": "int"
}
````
### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|OrderSendRequest|true|Request object

Attribute|Description
---|---|---|
orderId|Order id

### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

> Response model

````json
{
  "success": "bool",
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/refund

> Code samples

````shell
# You can also use wget
curl -X post https://api.radario.ru/v1/orders/refund
````

````http
POST https://api.radario.ru/v1/orders/refund HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/refund',
    method: 'post',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/refund', { method: 'POST'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.post 'https://api.radario.ru/v1/orders/refund', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.post('https://api.radario.ru/v1/orders/refund', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/refund");
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
````

`POST /v1/orders/refund`

Refund order

> Body parameter

````json
{
  "UserOrderId": "string",
  "TicketNumber": "string",
  "RefundInitiator": "string",
  "Comment": "string",
  "Reason": "string"
}
````
### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
request|body|RefundRequest|true|Request object

### Attributes

Attribute|Description
---|---|---|
userOrderId|Order id
ticketNumber|Ticket number
refundInitiator|Refund initiator. Allowed values: 'User', 'Company', 'null'
comment|Comment
reason|Refund reason

> Response model

````json
{
  "success": "bool",
  "data": { 
	"refundId": "int",
	"companyId": "int",
	"refundedMoney": "decimal",
	"refundedUserCash": "decimal",
	"refundMethod": "int",
	"refundType": "int",
	"tickets": [
		{
			"ticketTypeId": "int",
			"seatNumber": "int",
			"seatInfo": 
			{
				"rowName" : "string",
				"colName" : "string",
				"zoneName" : "string"
			},
			"price": "decimal",
			
		}
	],
	"ticketNumbers": "string"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
RefundId|Refund id
CompanyId|Company id
RefundedMoney|Refunded money
RefundedUserCash|Refunded user cash money
RefundMethod|Refund method code. Always 'ExternalApi' (RefundMethod = 7)
RefundType|Refund type code. Always 'Order' (RefundType = 2)
Tickets|Ticket list
Tickets[i].TicketTypeId|TicketType id
Tickets[i].SeatNumber|Ticket seat number
Tickets[i].SeatInfo|Ticket seat info
Tickets[i].SeatInfo.RowName|Ticket seat row name
Tickets[i].SeatInfo.ColName|Ticket seat column name
Tickets[i].SeatInfo.ZoneName|Ticket seat zone name
Tickets[i].Price|Ticket price
Tickets[i].Number|Ticket number
TicketNumbers|Numbers of ticket sepparated by commas

<aside class="notice">
This operation require authentication
</aside>

## /v1/orders/{id}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/orders/{id}
````

````http
GET https://api.radario.ru/v1/orders/{id} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/orders/{id}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/orders/{id}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/orders/{id}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/orders/{id}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/orders/{id}");
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
````

`GET /v1/orders/{id}`

Get order by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|Order id


> Response model

````json
{
  "success": "bool",
  "data": { 
	"id": "int",
	"isPaid": "bool",
	"eventId": "int",
	"creationDate": "datetime",
	"ticketCount": "int",
	"baseAmount": "double",
	"amount": "double",
	"tickets": [
	{
		"id": "int",
		"ticketTypeId": "int",
		"userOrderId": "int",
		"ticketTypeTitle": "string",
		"ticketTypeZoneId": "int",
		"number": "string",
		"price": "double",
		"discount": "double",
		"isUsed": "bool",
		"barcodeKey": "string",
		"seatNumber": "string",
		"seatName": "string",
		"rowName": "string",
		"participantName": "string",
		"seatInfo": "string"
	}],
	"orderNumber": "string",
	"distributionType": "string",
	"paymentType": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK
### Attributes

Attribute|Description
---|---|---|
id|Order id
isPaid|Indicate if order is paid
eventId|Order event id
creationDate|Order creation datetime
ticketCount|Order ticket amount
baseAmount|Summarу tickets price
amount|Order amount (with considering debit from user cash)
orderNumber|Order number
distributionType|Order DistributionType
paymentType|Order PaymentType
tickets|List of tickets
tickets[i].id|Ticket id
tickets[i].ticketTypeId|TicketType id
tickets[i].userOrderId|UserOrder id
tickets[i].ticketTypeTitle|TicketType title
tickets[i].ticketTypeZoneId|TicketType zone id
tickets[i].number|Ticket number
tickets[i].price|Ticket price
tickets[i].discount|Ticket discount
tickets[i].isUsed|Indicate if ticket is used
tickets[i].barcodeKey|Ticket barcode key
tickets[i].seatNumber|Ticket seat number
tickets[i].seatName|Ticket seat name
tickets[i].rowName|Ticket row name
tickets[i].participantName|Ticket participant name
tickets[i].seatInfo|Ticket customer name


<aside class="notice">
This operation require authentication
</aside>

## /host/orders/{orderId}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/host/orders/{orderId}
````

````http
GET https://api.radario.ru/host/orders/{orderId} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/host/orders/{orderId}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/host/orders/{orderId}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/host/orders/{orderId}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/host/orders/{orderId}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/host/orders/{orderId}");
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
````

`GET /host/orders/{orderId}`

Get order complex info by id. Get only orders that created for host current account belongs to.

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
orderId|path|integer|true|Order id


> Response model

````json
{
  "success": "bool",
  "data": {
		"order": {
			"id": "int",
			"paymentType": "string",
			"paymentDate": "datetime",
			"amount": "decimal",
			"promoCode": "string",
			"psOrderId": "string"
		},
		"user": {
			"email": "string"
		},
		"event": {
			"id": "int",
			"title": "string"
		},
		"partnerTrack": {
			"id": "int",
			"email": "string"
		},
		"tickets": [
			{
				"id": "int",
				"barcode": "string",
				"participantName": "string",
				"price": "decimal",
				"discount": "decimal",
				"type": {
					"id": "int",
					"title": "string",
					"zoneId": "int"
				}
			}
		]
	},
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Order id
paymentType|Payment type (always 'External')
paymentDate|Payment datetime
amount|Order amount
promoCode|Order promo code
psOrderId|External payment system payment id
user|Customer info
user.Email|Customer email
event|Event info
event.Id|Event id
event.Title|Event title
partnerTrack|Partner info
partnerTrack.Id|Partner id
partnerTrack.Email|Partner email
tickets|List of tickets info
tickets[i].Id|Ticket id|Category
tickets[i].Barcode|Ticket barcode
tickets[i].ParticipantName|Ticket participant name
tickets[i].Price|Ticket price
tickets[i].Discount|Ticket price discount
tickets[i].Type|Ticket TicketType info
tickets[i].Type.Id|TicketType id
tickets[i].Type.Title|TicketType title
tickets[i].Type.ZoneId|TicketType zone id

<aside class="notice">
This operation require authentication
</aside>

## /host/orders

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/host/orders
````

````http
GET https://api.radario.ru/host/orders HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/host/orders',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/host/orders', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/host/orders', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/host/orders', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/host/orders");
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
````

`GET /host/orders`
Get current account host orders complex info.

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
startDate|query|string|true|Payment date (from)
endDate|query|string|true|Payment date (to)
eventId|query|string|false|Event id


> Response model

````json
{
  "success": "bool",
  "data": {
		"orders": [
			{
				"order": {
					"id": "int",
					"paymentType": "string",
					"paymentDate": "datetime",
					"amount": "decimal",
					"promoCode": "string",
					"psOrderId": "string"
				},
				"user": {
					"email": "string"
				},
				"event": {
					"id": "int",
					"title": "string"
				},
				"partnerTrack": {
					"id": "int",
					"email": "string"
				},
				"tickets": [
					{
						"id": "int",
						"barcode": "string",
						"participantName": "string",
						"price": "decimal",
						"discount": "decimal",
						"type": {
							"id": "int",
							"title": "string",
							"zoneId": "int"
						}
					}
				]
			}
		]
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Order id
paymentType|Payment type (always 'External')
paymentDate|Payment datetime
amount|Order amount
promoCode|Order promo code
psOrderId|External payment system payment id
user|Customer info
user.Email|Customer email
event|Event info
event.Id|Event id
event.Title|Event title
partnerTrack|Partner info
partnerTrack.Id|Partner id
partnerTrack.Email|Partner email
tickets|List of tickets info
tickets[i].Id|Ticket id|Category
tickets[i].Barcode|Ticket barcode
tickets[i].ParticipantName|Ticket participant name
tickets[i].Price|Ticket price
tickets[i].Discount|Ticket price discount
tickets[i].Type|Ticket TicketType info
tickets[i].Type.Id|TicketType id
tickets[i].Type.Title|TicketType title
tickets[i].Type.ZoneId|TicketType zone id

<aside class="notice">
This operation require authentication
</aside>

# Tickets

## /v1/tickets/{ticketId}/pdf

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ruv1/tickets/{ticketId}/pdf
````

````http
GET https://api.radario.ru/v1/tickets/{ticketId}/pdf HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/tickets/{ticketId}/pdf',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/tickets/{ticketId}/pdf', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/tickets/{ticketId}/pdf', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/tickets/{ticketId}/pdf', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/tickets/{ticketId}/pdf");
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
````

`GET /v1/tickets/{ticketId}/pdf`

Get ticket in pdf format

### Responses

Returns pdf file

<aside class="notice">
This operation require authentication
</aside>

# Places

## /v1/places

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/places
````

````http
GET https://api.radario.ru/v1/places HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/places',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/places', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/places', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/places', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/places");
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
````

`GET /v1/places`

Get events places

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
cityId|query|integer|true|City id
onlyWithActualEvents|query|bool|false|Retrieve places that refers to actual event if parameter has 'true'
limit|query|integer|false|Specifies the number of items to return (default 30)
offset|query|integer|false|Specifies the number of items to skip


> Response model

````json
{
  "success": "bool",
  "data": {
	"items": [
	{
		"id": "int",
		"title": "string",
		"address": "string",
		"latitude": "double",
		"longitude": "double",
		"cityId": "int",
		"cityName": "string"
	}
	],
	"totalCount": "int"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Place id
title|Place title
address|Place address
latitude|Place latitude
longitude|Place longitude
cityId|Place city id
cityName|Place city name

## /v1/places/{id}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/places/{id}
````

````http
GET https://api.radario.ru/v1/places/{id} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/places/{id}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/places/{id}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/places/{id}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/places/{id}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/places/{id}");
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
````

`GET /v1/places/{id}`

Get event place by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|Place id


> Response model

````json
{
  "success": "bool",
  "data": {
		"id": "int",
		"title": "string",
		"address": "string",
		"latitude": "double",
		"longitude": "double",
		"cityId": "int",
		"cityName": "string"
	}
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

### Attributes

Attribute|Description
---|---|---|
id|Place id
title|Place title
address|Place address
latitude|Place latitude
longitude|Place longitude
cityId|Place city id
cityName|Place city name

# Promocodes

## /v1/promocodes

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/promocodes
````

````http
GET https://api.radario.ru/v1/promocodes HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/promocodes',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/promocodes', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/promocodes', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/promocodes', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/promocodes");
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
````

`GET /v1/promocodes`

Get Promocode

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
code|query|string|true|Promocode code
companyId|query|integer|true|Company id


> Response model

````json
{
  "success": "bool",
  "data": {
	"value": "double",
	"currency": "string",
	"isPercent": "bool",
	"validUntil": "datetime",
	"eventTitle": "string"
  },
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK
### Attributes

Attribute|Description
---|---|---|
value|Discount value (in percent or not)
currency|Currency
isPercent|Indicate if discount value is in percentage terms
validUntil|Indicate discount expiration datetime
eventTitle|Event title

<aside class="notice">
This operation require authentication
</aside>

# Schemes

## /v1/schemes/{id}

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/schemes/{id}
````

````http
GET https://api.radario.ru/v1/schemes/{id} HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````html
<script>
  $.ajax({
    url: 'https://api.radario.ru/v1/schemes/{id}',
    method: 'get',
    success: function(data) {
      console.log(JSON.stringify(data));
    }
  })
</script>
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/schemes/{id}', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

````ruby
require 'rest-client'
require 'json'

result = RestClient.get 'https://api.radario.ru/v1/schemes/{id}', params:
  {
    # TODO
  }

p JSON.parse(result)
````

````python
import requests

r = requests.get('https://api.radario.ru/v1/schemes/{id}', params={
  # TODO
})

print r.json()
````

````java
URL obj = new URL("https://api.radario.ru/v1/schemes/{id}");
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
````

`GET /v1/schemes/{id}`

Get place schema by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|Place schema id


> Response model

````json
{
  "success": "bool",
  "data": {
			"id": "int",
			"name": "string",
			"seatCount": "int",
			"zones": [
				{
					"id": "int",
					"name": "string",
					"withSeats": "bool",
					"rowCount": "int",
					"colCount": "int",
					"seats": [
						{
							"number": "int",
							"rowName": "string",
							"seatName": "string",
							"exists": "bool"
						}
					]
				}
			],
			"image": "string",
			"version": "int"
	}
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

Attribute|Description
---|---|---|
id|Place schema id
name|Place schema name
seatCount|Seats amount
zones|List of zone
zones[i].Id|Zone id
zones[i].Name|Zone name
zones[i].WithSeats|Indicate if zone with seat
zones[i].RowCount|Amount of rows in the zone
zones[i].ColCount|Amount of columns in the zone
zones[i].Seats|List of zone seats
zones[i].Seats[j].Number|Seat number
zones[i].Seats[j].RowName|Seat row name
zones[i].Seats[j].RowName|Seat name
zones[i].Seats[j].Exists|Indicate if seat is exist on grid
version|Scheme rendering method Enum (Html = 1; Svg = 2)

## /v1/schemes/{id}/raw

> Code samples

````shell
# You can also use wget
curl -X get https://api.radario.ru/v1/schemes/{id}/raw
````

````http
GET https://api.radario.ru/v1/schemes/{id}/raw HTTP/1.1
Host: api.radario.ru
Content-Type: application/json
Accept: application/json
````

````javascript
const request = require('node-fetch');
fetch('https://api.radario.ru/v1/schemes/{id}/raw', { method: 'GET'})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});
````

`GET /v1/schemes/{id}/raw`

Get place schema raw descriptor by id

### Parameters

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|integer|true|Place schema id


> Response model

````json
{
  "success": "bool",
  "data": {
			"id": "int",
			"descriptor": "string",
			"version": "int"
	}
  "error": {
    "errorCode": "int",
    "message": "string"
  }
}
````
### Responses

Status|Meaning|Description
---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK

Attribute|Description
---|---|---|
id|Place schema id
descriptor|Raw place schema descriptor
version|Scheme rendering method Enum (Html = 1; Svg = 2)
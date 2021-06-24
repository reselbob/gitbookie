# Airport Codes Lookup API

## Airport Codes Lookup API

A super great RESTful API that allows developers to lookup the codes for all the major international airports. Also, the API allows adminstrators to add a new airport code as needed.

Version: 0.0.9

BasePath:/breselman/GoodAirportCodes/0.0.9

Apache 2.0

http://www.apache.org/licenses/LICENSE-2.0.html

### Access

### Methods

#### Table of Contents

**Admins**

* [`post /airportCodes`]()

**Developers**

* [`get /airportCodes/{code}`]()
* [`get /airportCodes`]()

## Admins

adds a new Airport Code to the resource \(setAirportCode\)

Adds an new aiport code to the resource

#### Consumes

 This API call consumes the following media types via the request header:

* `application/json`

#### Request body

Body Parameter — The airport code to add

#### Return type

#### Example data

Content-Type: application/json

```text
{
  "code" : "LAX",
  "airport" : "Mock of Los Angeles International Aiport"
}
```

#### Produces

 This API call produces the following media types according to the request header; the media type will be conveyed by the response header.

* `application/json`

#### Responses

**200**

 Returns the newly created airport code [AirportCode]()

**400**

 bad input parameter [AirportCodeInputError]()

## Developers

 [Up]()

```text
get /airportCodes/{code}
```

gets a particular airport code \(getAirportCode\)

Gets airport information that corresponds to the submitted aiport code.

#### Path parameters

code \(required\)

Path Parameter — The airport code to lookup

#### Return type

#### Example data

Content-Type: application/json

```text
{
  "code" : "LAX",
  "airport" : "Mock of Los Angeles International Aiport"
}
```

#### Produces

 This API call produces the following media types according to the request header; the media type will be conveyed by the response header.

* `application/json`

#### Responses

**200**

 the result that corresponds to the submitted airport code [AirportCode]()

**400**

 bad input parameter [AirportCodeInputError]()

gets all airport codes that corresponds to the search term \(searchAirportCodes\)

Gets airport information that corresponds to the submitted search term. If no search term is provides, all codes are returned

#### Query parameters

searchterm \(optional\)

Query Parameter — search term to process

#### Return type

#### Example data

Content-Type: application/json

```text
""
```

#### Produces

 This API call produces the following media types according to the request header; the media type will be conveyed by the response header.

* `application/json`

#### Responses

**200**

 the result that corresponds to the submitted search term [AirportCodes]()

**400**

 bad request [AirportCodeInputError]()

### Models

 \[ Jump to Methods \]

#### Table of Contents

1. [`AirportCode` -]()
2. [`AirportCodeInputError` -]()
3. [`AirportCodes` -]()

#### [`AirportCode` -]() [Up]()

airport

example: Mock of Los Angeles International Airport

code

example: LAX


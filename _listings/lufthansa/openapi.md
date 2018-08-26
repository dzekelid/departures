---
swagger: "2.0"
x-collection-name: Lufthansa
x-complete: 1
info:
  title: LH Public
  version: "1.0"
host: api.lufthansa.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /operations/flightstatus/departures/{airportCode}/{fromDateTime}:
    get:
      summary: Flight Status at Departure Airport
      description: Status of all departures from a given airport up to 4 hours from
        the provided date time.
      operationId: OperationsFlightstatusDeparturesByAirportCodeAndFromDateTimeGet
      x-api-path-slug: operationsflightstatusdeparturesairportcodefromdatetime-get
      parameters:
      - in: header
        name: Accept
        description: 'http header: application/json or application/xml (Acceptable
          values are: application/json, application/xml)'
      - in: path
        name: airportCode
        description: Departure airport
      - in: path
        name: fromDateTime
        description: Start of time range in local time of departure airport (YYYY-MM-DDTHH:mm)
      - in: query
        name: limit
        description: Number of records returned per request
      - in: query
        name: offset
        description: Number of records skipped
      responses:
        200:
          description: OK
      tags:
      - Operations
      - Flightstatus
      - Departures
      - AirportCode
      - FromDateTime
---
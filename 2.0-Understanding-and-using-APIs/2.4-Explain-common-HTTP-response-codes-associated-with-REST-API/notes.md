<!-- cSpell:ignore  -->

# Common HTTP Response Codes

## Overview

* Rest API responses are broken down into three components:
    * HTTP Status
    * Header
    * Body

## HTTP status

 * HTTP status codes are always three digits long, the first digit belongs to a category and the last is arbitrary
 * A full list of status codes can be found [here](https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml)
 * HTTP status codes are broken down into five categories
    * 1xx -- Informational
        * Server received request but is still processing it
        * Client should expect a full response, but at a later time
        * Typically do not contain a body
    * 2xx -- Success
        * Server received and accepted the request
        * Synchronous APIs contain requested data in body (if required)
        * Asynchronous APIs responses do not contain body
            * 2xx code is typically just confirmation of the request in this case
    * 3xx -- Redirection
        * The client has another action to take before the request can be completed
        * Typically a different URL needs to be used
        * This is either a manual or automatic action, depending on how the REST API is written
    * 4xx -- Client Error
        * Error on the client side, such as syntax which means request cannot be completed
        * This needs to be resolved before resending the request
    * 5xx -- Server Error
        * Request is in theory 'valid', but the server cannot process it.
        * Client needs to request again/at another time
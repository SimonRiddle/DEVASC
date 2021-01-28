<!-- cSpell:ignore  spikey, DDOS,-->

# Identifying the constraints when using APIs

## Rate limiting

### Overview

* Used to mitigate against DDOS attacks etc
* Common status codes are 429 (Too many requests) and 403 (Forbidden)

### Algorithms

#### Leaky bucket

* FIFO queue
* Incoming requests can come in at any rate, but always processed at a fixed rate
* Common to have delay here, especially if your traffic is generally pretty spikey.

#### Token bucket

* Each user is given a token
* Amount of data tokens which can be used is incremented with time
* Buckets must have at least one token, every request means a token is used up
* If no tokens are in the bucket, requests are rejected

#### Fixed window counter

* Uses a counter which cannot be accumulated like the token bucket
* Fixed window is given - of time
* All requests made over the limit within a given window are rejected
* Client should use a retry algorithm to retry once the next window begins

#### Sliding window counter

* Fixed number of requests within a duration of time
* Not a fixed window, the timestamp of first request is stored on the server
* Clients should design a way to delay requests so they do not exceed allowed rate
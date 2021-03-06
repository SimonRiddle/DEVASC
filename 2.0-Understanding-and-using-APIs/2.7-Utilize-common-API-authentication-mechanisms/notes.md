<!-- cSpell:ignore  -->

# Utilize common API authentication methods

## Basic authentication

* Uses basic HTTP authentication scheme
* Username/password separated by a colon and encoded using Base64.
    * Encoded *not* encrypted!
* Provided in the HTTP header
* Considered simple, but insecure unless HTTPS is used (rather than HTTP)

```bash
Authorization basic <username>:<password>
```

## Bearer (token) authentication

* Token authentication, using Bearer HTTP authentication
* Utilizes OAuth and Single Sign-On (SSO)
* Provided in the HTTP header
* This should also really be HTTPS to enforce encryption

```bash
Authorization: Bearer <bearer token>
```

## API key

* Often referred to as an API token
* Typically cannot be regenerated
* Unique alphanumeric string, generated by the server and assigned to a user
    * All requests from said user, require the API key
* Only secure when using HTTPS
* Typically, API keys do not expire, just revoked/regenerated should it be lost or stolen.
* Authentication provided in the HTTP header, body data or in cookies

### API key types

* Public API key
    * Can be shared
    * Permits access to a subset of data/APIs
* Private API key
    * Must *not* be shared
    * Similar to your username and password

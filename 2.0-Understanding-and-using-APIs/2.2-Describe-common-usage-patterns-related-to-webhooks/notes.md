<!-- cSpell:ignore  -->

# Webhooks usage patterns

* Allow applications to get real time data.
* Webhooks are triggered by events or activities
* More efficient as you no long need to poll something
* Common referred to as reverse APIs
* Applications 'subscribe' to a webhook server via a webhook provider
    * Provider provides URI which is usually an API of the application required

## Webhooks requirements

* Application must be able to receive HTTP POST requests
* Application must register URI to webhook provider
* Application must be able to handle incoming notifications from webhook server
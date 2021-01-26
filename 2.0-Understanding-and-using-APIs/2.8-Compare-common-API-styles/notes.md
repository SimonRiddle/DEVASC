<!-- cSpell:ignore Fagan -->

# Compare Common API Styles

## Synchronous APIs

* Synchronous pace, first come first serve basis

### Synchronous APIs - Benefits

* Typically very fast, if designed correctly.
    * However, this can cause delays in applications if designed incorrectly as he application will need to wait for a response.

### Synchronous APIs - Client-side processing

* Applications must wait for a response before moving onto the next bit of code

## Asynchronous APIs

* Response does not contain any data
* Server process request, sends notification or triggers with the data, after request is processed.
* Usually designed in this type if the data isn't readily available and takes some time to respond
    * If the server has to go to a remote service to fetch data etc
* Even though they are typically slower, responses can be immediate, but just aren't guaranteed like synchronous are.

### Asynchronous APIs - Benefits

* Asynchronous APIs allow the application to continue to execute the code, without having to wait for a response

### Asynchronous APIs - Client-side processing

* Design dependant, but clients can establish a listener and await a callback mechanism for when the notifications are sent back.
    * This may require queuing of data
* Some designs require clients to poll the server for check in on the status of the request
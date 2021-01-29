<!-- cSpell:ignore  -->

# HTTP & API troubleshooting

## Client side error

* User error
    * URI correct?
        * Use Python requests library to verify
    * URL correct?
        * Use Python requests library to verify
    * Has this ever worked?
* Connectivity issue
    * Proxy, firewall or VPN issues?
    * SSL error?
* HTTP 4xx response

## Server side error

* Physical server issues
    * Is the power off?
    * Cabling issues?
* Changes
    * Has the domain name/URI changed?
    * Any recent changes?
* Is the network down?
* HTTP 5xx response
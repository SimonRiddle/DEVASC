<!-- cSpell:ignore  OWASP,CSRF,-->

# Identify application security issues related to secret protection, encryption

## Storage

* Storing too much data
    * Do you really *need* to store all the data you're storing?
    * Rather than storing credit card information - just store the authorization code
* Storing data on the cloud
    * Although the vendors will say your data is secure - you do not own the server, so ensure it's encrypted.
    * Employees of the cloud storage provider may have access to you data, so encrypt it
* Physical medium
    * No matter if data is stored on SSD or HDD it needs to be encrypted
    * It is hard to wipe SSD entirely, so ensure you encrypt where required

## Transport

* Mitigate against man-in-the-middle (MiTM attacks)
* Encrypt data in transit using
    * SSH
        * Used for connecting to servers or network devices
    * TLS
        * Used when browsing to web-sites via a browser
        * https:// vs http://
    * VPN
        * Used to protect traffic throughout a network using an overlay
        * Data inside a VPN *can* be encrypted when paired with IPSec
        * Integrity checks built in, so any data which is tampered or read in transit is seen and dealt with

## Data handling

* One-way encryption
    * Generate encrypted value, without said value you cannot un-encrypt it
    * This is good for data which should not be accessed once inputted into a database
        * Think passwords etc
* Two-way encryption
    * Data is encrypted with a key, the key is used to see that data in clear text format
    * This is needed if you need to access the original data
        * Think security numbers, medical records etc
<!-- cSpell:ignore  -->

# Compare data formats (XML, JSON & YAML)

## XML

### Overview

* XML body - the content of the document, excluding the first line (ignoring any comments)
* Typical data structure with < > to open and </ > to close
* Tags are user defined
    * Best practice to use something which can have hierarchy enforced and human readable
* Document is always surrounded by outer-most tag (root tag pair)
* Tree like structure, branches coming off of the root
    * Leaf nodes contain the data itself

### Special characters

* Special characters can be used using HTML entity encoding
    * Often not supported by the APIs that you interact against
    * Surround characters in [CDATA] blocks

### Prologue

* First line of any XML document
* Always begins/ends with <? and ?> respectively
* This is what is read by parsers when your data is being used, it's important to get this right

### Comments

* Can be placed anywhere in the document
* This is an example of how to insert a comment (minus the space)s< !-- -->

### Example

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!-- Instance list -->
<vms>
  <vm>
    <vmid>0101af9811012</vmid>
    <type>t1.nano</type>
  </vm>
  <vm>
    <vmid>0102bg8908023</vmid>
    <type>t1.micro</type>
  </vm>
</vms>
```

## JSON

### Overview

* JavaScript Object Notation
* Files are in .json file types
* Items are put in *key:value* pairs
* No support for comments in data
* Whitespace is insignificant in JSON data

### Data types

* Numbers, strings, Booleans, nulls

### Maps & lists

* Items in their key/value pairs can have lists, like Python directories
* The entire value needs to be surrounded in square brackets, value separated by commas

### Example

```JSON
{
  "edit-config":
  {
    "default-operation": "merge",
    "test-operation": "set",
    "some-integers": [2,3,5,7,9],
    "a-boolean": true,
    "more-numbers": [2.25E+2,-1.0735],
  }
}
```

## YAML

### Overview

* Stands for "YAML Ain't Markup Language"
* Superset of JSON, even easier human readability
* Used by a lot of configuration automation systems, Ansible etc
* YAML parses JSON but not visa versa
* Key: value pairs, separated by a colon

### File structure

* Opens with three dashes ---
* Close with three dots ...
* Multiple documents in a single file is supported, separate each with three dashes.

### File structure & indentation

* Enforces hierarchy using indentation
* Best practice is to use two spaces per indent level
    * This is arbitrary, but keep is consistent!

### Data types

* Numbers, strings, Booleans and nulls supported

### Comments

* Can be inserted anywhere
* Uses a # to start the comment

### Example

```YAML
---
edit-config:
  a-boolean: true
  default-operation: merge
  more-numbers:
  - 225.0
  - -1.0735
  some-integers:
  - 2
  - 3
  - 5
  - 7
  - 9
  test-operation: set
...
```
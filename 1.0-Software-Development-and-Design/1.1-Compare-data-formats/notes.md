<!-- cSpell:ignore  -->

# Compare data formats (XML, JSON & YAML)

## Data formats

### XML

#### Overview

* XML body - the content of the document, excluding the first line (ignoring any comments)
* Typical data structure with < > to open and </ > to close
* Tags are user defined
    * Best practice to use something which can have hierarchy enforced and human readable
* Document is always surrounded by outer-most tag (root tag pair)
* Tree like structure, branches coming off of the root
    * Leaf nodes contain the data itself

#### Special characters

* Special characters can be used using HTML entity encoding
    * Often not supported by the APIs that you interact against
    * Surround characters in [CDATA] blocks

#### Prologue

* First line of any XML document
* Always begins/ends with <? and ?> respectively
* This is what is read by parsers when your data is being used, it's important to get this right

#### Comments

* Can be placed anywhere in the document
* This is an example of how to insert a comment (minus the space)s< !-- -->

#### Example

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


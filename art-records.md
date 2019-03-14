# Art Records RDAP Extension

.ART domain names may have additional data elements describing Art Record information; this information is managed by registrars using the [EPP Art Record extension](https://gitlab.centralnic.com/centralnic/epp-artrecord-extension/blob/master/draft-brown-artRecord.txt).

## Conventions Used in This Document

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC2119](https://tools.ietf.org/html/rfc2119).

## RDAP Extension Identifier

This extension uses the RDAP extension identifier `artRecord` in accordance with Section 2.1 of [RFC7483](https://tools.ietf.org/html/rfc7483). The registration for the identifier can be found below in accordance with Section 8.1 of [RFC7480](https://tools.ietf.org/html/rfc7480).

## RDAP Conformance

RDAP servers which implement this extension MUST insert `artRecord_level_0` into the `rdapConformance` array in RDAP responses.

## Art Records

This extension defines a new JSON data structure for RDAP: an array of objects, where each object represents an Art Record data element.

	"artRecord_record": [
	  {
	    "title": "objectType",
	    "name": "Type of Object",
	    "value": "a moving-image"
	  },
	  {
	    "title": "materialsAndTechniques",
	    "name": "Materials & Techniques",
	    "value": "digitally processed film shot on camera"
	  },
	  {
	    "title": "dimensions",
	    "name": "Measurements",
	    "value": "1920x1080 px"
	  },
	  {
	    "title": "title",
	    "name": "Title",
	    "value": "John Doe"
	  },
	  {
	    "title": "dateOrPeriod",
	    "name": "Date or Period",
	    "value": "2018"
	  },
	  {
	    "title": "maker",
	    "name": "Maker",
	    "value": "Jane Doe"
	  }
	]

## Art Record Data Elements

Each data element is a JSON object containing the following values:

* `title` - the human-readable description of the data element
* `name` - the name of the data element
* `value` - the value of the data element

As of writing, the semantics of these data elements are not defined.

## IANA Registration

The information below will be registered with the IANA according to section 8.1 of [RFC7480](https://tools.ietf.org/html/rfc7480).

```
Extension identifier: artRecord

Registry operator: .ART

Published specification: this document

Person and email address to contact for further information: rdap@centralnic.com

Intended usage: common
```

# Copyright

Copyright 2019 CentralNic Ltd. All Rights Reserved.

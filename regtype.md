# Registration Type RDAP Extension

The .FEEDBACK top-level domain recognises to types of domains; "standard" domains and "hosted" domains, which are delegated to the nameservers of the registry operator. Registrars can indicate the "type" of a .FEEDBACK domain using the [EPP Registration Type Extension](https://gitlab.centralnic.com/centralnic/epp-registration-type-extension/blob/master/draft-brown-regtype.txt).

## Conventions Used in This Document

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC2119](https://tools.ietf.org/html/rfc2119).

## RDAP Extension Identifier

This extension uses the RDAP extension identifier `regType` in accordance with Section 2.1 of [RFC7483](https://tools.ietf.org/html/rfc7483). The registration for the identifier can be found below in accordance with Section 8.1 of [RFC7480](https://tools.ietf.org/html/rfc7480).

## RDAP Conformance

RDAP servers which implement this extension MUST insert `regType_level_0` into the `rdapConformance` array in RDAP responses.

## Registration Types

This extension defines a new property for domain objects, named `regType`, whose value is a string which indicates the registration type of the domain:

	"regType_regType": "standard"

The semantics of this value are server-specific and not currently defined.

## IANA Registration


```
Extension identifier: regType

Registry operator: CentralNic

Published specification: this document

Person and email address to contact for further information: rdap@centralnic.com

Intended usage: common
```

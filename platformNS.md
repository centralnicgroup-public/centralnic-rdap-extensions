# Platform Nameservers RDAP Extension

.FEEBACK domains which have the "hosted" registration type (see above) have an additional set of "platform" nameservers to which the domain is delegated; these nameservers handle DNS queries for the domains, answering some queries directly, and forwarding some queries to the domain's configured nameservers.

## Conventions Used in This Document

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC2119](https://tools.ietf.org/html/rfc2119).

## RDAP Extension Identifier

This extension uses the RDAP extension identifier `platformNS` in accordance with Section 2.1 of [RFC7483](https://tools.ietf.org/html/rfc7483). The registration for the identifier can be found below in accordance with Section 8.1 of [RFC7480](https://tools.ietf.org/html/rfc7480).

## RDAP Conformance

RDAP servers which implement this extension MUST insert `platformNS_level_0` into the `rdapConformance` array in RDAP responses.

## Platform Nameservers

This extension defines a new property for domain objects, named `platformNS_nameservers`, which is an array containing the platform nameservers for the domain:

	"platformNS_nameservers": [
		{
			"objectClassName":"nameserver",
			"ldhName":"ns1.example.com",
		},
		{
			"objectClassName":"nameserver",
			"ldhName":"ns2.example.net",
		}
	]

The members of the array are nameserver objects.

## IANA Registration


```
Extension identifier: platformNS

Registry operator: CentralNic

Published specification: this document

Person and email address to contact for further information: rdap@centralnic.com

Intended usage: common
```

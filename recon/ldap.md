# Lightweight Directory Access Protocol (LDAP)

## What is LDAP?

### Basics of LDAP
- Many organizations store information relating to users, e.g. their names,
  locations, phone numbers, email addresses, etc.
- These lists of information are known as **directories**.
- LDAP is a protocol for reading and writing directories over an IP network.
- LDAP follows the **X.500 Standard** (the standard for storing directory
  information) written by the International Telecommunications Union (ITU).

### X.500 Distinguished Names
- X.500 distinguished names follows `attribute=value` pairs.
- Commonly used attributes:

|Attribute|Field|Usage|
|:--------|:----|:----|
|`CN`|Common name|Identifies the person or object.|
|`OU`|Organizational unit|A unit or department within the organization.|
|`O`|Organization|The name of the organization.|
|`L`|Locality|Usually a city or area.|
|`ST`|State|A state, province, or county within a country.|
|`C`|Country|The country's 2-character ISO code (e.g. US, GB).|
|`DC`|Domain component||

- X.500 builds a _tree_ of organization.

### LDAP user access and security

#### Simple Authentication and Security Layer (SASL) 
- Available in LDAPv3
- Three modes
    - **No authentication.** Anonymous access is allowed.
    - **Simple authentication.** Client provides DN and password.
    - **Simple authentication and security layer.** Client and server
      negotiate a security mechanism such as Kerberos or TLS.
- Usully two levels of access
    - Read-only
    - Read-write

#### LDAP over SSL (LDAPS)
- LDAP is transferred in cleartext.
- Active directory uses LDAPS on TCP port 636.

## Enumeration
- `ldapsearch -h <host> -x -s base namingcontexts`

## References
- Professor Messer, _LDAP and Secure LDAP; CompTIA Security+ SY0-401: 5.1_. ([youtube](https://www.youtube.com/watch?v=5rEA7vRV3VE))

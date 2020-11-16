# Service Message Block (SMB)

The SMB protocol enables _inter-process communication (IPC)_, allowing
applications and services on a network to communicate with each other.

Current versions of SMB run on TCP (pre-Windows 2000 version ran on NetBIOS).

Port 139 is the old NetBIOS port used by SMB. Port 445 is the TCP port used by
SMB. Using TCP also allows SMB to work over the internet.

## Different implementations of SMB

### CIFS
- CIFS is a specfic implementation of SMB that enables file sharing.

### Samba
- Samba is an open-source implementation of Active Directory that allows
  non-Windows machines to communicate with a Windows network.

## SMB Attacks
- NTLMv1/v2 relaying
  - Byte Bleeder:
  [original](https://byt3bl33d3r.github.io/practical-guide-to-ntlm-relaying-in-2017-aka-getting-a-foothold-in-under-5-minutes.html),
  [archive](http://archive.is/7sAPJ)
  - SANS:
  [original](https://www.sans.org/blog/smb-relay-demystified-and-ntlmv2-pwnage-with-python/),
  [archive](https://archive.is/BfQ8j)

## References

- Varonis, _What is an SMB Port + Ports 445 and 139 explained._
  ([original](https://www.varonis.com/blog/smb-port/),
  [archive](https://archive.is/lnbmM))



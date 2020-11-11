
## Covert infrastructure

### General
- Segregate all assets based on function
- Place a redirector in front of every asset
- Blend in with normal traffic for the target
- Configure assets so that individual pieces can be rolled
- Document _everything_

### Domains
- Always use **categorized domains**
- Using healthcare/finance categories can help prevent MITM sniffing
- Pick domains that match industry (i.e. what the users might browse)

### Payloads
- Types
    - HTA
    - LNK
    - Powershell
- Delivery method
    - Attachment
    - Download link
- Access control options
    - IP/fingerprint-based restrictions
    - Expiring payload links

### Payload redirection
- Dumb pipe
    - socat, iptables
- Filtering
    - Apache mod_rewrite, nginx

### C2
- Longhaul
    - Persistence
    - Slow checkins
    - Used for regaining access
- Shorthaul
    - Burned frequently
    - Used for primary operations
- Protocols
    - HTTPS
    - DNS
    - Domain-fronting
- Keep servers separate!

### SMTP
- Need to set up DKIM, SPF, and PTR
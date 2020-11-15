# General OPSEC

## Framework
1. List adversaries by **intent** and **capability**.
2. Examine what you are trying to protect
  - List your secrets
    - Identity
    - Clandestine activity
    - Association with the activity
  - Group them based on the negative impact it would have if they were leaked
3. Identify the phases of your operation.
  1. Target selection
    - Determine your strategic objectives.
  2. Planning and surveillance
  3. Deployment
  4. Execution
  5. Escape and evasion
4. Perform counterintelligence.

## Compartmentalization
- Use dedicated hardware and pseudononymous internet connection ("aircard").
- Compartmentalize each operation to avoid linking separate operations
  together. Don't forget to sanitize at the beginning and end of an operation.

## Secure Communications
- Goals
  1. Make the content unreadable. (cryptography)
  2. Make the meaning inaccessible. (codes)
  3. Avoid traffic analyisis; don't let others know a connection exists between the two parties.
  4. Avoid knowledge of the communication; don't let others know that two parties have a communication channel.
- Codes
  - Keep them generic; typically about a topic, rather than a phrase.
  - Keep them consistent.
  - Limit use to simple signalling.
- Email _is not_ a secure format to transmit sensitive data (especially at rest).

## Counterintelligence
- When planning an operation, know how the adversary will respond.  If you do
  not know how your adversary will respond, then their response will be a
  surprise.

## Other tips
- Security is only as strong as third-party vendors.
- Hackers mostly use social engineering techniques.
- Perform business process documentation and data loss prevention.
- Inventory your critical assets.
- Test business continuity planning/disaster recovery procedures (BCP/DR)
- Secure IoT devices (or don't have them).
- Assume all data on the Internet is public.
- Migrate communications infrastructure and change identities regularly.
- Don't keep logs.
- Avoid reducing the set of suspects.

## Digital trails
- Geolocation
- Patterns in activity

## References
- Overlooked aspects of OPSEC programs. ([original](https://digitalguardian.com/blog/overlooked-components-of-opsec-programs), [archive](https://archive.is/HXv1i))
- Erase memory, the memtest86+ way. ([original](https://tails.boum.org/blueprint/more_efficient_memory_wipe/memtest86plus/), [archive](https://archive.is/IIegO))
- A guide to digital OPSEC. ([archive](https://archive.is/CoJgs))

#### what is cap in linux ?
Normally, the root user (UID 0) has full system privileges, while normal users have very limited rights. 
Capabilities break down the all-powerful root privileges into smaller, specific units. This allows processes 
to have just the permissions they need instead of full root access.
#### Finding cap binaries set
- getcap -r / 2>/dev/null
- after finding the binaries we need to find the suspious one.
- suppose we find vim has capabilites is set then go to gtfobin website search for vim and took the capabilites payloads
#### Resources
- https://www.hackingarticles.in/linux-privilege-escalation-using-capabilities/
- https://www.youtube.com/watch?v=r34I-SPWHPA&list=PL-DxAN1jsRa818Ew7WI1_ngpULwDDESSI&index=6

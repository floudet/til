# 'grep' IOS output

`include` ('`i`') filters all lines that match the criteria. 

Example:
```
GFW-ASA01# sh run | i crypto
crypto ipsec ikev1 transform-set AES-256-SHA esp-aes-256 esp-sha-hmac
crypto ipsec security-association pmtu-aging infinite
crypto map IPSEC 5 match address VPN
crypto map IPSEC 5 set pfs
crypto map IPSEC 5 set peer 219.143.253.6
[...]
```

[Source](https://supportforums.cisco.com/t5/ip-telephony/grep-in-ios-output/td-p/2186041)

**Note:** The '`s`' or '`section`' option specified in the page above didn't work on a *Cisco ASA5515-K9*. 

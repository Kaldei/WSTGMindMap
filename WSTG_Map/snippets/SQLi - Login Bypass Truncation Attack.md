#sqli 

The attacks consist in impersonating a user by adding a new user (example admin), adding a lot of spaces to exceed max allowed number of characters, and then add a random character. Then connect with the user and the new password (database will truncate somewhere in the spaces and only use the part before the spaces).

Login:
```sql
admin                                                                                            a
```

Password:
```sql
myPassword
```
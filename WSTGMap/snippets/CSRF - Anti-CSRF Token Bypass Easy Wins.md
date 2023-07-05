#csrf

## Manual
- Try remove CSRF Token (token not verified if not present)
- Try GET instead of POST (token not verified with GET)
- Try submit CSRF of another user (token non tied to user sessions)

## Tool xsrfprobe
```py
pip3 install xsrfprobe
```

```py
xsrfprobe -u https://[TARGET_IP]/endpoint
```
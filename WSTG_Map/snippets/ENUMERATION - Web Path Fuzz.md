#web_path 

## Word Lists
- Fast: `/usr/share/wordlists/dirb/common.txt/`
- Fast: `/usr/share/seclists/Discovery/Web-Content/quickhits.txt`
- Medium: `/usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt/`
- Exhaustive: `/usr/share/wordlists/drib/big.txt/`

## Tools
#### DIRSEARCH
```bash
dirsearch -t 5 --max-rate=15 --proxy=127.0.0.1:[BURP_PORT] -w [WORDLIST] -u https://[TARGET_IP]
```

#### GOBUSTER
```bash
gobuster dir --proxy=127.0.0.1:[BURP_PORT] -u http://[TARGET_IP]:[TARGET_PORT] -w [WORDLIST]
```

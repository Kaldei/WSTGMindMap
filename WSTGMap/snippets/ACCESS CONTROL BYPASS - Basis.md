#access_control_bypass

## URL-based Access Control
- Try request / and ad non-standard HTTP Headers :  
	- X-Original-URL: /admin
	- X-Rewrite-URL: /admin

## Method-based Access Control
- Try to change the method: POST -> GET

## Referer-based Access Control
- Try `Referer: http://[TARGET_IP]/admin`
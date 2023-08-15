#password_reset 

## The application uses the `Host` header to create the reset link
1. Set up a listener (e.g. Burp Collaborator).
2. Reset password for user and intercept the request.
3. Change the `Host` header to the listener address: `Host: [ATTACKER_IP]`
4. The user will get an email with a link which should look like this: `https://[ATTACKER_IP]/reset?token=random_token`
5. Then go back to the website and go to `/reset?token=random_token`

## The application uses the `X-Forwarded-Host`header to create the reset link
1. Set up a listener (e.g. Burp Collaborator).
2. Reset password for user and intercept the request.
3. Change the `Host` header to the listener address: `X-Forwarded-Host: [ATTACKER_IP]`
4. The user will get an email with a link which should look like this: `https://[ATTACKER_IP]/reset?token=random_token`
5. Then go back to the website and go to `/reset?token=random_token`
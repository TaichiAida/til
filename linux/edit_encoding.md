# Encoding
There are some type of encoding,
* UTF-8
* EUC-JP
* Shift-JIS  
I want to use only UTF-8, but the file made by someone may be other one.  
Therefore, I learned how to check, and convert it.

## Check Encoding
This chapter shows that the way to check encoding of file.
I suggest to use *file* command like below,
```
$file (something).txt

// Output UTF-8|cp932(= Shift-JIS)|ISO-8859(= EUC-JP)
```

## Convert Encoding
Next, I will explain how to convert the type of encoding.
```
$ nkf -w --overwrite (something).txt

// You can get the file (encoding=UTF-8).
```
The arguments are below,
* -w: convert to UTF-8
* -e: convert to EUC-JP
* -s: convert to Shift-JIS
* --overwrite: overwriting directly


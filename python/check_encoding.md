# Detect a file encoding
last year, I learned how to check and change a file encoding in linux command **file** and **nkf**. [[link](https://github.com/a1da4/til/blob/master/linux/edit_encoding.md)]  
Today I learned that check a file encoding and read it by optimal encoding type in python.  

## Installation
First, install chardet by pip.
```
$pip install chardet
```

## Detect
Second, use **detect** module.
```
import chardet  

def detect_unicode(file_path):
    """
    :param file_path: path of file
    :return: dict[encoding, confidence, language]
    """
    with open(file_path, "rb") as f:
        chardet_dict = chardet.detect(f.read())

    return chardet_dict
```
*chardet_dict* contains:  
* encoding  
* confidence
* language

## Read file with optimal encoding type
Finally, use *chardet_dict* for reading the file.  
```
def read_file(file_path, chardet_dict):
    unicode = chardet_dict["encoding"]
    print(f"Encoding: {unicode}")
    with open(file_path, encoding=unicode) as f:
        f.read()
```


# Byte to str [[link](https://docs.python.org/ja/3/library/stdtypes.html#bytes)]
When I read the file(~.rpt.gz) using the code below, the type was 'byte'.  
```
with open(~.rpt.gz) as f:
  lines = f.readlines()
  print(type(lines[0]))
```

I wanted to read that file, so I refered above url.  

I often use ```str()``` to convert other types into str.  
```
int_ = 123
print(str(int_))

# output: '123'
```

But, ```str()``` has some arguments.  
```str(byte, encoding, error)```  
To decode byte into str, we have to use second arguments.  
```
byte2str = str(byte_, encoding='UTF-8')
print(type(byte2str))

# output: 'str'
```

Therefore, we can read ```byte()``` file as ```str()```  
```
with open(~.rpt.gz) as f:
  lines = f.readlines()
  for line in lines:
    print(str(line, encoding='UTF-8'))
```

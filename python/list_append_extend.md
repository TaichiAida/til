# The difference between *append* and *extend*
Today, I investigated words that exist in both files.  
However, I misused the method *append* and *extend*.  
The structure of the datasets like below,  
```
# File A|B
word1   count(word1)
word2   count(word2)
word3   count(word3)
...     ...

```
So I wrote the code to make the list of words in *fileA*,  
then, read *fileB* to compare the words in *fileB* and the list.
```
# compare_words_from_two_files.py

words_A = []
with open(fileA) as f:
    lines = f.readlines()
    for line in lines:
        line = line.split("\t")
        words_A.extend(line[0])

with open(fileB) as f:
    lines = f.readlines()
    for line in lines:
        line = line.split("\t")
        if line[0] in words_A:
            print(line[0])

# Outputted UNIGRAM of words...
```
That is terrible...  
Its problem was using *extend* method. 
To solve this, I have to use *append* method.  
The difference between *append* and *extend* is below,  
```
line = "apple   10"
line = line.split("\t")
# line: ["apple", "10"]

# extend
words_A.extend(line[0])
# words_A: ["a", "p", "p", "l", "e"]

# append
words_A.append(line[0])
# words_A: ["apple"]
```
As above, *extend* breaks the element and adds it to the list,  
*append* adds the element to the list as it is.  



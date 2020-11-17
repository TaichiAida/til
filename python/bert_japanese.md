# Japanese BERT
## Problem
I used pre-trained Japanese BERT model as follows  
```
from transformers import BertModel, BertTokenizer

model = BertModel.from_pretrained('cl-tohoku/bert-base-japanese', return_dict=True)
tokenizer = BertTokenizer.from_pretrained('cl-tohoku/bert-base-japanese')

sent = 'サッカーの試合を見る'
tokenized = tokenizer.tokenize(sent)
print(tokenized)
# Output: ['サッカー', '##の', '試', 合', 'を', '見', 'る']
```
In above case, a word '試合' means 'match' is separated.


## Solution
```
!pip install transformers["ja"]
```
```
from transformers import BertModel, BertJapaneseTokenizer

model = BertModel.from_pretrained('cl-tohoku/bert-base-japanese', return_dict=True)
tokenizer = BertJapaneseTokenizer.from_pretrained('cl-tohoku/bert-base-japanese')
sent = 'サッカーの試合を見る'
tokenized = tokenizer.tokenize(sent)
print(tokenized)
# Output: ['サッカー', 'の', '試合', 'を', '見る']
```

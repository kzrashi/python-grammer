# defaultdict

## 1. overview
- 辞書型の型を指定することが出来る

## 2. 引数

|型|説明
|:--|:--
|int |defaultdict(int)
|str |defaultdict(str)
|bool|defaultdict(bool)
|list|defaultdict(list)
|set |defaultdict(set) 


## 3. basic
### 3.1. NG例
```python title="python ソースコード"
hashmap = {}

hashmap["a"] = 1
hashmap["a"] += 1
hashmap["b"] += 1 ★
```

```python  title="python 出力結果"
  File "/Users/kaz/Work/python-sandbox/sample.py", line 418, in <module>
    hashmap["b"] += 1
KeyError: 'b'

```
### 3.2. OK例(defaultdict)

```python title="python ソースコード"
from collections import defaultdict

hashmap = defaultdict(int)
hashmap["a"] = 1
hashmap["a"] += 1
hashmap["b"] += 1 ★defaultdictでint型を指定しているためエラーにならない
print(hashmap)
```

```python  title="python 出力結果"
defaultdict(<class 'int'>, {'a': 2, 'b': 1})
```

## 4. reference
- [Python defaultdict の使い方](https://qiita.com/xza/items/72a1b07fcf64d1f4bdb7)
- [Learning about defaultdict in Python](https://www.educative.io/edpresso/learning-about-defaultdict-in-python)
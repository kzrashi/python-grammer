# 文字列型(str)関数


## 1. 検索系
### 1.1. in
- 文字(文字列)が存在するか判定する

```python
word = "abbcdefg"
print('ab' in word)
print('z' in word)
```
```python title="結果"
True
False
```

### 1.2. find
- 引数で指定した文字(文字列)を先頭から検索して最初に一致するインデックス位置を返す
存在しない場合、-1を返却する

```python
word = "abbcdefg"
print(word.find("b"))
print(word.find("cd"))
print(word.find("z"))
```
```python title="結果"
1
3
-1 
```
### 1.3. rfind
- 引数で指定した文字(文字列)を後ろから検索して最初に一致するインデックス位置を返す
- 存在しない場合、-1を返却する

```python
word = "abbcdefg"
print(word.rfind("b"))
```
```python title="結果"
2
```

### 1.4. startswith
- 引数に指定した文字列が先頭に一致するか判定する
- startsの**s**が入るのがポイント

```python
word = "abbcdefg"
print(word.startswith("abb"))
print(word.startswith("ac"))
```
```python title="結果"
True
False
```

### 1.5. endswith
- 引数に指定した文字列が最後尾に一致するか判定する
- endsの**s**が入るのがポイント

```python
word = "abbcdefg"
print(word.endswith("g"))
print(word.endswith("z"))
```
```python title="結果"
True
False
```

### 1.6. count
- 引数に指定した文字(文字列)の数を取得する関数

```python
word = "abbcdefg"
print(word.count("a"))
print(word.count("b"))
print(word.count("ab"))
```
```python title="結果"
1
2
1
```


## 2. 置換系
### 2.1. replace
- 1つ目の引数に一致する文字(文字列)を2つ目の引数に変換する
- findと異なり、**一致する全ての文字を変換する**ことに注意
- 元の変数は書き換わることがない

```python
word = "abbcdefg"
print(word.replace("b","z"))
print(word)
```
```python title="結果"
azzcdefg
abbcdefg
```


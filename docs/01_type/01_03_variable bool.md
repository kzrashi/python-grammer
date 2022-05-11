#  真偽型(bool)

## 1. basic
- 真(True) or 偽(False)のどちからの値を取る型
- Camel case(１文字目が大文字、２文字目以降が小文字)で記載することに注意

```python title="python ソースコード"
ソースコード
```python
# 変数の宣言
valid = True

# 変数の内容の表示
print(valid) 

# 変数の型の表示
print(type(valid)) 
``` 

```python  title="python 出力結果"
True
<class 'bool'>
```

## 2. True/Falseの入れ替え


```python title="python ソースコード"
valid = True
print(valid)

valid = not valid
print(valid)
```

```python  title="python 出力結果"
True
False
```


## 3. 注意点
```python title="python ソースコード"
valid = true
valid = TRUE
```

```python  title="python 出力結果"
    valid = true
NameError: name 'true' is not defined
    valid = TRUE
NameError: name 'TRUE' is not defined
```


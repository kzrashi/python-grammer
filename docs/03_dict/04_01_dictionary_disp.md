# 辞書 基本
- Key と Value で１対１でデータを取得することが出来る

- **{ Key : Value }**の形で宣言する  
  リストと異なり、{==**[ ]**ではないことに注意==}

- 参照はリストと同じ**変数名[Key 値]**でValue 値を参照することが出来る  
  (宣言以外は**[]**を使用することが多いことがポイント)

### 宣言

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}
```

### 辞書(Dictionary) 表示系
#### 一覧を表示
ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}

print(dict)
```

出力結果
```python
{'apple': 100, 'orange': 200, 0: 'xxx'}
```

#### KEY値に対応するvalueを表示
- **変数名[Key値]**でValue値を表示する

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}

print(dict["apple"])
```

出力結果
```python
dict_values([100, 200, 'xxx'])
```

#### Key 一覧を表示
- keys()を使用する

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}

print(dict.keys())
```

出力結果
```python
dict_keys(['apple', 'orange', 0])
```

#### Value 一覧を表示
- values()を使用する

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}

print(dict.values())
```

出力結果
```python
dict_values([100, 200, 'xxx'])
```

#### 辞書数を表示
- リストと同じくlen()を使用する

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}

print(len(dict))
```

出力結果
```python
3
```

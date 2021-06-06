# 辞書(Dictionary) 削除

#### 全要素削除
ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}
dict.clear()

print(dict)
```

出力結果
```python
{}
```

#### インデックス指定で削除

ソースコード
```python
# 辞書を作成
dict = {"apple": 100, "orange": 200, 0: "xxx"}

# "apple": 100を削除する
del dict["apple"]

# 表示
print(dict)
```

出力結果
```python
{'orange': 200, 0: 'xxx'}
```


#### インデックス指定で削除して値を取得する
ソースコード
```python
# 辞書を作成
dict = {"apple": 100, "orange": 200, 0: "xxx"}

# "apple": 100を削除してValue値の100を取得
delValue =  dict.pop("apple")

# 表示
print(dict)
print(delValue)
```

出力結果
```python
{'orange': 200, 0: 'xxx'}
100
```



# 辞書(Dictionary)  追加(更新)

#### Key未登録
- Keyが未登録の場合、新しく追加される

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}
dict["str"] = "mozi"

print(dict)
```

出力結果
```python
{'apple': 100, 'orange': 200, 0: 'xxx', 'str': 'mozi'}
```

#### Key登録済み
- Keyが登録済みの場合、Value値を更新する

ソースコード
```python
dict = {"apple": 100, "orange": 200, 0: "xxx"}
dict["apple"] = 500

print(dict)
```

出力結果
```python
{'apple': 500, 'orange': 200, 0: 'xxx'}
```

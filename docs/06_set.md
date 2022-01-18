# 集合(Set)

- 数学の集合のようなもの
- 一意にデータしか格納されない
- 格納される順番は順不同

## 1. 宣言
### 1.1. 空宣言
ソースコード
```python
# 宣言
set1 = set()

# 出力
print(set1)
print(type(set1))
```

出力結果
```python
set()
<class 'set'>
```

### 1.2. 文字列形式
文字列を文字単位で設定する
ソースコード
```python
# 宣言
set1 = set("abbcc")

# 出力
print(set1)
```

出力結果
```python
{'b', 'c', 'a'}
```

### 1.3. 　リスト形式
リスト形式で宣言＆設定する

ソースコード
```python
# 宣言
set1 = {"a","b","b","c","c"}

# 出力
print(set1)
```

出力結果
```python
{'a', 'b', 'c'}
```


## 2. 追加(add())
- add()関数を使用する

ソースコード
```python
# 宣言
set1 = set()

# 出力
print(set1)

# 追加
set1.add(3)

# 出力
print(set1)
```

出力結果
```python
set()
{3}
```


## 3. 削除

### 3.1. 要素指定で削除(discard())
- discard()関数を使用する
- 指定した要素を削除する
- 要素が存在しない場合は**何もしない**  

ソースコード
```python
# 宣言
set1 = {1,2,3}

# 出力
print(set1)

# 要素(1)を削除
set1.discard(1) # 対象の要素を削除する

# 出力
print(set1)

# 要素(4)を削除
# ※要素が登録されていない場合何もしない
set1.discard(4)

# 出力
print(set1)
```

出力結果
```python
{1, 2, 3}
{2, 3}
{2, 3}
```

### 3.2. ランダムに要素を取り出して削除する(pop())

ソースコード
```python
# 宣言
set1 = {1,2,3}

# 出力
print(set1)

# 削除
print(set1.pop())

# 出力
print(set1)

# 削除
print(set1.pop())

# 出力
print(set1)
```


## 4. 全削除(clear())
- clear()関数を使用する

ソースコード
```python
# 宣言
set1 = {1,2,3}

# 出力
print(set1)

# 全削除
set1.clear()

# 出力
print(set1)
```

出力結果
```
{1, 2, 3}
set()
```

## 集合⇔リスト変換
- list()関数、set()関数を使用することで相互変換が出来る

```python
#宣言
set1 = {1,2,3}

#出力
print(set1)

# 集合 -> リストへの変換
list1 = list(set1)

# 出力
print(list1)

# リスト -> 集合
set2 = set(list1)

# 出力
print(set2)
```

出力結果
```python
{1, 2, 3} # 集合
[1, 2, 3] # リスト
{1, 2, 3} # 集合
```


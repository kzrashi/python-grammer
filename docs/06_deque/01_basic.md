# deque

## 1. basic
- collectionsモジュール内にdequeクラスが提供されている
- エンキュー(enqueue)、デキュー(dequeue)の機能を提供している
- 先頭、末尾へのデータ追加・削除が`O(1)`で処理出来る(listは先頭の追加・削除では`O(N)`かかる)


## 2. example
- インスタンス宣言時に第一引数でデキューのタイプを指定する
- 第２引数でキューの最大サイズを指定する
- 末尾への追加は`pop()`メソッドで行う    ←★リストと同じ
- 末尾からの削除は`pop()`メソッドで行う  ←★リストと同じ
- 先頭への追加は`popleft()`メソッドで行う    ←★メソッド名の後ろに`left`を追加する
- 先頭からの削除は`popleft()`メソッドで行う  ←★メソッド名の後ろに`left`を追加する
- dequeが空の場合、`削除(pop(), popleft`はエラーが発生することに注意！！！


```python title="python ソースコード"
# collectionsモジュールをインポートする
import collections

# 初期化(引数にタイプを指定する)
d = collections.deque([],3)

# 末尾に追加
d.append(1)
d.append(2)
print(d)

# 先頭に追加
d.appendleft(3)
print(d)

# 末尾を削除(取得)
print(d.pop())
print(d)

# 先頭を削除(取得)
print(d.popleft())
print(d)


d.append(11)
d.append(12)
print(d)

# 最大サイズ以上追加すると、
# 逆側の要素(ここでは先頭)が削除される
d.append(13)
print(d)

# 最大サイズ以上追加すると、
# 逆側の要素(ここでは末尾)が削除される
d.appendleft(14)
print(d)
```

```python  title="python 出力結果"
deque([1, 2])     ★末尾に追加

deque([3, 1, 2])  ★先頭に追加

2                 ★末尾を削除して取得
deque([3, 1])

3                 ★先頭を削除して取得
deque([1])

deque([1, 11, 12], maxlen=3)
deque([11, 12, 13], maxlen=3) ★逆側を自動的に削除
deque([14, 11, 12], maxlen=3) ★逆側を自動的に削除
```

### 2.1. その他のメソッド
### 2.2. 削除(clear())
- クリアする

```python title="python ソースコード"
import collections

d = collections.deque([1,2,3])
print(d)

# 削除
d.clear()
print(d)
```

```python  title="python 出力結果"
deque([1, 2, 3])
deque([])
```

### 2.3. count()
- 引数で指定した値が何個存在するか確認する

```python title="python ソースコード"
import collections

d = collections.deque([1,5,7,5,5,7])
print(d)

# 削除
print(d.count(5))
print(d.count(7))
print(d.count(0))
```

```python  title="python 出力結果"
deque([1, 5, 7, 5, 5, 7])
3
2
0
```









## 3. reference
- [TimeComplexity](https://wiki.python.org/moin/TimeComplexity)



```python title="python ソースコード"

```

```python  title="python 出力結果"
```

# sort

## 1. Overview
- 組み込み関数

- 複数の型を入れることが出来る
- 後からリストの追加・置換・削除が可能
- **[　]**で値を定義する

## 2. 基本
### 2.1. メソッド
- 元の配列を直接編集する
- 降順(descending order)でソートしたい場合には、`reverse=True`を設定する
```python title="python ソースコード"
my_list = [13,9,4]

print(my_list)

my_list.sort()

print(my_list)

my_list.sort(reverse=True)

print(my_list)


```

```python  title="python 出力結果"
[13, 9, 4]
[4, 9, 13] ★ asc_order
[13, 9, 4] ★ dsec_order
```

### 2.2. 組み込み関数
- 元の変数は変更しない

```python title="python ソースコード"
my_list = [13,9,4]

print(my_list)

af_list = sorted(my_list)

print(my_list)
print(af_list)
```

```python  title="python 出力結果" hl_lines="3"
[13, 9, 4]
[13, 9, 4]
[4, 9, 13]
```

## 3. 応用
- 2次元配列の指定した一つ目の引数でソートする
- `lambda`を使用して引数のkeyにソート対象の情報を渡す

### 3.1. メソッド形式

```python title="python ソースコード"
my_list = [
    [13,1],
    [3,4],
    [4,2],
]

print(my_list)

my_list.sort(key= lambda x: x[0])

print(my_list)

my_list.sort(key= lambda x: x[1])

print(my_list)
```

```python  title="python 出力結果"
[[13, 1], [3, 4], [4, 2]]
[[3, 4], [4, 2], [13, 1]] ★1つ目でソートした場合
[[13, 1], [4, 2], [3, 4]] ★2つ目でソートした場合
```

### 3.2. 組み込み関数

```python title="python ソースコード"
my_list = [
    [13,1],
    [3,4],
    [4,2],
]

print(my_list)

af_list1 = sorted(my_list, key= lambda x: x[0])
af_list2 = sorted(my_list, key= lambda x: x[1])

print(my_list)
print(af_list1)
print(af_list2)
```

```python  title="python 出力結果" hl_lines="3"
[[13, 1], [3, 4], [4, 2]]
[[3, 4], [4, 2], [13, 1]] ★1つ目でソートした場合
[[13, 1], [4, 2], [3, 4]] ★2つ目でソートした場合
```


## 4. reference
- [Pythonでリストをソートするsortとsortedの違い](https://note.nkmk.me/python-list-sort-sorted/)
- [Pythonでlambda式を利用してソート処理する方法を現役エンジニアが解説【初心者向け】](https://techacademy.jp/magazine/30597)
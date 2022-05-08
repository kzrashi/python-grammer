# リスト内包表記(List Comprehensions)

## basic
- リスト**ないほうひょうき**と読む
- リストを初期化時に、１行で特定のルールで変数を代入出来る
- for文で代入するより**処理速度が早い**
- `[代入 iteration文]`や`[代入 iteration文 条件式]`の形で記述する


```python title="python ソースコード"  hl_lines="1-3"
# リスト内包表記を使用しない場合
my_list1 = []
for i in range(10):
    my_list1.append(i)
print(my_list1)

# ↓
# ↓

# リスト内包表記を使用する場合
my_list2 = [i for i in range(10)]
print(my_list2)
```

```python  title="python 出力結果"
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

<br>

```python title="python ソースコード"  hl_lines="1 3"
# リスト内包表記を使用しない場合
my_list3 = []
for i in range(10):
    if i % 2 == 0:
        my_list3.append(i)
print(my_list3)

# ↓
# ↓

# リスト内包表記を使用する場合
my_list4 = [i for i in range(10) if i % 2 == 0]
print(my_list4)
```

```python  title="python 出力結果"
[0, 2, 4, 6, 8]
[0, 2, 4, 6, 8]
```



## 4. reference

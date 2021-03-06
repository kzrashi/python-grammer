# 条件式()

- 文字列も数値も簡単に比較することが出来る
- 特に他の言語と異なり、**in**演算子が便利

###

| 記号   | 意味           |
| :----- | :------------- |
| ==     | 等しい場合     |
| !=     | 等しくない場合 |
| in     | 含む場合       |
| is     | id が一緒か    |
| is not | id が一緒か    |
| <      |                |
| <=     |                |
| >      |                |
| >=     |                |

### 等しい(==)

```python
# 成功ケース
print(1 == 1)
True
print("str" == "str")
True

# 失敗ケース
$ print(1 == 2)
False

$ print("str" == "star")
False
```

### 等しくない(!=)

```python
# 真(True)となるケース
$ print(1 != 2)
True
$ print("str" != "stra")
True


# 儀(False)となるケース
$ print(1 != 1)
False
$ print("str" != "str")
False
```

# 含む(in)

```python
# 真(True)となるケース
#   文字列の場合
$ print("bb" in "aabbcc")
True

#   リストの場合
$ print("bb" in ["aa", "bb", "cc", "dd"])
True

#   タプルの場合
$ print("cc" in ("aa", "bb", "cc", "dd"))
True

#   辞書の場合(Keyがあればヒットする)
$ print("cc" in {"aa": 0, "bb": 1, "cc": 2, "dd": 3})
True


# 儀(False)となるケース

# 文字列の場合
$ print("dd" in "aabbcc")
False

# リストの場合
$ print("ee" in ["aa", "bb", "cc", "dd"])
False

# タプルの場合
$ print("ee" in ("aa", "bb", "cc", "dd"))
False

# 辞書の場合(Keyがあればヒットする)
$ print("ee" in {"aa": 0, "bb": 1, "cc": 2, "dd": 3})
False

```

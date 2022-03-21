

### 数値 -> リスト(int)の変換
- 数値を文字列に変換
- １文字づつ、数値に戻してリストに入れる

```python
num = 1234

# conver int to string
word = str(num)

# iterate charactor 
list = []
for i in word:
    list.append(int(i))

print(list)
```

```python
num = 1234

list = [int(i) for i in str(num)]

print(list)

```
# rule


## 1. import
- 標準 -> 3rd party -> 自作の順にimportする
- アルファベット順に並べる
- importとconst値の間は２行空ける
- constと関数宣言の間は２行空ける
```python
import xxx
import yyy

import zzzz

import custom
★
★
AAA = 200
★
★
def func()



```

## 2. mainの書き方
```python


def main():
    print("aaa")


if __name__ == '__main__':
    main()

```

## 3. 変数宣言
- `変数名`, `=` `値`でインデントは合わせない
```python
# NGケース
x         = 100
yyy       = 200
zzzzzzzzz = 300


# OKケース
x = 100
yyy = 200
zzzzzzzzz = 300
```

## 4. 判定文
### 4.1. notを使うポイント
- booleanの判定ではnotを使う
```python
x = True
if not x:
    print('NG')
```

- リストの空判定で使用する
- 辞書のキーが
```python title="python ソースコード"
x = [1, 2, 3]
if x:
    print('list has elements.')

y = []
if not y:
    print("list doesn't have elements.")
```

```python  title="python 出力結果"
list has elements.
list doesn't have elements.
```

### 4.2. Noneを使うポイント
- アドレスの判定ではNoneを使うべき

```python title="python ソースコード"
def func(node):
    if node is None:
        print("error")
```


## 5. 80文字を超える場合
### 5.1. 関数
- 引数の区切りで改行する
- 上の引数と位置をあわせる
- 次の引数の頭にはスペース1つを挿入する
- デフォルト引数の`=`前後には**スペースはあけない**
```python
def func(num1, num2, num3,
              ^★
         num4=2)
         ^★ ^^        
```

## 6. 判定条件
- 基本的に`()`はつけない
- 複数条件で必要な場合に`()`を付与する

```python
if x ==1 and y == 1:
    xxx

if (x == 1 and y ==1 ) or (z == 1 and a == 2):
    xxx

```



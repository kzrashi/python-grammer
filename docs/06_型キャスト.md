# 型キャスト

### 基本

- int は小数点以下が**切り捨てられる**
- bool 型は以下のルールで変換される
  - 0 は false
  - **0 以外は true**

```python
$ print(int(2.5))
2

$ print(float("4.56"))
4.56

$ print(str(123))
123

# book型のキャスト
$ print(bool(0))
False

$ print(bool(1))
True

$ print(bool(2))
True

$ print(bool("0"))
True

$ print(bool("str"))
True

```

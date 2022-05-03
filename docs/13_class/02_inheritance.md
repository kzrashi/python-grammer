# 継承(inheritance)
他のクラスを継承して再利用することが出来る機能

## 1. 基本
- クラス名の引数に継承したいクラス名を記述する
- 親クラスのンストラクタを`super().__init__()`で呼び出す必要あり
- 子クラスのメンバ変数やメソッドはそのままアクセス可能

```python title="python ソースコード"
class MyClass(object):
    def __init__(self):
        self._num = 100
        print("myclass")
    def output(self):
        print("output",self._num)

class SubClass(MyClass):
               ^^^^^^^★

    def __init__(self):
        super().__init__()
        ^^^^^^^^^^^^^^^^^^★
        self._sub_num = 200
        print("subclass")
    
    def sub_output(self):
        print("sub_output",self._num, self._sub_num)
　　　　　　　　　　　         ^^^^^^^^^★

subclass = SubClass()
subclass.output()
         ^^^^^^^★
subclass.sub_output()
```

## 2. 上書き(override)
- 親クラスのメンバ変数やメソッド名を定義した場合、子クラス側のものが実行される
```python title="python ソースコード"
class MyClass(object):
    def __init__(self):
        self._num = 100

    def output(self):
        print("output",self._num)

class SubClass(MyClass):
    def __init__(self):
        super().__init__()
        self._num = 200

    def output(self):
        print("sub_output",self._num)

subclass = SubClass()
subclass.output()
```

```python  title="python 出力結果"
sub_output 200
```

## 3. 親クラスのメソッドの呼び出し()
- 子クラス内で、親クラスのメソッド名の先頭に`super.`を付与すると、呼び出すことが出来る


```python title="python ソースコード"
class MyClass(object):
    def __init__(self):
        self._num = 100

    def output(self):
        print("output",self._num)

class SubClass(MyClass):
    def __init__(self):
        super().__init__()
        self._num = 200

    def output(self):
        super().output()
        ^^^^^^^^★

subclass = SubClass()
subclass.output()
```

```python  title="python 出力結果"
output 200
```

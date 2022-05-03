# 静的な定義

## メンバ変数/静的メンバ変数
- メソッド外で定義すると全クラス共通のメンバ変数として使用出来る
- `クラス名.メンバ変数名`でアクセス可能(インスタンス化しなくても参照することが出来る)

```python title="python ソースコード"
class StaticMyClass():
    data = "test"

myclass = StaticMyClass()
myclass2 = StaticMyClass
print(myclass.data)
print(myclass2.data)
print(StaticMyClass.data)  ←インスタンス化しなくても参照可能
```

```python  title="python 出力結果"
test
test
test
```
## クラスメソッド
- メソッド名の上に`@classmethod`の属性を記載する
- 引数には`self`の代わりに`cls`を記述する
- クラス変数を参照したい場合、メンバ変数の頭に`cls.`を付与する
- `クラス名.メソッド名`でアクセス可能(インスタンス化しなくても参照することが出来る)

```python title="python ソースコード"
class StaticMyClass(object):
    num = 1

    @classmethod
    def func(cls):
        print("sample",cls.num)

myclass = StaticMyClass()
myclass2 = StaticMyClass
myclass.func()
myclass2.func()
StaticMyClass.func()　←インスタンス化しなくても参照可能
```

```python  title="python 出力結果"
sample 1
sample 1
sample 1
```

## スタティックメソッド
- メソッド名の上に`@staticmethod`の属性を記載する
- 引数には`self`や`cls`は不要
- **メンバ変数にアクセスすることができない！**




```python title="python ソースコード"
class StaticMyClass(object):
    @staticmethod
    def func():
        print("sample")

myclass = StaticMyClass()
myclass2 = StaticMyClass
myclass.func()
myclass2.func()
StaticMyClass.func()
```

```python  title="python 出力結果"
sample
sample
sample
```





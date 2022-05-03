# Class

## 1. basic
- クラス名はCamelCaseで記載する
- インストラクタは`def __init__(self,[変数名]):`で記述する **←後ろの`__`をよく忘れるので注意**
- デストラクタは`def __del__(self):`で記述する
- メソッドの第一引数は`self`が必須(呼び出し時は第一引数は設定不要) **←よく忘れるので注意**
- メンバ変数の第一引数は`self`が必須 **←よく忘れるので注意**
- クラス内からメンバ変数やメソッドにアクセスする場合には、`self.`をつける **←よく忘れるので注意**
- pythonには厳密なprivate変数は存在しない
  そのため、下記のどちらかのルールで明示的に記載する
  - 変数名の先頭にアンダースコアを**1つ**つける
  - 変数名の先頭にアンダースコアを**2つ**つける(ネームマングリングされるため)

```python title="python ソースコード"
class MyClass(object):
    # コンストラクタ
    def __init__(self,num=1):
        # メンバ変数
        self._num = num

    # デストラクタ
    def __del__(self):
        print("finish")
    
    # メソッド
    def output(self):
        self.doubleoutput()
    def doubleoutput(self):
        print(self._num * 2)

#------------------------
myclass1 = MyClass(10)
myclass1.output()

myclass2 = MyClass()
myclass2.output()
```

```python  title="python 出力結果"
20
2
finish
finish
```

## 2. 何も書かない場合
- passを指定するとメンバ変数・メソッド・コンストラクタ等を記述しないクラスを作成出来る

```python title="python ソースコード"
class VoidClass(object):
    pass
```

```python  title="python 出力結果"
voidclass = VoidClass()
```

## 3. クラス変数
- 全クラスで共有することが可能なメンバ変数
```python title="python ソースコード"
```

```python  title="python 出力結果"
```



## 4. settrt/getter
- インスタンス変数を外部に公開する際に、使用すると便利な機能
- getter関数の上に`@property`を記述する
- 外部からアクセスする際には、`インスタンス変数名.getterメソッド名`でアクセスする
- setter関数の上に`@setter関数名.setter`を記述する

```python title="python ソースコード"
class MyClass(object):
    def __init__(self):
        self.__num = 1

    @property
    def num(self):
        return self.__num
    @num.setter
    def num(self,num):
        self.__num = num


myclass = MyClass()
print(myclass.num)
      ^^^^^^^^^^^★getter関数のアクセス
myclass.num = 100
print(myclass.num)
```

```python  title="python 出力結果"
1
100
```





## 5. 参考
- [Pythonの_(アンダースコア)の扱いまとめ](https://mako-note.com/ja/python-underscore/#:~:text=1%E3%81%A4%E4%BB%98%E4%B8%8E-,%E3%82%AF%E3%83%A9%E3%82%B9%E5%86%85%E3%81%AE%E5%A4%89%E6%95%B0%E3%82%84%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%81%AE%E5%85%88%E9%A0%AD%E3%81%AB%E3%82%A2%E3%83%B3%E3%83%80%E3%83%BC,%E5%A4%89%E6%95%B0%E3%83%BB%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%81%A8%E3%81%84%E3%81%86%E3%81%93%E3%81%A8%E3%81%A7%E3%81%99%E3%80%82)

- [9. Classes](https://docs.python.org/3/tutorial/classes.html)
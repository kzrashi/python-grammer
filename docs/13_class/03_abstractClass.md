# 抽象クラス(Abstract Class)
- JavaやC++等で提供されている抽象クラス機能をpythonでも使用することが出来る
- **pythonでは本機能の使用はあまり奨励されていない**

## basic
- 継承先のベースとして定義するクラス。継承先で定義してほしいメソッドを記述することで継承先のクラスをパターン化出来る
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

## 何も書かない場合
- passを指定するとメンバ変数・メソッド・コンストラクタ等を記述しないクラスを作成出来る

```python title="python ソースコード"
class VoidClass(object):
    pass
```

```python  title="python 出力結果"
voidclass = VoidClass()
```




## 参考
- [Pythonの_(アンダースコア)の扱いまとめ](https://mako-note.com/ja/python-underscore/#:~:text=1%E3%81%A4%E4%BB%98%E4%B8%8E-,%E3%82%AF%E3%83%A9%E3%82%B9%E5%86%85%E3%81%AE%E5%A4%89%E6%95%B0%E3%82%84%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%81%AE%E5%85%88%E9%A0%AD%E3%81%AB%E3%82%A2%E3%83%B3%E3%83%80%E3%83%BC,%E5%A4%89%E6%95%B0%E3%83%BB%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%81%A8%E3%81%84%E3%81%86%E3%81%93%E3%81%A8%E3%81%A7%E3%81%99%E3%80%82)

- [9. Classes](https://docs.python.org/3/tutorial/classes.html)
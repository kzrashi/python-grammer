# for文()
pythonはforeach文でのループ方式を採用している


## 

```python
for 変数 in リスト:
    処理

```

#### ５回(0から4まで)ループを繰り返す場合

- python

```python
for i in (0,1,2,3,4):
    print(i)

```

or

```python
for i in range(5):
    print(i)

```

or 

```python
for i in range(0,5):
    print(i)
```

```python
0
1
2
3
4
```

- C/C++の場合

```C++
for(unsigned int i=0; i<5; i++){
     std::cout << i << std::endl;
}
```

※C++11であれば、以下の記述も可能
```C++
    int nums[] = {0, 1, 2, 3, 4};
    for(int x : nums){
	    std::cout << x << std::endl;
    }
```



#### リスト(a,b,c,d)をループする場合

- python


```python
myList = ["a", "b", "c", "d"]
for str in myList:
    print(str)
```


```python
a
b
c
d
```
or 

```python
>>> myList = ["a", "b", "c", "d"]
>>> for i,str in enumerate(myList):
...     print("{num} => {mozi}".format(num=i,mozi=str))
...
0 => a
1 => b
2 => c
3 => d
```

####  リスト＋インデックスを表示する場合

python
```python
names = ["a", "b", "c", "d"]

for i,name in enumerate(names):
    print(i,name)
```

結果
```python
0 a
1 b
2 c
3 d
```


####  ２つ以上のリストを表示する場合
- zip関数を使う
- リストの数が異なる場合、少ない方に合わせられる


python
```python
names = ["a", "b", "c", "d"]
prices = ["100", "200", "300"]

for name,price in zip(names,prices):
    print(name, price)
```

結果
```python
a 100
b 200
c 300
```

####  組み合わせ
- zip関数を使う
- リストの数が異なる場合、少ない方に合わせられる


```python:"python"
names = ["a", "b", "c", "d"]
prices = ["100", "200", "300"]

for name,price in zip(names,prices):
    print(name, price)
```

```python:"結果"
a 100
b 200
c 300
```


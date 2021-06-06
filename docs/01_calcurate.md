# 演算

#### 足し算(addition)

ソースコード
```python
num = 3 + 2
print(num)
```

出力結果
```python
5
```


#### 引き算(subtraction)

ソースコード
```python
num = 3 - 2
print(num)
```

出力結果
```python
1
```

#### 掛け算(multiplication)

ソースコード
```python
num = 3 * 2
print(num)
```

出力結果
```python
6
```

#### 割り算(division)
- 他の言語と異なり、pythonでは **/** を使用する割り算では、小数点以下まで計算される  
  小数点以下も含めて計算する場合には **//** を使用する  
  
##### 小数点を切り捨てせずに計算する
=== "python"

    ソースコード
    ```python
    num = 5 / 2
    print(num)
    ```
    
    出力結果
    ```python
    2.5
    ```


=== "c++"
    - C++では整数型の割り算をすると、小数点以下は切り捨てられるため、浮動小数点型に変換して計算する

    ```C++
    #include <iostream>  //stdクラスを使用するのに必要
    
    std::cout << static_cast<float>(5) / static_cast<float>(2) << std::endl;
    ``` 


##### 小数点を切り捨てる
=== "python"
    ソースコード
    ```python
    num = 5 // 2
    print(num)
    ```
    
    出力結果
    ```python
    2
    ```

=== "c++"

    ```C++
    #include <iostream>  //stdクラスを使用するのに必要
    
    std::cout << 5 / 2 << std::endl;
    ```

#### 剰余(余り)計算
=== "python"
    ソースコード
    ```python
    num = 5 % 3
    print(num)
    ```
    
    出力結果
    ```python
    2
    ```

=== "c++"

    ```C++
    ```
#### 累乗計算(Exponentiation)
=== "python"
    - **\*\***を使用する

    ソースコード
    ```python
    num = 2 ** 4
    print(num)
    ```
    
    出力結果
    ```python
    16
    ```

=== "c++"

    ```C++
    ```

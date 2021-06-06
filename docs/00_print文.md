# 標準出力

## 固定文字列を出力する場合
- 固定文字列や変数を出力するにはprintを使用します。

=== "python"
    ```python
    >> print("Hello World") 
    Hello World

    # 数値でも表示出来る
    >> print(123) 
    123
    ``` 

=== "c++"
    ```C++
    #include <iostream>
    
    // 改行するためには、最後にstd::coutが必要
    std::cout << "Hello world" << std::endl;

    std::cout << 123 << std::endl;
    
    ``` 

## 変数を表示する場合

=== "python"
    - 文字列(str)型の変数の場合
    ```python
    >> str="Hello World"
    >> print(str)
    Hello World
    ``` 

    - 数値(int)型の変数を出力する場合
    ```python
    >> num=123
    >> print(num)
    123
    ``` 

    - bool型の変数を出力する場合
    ```python
    >> valid = False
    >> print(valid)
    False
    ``` 

=== "c++"
    - 文字列(str)型の変数の場合
    ```C++
    #include <iostream>  //stdクラスを使用するのに必要

    std::string str="Hello World";
    std::cout << str << std::endl;
    ``` 

    - 数値(int)型の変数を出力する場合
    ```C++
    #include <iostream>  //stdクラスを使用するのに必要

    int num = 123;
    std::cout << num << std::endl;
    ``` 

    - bool型の変数を出力する場合
    ```C++
    #include <iostream>  //stdクラスを使用するのに必要

    bool valid = false;
    std::cout << valid << std::endl;
    ``` 

## 複数の変数を表示したい場合
- 以下の３つある  

| 種類                                       | 記述方法              |pythonのバージョン|
| -----------------------------              | ----------------- | ---|
| フォーマット済み文字列リテラル<br>(f-string) | f"{変数名}"          | Python3.6以降|
| format関数                                  | "{0}".format(変数名) |Python 2.6以降|
| %記法                                  | "%d" % (変数名) ||


### フォーマット済み文字列リテラル(f-string)を使用する場合
=== "python"
    - 変数を表示したいポイントに**{変数名}**を記載すると表示してくれる

    ```python
    >> str="Hello World"
    >> num=12
    >> print(f"{str} {num}")
    Hello World 12
    ``` 

=== "c++"
    ```C++
    #include <iostream>  //stdクラスを使用するのに必要
    
    std::string str="Hello";
    int num=12;
    std::cout << str << num << std::endl;
    
    ``` 


### format関数を使用する場合
- 変数を表示したいポイントに**{}**の置換フィールドを記載して、後ろにformat関数で変数を記載すると表示してくれる
- 置換フィールド部分には{str}等のキーワード引数を入れた方がformat関数側でも対応付けがされて見やすい

```python
>> str="Hellor World"
>> num=123
>> print("{} {}".format(str, num))
Hellor World 123
``` 
```python
>> str="Hellor World"
>> num=123
>> print("{string} {number}".format(string=str, number=num))
Hellor World 123
``` 

### %記法を使用する場合

    ```python
    >> str="Hellor World"
    >> num=123
    >> print("%s %d" % (str, num))
    Hellor World 123
    ``` 

    ※以下のように変数名と%の型が間違っているとエラーになる
    ```python
    >> str="Hellor World"
    >> num=123
    >> print("%d %s" % (str, num))
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
    TypeError: %d format: a number is required, not str
    ``` 

## フォーマット済み文字列リテラル(f-string)・format記法の色々な使い方
- 数値型の変数を表示する場合、**{}**の置換フィールドに書式を指定することで表示する内容をカスタマイズすることが出来ます。



|書式| 内容| 例<br>(num変数には123456が設定している)|結果|
|:--|:--|:--|:--|
|b  | 2進数で表示 | f"{num}:b}"|11110001001000000|
|d  | 10進数で表示 |f"{num:d}"|123456  |
|x  | 16進数(小文字)で表示 |f"{num:x}"|1e240  |
|x  | 16進数(大文字)で表示 |f"{num:X}"|1e240  |
|表示幅指定 |表示幅指定|f"{num:8d}"|　123456|
|パディング文字+表示幅指定 |パディング文字と表示幅指定|f"{num:08d}"|  00123456|
|< |左寄せ|f"{num:<8d}"|123456|
|> |左寄せ|f"{num:>8d}"|　123456|
|, |**３桁毎**の区切り文字|{num:,}"|123,456|


もう少し詳細な指定を知りたい場合、こちらのサイトで纏められた内容が凄くわかりやすいです。  
<https://hibiki-press.tech/python/format/1015>

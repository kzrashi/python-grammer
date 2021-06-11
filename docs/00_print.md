# 標準出力
print関数を使うことで画面に文字や数値を出力することが出来ます。


### 固定文字列の出力
- print("出力したい文字列")やprint(出力したい変数名)を指定出力します。

=== "python"
    ソースコード
    ```python
    # print文で出力する
    print("Hello World") 

    # 数値でも表示出来る
    print(123) 
    ``` 

    出力結果
    ```python
    Hello World

    123
    ``` 

=== "c++"
    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要
    
    int main(void){

        // 改行するためには、最後にstd::endlが必要
        std::cout << "Hello world" << std::endl;
  
        // 数値でも表示出来る
        std::cout << 123 << std::endl;
    }
    ``` 

    出力結果
    ```c++
    Hello world

    123
    ```

### 変数の出力

=== "python"
    - 文字列(str)型の変数を出力する場合

    ソースコード
    ```python
    str="Hello World"
    print(str)
    ```

    出力結果
    ```python
    Hello world
    ```

    - 数値(int)型の変数を出力する場合

    ソースコード
    ```python
    num=123
    print(num)
    ``` 

    出力結果
    ```python
    123
    ```

    - bool型の変数を出力する場合

    ソースコード
    ```python
    valid = False
    print(valid)
    ``` 

    出力結果
    ```python
    False
    ```

=== "c++"
    - 文字列(str)型の変数の場合

    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要
    int main(void){

        std::string str="Hello World";

        // 変数の表示
        // 改行するためには、最後にstd::endlが必要
        std::cout << str << std::endl;
    }
    ```

    出力結果
    ```c++
    False
    ```

    - 数値(int)型の変数を出力する場合
 
    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){

        int num = 123;

        // 変数の表示
        // 改行するためには、最後にstd::endlが必要
        std::cout << num << std::endl;
    }
    ```

    出力結果
    ```c++
    123
    ```

    - bool型の変数を出力する場合
 
    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){

        bool valid = false;

        // 変数の表示
        // 改行するためには、最後にstd::endlが必要
        std::cout << valid << std::endl;
    }
    ```

    出力結果
    ```c++
    0
    ```

### ２つ以上の変数の出力
固定文字列＋複数の変数(例：変数numの値はXXです。)の形式で出力することが多いと思います。  
以下の方法で出力することが出来ます。


| 種類                                       | 記述方法              |pythonのバージョン|
| -----------------------------              | ----------------- | ---|
| フォーマット済み文字列リテラル(f-string) | f"{変数名}"          | Python3.6以降|
| format関数                                  | "{0}".format(変数名) |Python 2.6以降|
| %記法                                  | "%d" % (変数名) ||


#### f-string
- 変数を表示したいポイントに**{変数名}**を記載すると表示してくれる

```python
>> str="Hello World"
>> num=12
>> print(f"{str} {num}")
Hello World 12
``` 

#### format関数
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

#### %記法

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

## 数値の書式指定
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


```python
>> str="Hellor World"
>> num=123
>> print("%s %d" % (str, num))
Hellor World 123
``` 



もう少し詳細な指定を知りたい場合、こちらのサイトで纏められた内容が凄くわかりやすいです。  
<https://hibiki-press.tech/python/format/1015>

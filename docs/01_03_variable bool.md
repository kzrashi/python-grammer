#  真偽型(bool)
- 真(True) or 偽(False)のどちからの値を取る型
- Camel case(１文字目が大文字、２文字目以降が小文字)で記載することに注意


=== "python"
    ソースコード
    ```python
    # 変数の宣言
    valid = True
    
    # 変数の内容の表示
    print(valid) 
    
    # 変数の型の表示
    print(type(valid)) 
    ``` 

    出力結果
    ```python
    True
    <class 'bool'>
    ```

    ※以下のように、**TRUE**や**true**と書くとエラーになる

    ソースコード
    ```python
    # 変数の宣言
    valid = TRUE
    ``` 

    出力結果
    ```python
    Traceback (most recent call last):
      File "Main.py", line 2, in <module>
      valid = TRUE
    NameError: name 'TRUE' is not defined
    ```

    ソースコード
    ```python
    # 変数の宣言
    valid = true
    ``` 

    出力結果
    ```python
    Traceback (most recent call last):
      File "Main.py", line 2, in <module>
      valid = true
    NameError: name 'true' is not defined
    ```

=== "c++"
    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
       //変数(valid)の前に使用したい型を記述する
       bool valid = true;
       
       // 変数の内容の表示
       // 改行するためには、最後にstd::endlが必要
       std::cout << valid << std::endl;

       // 変数の型の表示
       std::cout << typeid(valid).name() << std::endl;
    }
    ```

    出力結果
    
    ```c++
    # Ｃ言語側ではfalseは0、trueは1で表示される
    1
    b
    ```
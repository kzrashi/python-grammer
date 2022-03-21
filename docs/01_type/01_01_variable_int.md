#  整数型(int)
- 整数を扱うための型

=== "python"
    ソースコード
    ```python
    # 変数の宣言
    num = 3

    # 変数の内容の表示
    print(num) 

    # 変数の型の表示
    print(type(num)) 
    ``` 

    出力結果
    ```python
    3
    <class 'int'>
    ```

=== "c++"
    - Ｃ言語では、変数を使う際に、どの型を使うか指定する必要があります  

    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
       //変数(num)の前に使用したい型を記述する
       int num =3;
       
       // 変数の内容の表示
       // 改行するためには、最後にstd::endlが必要
       std::cout << num << std::endl;

       // 変数の型の表示
       std::cout << typeid(num).name() << std::endl;
    }
    ```

    出力結果
    ```c++
    3
    i
    ```

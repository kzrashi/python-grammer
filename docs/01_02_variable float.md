#  浮動小数点数型(float)
- 小数点が含まれた数値を扱うための型

=== "python"
    ソースコード
    ```python
    # 変数の宣言
    num = 1.2

    # 変数の内容の表示
    print(num) 

    # 変数の型の表示
    print(type(num)) 
    ``` 

    出力結果
    ```python
    1.2
    <class 'float'>
    ```

=== "c++"
    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
       //変数(num)の前に使用したい型を記述する
       float num =1.2;
       
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
# 文字列型(str)
- 文字列を扱うための型
- 文字部分をシングルクォーテーション(')かダブルクオーテーション(")で括って記述する

### 基本
=== "python"
    ソースコード
    ```python
    # 変数の宣言
    str = "mozi"
    
    # 変数の内容の表示
    print(str) 
    
    # 変数の型の表示
    print(type(str)) 
    ``` 

    出力結果
    ```python
    mozi
    <class 'str'>
    ```

=== "c++"
    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
       //変数(str)の前に使用したい型を記述する
       std::string str = "mozi";
       
       // 変数の内容の表示
       // 改行するためには、最後にstd::endlが必要
       std::cout << str << std::endl;

       // 変数の型の表示
       std::cout << typeid(str).name() << std::endl;
    }
    ```

    出力結果
    ```c++
    mozi
    NSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEE
    ```


### 文字列の長さを取得する

=== "python"
    - len関数を使用する

    ソースコード
    ```python
    # 変数の宣言
    str = "mozi"
    
    # 変数strの長さを表示
    print(len(str)) 
    
    ``` 

    出力結果
    ```python
    4
    ```

=== "c++"
    - size()メソッドを使用する

    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
       //変数(str)の前に使用したい型を記述する
       std::string str = "mozi";
       
       // 変数の内容の表示
       // 改行するためには、最後にstd::endlが必要
       std::cout << str.size() << std::endl;
    }
    ```

    出力結果
    ```c++
    4
    ```

### インデックス指定で取得


=== "python"
    - 変数名の後ろに**[取得位置]**のつけて使用する
    - **１文字取得するときに便利**
    - 負数を使用すると文字列の後ろからの位置を指定出来る
    - 先頭は0番目になる

    ソースコード
    ```python
    # 変数の宣言
    str = "mozi"
    
    # 先頭の１文字を表示
    print(str[0]) 

    # ３文字目を表示
    print(str[2]) 

    # 最後を表示
    print(str[-1]) 

    ``` 

    出力結果
    ```python
    m
    z
    i
    ```

=== "c++"
    - 変数名の後ろに**[取得位置]**のつけて使用する
    - **１文字取得するときに便利**
    - 後ろから参照する場合、xxx.size()で全体のサイズを取得してさらに計算するので、pythonの記述と比較すると少し難解。
    - 先頭は0番目になる

    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
       //変数(valid)の前に使用したい型を記述する    
       std::string str = "mozi";
    
        //先頭の１文字を表示
        std::cout << str[0] << std::endl;
    
        //３文字目を表示
        std::cout << str[2] << std::endl;
    
        // 最後を表示
        std::cout << str[str.size() - 1] << std::endl;
    }
    ```

    出力結果
    ```c++
    m
    z
    i
    ```

### スライス指定で取得する

=== "python"
    - **[開始位置:終了位置]**のスライスを使用する
    - 開始位置を省略すると、先頭(0)と判断される
    - 終了を省略すると、最後(xxx)と判断される
    - 負数を使用すると文字列の後ろからの位置を指定出来る
    - 先頭は0番目になる

    ソースコード
    ```python
    # 変数の宣言
    str = "mozi"
    
    # 1文字と2文字目表示
    print(str[0:2]) 
    
    # 2文字以降を表示
    print(str[1:]) 
    
    # 先頭から2文字以降を表示
    print(str[:2]) 
    
    # 最後から２文字～最後まで表示
    print(str[-2:]) 
    ``` 

    出力結果
    ```python
    mo
    ozi
    mo
    zi
    ```

=== "c++"
    - **substr(開始インデックス, 文字数)**で指定する

    ソースコード
    ```c++
    #include <iostream>  //stdクラスを使用するのに必要

    int main(void){
        //変数(valid)の前に使用したい型を記述する    
        std::string str = "mozi";
    
        // 1文字と2文字目表示
        // 1文字目から2文字分表示
        std::cout << str.substr(1,2) << std::endl;
        
        // 2文字以降を表示
        std::cout << str.substr(1) << std::endl;
    
        // // 最後から２文字～最後まで表示
        std::cout << str.substr(str.size() - 2) << std::endl;
    }
    ```

    出力結果
    ```c++
    mo
    oxi
    zi
    ```

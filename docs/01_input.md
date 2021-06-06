# 標準入力
- 画面から数値や文字を入力する機能
- input()関数を使うと入力した内容を文字列として取得出来る
- {== 数値を入力しても**文字列として取得してしまう**ことに注意！！！  ==}

### 基本

=== "python"
    ソースコード
    ```python
    # 入力
    #  入力はmoziを入力する想定
    input_str = input()

    # 入力結果を表示
    print(input_str) 
    ``` 

    出力結果
    ```python
    mozi  ←これは入力したイメージ
    mozi
    ```


=== "c++"
    ```C++
    ``` 

### 補助メッセージ出力
- 入力時に補助メッセージを出力したい場合、input("出力したい文字列")を記載する

=== "python"
    ソースコード
    ```python
    # 入力
    #  入力はmoziを入力する想定
    input_str = input("please input string: ")

    # 入力結果を表示
    print(input_str) 
    ``` 

    出力結果
    ```python
    please input string: mozi  ←これは入力時の表示エリア
    mozi
    ```

### その他
#### 取得した数値を数値で扱いたい場合

=== "python"
    - 取得した文字をint関数で文字型から数値型に型変換することで数値として扱うことが出来る

    ソースコード
    ```python
    # 入力
    #  入力は123を入力する想定
    input_str = input()
    
    # str -> intに変換する
    input_num = int(input_str)
    
    # 入力結果を表示
    print(input_num)
    ``` 

    出力結果
    ```python
    123  ←これは入力時の表示エリア

    123
    ```


=== "c++"
    ```C++
    ``` 


#### 取得した数値を数値で扱いたい場合

=== "python"
    - 空白で入力した複数の文字をリストに格納したい場合、split("区切り文字")関数を使うことで実現出来る。

    ソースコード
    ```python
    # 入力
    #  入力は"AAA BBB CCC"AAAを入力する想定
    input_str = input()
    
    # split関数で半角スペースで区切ってリストに設定す    る
    input_list = input_str.split(' ')
    
    # 入力結果(str型)を表示
    print(input_str)
    
    # 入力結果(リスト型)を表示
    print(input_list)
    ``` 

    出力結果
    ```python
    AAA BBB CCC  ←これは入力時の表示エリア

    AAA BBB CCC
    ['AAA', 'BBB', 'CCC']
    ```


=== "c++"
    ```C++
    ``` 

# リスト(List)

- 複数の型を入れることが出来る
- 後からリストの追加・置換・削除が可能
- **[]**で値を定義する

### 宣言＆参照＆リストサイズ取得
#### 空の配列を作成する場合

=== "python"
    ソースコード
    ```python
    # リスト作成
    myList = []
    
    # リストを表示
    print(myList)
    
    # リストサイズを表示
    print(len(myList))
    ```

    出力結果
    ```python
    []
    0
    ```

=== "c++"
    - C++ではvectorクラスを使用した処理が一番近い
    - **std::vector<型> 変数名**で定義する
    - リストサイズはsize()メソッドで取得する

    ```C++
    #include <iostream> //stdクラスの使用で必要
    #include <vector>   //vectorクラスの使用で必要
    
    // vector作成
    std::vector<int> v;

    // リストサイズを表示
    std::cout << v.size() << std::endl;
    ``` 

#### １次元配列を作成する場合

=== "python"

    ソースコード
    ```python
    # リスト作成
    myList = [1, 2, 3, "str"]
    
    print(myList)
    
    # リストの０番目を表示
    print(myList[0])
    
    # リストの３番目を表示
    print(myList[3])
    
    # リストサイズを表示
    print(len(myList))
    ```

    出力結果
    ```python
    [1, 2, 3, 'str']
    1
    str
    4
    ```


=== "c++"
    - vector内に複数のデータ型(intとstr型など)を入れることが出来ない

    ```C++
    #include <iostream> //stdクラスの使用で必要
    #include <vector>   //vectorクラスの使用で必要
    
    // vector作成
    std::vector<int> v = {1,2,3,4};

    // リストの０番目(1)を表示
    std::cout << v[0]<< std::endl;

    // リストの２番目(3)を表示
    std::cout << v[2]<< std::endl;

    // リストサイズを表示
    std::cout << v.size() << std::endl;
    ``` 


#### 多次元配列を作成する場合

=== "python"
    ソースコード
    ```python
    # ２次元配列の作成
    myList = [
        [1, 2, 3],
        [11, 12, 13,14]
    ]
    
    # 出力
    print(myList)
    
    # １次元目[0]の２次元目[0]の値を表示
    print(myList[0][0])
    
    # １次元目[1]の２次元目[2]の値を表示
    print(myList[1][2])
    
    # １次元目のリストサイズ([1,2,3]と[11,12,13,14]の２グループあること)を表示
    print(len(myList))
    
    # 2次元目の0番目[1,2,3])のリストサイズを表示
    print(len(myList[0]))
    
    # 2次元目の0番目[11,12,13,14])のリストサイズを表示
    print(len(myList[1]))
    ```

    出力結果
    ```python
    [[1, 2, 3], [11, 12, 13,14]]
    1
    13

    2
    3
    4
    ```

=== "c++"
    - **std::vector<std::vector<型>> 変数名**で定義する

    ```C++
    #include <iostream> //stdクラスの使用で必要
    #include <vector>   //vectorクラスの使用で必要
    
    // vector作成
    std::vector<std::vector<int>> v = { {1,2,3},{11,12,13,13}};

    // リストの０番目(1)を表示
    std::cout << v[0][0]<< std::endl;

    // リストの２番目(3)を表示
    std::cout << v[1][2]<< std::endl;

    // リストサイズを表示
    std::cout << v.size()<< std::endl;

    // 2次元目の0番目[1,2,3])を表示
    std::cout << v[0].size()<< std::endl;
    
    // 2次元目の0番目[11,12,13,14])を表示
    std::cout << v[1].size()<< std::endl;

    ``` 


### 追加
#### 最後尾に追加

=== "python"
    ソースコード
    ```python
    # リスト作成
    myList = [1, 2, 3, "str"]
    
    # リストを表示
    print(myList)
    
    # 最後尾に追加
    myList.append(4)
    
    # リストを表示
    print(myList)
    ```

    出力結果
    ```python
    [1, 2, 3, 'str']
    [1, 2, 3, 'str', 4]
    ```

=== "c++"
    ```C++
    #include <iostream> //stdクラスの使用で必要
    #include <vector>   //vectorクラスの使用で必要
    
    // vector作成
    std::vector<int> v = {1,2,3};
    //末尾に追加
    v.push_back(4);
    ``` 

#### 最後尾にリストを追加

ソースコード
```python
# リスト作成
myList = [1, 2, 3, "str"]

# リストを表示
print(myList)

# 最後尾に追加
myList = myList + [4, "mozi"]

# リストを表示
print(myList)
```

出力結果
```python
[1, 2, 3, 'str']
[1, 2, 3, 'str', 4, 'mozi']
```



#### 位置を指定して挿入する
- insert(挿入位置、挿入する値 or リスト)

ソースコード
```python
# リスト作成
myList = [1, 2, 3, "str"]

# リストを表示
print(myList)

# 最後尾に追加
myList.insert(1,123)

# リストを表示
print(myList)
```

出力結果
```python
[1, 2, 3, 'str']
[1, 123, 2, 3]
```

### 置換
#### 置換する範囲を指定してリストを変更する

ソースコード
```python
# リスト作成
myList = [1, 2, 3, "str"]

# リストを表示
print(myList)

# １番目～3番目の範囲(2,3)を削除して差し替える
myList[1:3] = [ 100,200,"mozi"]

# リストを表示
# (「2,3」が「100,200,"mozi"」に置換されている)
print(myList)
```

出力結果
```python
[1, 2, 3, 'str']
[[1, 100, 200, 'mozi', 'str']
```


### 削除

#### 全要素削除
ソースコード
```python
# リスト作成
myList = [1, 2, 3, "str"]

# 削除前
print(myList)

# 全要素を削除
myList.clear()

# 削除後
print(myList)
[]
```

出力結果
```python
[1, 2, 3, 'str']
[]
```


#### インデックス指定で削除

ソースコード
```python
# リスト作成
myList = [1, 2, 3, "str"]

# 削除前
print(myList)

# インデックス１の要素を削除
del myList[2]

# 削除後
print(myList)
```

出力結果
```python
[1, 2, 3, 'str']
[1, 3, 'str']
```

#### インデックス指定で削除し、値を取得する

ソースコード
```python
# リスト作成
myList = [1, 2, 3, "str"]

# 削除前
print(myList)

# インデックス１の要素を削除
data = myList.pop(1)

# 削除後
print(myList)

# 削除した値を表示
print(data)

```

出力結果
```python
[1, 2, 3, 'str']
[1, 3, 'str']
2
```


#### 要素(中身データ)を検索して一致したものを削除
- リスト内に指定した値が複数含まれていた場合、インデックスの小さい値が削除される

ソースコード
```python
# リスト作成
myList = [1, 2, 1, "str"]

# 削除前
print(myList)

# 1が含まれている要素を削除
myList.remove(1)

# 削除後
# 先頭の1が削除されている
# ３つ目の1は削除されないことに注意！！！
print(myList)
```

出力結果
```python
[1, 2, 1, 'str']
[2, 1, 'str']
```

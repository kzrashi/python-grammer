# for文(For Loops)

## 

```python
for 変数 in リスト:
    処理

```

#### 0から4までを繰り返す場合

=== "python"
    - 処理

    ```python
    >>> for i in (0,1,2,3,4):
    ...     print(i)
    ...
    0
    1
    2
    3
    4
    ```
    or 
    
    ```python
    >>> for i in range(5):
    ...     print(i)
    ...
    0
    1
    2
    3
    4
    ```
    or 
    ```python
    >>> for i in range(0,5):
    ...     print(i)
    ...
    0
    1
    2
    3
    4
    ```

=== "(参考) C言語の場合"
    ```C++
    for(unsigned int i=0; i<5; i++){
        std::cout << i << std::endl;
    }
    ```


#### リスト(a,b,c,d)をループする場合

=== "python"
    - 処理

    ```python
    >>>> myList = ["a", "b", "c", "d"]
    >>> for str in myList:
    ...     print(str)
    ...
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

=== "(参考) C言語の場合"
    ```C++
    for(unsigned int i=0; i<5; i++){
        std::cout << i << std::endl;
    }
    ```

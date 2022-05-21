# collectionsタイプの比較


## 1. list/tuple/dict/set
|       xxx        |    list     |    tuple    |            dict             |     set      | 補足説明 |
| :--------------- | :---------- | :---------- | :------------------------- | :----------- | :------- |
| 空宣言           | x = []       | x = ()      | -                          | x = {}       |          |
| 空宣言2          | x = list()   | x = tuple() | x = dict()                  | x = set()    |          |
| 宣言2            | x = [1, 2]   | x = (1, 2)  | x = {"key"1: 1, "key2": 2} | x = {1, 2}   |          |
| アクセス         | x[0]         | -           | x['key1']                  | -            |          |
| アクセス2        |              |             |                            |              |          |
| 追加             | x.append(4) | -           | x['key1']=4                | x.add(4)     |          |
| 更新             | x[0]=100    |  -           | x['key1']=100              | -             |          |
| 削除(最初) | del x[0]           |             |                            | x.discard(1) |          |
| 削除(最後尾) | x.pop()        |             |                            | x.discard(1) |          |
| 削除(キー指定) |x.pop(index)   |             |                            | x.discard(key) |          |
| 削除(エラーなし) |             |             |                            | x.discard(1) |          |
| 削除(エラーあり) |  x.remove(1) |             |                            | x.remove(1)  |          | listは値で削除
| 全削除           | x.clear()   |             |                            | x.clear()    |          |



## 2. strとlistの比較

|      xxx       |      str型      |      List型      |                補足説明                 |
| :------------- | :-------------- | :--------------- | :-------------------------------------- |
| 検索           | xxx.find("yyy") | xxx.index("yyy") | リストはインデックスなのでindexと覚える |
| 文字のカウント | xxx.count("y")  | xxx.count("y")   | 同じ                                    |
| 挿入           |                 |                  |                                         |
|                |                 |                  |                                         |

## 3. list/deque/heapの比較

|     xxx      |     list型     |           deque型            |         heap型          |          補足説明           |
| :----------- | :------------- | :--------------------------- | :---------------------- | :-------------------------- |
| 空宣言       | x= []          | x = collections.deque([],3)  | x= []  heapq.heapify(x) | dequeは第２引数でサイズ指定が可能 |
| 宣言         | x= [1]         | x = collections.deque([1],3) | x= [1] heapq.heapify(x) |                             |
| 末尾に挿入   | x.append(1)    | x.append(1)                  | heapq.heappush(1)       | heapは最小値が              |
| 末尾から削除 | x.pop()        | x.pop()                      | -                       |                             |
| 先頭に挿入   | x.insert(0, 1) | x.appendleft(1)              | heapq.heappush(1)       | heapは最小値が先頭に来る    |
| 先頭から削除 | del x[0]       | x.popleft()                  | heapq.heappop()         |                             |

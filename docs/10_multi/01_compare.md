# collectionsタイプの比較


|       xxx        |    list     |    tuple    |            map             |     set      | 補足説明 |
| :--------------- | :---------- | :---------- | :------------------------- | :----------- | :------- |
| 空宣言           | x = []      | x = ()      | -                          | x = {}       |          |
| 空宣言2          | x = list()  | x = tuple() | x = map()                  | x = set()    |          |
| 宣言2            | x = [1, 2]  | x = (1, 2)  | x = {"key"1: 1, "key2": 2} | x = {1, 2}   |          |
| アクセス         | x[0]        | -           | x['key1']                  | -            |          |
| アクセス2        |             |             |                            |              |          |
| 追加             | x.append(4) | -           | x['key1']=4                | x.add(4)     |          |
| 更新             | x[0]=100  |  -           | x['key1']=100              | -             |          |
| 削除(最後尾) | x.pop()        |             |                            | x.discard(1) |          |
| 削除(キー指定) |x.pop(index)   |             |                            | x.discard(key) |          |
| 削除(エラーなし) |             |             |                            | x.discard(1) |          |
| 削除(エラーあり) |  x.remove(1) |             |                            | x.remove(1)  |          | listは値で削除
| 全削除           | x.clear()   |             |                            | x.clear()    |          |
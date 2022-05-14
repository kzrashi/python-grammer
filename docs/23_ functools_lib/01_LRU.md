# lru_cache

## 1. overview
LRU(Least Recently Used)キャッシュとは、対象の関数の引数の組み合わせが同じばった場合には結果をキャッシュしておき、次回以降同じ組み合わせだった場合には、再計算せずにキャッシュを利用することで処理が早くなる  
デメリットはキャッシュ毎にメモリを使用すること

## 2. usage
- 標準のfunctoolモジュール内の`lru_cache`デコレータをimportする
- LRUキャッシュしたい関数の頭に`@lru_cache`のデコレータを付与する

```python  title="python 出力結果" hl_lines="2 10"
import time
from functools import lru_cache

def fib1(n):
    if n <= 1:
        return 1
    else:
        return fib1(n-1) + fib1(n-2)

@lru_cache(maxsize=None)
def fib1_cache(n):
    if n <= 1:
        return 1
    else:
        return fib1_cache(n-1) + fib1_cache(n-2)

# LRU cacheなし
start_time = time.perf_counter()
time.sleep(1)
fib1(39)
end_time = time.perf_counter()

# LRU cache有り
start_time2 = time.perf_counter()
time.sleep(1)
fib1_cache(39)
end_time2 = time.perf_counter()

# 経過時間を出力(秒)

print(end_time - start_time)
print(end_time2 - start_time2)
```

cacheすると、実質22s->0.003s(1秒waitを入れているため)まで高速化する
```python  title="python 出力結果"
22.380674303        ★cacheなし
1.0034929239999997  ★cacheあり
```


## 3. 参考
- [🍺Python3でLRUキャッシュを用いてプログラムを高速化](https://qiita.com/kotaroooo0/items/4d471932e299edd08b24)

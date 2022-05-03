# Counter
リストを出現率をカウントしてくれる


## basic

```python
import collections

l = [1,1,2,3,4,1,2]

collections.Counter(l)

```

## most_common()
降順に表示する

```python
import collections

l = [1,1,2,3,4,1,2]

counter = collections.Counter(l)

print(counter.most_common())
```
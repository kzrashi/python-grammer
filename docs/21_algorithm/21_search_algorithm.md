# 検索アルゴリズム




## 1. 線形検索(linear search / Sequential Search)
- 前提条件
  - リストがソートされている必要がある
  - 計算量(Time complexity): O(n)
  - 領域計算量(space complexity): 



python
```python
class SearchClass(object):
    def linearSearch(self, 
            nums:List[int], 
            target:int) -> bool:


        for num in nums:
            if num == target:
                return True

        # when not found target
        return False

if __name__ == "__main__":
    nums = [1,5,10,12,20,50]
    c = SearchClass()

    #一致する場合
    print(c.linearSearch(nums,5))
    #一致しない場合
    print(c.linearSearch(nums,6))
```

result
```python
True
False
```

## 2. バイナリサーチ(binary search)
### 2.1. 基本パターン
python
```python
class SearchClass(object):
    def binarySearch(self, 
            nums:List[int], 
            target:int) -> bool:

        sp = 0
        ep = len(nums) - 1
        
        while sp <= ep:
            mid = (sp + ep) // 2
            if nums[mid] == target:
                return True
            elif nums[mid] < target:
                sp = mid + 1
            else:
                ep = mid - 1

        # when not found target
        return False

if __name__ == "__main__":
    nums = [1,5,10,12,20,50]
    c = SearchClass()

    #一致する場合
    print(c.linearSearch(nums,5))
    #一致しない場合
    print(c.linearSearch(nums,6))
```

### 2.2. 再帰パターン1
```python
class SearchClass(object):
    def binarySearchRecursive1(self, 
            nums:List[int], 
            sp:int, 
            ep:int, 
            target:int) -> bool:

        if sp > ep:
            return False
        
        mid = (sp + ep) // 2
        if nums[mid] == target:
            return True
        elif nums[mid] < target:
            return self.binarySearchRecursive1(nums, mid+1, ep, target)
        else:
            return self.binarySearchRecursive1(nums, sp, ep-1, target)

if __name__ == "__main__":
    nums = [1,5,10,12,20,50]
    c = SearchClass()

    #一致する場合
    print(c.binarySearchRecursive1(nums,0,len(nums)-1,5))
    #一致しない場合
    print(c.binarySearchRecursive1(nums,0,len(nums)-1,6))
```

### 2.3. 再帰パターン2
```python
class SearchClass(object):
    def binarySearchRecursive2(self,
            nums:List[int], 
            target:int) -> bool:

        mid = (len(nums) - 1) // 2
        if nums[mid] == target:
            return True
        elif len(nums) <= 1:
            # not found targe
            return False
        elif nums[mid] < target:
            return self.binarySearchRecursive2(nums[mid+1:], target)
        else:
            return self.binarySearchRecursive2(nums[:mid], target)

if __name__ == "__main__":
    nums = [1,5,10,12,20,50]
    c = SearchClass()

    #一致する場合
    print(c.binarySearchRecursive2(nums,5))
    #一致しない場合
    print(c.binarySearchRecursive2(nums,6))
```



result
```python
True
False
```

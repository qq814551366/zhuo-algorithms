# counter计数类

```
class Solution:
    def canConstruct(self, ransomNote: str, magazine: str) -> bool:
        a = Counter(ransomNote) 
        b = Counter(magazine)
		# 与操作可以获得并集，并集对第一个数进行判断
        return (a & b) == a
```

# 一行for循环
``` python
class Solution:
    def majorityElement(self, nums: List[int]) -> List[int]:
        n = len(nums) // 3
        b = Counter(nums)
        return [k for k,v in b.items() if v>n ]
```
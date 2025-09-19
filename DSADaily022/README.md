## 704. Binary Search
leetcode problem link: `https://leetcode.com/problems/binary-search/description/`
## Solution (Python)

the search is done over sorted array.
but the question is why. why binary search requires sorted array and how does it function.
 

```python
def search(nums, target):
  left = 0
  right = len(nums) - 1
  while left <= right:
    mid = (left + right) // 2
    if nums[mid] == target:
      return mid 
    elif nums[mid] < target:
      left = mid + 1 
    else:
      right = mid - 1  
  
  return -1
```


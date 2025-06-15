## 167. Two Sum II - Input Array Is Sorted
leetcode problem link: `https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/description/`
## Solution (Python)

to add *key,value* pair in an empty dict: `my_dict["key"] = "value"`, here we used *element : index*

```python
def twoSum(numbers, target):
  lis = {}
  for i in range(len(numbers)):
    fin = target - numbers[i]
    if fin in lis:
      return [lis[fin] + 1, i + 1]
    lis[numbers[i]] = i
```


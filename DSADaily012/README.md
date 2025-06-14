## 128. Longest Consecutive Sequence
leetcode problem link: `https://leetcode.com/problems/longest-consecutive-sequence/description/`
## Solution (Python)

to sort and remove the dupliclates in an array- **`a= sorted(set(nums))`**

```python
def longestConsecutive(nums):
  if not nums:
    return 0
  nums = sorted(set(nums))
  least = nums[0]
  ccur = 1
  longest = 1

  for i in nums[1:]:
    if i == least + 1:
      ccur += 1
      longest = max(longest, ccur)
    else:
      ccur = 1
      least = i
  return longest

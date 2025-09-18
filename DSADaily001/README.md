## 49. Group Anagrams
leetcode problem link: `https://leetcode.com/problems/group-anagrams/description/`

- used defaultdict to group words by sorted letters (anagrams)
- sorted(word) ensures letter counts are considered
## Solution (Python)
```python
def groupAnagrams(self, strs):
from collections import defaultdict

a = defaultdict(list)
for word in strs:
  key = ''.join(sorted(word))
  a[key].append(word)

return list(a.values())
```

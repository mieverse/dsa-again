## 125. Valid Palindrome
leetcode problem link: `https://leetcode.com/problems/valid-palindrome/description/`
## Solution (Python)

it is to be noted that: *valid palindrome condition depends on **symmetry**, not length.*

to convert to lower case: **`a= text.lower()`**

to remove non alphanumerical chars: **`clean= ''.join(char for char in text if char.isalnum())`**

there are few approaches that i can think of:
- reverse string
- two pointers ✔

```python

  clean = ''.join(char.lower() for char in s if char.isalnum())
  if not clean:
    return True
  i = 0
  j = len(clean) - 1
  while i <= j:
    if clean[i] == clean[j]:
      i += 1
      j -= 1
    else:
      return False 
  return True
```


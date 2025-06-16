## 206. Reverse Linked List
leetcode problem link: `https://leetcode.com/problems/reverse-linked-list/description/`

Definition for singly-linked list:
```python
class ListNode(object):
  def __init__(self, val=0, next=None):
    self.val = val
    self.next = next
```
## Solution (Python)
```python
def reverseList(head):
  prev = None
  curr = head
  while curr:
    temp = curr.next
    curr.next = prev
    prev = curr
    curr = temp
  return prev
```

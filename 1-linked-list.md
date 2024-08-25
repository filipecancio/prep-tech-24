# 876. Middle of the Linked List
### Important links
- [back to home](https://github.com/filipecancio/leetcode-exercises)
- [Leetcode Description] (https://leetcode.com/problems/middle-of-the-linked-list/)
- [Related issue](https://github.com/filipecancio/leetcode-exercises/issues/1)

### Solutions
<details>
  <summary>Kotlin solution </summary>
    
```kotlin
/**
 * Example:
 * var li = ListNode(5)
 * var v = li.`val`
 * Definition for singly-linked list.
 * class ListNode(var `val`: Int) {
 *     var next: ListNode? = null
 * }
 */
class Solution {
    fun middleNode(head: ListNode?): ListNode? {
        var i = head
        var j = head
        while (i?.next?.next != null){
            j = j?.next
            i = i?.next?.next
        }
        if(i?.next != null) j = j?.next
        return j
    }
}
```
    
</details>

<details>
  <summary>Python solution </summary>

```python3
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if head == None or head.next == None:
            return head

        i = head
        j = head

        while i.next != None and i.next.next != None:
            j = j .next
            i = i.next.next

        if i.next != None:
            j = j.next
        return j
```

</details>

<details>
  <summary>Dart solution </summary>


```dart
/**
 * Definition for singly-linked list.
 * class ListNode {
 *   int val;
 *   ListNode? next;
 *   ListNode([this.val = 0, this.next]);
 * }
 */
class Solution {
  ListNode? middleNode(ListNode? head) {
        ListNode? i = head;
        ListNode? j = head;

        while (i?.next?.next != null) {
            j = j?.next;
            i = i?.next?.next;
        }

        if( i?.next != null) j = j?.next;

        return j;
  }
}
```

</details>

# 876. Middle of the Linked List
### Important links
- [back to home](https://github.com/filipecancio/leetcode-exercises)
- [Leetcode Description] (https://leetcode.com/problems/middle-of-the-linked-list/)

### Kotlin solution
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

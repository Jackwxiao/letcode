**题目描述：**

给你单链表的头节点 head ，请你反转链表，并返回反转后的链表
输入：` head = [1,2,3,4,5] `
输出：` [5,4,3,2,1] `

js解法:

```js
var reverseList = function (head) {
    let prev = null
    let curr = head
    while (curr) {
        const next = curr.next
        curr.next = prev
        prev = curr
        curr = next
    }
    return prev
}
```

python 解法：

```python
def reverseList(self, head: ListNode) -> ListNode:
    prev, curr = None, head
    while curr is not None:
        next = curr.next
        curr.next = prev
        prev = curr
        curr = next
    return prev
```
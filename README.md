# LL: Find Kth Node From End ( ** Interview Question)

Implement the `find_kth_from_end` function, which takes the `LinkedList` (`ll`) and an integer `k` as input, and returns the k-th node from the end of the linked list **WITHOUT USING LENGTH**.

Given this LinkedList:
`1 -> 2 -> 3 -> 4`

- If `k=1` then return the first node from the end (the last node) which contains the value of `4`.
- If `k=2` then return the second node from the end which contains the value of `3`, etc.
- If the index is out of bounds, the program should return `None`.

### Requirements

The `find_kth_from_end` function should follow these requirements:

- The function should utilize two pointers, `slow` and `fast`, initialized to the head of the linked list.
- The `fast` pointer should move `k` nodes ahead in the list.
- If the `fast` pointer becomes `None` before moving `k` nodes, the function should return `None`, as the list is shorter than `k` nodes.
- The `slow` and `fast` pointers should then move forward in the list at the same time until the `fast` pointer reaches the end of the list.
- The function should return the `slow` pointer, which will be at the k-th position from the end of the list.

**Note:** This is a separate function that is not a method within the LinkedList class. This means you need to indent the function all the way to the LEFT.

### Pseudo Code
initialize slow and fast pointers to the head of the linked list

    for i in range(k):

      if fast pointer is None:
        return None (list is shorter than k)
      move fast pointer to the next node

    while fast pointer is not None:
      move slow pointer to the next node
      move fast pointer to the next node

    return the slow pointer # k-th node from the end

Stack is an Abstract Data Type (ADT) that defines a collection of elements with operations based on the LIFO (Last In, First Out) principle. A stack ADT describes what operations can be performed, but not how they are implemented.

The main operations of Stack ADT are:

push(x): Insert an element on top of the stack.

pop(): Remove and return the top element.

peek() / top(): Return the top element without removing it.

isEmpty(): Check if the stack has no elements.

isFull(): (Optional) Check if the stack is full.

size(): Returns number of elements.

Note:

Stack ADT does not specify if stack is implemented using array, linked list, or anything else.

It only defines the behavior and operations.


Example: Stack ADT — Logical Explanation

Imagine you're designing a system where multiple programmers will use a stack.

To keep the system flexible, you don’t tell them how the stack works internally.
You only tell them the rules (operations) they are allowed to perform:

push(x) → insert an element

pop() → remove and return top element

top() → read the top

isEmpty()

size()

This is the Stack ADT:

A specification of operations without revealing or depending on the internal implementation.

Now the logical part:

You can implement this ADT in different ways:

Implementation A → Array

top moves from 0 → n-1

memory is fixed

push = arr[++top]

pop = arr[top--]

Implementation B → Linked List

top is a pointer to the head node

memory grows dynamically

push = create new node

pop = delete head

Implementation C → Dynamic array (vector)

size doubles automatically

no overflow

But here’s the logical point:

Even though the internal mechanisms are different, the outside behavior remains EXACTLY the same, because all follow the Stack ADT rules.

That’s what makes it an ADT.

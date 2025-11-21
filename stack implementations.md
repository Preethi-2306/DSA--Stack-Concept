[KEEP BESIDE THE RUNNING NOTES THE CODING BOOK]
1)STACK DEFINITION :-A stack is a linear data structure that follows the LIFO (Last In, First Out) principle. Both insertion and deletion take place only at one end, called the top of the stack. Common operations include push, pop, and peek.
<img width="660" height="405" alt="image" src="https://github.com/user-attachments/assets/6befe54c-5140-4693-8095-8075468f9a9f" />

2)STACK EXAMPLE:- ,stack of plates ,undo/redo, recursion, back button or real life example
Basic Terminologies of Stack
Top: The position of the most recently inserted element. Insertions (push) and deletions (pop) are always performed at the top.
Size: Refers to the current number of elements present in the stack.

3)Types of Stack:
Fixed Size Stack-A fixed size stack has a predefined capacity.
->Once it becomes full, no more elements can be added (this causes overflow).
->If the stack is empty and we try to remove an element, it causes underflow.
->Typically implemented using a static array.Example: Declaring a stack of size 10 using an array.

Dynamic Size Stack
A dynamic size stack can grow and shrink automatically as needed.
If the stack is full, its capacity expands to allow more elements.
As elements are removed, memory usage can shrink as well.
Can be implemented using:
-> Linked List → grows/shrinks naturally.
-> Dynamic Array (like vector in C++ or ArrayList in Java) → resizes automatically.
Example: Stack implementation using linked list or resizable array.

4)Stack is an Abstract Data Type (ADT) that defines a collection of elements with operations based on the LIFO (Last In, First Out) principle. A stack ADT describes what operations can be performed, but not how they are implemented.

The main operations of Stack ADT are:- push(x): Insert an element on top of the stack.->pop(): Remove and return the top element.
->peek() / top(): Return the top element without removing it.
->isEmpty(): Check if the stack has no elements.
->isFull(): (Optional) Check if the stack is full.
->size(): Returns number of elements.

Note:Stack ADT does not specify if stack is implemented using array, linked list, or anything else.It only defines the behavior and operations.

Example: Stack ADT — Logical ExplanationImagine you're designing a system where multiple programmers will use a stack.To keep the system flexible, you don’t tell them how the stack works internally.You only tell them the rules (operations) they are allowed to perform:

push(x) → insert an element
pop() → remove and return top element
top() → read the top
isEmpty()
size()

This is the Stack ADT:A specification of operations without revealing or depending on the internal implementation.

Now the logical part:You can implement this ADT in different ways:

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
Even though the internal mechanisms are different, the outside behavior remains EXACTLY the same, because all follow the Stack ADT rules.That’s what makes it an ADT.

5) STACK IMPLEMENTATION:-
[STACK USING ARRAY]- All these have same time complexity O(1) except for push the O(n)will occur for vecto
We maintain two important things:
->arr[]: The array to store stack elements.
->top: An integer which stores the index of the current top. Initially, top = -1. 
size: Maximum number of elements stack can hold (size of array). 
[push()]- 
->The push operation inserts a new element at the top of the stack.
->Before inserting, it must check for overflow: if top == max - 1, the stack is full and no new element can be added.
->If there is space, the operation increments top by one and stores the incoming value at stack[top].
->Since both the array and the top variable are used by all stack functions, they are usually declared globally for easier access.
->Push does not return anything; it simply updates the stack by placing the new value in the next available position.

[pop()]-very important]
->The stack stores elements in an array, and `top` always points to the current top index.
->During a pop, the element cannot be physically removed from the array, so the top element is first saved in a temporary variable and then `top` is simply decremented.
->This makes the stack treat the next element as the new top, while the old value remains in memory but is ignored. The saved value is returned to the caller. Before doing this, the function must check for underflow: if `top == -1`, the stack is empty and popping is not allowed.
 <img width="857" height="478" alt="image" src="https://github.com/user-attachments/assets/28e7bd2b-6d83-4ba6-8261-a2f204b18df3" />
UNDERFLOW CONDITION:- <img width="848" height="466" alt="image" src="https://github.com/user-attachments/assets/75f6b8cc-8edc-4ad8-8126-243344e69cea" /> and so the exit(1);-means abnormal termination.

[IsFull & IsEmpty]-Return type:-Both functions return integers (0 or 1), so return type must be int.

Why isFull() is needed
In the push function, we normally check top == max - 1 to detect stack overflow.But sometimes the user may want to check if the stack is full separately, not only during push.So we write a separate function isFull() to check stack fullness anytime.
->How isFull() works
It checks: top == max - 1
If true → return 1 (stack is full)
If false → return 0 (stack is not full)
The push function can simply call isFull() instead of writing the condition again.

->Why isEmpty() is needed
In pop(), we normally check top == -1 to detect stack underflow.But sometimes the user may want to check if the stack is empty separately, before popping or for some other purpose.So we write a separate function isEmpty().

->How isEmpty() works
It checks: top == -1
If true → return 1 (stack is empty)
If false → return 0 (stack has elements)
The pop() function can call isEmpty() instead of repeating the condition.

6) STACK OPERATIONS:-
  <img width="994" height="686" alt="image" src="https://github.com/user-attachments/assets/3615d958-8edc-4f84-a4d1-b3557c5ef567" />

7) TIME COMPLEXITIES:-  all in notes

8) VERY IMPORTANT STACK APPLICATIONS:- A) Reversing a String or List-Elements pushed and popped to reverse order. B)Balanced Parentheses Checking-To verify valid brackets in expressions.C)Browser Navigation-Back/forward operations use stacks.D)Expression Conversion-Used to convert infix → postfix/prefix.
E)Function Calls / Recursion-Call stack stores activation records.F)Undo/Redo Operations-Editors and software maintain history using stacks

9) STACK PROBLEMS:-
10) EDGE CASES:-
11) VISUALIZATIONS

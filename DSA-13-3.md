# Data-Structures-using-Python-13-3
## AIM:

To implement a Stack using Python lists and built-in methods append() and pop().

## ALGORITHM:

Step 1 : Create a class Stack with:

a) push(L): Push all elements from list L to stack.

b) pop(x): Pop x elements from the stack.

c) peek(): Display current elements in the stack.

Step 2 : Get size of list from user input.

Step 3 : Create a list of odd numbers up to the input size.

Step 4 : Get the number of elements to pop from user.

Step 5 : Call respective methods for push, pop, and peek.

## PROGRAM :

```
stack = []
class st:
    def push(self,S):
        for i in S:
            stack.append(i)
        return
    def pop(self):
        if stack:
            print("Element popped : ",stack.pop())
        else:
            print("stack is empty")
        return
    def peek(self):
        if stack:
            print("Elements in the stack\n",stack)
        return
    
s=st()
size=int(input())
l=[i for i in range(1,size) if i%2!=0]
s.push(l)
s.peek()
s.pop()
s.peek()
```

## OUTPUT :

![image](https://github.com/user-attachments/assets/8d130b29-ec86-4cf4-a563-10aca141a22b)

## RESULT : 

Thus the implemention of a Stack using Python lists and built-in methods append() and pop() is successfully verified.

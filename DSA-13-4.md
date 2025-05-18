# Data-Structures-using-Python-13-4

## AIM : 

To implement a Python program that evaluates a valid prefix expression using a stack and supports basic binary operators (+, -, *, /) with single-digit numbers.

## ALGORITHM :

Step 1 : Define a set of operators: +, -, *, /.

Step 2 : Read the prefix expression as a space-separated string from the user.

Step 3 : Split the string into tokens and reverse the order for evaluation (since it's prefix).

Step 4 : Traverse each token:

a) If it's a number, convert it to float and push onto the stack.

b) If it's an operator, pop two values from the stack, apply the operator, and push the result back.

Step 5 : After traversal, the stack will have one element — the final result.

Step 6 : Return and display the result.

## PROGRAM :

```
OPERATORS=set(['*','-','+','/'])
stack=[]
    
def prefix_Eval(x):
    for i in x[::-1]:
        if i not in OPERATORS:
            stack.append(float(i))
        else:
            a=stack.pop()
            b=stack.pop()
            
            if i=='+':
                stack.append(a+b)
            elif i=='-':
                stack.append(a-b)
            elif i=='*':
                stack.append(a*b)
            elif i=='/':
                stack.append(a/b)
    return stack[0]

m =input()
print("The prefix expression is",m)
n=m.split()
print("The result is",prefix_Eval(n))
```

## OUTPUT :

![image](https://github.com/user-attachments/assets/9424a18b-8e5f-4ae0-b560-162da1643fd8)

## RESULT :

Thus the  implemention of  a Python program that evaluates a valid prefix expression using a stack and supports basic binary operators (+, -, *, /) with single-digit numbers is verified successfully.

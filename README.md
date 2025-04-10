# Data-Structures-using-Python-13-Module-1


##AIM:

To convert an infix expression into its equivalent postfix expression by using a stack. 


##PROGRAM:

```
Operators = set(['+', '-', '*', '/', '(', ')', '^'])  
Priority = {'+':1, '-':1, '*':2, '/':2, '^':3} 
 
 
def infixToPostfix(expression): 

    stack = [] 
    output = '' 
    for char in expression:
        if char not in Operators:
            output+=char
        elif char=='(':
            stack.append('(')
        elif char==')':
            while stack and stack[-1]!='(':
                output+=stack.pop()
            stack.pop()
        else:
            while stack and stack[-1]!='(' and Priority[char]<=Priority[stack[-1]]:
                output+=stack.pop()
            stack.append(char)
    while stack:
        output+=stack.pop()
    return output
    
expression = input()
print("Infix notation: ",expression)
print("Postfix notation: ",infixToPostfix(expression))

```


##OUTPUT:

![image](https://github.com/user-attachments/assets/0fdf0065-f275-48b7-ace2-af211b590937)


##RESULT:

Thus conversion of infix expression into its equivalent postfix expression by using a stack is proved successfully.

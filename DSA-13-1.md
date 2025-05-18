# Data-Structures-using-Python-13-1


## AIM:

To convert an infix expression into its equivalent postfix expression by using a stack. 

## ALGORITHM:

Step 1 : Start the program.

Step 2 : Initialize an empty stack to hold operators and an empty string for the output.

Step 3 : For each character in the infix expression:

a) If the character is an operand , add it directly to the output.

b) If the character is a left parenthesis (, push it onto the stack.

c) If the character is a right parenthesis ), pop from the stack to the output until a left parenthesis.

d) If the character is an operator, pop operators from the stack to the output while they have greater or equal precedence than the current operator.
           
Step 4 : After reading all characters, pop any remaining operators from the stack to the output.

Step 5 : Return the output string as the postfix expression.

Step 6 : Stop the program.

## PROGRAM:

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


## OUTPUT:

![image](https://github.com/user-attachments/assets/0fdf0065-f275-48b7-ace2-af211b590937)


## RESULT:

Thus conversion of infix expression into its equivalent postfix expression by using a stack is proved successfully.

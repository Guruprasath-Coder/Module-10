# # Stack-Stack Reversal Program 🔁

This Python program demonstrates how to reverse the values in a stack using basic stack operations like push and pop.

## 🎯 Aim

To write a Python program that reverses the values in a stack using standard stack operations.

## 📋 Algorithm

1. Create an empty stack.
2. Read an integer `n` from the user (number of elements to push).
3. Loop `n` times:
   - Read an integer from the user.
   - Push it onto the stack.
4. Create an empty list called `reverse`.
5. While the stack is not empty:
   - Pop the top element.
   - Append it to `reverse`.
6. Print the reversed list.


### Program:
~~~
def insertAtBottom(s, item):
    if not s:
        s.append(item)
        return
    top = s.pop()
    insertAtBottom(s, item)
    s.append(top)

def reverseStack(s):
 
    if not s:
        return
 
    item = s.pop()
    reverseStack(s)
 
    insertAtBottom(s, item)
    return s
l=[]
n=int(input())
for i in range(n):
    l.append(int(input()))
print(reverseStack(l))
~~~

## 🧪 Sample Input and Output
<img width="604" height="289" alt="image" src="https://github.com/user-attachments/assets/04d483da-1f63-4739-9d14-d32501de8700" />


## Result
Thus the output is verified.

# Queue-Remove Two String Values from the Rear End in Python 🧵

This Python program demonstrates how to manage a list of strings and remove the last two elements (i.e., from the rear of the list).

## 🎯 Aim

To write a Python program to:
- Accept `n` string values from the user
- Remove the last two values (rear end of the list)
- Display the updated list

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` from the user (number of strings).
3. Loop `n` times:
   - Read a string input.
   - Append it to the list `q`.
4. Remove the last element using `pop()`.
5. Remove the next last element using `pop()` again.
6. Display the updated list.

##  Program:
```python
# Initialize empty list
q = []

# Number of string elements
n = int(input("Enter number of string elements: "))

# Read string inputs
for i in range(n):
    val = input(f"Enter string element {i+1}: ")
    q.append(val)

# Remove last two elements
if len(q) >= 2:
    q.pop()
    q.pop()
elif len(q) == 1:
    q.pop()

# Display the updated list
print("Updated list after removing last two elements:")
print(q)


### Output:
Enter number of string elements: 5
Enter string element 1: apple
Enter string element 2: banana
Enter string element 3: cherry
Enter string element 4: date
Enter string element 5: elderberry
Updated list after removing last two elements:
['apple', 'banana', 'cherry']

## Result:
The Python program successfully removes the last two string values from the list and displays the updated list.

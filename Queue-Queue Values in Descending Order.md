# Queue-Queue Values in Descending Order Using Python 🧮

This Python program simulates a queue using a list, removes the first two elements (FIFO order), and displays the remaining values in descending order.

## 🎯 Aim

To write a Python program to:
- Accept user inputs into a list (queue)
- Remove the first two elements (simulating dequeue)
- Display the remaining values in **descending order**

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` to determine how many elements will be added.
3. Loop `n` times:
   - Read an input value.
   - Append it to the list `q`.
4. Remove the first element using `pop(0)`.
5. Remove the second element using `pop(0)` again.
6. Sort the list in descending order.
7. Print the updated list.

## 🧪 Program: 
```python
# Initialize empty queue
q = []

# Number of elements
n = int(input("Enter number of elements in the queue: "))

# Read elements
for i in range(n):
    val = int(input(f"Enter element {i+1}: "))
    q.append(val)

# Remove first two elements (FIFO)
if len(q) >= 2:
    q.pop(0)
    q.pop(0)
elif len(q) == 1:
    q.pop(0)

# Sort remaining elements in descending order
q.sort(reverse=True)

# Display the result
print("Queue after removing first two elements and sorting in descending order:")
print(q)

### Output:
Enter number of elements in the queue: 5
Enter element 1: 10
Enter element 2: 20
Enter element 3: 5
Enter element 4: 15
Enter element 5: 25
Queue after removing first two elements and sorting in descending order:
[25, 15, 5]

## Result:
The Python program successfully simulates a queue, removes the first two elements, and displays the remaining values in descending order.

# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
```python
class CircularQueue:
    def __init__(self, size):
        self.size = size
        self.queue = [None] * size
        self.front = -1
        self.rear = -1

    def enqueue(self, value):
        # Check if queue is full
        if (self.rear + 1) % self.size == self.front:
            print("Queue is Full! Cannot insert:", value)
            return

        # Insert first element
        if self.front == -1:
            self.front = 0
            self.rear = 0
            self.queue[self.rear] = value
        else:
            self.rear = (self.rear + 1) % self.size
            self.queue[self.rear] = value

    def dequeue(self):
        # Check if queue is empty
        if self.front == -1:
            print("Queue is Empty! Cannot dequeue.")
            return None

        removed = self.queue[self.front]

        # If only one element
        if self.front == self.rear:
            self.front = -1
            self.rear = -1
        else:
            self.front = (self.front + 1) % self.size

        return removed

    def display(self):
        if self.front == -1:
            print("Queue is Empty!")
            return
        i = self.front
        print("Queue elements:", end=" ")
        while True:
            print(self.queue[i], end=" ")
            if i == self.rear:
                break
            i = (i + 1) % self.size
        print()


# ---- Main Program ----
cq = CircularQueue(5)

print("Enter 3 values for the queue:")
for _ in range(3):
    val = int(input("Enter value: "))
    cq.enqueue(val)

print("\nInitial Queue State:")
cq.display()

print("\nRemoving 3 values:")
for _ in range(3):
    removed = cq.dequeue()
    if removed is not None:
        print("Removed:", removed)

print("\nFinal Queue State:")
cq.display()


### Output:
Enter 3 values for the queue:
Enter value: 10
Enter value: 20
Enter value: 30

Initial Queue State:
Queue elements: 10 20 30 

Removing 3 values:
Removed: 10
Removed: 20
Removed: 30

Final Queue State:
Queue is Empty!

## Result:

The Circular Queue was successfully implemented in Python. The program:

Accepted 3 values from the user.

Performed enqueue and dequeue operations.

Displayed the removed values and final queue state.

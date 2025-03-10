# Stack and Queue Data Structures

## Stack
### What is a Stack?
A **stack** is a linear data structure that follows the **Last In, First Out (LIFO)** principle. This means that the last element added to the stack is the first one to be removed.

### How does it work?
A stack works by allowing operations at only one end, called the **top** of the stack. It functions like a stack of plates—when you add a plate, you place it on top, and when you remove one, you take it from the top.

![Stack Diagram](file-C6pgPNzTX7F3jMPfcnjxQf)

### Where is it used?
Stacks are widely used in:
- **Function calls and recursion** (call stack management)
- **Expression evaluation** (infix to postfix conversion, postfix evaluation)
- **Undo/Redo functionality** in text editors
- **Backtracking algorithms** (like maze solving, depth-first search in graphs)
- **Balancing symbols** (like checking balanced parentheses in expressions)

### Why do we use it?
Stacks provide a simple way to manage data where the order of processing is important. They are used when we need to **store and retrieve data in a LIFO order** efficiently.

### Time and Space Complexity
- **Push operation:** O(1)
- **Pop operation:** O(1)
- **Peek operation:** O(1)
- **Space complexity:** O(n) (where n is the number of elements in the stack)

### Stack Operations:
1. **Push** - Add an element to the top of the stack.
2. **Pop** - Remove the top element from the stack.
3. **Peek/Top** - Get the top element without removing it.
4. **isEmpty** - Check if the stack is empty.
5. **Size** - Get the number of elements in the stack.

### C++ Implementation
```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> s;
    s.push(10);
    s.push(20);
    s.push(30);
    
    cout << "Top element: " << s.top() << endl;
    s.pop();
    cout << "Top after pop: " << s.top() << endl;
    cout << "Stack size: " << s.size() << endl;
    
    return 0;
}
```

### JavaScript Implementation
```js
class Stack {
    constructor() {
        this.items = [];
    }
    push(element) {
        this.items.push(element);
    }
    pop() {
        return this.items.pop();
    }
    peek() {
        return this.items[this.items.length - 1];
    }
    isEmpty() {
        return this.items.length === 0;
    }
    size() {
        return this.items.length;
    }
}

const s = new Stack();
s.push(10);
s.push(20);
s.push(30);
console.log("Top element:", s.peek());
s.pop();
console.log("Top after pop:", s.peek());
console.log("Stack size:", s.size());
```

---

## Queue
### What is a Queue?
A **queue** is a linear data structure that follows the **First In, First Out (FIFO)** principle. This means that the first element added is the first one to be removed.

### How does it work?
A queue works like a real-life queue (such as people standing in line for a bus). The element inserted first is processed first. It has two ends:
- **Front**: The end where elements are removed.
- **Rear**: The end where elements are added.

![Queue Diagram](file-5yNe1pqbjMc1MT918yAsDT)

### Where is it used?
Queues are widely used in:
- **Task scheduling** (CPU scheduling, job scheduling)
- **Handling requests** in web servers
- **Breadth-first search (BFS)** in graphs and trees
- **Printing tasks in a printer queue**
- **Data transmission in networking**

### Why do we use it?
Queues provide an efficient way to process elements in a **FIFO manner**. They are useful when data needs to be processed in order, without skipping elements.

### Time and Space Complexity
- **Enqueue operation:** O(1)
- **Dequeue operation:** O(1)
- **Front operation:** O(1)
- **Space complexity:** O(n) (where n is the number of elements in the queue)

### Queue Operations:
1. **Enqueue** - Add an element to the rear of the queue.
2. **Dequeue** - Remove an element from the front of the queue.
3. **Front** - Get the front element without removing it.
4. **isEmpty** - Check if the queue is empty.
5. **Size** - Get the number of elements in the queue.

### C++ Implementation
```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<int> q;
    q.push(10);
    q.push(20);
    q.push(30);
    
    cout << "Front element: " << q.front() << endl;
    q.pop();
    cout << "Front after dequeue: " << q.front() << endl;
    cout << "Queue size: " << q.size() << endl;
    
    return 0;
}
```

### JavaScript Implementation
```js
class Queue {
    constructor() {
        this.items = [];
    }
    enqueue(element) {
        this.items.push(element);
    }
    dequeue() {
        return this.items.shift();
    }
    front() {
        return this.items[0];
    }
    isEmpty() {
        return this.items.length === 0;
    }
    size() {
        return this.items.length;
    }
}

const q = new Queue();
q.enqueue(10);
q.enqueue(20);
q.enqueue(30);
console.log("Front element:", q.front());
q.dequeue();
console.log("Front after dequeue:", q.front());
console.log("Queue size:", q.size());
```

---

## Priority Queue
A **priority queue** is a special type of queue where elements are dequeued based on priority rather than FIFO order.

### Use Cases:
- **Dijkstra’s shortest path algorithm**
- **Task scheduling in operating systems**
- **Huffman coding (data compression)**

### Deque (Double-Ended Queue)
A **deque** allows insertion and deletion at both ends.

### Circular Queue
A **circular queue** is a queue where the last position is connected back to the first, making it efficient in memory usage.

I will add detailed explanations and code for these advanced queues next!

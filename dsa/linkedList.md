# Linked List Data Structure

## Introduction
A **Linked List** is a linear data structure in which elements (nodes) are stored in memory non-contiguously. Each node consists of two parts:
1. **Data**: The value stored in the node.
2. **Pointer**: A reference to the next node in the sequence.

Unlike arrays, linked lists do not require a contiguous block of memory and can dynamically grow or shrink during execution.

## Types of Linked Lists
1. **Singly Linked List**: Each node points to the next node.
2. **Doubly Linked List**: Each node contains pointers to both the next and previous nodes.
3. **Circular Linked List**: The last node points back to the first node, making a circular structure.

## Basic Operations
- **Insertion**: Add a node at the beginning, end, or a specific position.
- **Deletion**: Remove a node from the beginning, end, or a specific position.
- **Search**: Find a node with a specific value.
- **Traversal**: Visit all nodes in sequence.

## Singly Linked List Implementation

### **C++ Implementation**
```cpp
#include <iostream>
using namespace std;

class Node {
public:
    int data;
    Node* next;
    Node(int val) { data = val; next = nullptr; }
};

class LinkedList {
public:
    Node* head;
    LinkedList() { head = nullptr; }

    void insertAtEnd(int val) {
        Node* newNode = new Node(val);
        if (!head) {
            head = newNode;
            return;
        }
        Node* temp = head;
        while (temp->next) temp = temp->next;
        temp->next = newNode;
    }

    void display() {
        Node* temp = head;
        while (temp) {
            cout << temp->data << " -> ";
            temp = temp->next;
        }
        cout << "NULL" << endl;
    }
};

int main() {
    LinkedList list;
    list.insertAtEnd(10);
    list.insertAtEnd(20);
    list.insertAtEnd(30);
    list.display();
    return 0;
}
```

### **JavaScript Implementation**
```javascript
class Node {
    constructor(value) {
        this.value = value;
        this.next = null;
    }
}

class LinkedList {
    constructor() {
        this.head = null;
    }

    insertAtEnd(value) {
        const newNode = new Node(value);
        if (!this.head) {
            this.head = newNode;
            return;
        }
        let temp = this.head;
        while (temp.next) {
            temp = temp.next;
        }
        temp.next = newNode;
    }

    display() {
        let temp = this.head;
        let result = "";
        while (temp) {
            result += temp.value + " -> ";
            temp = temp.next;
        }
        result += "NULL";
        console.log(result);
    }
}

const list = new LinkedList();
list.insertAtEnd(10);
list.insertAtEnd(20);
list.insertAtEnd(30);
list.display();
```

## Summary
- Linked Lists provide dynamic memory allocation.
- Different types include Singly, Doubly, and Circular Linked Lists.
- Operations such as insertion, deletion, traversal, and search are fundamental.
- Implementation in both **C++** and **JavaScript** shows practical usage.

This documentation provides an overview of linked lists, their operations, and practical implementations in **C++** and **JavaScript**.

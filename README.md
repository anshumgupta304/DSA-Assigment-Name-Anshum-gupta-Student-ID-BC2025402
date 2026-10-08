# DSA-Assigment-Name-Anshum-gupta-Student-ID-BC2025402
this is my first project in DSA
Circular Queue Using Array

Description

This project implements a Circular Queue using an array in C language.

A Circular Queue follows the FIFO (First In, First Out) principle. Unlike a simple linear queue, it reuses the empty positions created after deletion.

Operations

The queue supports the following operations:

- ENQUEUE(x) - Inserts an element into the queue.
- DEQUEUE() - Removes an element from the front.
- FRONT() - Displays the front element.
- DISPLAY() - Displays all queue elements.
- EXIT - Terminates the program.

Full and Empty Conditions

Empty Queue

The queue is empty when:

"front == -1"

Full Queue

The queue is full when:

"(rear + 1) % SIZE == front"

This condition helps distinguish a full queue from an empty queue.

Circular Queue vs Linear Queue

Feature| Linear Queue| Circular Queue
Memory utilization| Less efficient| Better utilization
Reuses deleted positions| No, normally not| Yes
Rear movement| Only forward| Wraps around
ENQUEUE| O(1)| O(1)
DEQUEUE| O(1)| O(1)
Space| O(n)| O(n)

Why Circular Queue Uses Memory Better

In a linear queue, after some elements are deleted from the beginning, those empty positions generally cannot be reused once "rear" reaches the last array index.

A circular queue solves this problem by connecting the last position back to the first position. Therefore, the queue can reuse previously freed positions.

Problem in Linear Queue

Suppose the queue size is 5:

"[_, _, 30, 40, 50]"

Here, the first two positions are empty. However, if "rear" has already reached index 4, a simple linear queue may report that the queue is full even though two positions are unused.

This situation is called false overflow.

Complexity

Time Complexity

- ENQUEUE: O(1)
- DEQUEUE: O(1)
- FRONT: O(1)
- DISPLAY: O(n)

Space Complexity

- O(n)

where "n" is the size of the queue.

Language

C

How to Run

Compile:

gcc circular_queue.c -o circular_queue

Run:

./circular_queue

On Windows:

circular_queue.exe

# Data Structures Menu Program in C

A menu-driven C program that puts the core data structures and algorithms from my data structures course in one place. Pick an option, try it out, and go back to the main menu when you're done.

## Features

| Menu | What's inside |
|------|---------------|
| **Search** | Linear search, Binary search (sorts the array first) |
| **Sort** | Bubble, Selection, Insertion, Quick, Merge (ascending and descending for Bubble) |
| **Singly Linked List** | Insert at first / before position / after position / end, delete from first / position / end, display |
| **Doubly Linked List** | Same operations as above, plus forward and reverse display |
| **Stack** | Array version (size `n` from the user) and Linked List version: push, pop, peek, display |
| **Queue** | Array version (size `n` from the user) and Linked List version: enqueue, dequeue, peek, display |

## Build and Run

```bash
gcc ds_menu.c -o ds_menu
./ds_menu
```

Works with any standard C compiler (gcc, clang, MinGW). No `conio.h` needed.

## Notes

- Search and sort work on an array of **10 elements**.
- The array stack and array queue ask for the maximum size `n` when you open them. Memory is allocated with `malloc`/`realloc`, and re-entering the menu with a new `n` reuses it.
- The array queue is a simple linear queue, so slots at the front aren't reused after a dequeue.
- Linked list stack/queue and both linked lists grow dynamically using `malloc`.
- Invalid menu choices are handled with an "Invalid Choice" message.

## Time Complexity (quick reference)

| Algorithm | Best | Average | Worst |
|-----------|------|---------|-------|
| Linear search | O(1) | O(n) | O(n) |
| Binary search | O(1) | O(log n) | O(log n) |
| Bubble sort* | O(n²) | O(n²) | O(n²) |
| Selection sort | O(n²) | O(n²) | O(n²) |
| Insertion sort | O(n) | O(n²) | O(n²) |
| Quick sort | O(n log n) | O(n log n) | O(n²) |
| Merge sort | O(n log n) | O(n log n) | O(n log n) |

\*This bubble sort has no early-exit check, so even a sorted array takes O(n²). Adding a "swapped" flag makes the best case O(n).

## Concepts Covered

Arrays, pointers, structs, dynamic memory (`malloc` / `realloc`), recursion, singly and doubly linked lists, stacks, queues, and searching/sorting algorithms.

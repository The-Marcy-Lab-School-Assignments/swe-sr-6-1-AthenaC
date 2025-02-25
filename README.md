# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1

> Arrays, Linked Lists, and Doubly Linked Lists all store data in order, but they work differently.
>
> - Arrays are best when you need quick access to any item (O(1) time), but adding or removing elements in the middle is slow (O(n) time) because everything shifts.
> - Linked Lists make inserting and deleting easy (O(1) at the start), but finding a specific item takes longer (O(n) time) since you must go through each one.
> - Doubly Linked Lists are like Linked Lists but can move forward and backward, making some operations easier, though they use more memory.
>
>   Choose arrays for fast access, linked lists for frequent inserts/removals, and doubly linked lists when you need to move in both directions easily.

## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage.

Would you use a stack or a queue to implement this functionality?

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

> Abstract Data Type is a conceptual model that defines a set of operations and behaviors for a data structure, without specifying how these operations are implemented or how data is organized in memory. They are important to help developers to focus on WHAT it does and not HOW it does the job. It does not specify how data will be organized in memory and what algorithms will be used for implementing the operations. It is called "abstract" because it doesn't depend on a specific way of implementing it.

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works.

### Response 4

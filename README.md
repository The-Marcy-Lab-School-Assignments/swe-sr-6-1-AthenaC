# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1


## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage. 

Would you use a stack or a queue to implement this functionality? 

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2
I would use a stack, a linear data structure ordered by last-in, first-out to implement this "back" button functionality. Since a stack's functions for adding (`push`) and removing (`pop`) elements both do so to its "top", the user's initial webpage, at the "top" can be popped, making way for their previously visited webpage to now be at the "top" of their browser's stack. While a queue is also a linear, sequential data structure, it is based on first-in, first-out, such that the methods for adding and removing elements do not affect the same ends of the queue: while `enqueue` adds to its end, `dequeue` removes from the front. This means that queues cannot as straightforwardly remove elements in the same order they were added. Given how queues' methods affect different ends, accessing the most recent, previous tab would require the removal or dequeuing of all other tabs, preventing further access to past history.

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works. 

### Response 4

```js
const isBalanced = (str) => {
	if (inputString[0] === ")") return false;

    let bal = new Stack();
    for (let i = 0; i < inputString.length; i++) {
        if (inputString[i] === ")" && bal.peek() === "(") {
            bal.pop();
            continue;
        }
        bal.push(inputString[i]);
    }
    return bal.isEmpty();
}

```

This function takes in a String parameter, named `str`, which has a length greater than zero and contains only start and end parentheses. If the zeroth index value of `str` is an end parenthese, it immediately returns false because that set of parentheses is incomplete: it lacks a starting parenthese, which must come before the end. Next, `bal`, a Stack is created. Through iteration, this function either adds the value of the index `i` in `str` being checked to `bal` or, if the value at the current index is a closing parenthese, and the most recent value in `bal` is a starting parenthese, removes that starting parenthese from `bal` and moves on to the next iteration. After all iterations are complete, the function returns a Boolean based on whether `bal` is empty. This works because balanced sets of parentheses will, after numerous removals and even if nested, eventually comprise of consecutive opening and closing parentheses. When parentheses of `str` are nested, this function removes the innermost set of parentheses and removes each set toward the outermost. If a closing parenthese is not part of a balanced set, it will not be removed, such that the stack will not be empty and the length of `bal` will be greater than zero.

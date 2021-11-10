# Stacks and Queues

## **Stacks**

## **WHAT**

stacks is a linear data structure that follows a particular order in which the operations are performed. the order may be LIFO or FILO.

its consists of Nodes, and each node references the next Node in the stack but does not reference the previous Node.

- Common methods of stacks:

    1. Push: which push a node or items that are put into the stack pushed(Add element to the stack).

    2. Pop: which pop a node or items from the stack.(removing). Also when pop from an empty stack an exception will be thrown.

    3. Top: which is the of of the stack.

    4. Peek: returns the top element of the stack. Also when peek from an empty stack an exception will be thrown.

    5. isEmpty: returns true if the stack is empty otherwise returns false.

- Concepts of the stack:

    1. FIFO(first in first out): first item added in the stack will be the last one to pop out from the stack.

    2. LIFO(last in first out): last item added in the stack will be the first one to pop out from the stack

- Visualization of the stack:

    ![stack](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

## **HOW**

- Explanation of methods stack:

    1. Push:the time complexity will always be O(1) since its do one operation at time. no matter how Node we have in a stack.

        - steps of how to push:

            - we should have a node of data that we want to push

            - we need to assign the next of the new node to the top , then we assign the top value to the new node

            ```python

            ALGORITHM push(new_value)
            node = Node(new_value)
            node.next = top
            top = node

            ```

    2. POP: the time complexity will be O(1), when doing a pop, we need to check if its empty before to ensure that the exception is not thrown.

        - steps to pop:

            - The main idea is we will pop the top and the reassign the top to the next node.

            - To remove the top one is to create a temp variable that points to the same node that top point to.

            - After that, we will assign the top to the its next node and we can remove the temp variable. and return the value of it.

            ```python

            ALGORITHM pop()
            
            temp = top
            top = top.next
            temp.next = null
            return temp.value

            ```

    3. Peek: the time complexity will be O(1), when doing a peek, we need to check if its empty before to ensure that the exception is not thrown.

        - steps: since we are handling with the top so we gonna return its value

        ```python

            ALGORITHM peek()
            
            return top.value

        ```

    4. isEmpty: returns true if its empty otherwise returns false.

         ```python

            ALGORITHM isEmpty()
            
            return top = None

        ```

-----------

## **Queues**

## ***WHAT***

A Queue is a linear structure which follows a particular order in which the operations are performed. The order is (FIFO) and (LILO).

First In First Out means that the first item in the queue will be the first item to go out of the queue.

List In Last out means that the last item in the queue will be the last item to go out of the queue.

- Visualization Queues:
    ![queue](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)

## ***HOW***

- Common methods of queue:

    1. Enqueue: adding an item to the queue and its time complexity is o(1)/

        steps:
         - first we need to change the last element pointer to the new node that we want to add, the only access to it is the rear so we change its next pointer to next.

         > front stores the front node.
         > rear stores the last node.

         ```python

                ALGORITHM enqueue(new_value)
                new_node = Node(new_value)
                rear.next = new_node
                rear = new_node

            ```

    2. Dequeue: removing an item from the queue and its time complexity is o(1)/

        steps:
         - we need to check if the queue is empty or not to ensure that the exception is not thrown.

         - first, we need ti create a temp variable and assign it to the same front point to.

         - we need to re assign the front to the next value that the front os referencing to. and then we can assign the temp value to null.

         - now since we assign the front value to the next value we can now Dequeue it. then return the temp value.

         ```python

                ALGORITHM dequeue()
                temp = front
                front = front.Next
                temp.next = null
                return temp.value

            ```

    3. Peek: the time complexity will be O(1), when doing a peek, we need to check if its empty before to ensure that the exception is not thrown.

        - steps: since we are handling with the top so we gonna return its value

            ```python

                ALGORITHM peek()
                
                return front.value

            ```

    4. isEmpty: returns true if its empty otherwise returns false.

         ```python

            ALGORITHM isEmpty()
            
            return front = None
            ```

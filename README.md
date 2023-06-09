# Doubly Linked Lists

## Objectives

- Construct a Doubly Linked List
- Compare and contrast Doubly and Singly Linked Lists
- Implement basic operations on a Doubly Linked List

## what is it ?

- We know what lists are...but doubly? Almost identical to Singly Linked Lists, except every node has another pointer, to the previous node!

![Doubly Linked List](https://res.cloudinary.com/practicaldev/image/fetch/s--zEN6ebwP--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pdgwi91nt6c7pb5kaoyp.png)

## Implementation

### PUSHING

- Adding a node to the end of the Doubly Linked List

### Pushing pseudocode

- Create a new node with the value passed to the function
- If the head property is null set the head and tail to be the newly created node
- If not, set the next property on the tail to be that node
- Set the previous property on the newly created node to be the tail
- Set the tail to be the newly created node
- Increment the length
- Return the Doubly Linked List

### The code

![push method](./images/push.png)

### POPPING

- Removing a node from the end of the Doubly Linked List

### Popping pseudocode

- If there is no head, return undefined
- Store the current tail in a variable to return later
- If the length is 1, set the head and tail to be null
- Update the tail to be the previous Node.
- Set the newTail's next to null
- Decrement the length
- Return the value removed

### The code

![pop method](./images/pop.png)

### SHIFTING

- Removing a node from the beginning of the Doubly Linked List

### If length is 0, return undefined

- Store the current head property in a variable (we'll call it old head)
- If the length is one
  - set the head to be null
  - set the tail to be null
- Update the head to be the next of the old head
- Set the head's prev property to null
- Set the old head's next to null
- Decrement the length
- Return old head

### The code

![shift method](./images/shift.png)

### UNSHIFTING

- Adding a node to the beginning of the Doubly Linked List

### Unshifting pseudocode

- Create a new node with the value passed to the function
- If the length is 0
  - Set the head to be the new node
  - Set the tail to be the new node
- Otherwise
  - Set the prev property on the head of the list to be the new node
  - Set the next property on the new node to be the head property
  - Update the head to be the new node
- Increment the length
- Return the list

### The code

![unshift method](./images/unshift.png)

### GET

- Accessing a node in a Doubly Linked List by its position

### Get Pseudocode

- If the index is less than 0 or greater or equal to the length, return null
- If the index is less than or equal to half the length of the list
  - Loop through the list starting from the head and loop towards the middle
  - Return the node once it is found
- If the index is greater than half the length of the list
  - ​Loop through the list starting from the tail and loop towards the middle
  - Return the node once it is found

### The code

![get method](./images/get.png)

### SET

- Replacing the value of a node to the in a Doubly Linked List

### Set pseudocode

- Create a variable which is the result of the get method at the index passed to the function
- If the get method returns a valid node, set the value of that node to be the value passed to the function
- Return true
- Otherwise, return false

### The code

![set method](./images/set.png)

### INSERT

- Adding a node in a Doubly Linked List by a certain position

### Insert pseudocode

- If the index is less than zero or greater than or equal to the length return false
- If the index is 0, unshift
- If the index is the same as the length, push
- Use the get method to access the index -1
- Set the next and prev properties on the correct nodes to link everything together
- Increment the length
- Return true

### The code

![insert method](./images/insert.png)

### REMOVE

- Removing a node in a Doubly Linked List by a certain position

### Remove pseudocode

- If the index is less than zero or greater than or equal to the length return undefined
- If the index is 0, shift
- If the index is the same as the length-1, pop
- Use the get method to retrieve the item to be removed
- Update the next and prev properties to remove the found node from the list
- Set next and prev to null on the found node
- Decrement the length
- Return the removed node.

### The code

![remove method](./images/remove.png)

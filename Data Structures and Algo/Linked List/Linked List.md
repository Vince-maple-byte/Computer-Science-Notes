Linked List are a form of data structures that are composed of nodes pointing one to another in the form of a list.


Example 
![[Linkedlist.png]]
The example above is a single linked list. It has a starting point in named head and the way we iterate through this list is by going from next of the current node until the next node would be a null.

Example of a double linked list:
![[Doublelinkedlist.png]]
The main difference between double and single is that in the double list we can access the next node and the previous node while in the single we only have access to the next node.

Key tips:
In linked list, the head is thought of a pointer to the linked list it self, so when traversing through a single linked list it is important to have another pointer set = to head in order to not lose the position of head.
On a similar note keep in my mind when deleting or changing node order when having a pointer set = to head. Doing this would change the list similar to if you were accessing the list through head. So if you are going the make a change to the list, but want to keep the original list that head was positioned in, then make a new copy linked list and do your changes there.
#data-structure #algo #linked-list
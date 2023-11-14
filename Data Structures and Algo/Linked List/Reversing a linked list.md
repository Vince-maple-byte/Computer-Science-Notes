To reverse a linked list we can simply do this in java
```
public LinkedList reverse(LinkedList head){
	LinkedList previous = null;
	LinkedList next = null;
	LinkedList current = copyLinkedList(head);
	
	while(current != null){
		next = current.next;
		current.next = previous;
		previous = current;
		current = next;
	}
	return previous;
}
```
Keep in mind that the copyLinkedList(head) function creates a copy of the linked list head. We do this so that we don't mess with the head function. 
#data-structure #algo #linked-list 
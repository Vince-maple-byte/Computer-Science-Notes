To make a copy of a linked list we can do this:
```
	public LinkedList copy(LinkedList head){
		LinkedList copy = new LinkedList(head.val);
		LinkedList copyHead = copy;
		LinkedList current = head.next;
		
		while(current != null){
			LinkedList newNode = new LinkedList(current.val);
			copyHead.next = newNode;
			current = current.next;
			copyHead = copyHead.next;
		}
		return copy;
	}
```
#data-structure #algo #linked-list 


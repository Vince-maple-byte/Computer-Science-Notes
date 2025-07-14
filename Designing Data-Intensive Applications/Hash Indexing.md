Hash indexing is an indexing algorithm to find the location of the key in a [[Log Structured Database]]. 
## How does this work?
With a simple hash index algorithm, we would have an in-memory [[Hash Map]] to keep track of where the key is located in the [[Segment Files]]. Each segment file that we create needs a separate hash map to keep track of where the individual keys are located in that segment file.
## Limitations of Hash Indexing
- Since all of the indexing is done in memory, if the system crashes we would need to reinstate all of the hash maps being used which in turn can be really expensive.
- The hash map doesn't allow for us to search for a range of keys efficiently since the keys can be stored in any random order.

#algo #backend #computer-memory #databases #designing-data-intensive-applications-book 
Hash indexing is an indexing algorithm to find the location of the key in a [[Log Structured Database]]. 
## How does this work?
With a simple hash index algorithm, we would have an in-memory [[Hash Map]] to keep track of where the key is located in the [[Segment Files]]. Each segment file that we create needs a separate hash map to keep track of where the individual 
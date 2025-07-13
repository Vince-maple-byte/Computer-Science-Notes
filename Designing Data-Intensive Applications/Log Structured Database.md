## What is a log? 
In databases, a log refers to an append only sequence of records.

## So how does a log structured database work?
Typically for a simple log structured database, a key-value based structure is used to store the data (similar to a Hash Table). Any new data written to the database will be stored at the bottom of an append-only file. In this append-only file any updates or deletions in the database are just written in the database at the end of the file as a new record.

## How to prevent the append-only file from growing too large?
With the simple log structured database we would continue to add records to the append only file until it grows too large for us to make any lookups efficiently or no more writes can be done. To fix this issue, use [[Segment Files]]. 

## But how does log structured databases keep track of the location of the key-value pair?
To keep track of the location of the key-value pair in the disk, we would need to use an [[Index]]. Without an [[Index]] to do reads for our key-value pairs we would need to do view each record at a time until we find the latest version of the key-value pair that we need. This is an O(n) time complexity read which is extremely slow for a database. 

Log structured databases use these three different indexing algorithms to perform this disk lookup more efficiently [[Hash Indexing]], [[SSTables]], [[LSM Trees]].

#backend #databases #designing-data-intensive-applications-book #unfinished 
# Hash Tables

Hash Table Terminology: 
  - HASH: 
    - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array
  - BUCKETS: 
    - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs
  - Collisions: 
    - A collision is what happens when more than one key gets hashed to the same location of the hashtable

What are they?
  - Hash Tables are data structures that utilize `[key]:[value]` pairs.
  - Every Bucket / Node will have a key and value
  - Basic implementation will have the ability to store a key into the strucutre and retrieve its value.
  - Completed through a hash. (see above in terms)

How are the implemented?
  - Two Steps:
    - An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table
    - The element is stored in the hash table where it can be quickly retrieved using hashed key

For a good hashing mechanism, a few basic requirements:
  - Easy to compute: It should be easy to compute and must not become an algorithm in itself.
  - Uniform distribution: It should provide a uniform distribution across the hash table and should not result in clustering.
  - Less collisions: Collisions occur when pairs of elements are mapped to the same hash value. These should be avoided.

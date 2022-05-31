# Class 30

## Hash Cheats

1. *Hash* - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
2. *Buckets* - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
3. *Collisions* - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

- Every **`Node`** or **`Bucket`** has both a key, and a value.
- A **`hash`** is the ability to encode the key that will eventually map to a specific location in the data structure.
- Since we are able to **`hash`** our key and determine the exact location hashes have a O(1) time complexity.
- A hash code turns a key into an integer
- A hashtable traditionally is created from an array.
- collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions.
- Collisions are solved by changing the initial state of the buckets.
- Hash maps do this to store values:
  - accept a key
  - calculate the hash of the key
  - use modulus to convert the hash into an array index
  - store the key **with** the value by appending both to the end of a linked list
- Hash maps do this to read value:
  - accept a key
  - calculate the hash of the key
  - use modulus to convert the hash into an array index
  - use the array index to access the short LinkedList representing a bucket
  - search through the bucket looking for a node with a key/value pair that matches the key you were given

    Internal Methods:

  - **Add()** - adds a new key/value pair to a hashtable
  - **Find() -** takes in a key, gets the Hash, and goes to the index location specified
  - **Contains() -** accepts a key, and return a bool on if that key exists inside the hashtable.
  - **GetHash() -** accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

  - Irrespective of how good a hash function is, collisions are bound to occur. Therefore, to maintain the performance of a hash table, it is important to manage collisions through various collision resolution techniques.

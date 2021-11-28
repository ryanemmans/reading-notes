# CLASS 30 NOTES - HashTables

- [https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

- - -

Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

## **Terminology**

- **Hash** - the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
- **Buckets** - what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
- **Collisions** - when more than one key gets hashed to the same location of the hashtable.

We use hashtables to hold unique values, or as a dictionary or library.

A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

- We can do a lookup in an O(1) time complexitiy.
- Instead of adding elements to an array, a hash map uses a "hash function" to place each item at a precise index location based off it's key
  - Takes a key and returns an integer
    - Determines where key/value pair should be placed in the array

## Structure

### Hashing

- It's important that hash codes are deterministic - output determined only by input
  - Should never have randomness
  - Same key should always produce same hash code

### Creating a Hash

Traditionally created from an array

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo (%) to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

Each Index of the array contain “buckets”.

- Each bucket holds one key/value pair combination.
- When there is no entry in a specific bucket, the buckets (each index of the array) all start `null`.
- The hash table starts each bucket empty and overwrites their value once a key generates a hashCode that corresponds with an index.

### Collisions

When more than one key hashes to the same index in an array.

- A "perfect hash" will never have any collisions.
- Collisions are solved by changing the initial state of the buckets.
  - Instead of starting them all as null we can initialize a LinkedList in each one.
- Since different keys can lead to the same bucket it’s important to store the entire key/value pair in the bucket, not just the value.

How hash maps *store* values:

- Accept a key
- Calculate the hash of the key
- Use modulus to convert the hash into an array index
- Store the key with the value by appending both to the end of a linked list

How hash maps *read* values:

- Accept a key
- Calculate the hash of the key
- Use modulus to convert the hash into an array index
- Use the array index to access the short LinkedList representing a bucket
- Search through the bucket looking for a node with a key/value pair that matches the key you were given

### Bucket Sizes

Hash Maps can have any number of buckets.

- Only a few buckets: densely full and have many collisions.
- More buckets: sparsely populated, less collisions, may be a lot of extra empty space

Load factor - tells us something about how full the hash table is.

- A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.

## Internal Methods

`Add()` - when adding a new key/value pair to a hashtable:

1. Send the key to the `GetHash` method
2. Determine index of where it should be placed, go to that index
3. Check if something already exists at the index. If not, add with key/value pair
4. If so, add key/value pair to data structure (linked list) within that bucket (chaining).

`Find()` - takes in a key, gets the Hash, and goes to the index location specified.

`Contains()` - will accept a key and return a boolean if that key exists inside the hashtable.

- Call the `GetHash` and check if key exists in table given the index returned.

`GetHash()` - will accept a key as a string, conduct the hash, return index of the array where key/value should be placed.

- - -

- [https://www.youtube.com/watch?v=MfhjkfocRR0](https://www.youtube.com/watch?v=MfhjkfocRR0)
- [https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

- - -

Large keys are converted into small keys by using **hash functions**.

- The values are then stored in a **hash table**.

Hashing is implemented in two steps:

1. An element is converted into an interger by using a hash function.
    - Can be used as index to store original element, which falls into hash table.
2. Element is stored in hash table where it can be quickly retrieved using hashed key.
    - `hash = hashfunc(key)`
    - `index = hash % array_size`

Hash functions should be easy to compute, have uniform distribution, and less collisions.

The index for a specific string equals the sum of the ASCII values of the characters modulo 599 (prime number).

## Collision Resolution Techniques

- Separate chaining (open hashing) is one of the most commonly used collision resolution techniques.
  - Usually implemented using linked lists.
  - Average cost of a lookup depends only on the average number of keys per linked list.

- - -

- [https://en.wikipedia.org/wiki/Hash_table](https://en.wikipedia.org/wiki/Hash_table)

- - -

A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found.

- During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

- - -

[back](../README.md)

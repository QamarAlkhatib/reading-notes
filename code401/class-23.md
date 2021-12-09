# Hash Tables

## What is a Hashtable?

1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

## Why do we use them?

- Hold unique values
- Dictionary
- Library

## What Are they

Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

## Structure

Hashing

Basically, a hash code ```turns a key into an integer.``` It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

## Creating a Hash

Hashtables are created from an array, to create the hash table we need to spcify its size. after that we are gonna so some logic to turn the key into a numeric value and we can do it by:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

- Example:

```
Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 
```

Hash maps do this to store values:

    accept a key
    calculate the hash of the key
    use modulus to convert the hash into an array index
    store the key with the value by appending both to the end of a linked list

Hash maps do this to read value:

    accept a key
    calculate the hash of the key
    use modulus to convert the hash into an array index
    use the array index to access the short LinkedList representing a bucket
    search through the bucket looking for a node with a key/value pair that matches the key you were given

### Sizes of Buckets

Any number of buckets can be used in a hash map. A hash map with only a few buckets will be heavily packed and have a lot of collisions. A hash map with more buckets will be poorly populated, resulting in fewer collisions but potentially a lot of vacant space.

The "load factor" of a hash table can be calculated. The load factor indicates how much space the hash table has. A hash table can begin with only a few buckets, compute its own load factor, identify when it becomes overburdened, and grow and add more buckets to itself to accommodate more data.

### Hashing is implemented in two steps

 1. An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
 2. The element is stored in the hash table where it can be quickly retrieved using hashed key.

    hash = hashfunc(key)
    index = hash % array_size

## Internal Methods

- ```Add()```

When adding a new key/value pair to a hashtable:

1. send the key to the GetHash method.
2. Once you determine the index of where it should be placed, go to that index
3. Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
4. If something does exist, add the new key/value pair to the data structure within that bucket.

- ```Find()```

The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

- ```Contains()```

The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

- ```GetHash()```

The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.


<https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html>

<https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/>

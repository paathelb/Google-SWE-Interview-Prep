### HASH TABLES

A hash table is data structure used to store keys, optionally, corresponding a values.Inserts,
deletes and lookups run in time O(1) on average.

A hash function has one hard requirement-equal keys should have equal hash codes.

A hash table is a good data structure to represent a dictionary of strings, i.e., a set.
Anytime you need to store a set of strings, a hash table is an excellent choice.

Hash tables have the best theoretical and real-world performance for lookup, insert, and delete with O(1) time complexity. 

HASH TABLE LIBRARIES
There are multiple hash table-based data structures commonly used in Python-set, dict,
collections. defaultdict, and collections. Counter. The difference between set and the other
three is that a set simply stores keys, whereas the others store key-value pairs. All have the
property that they do not allow for duplicate keys, unlike, for example, list.

In a dict, accessing value associated with a key that is not present leads to a KeyError exception.
However, a collections.defaultdict returns the default value of the type that was specified when
the collection was instantiated, e.g.,if d = collections.defaultdict(list), then if k not in d
then d [k] is tl. A collections.Counter is used for counting the number of occurrences of keys,
with a number of setlike operations, as illustrated below.

The most important operations for set are s.add(42), s.remove(42), s.discard(123), x in s,
as well as s <= t (is a subset of t), and s - t (elements in s that are not in t).

Iteration over a key-value collection yields the keys. To iterate over the key-value
pairs, iterate over items(); to iterate over values, use values(). The keys() method returns an
iterator to the keys.



### SORTING
- Naive sorting algorithms run in O(n^2) time.
- A number of sorting algorithms run in O(n log n) time - heapsort, merge sort, and quicksort are examples.
- A well-implemented quicksort is usually the best choice for sorting.
- The time complexity of any reasonable library sort is O(n log n) for an array with n entries. Most
library sorting functions are based on quicksort, which has O(1) space complexity.

Sorting Libraries
- To sort a list in-place, use the sort() method; to sort an iterable, use the function sorted().
- sort() method takes two arguments, both optional: key=None, and reverse=False.
For example, b = sorted(a, key=lambda x: str(x))


### BINARY SEARCH TREES
- BSTs are a workhorse of data structures and can be used to solve almost every data structures problem reasonably efficiently. 
- They offer the ability to efficiently search for a key as well as find the min and max elements, look for the successor or predecessor of a search key (which itself need
not be present in the BST), and enumerate the keys in a range in sorted order.
- However, unlike with a sorted array, keys can be added to and deleted from a BST efficiently.

- The keys stored at nodes have to respect the BST property - the key stored at a node is greater than or equal to the keys stored at the nodes of its left subtree and less than or equal to the keys stored in the nodes of its right subtree.

- Key lookup, insertion, and deletion take time proportional to the height of the tree, which can in worst-case be O(n). However, there are implementations of insert and delete which guarantee that the tree has height O(log n)

- A common mistake with BSTs is that an object that's present in a BST is not updated. As a rule,
avoid putting mutable objects in a BST. Otherwise, when a mutable object that's in a BST is to be
updated, always first remove it from the tree, then update it, then add it back.


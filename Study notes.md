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

BST Libraries
- Python does not come with built-in BST library
- functionalities added by bintrees
- insert(e) inserts new element e in the BST.
- discard(e) removes e in the BST if present.
- min_item()/max_item() yield the smallest and largest key-value pair in the BST.
- min_key()/max_key() yield the smallest and largest key in the BST.
- pop_min()/pop_max() remove the return the smallest and largest key-value pair in the BST.
- These operations take O(logn), since they are backed by the underlying tree.

### Recursion
- Recursion is an approach to problem solving where the solution partially depends on solutions to smaller of instances related problems
- More generally, searching, enumeration, divide-and-conquer, and decomposing a complex problem into a set of similar smaller instances are all scenarios where recursion may be suitable.
- A divide-and-conquer algorithm works by repeatedly decomposing a problem into two or more smaller independent subproblems of the same kind, until it gets to instances that are simple enough to be solved directly. Merge sort and quicksort are classical examples of divide-and-conquer.
- Divide-and-conquer is not synonymous with recursion. In divide-and-conquer, the problem is divided into two or more independent smaller problems that are of the same type as the original problem. Recursion is more general:
  - there may be a single subproblem, e.g., binary search
  - the subproblems may not be independent, e.g., dynamic programming
  - they may not be of the same type as the original, e.g., regular expression matching.
- Sometimes, in order to improve runtime and occasionally reduce space complexity, a divide-and-conquer algorithm is implemented using iteration instead of recursion.




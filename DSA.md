## Hashmap:
- [ ] definition
	- [ ] A key-value store that uses an array and a hashing function to save and retrieve values.
	- [ ] Key: The identifier given to a value for later retrieval.
	- [ ] Hash function: A function that takes some input and returns a number.
	- [ ] Compression function: A function that transforms its inputs into some smaller range of possible outputs.
- [ ] collisions:
	- [ ] A hash collision is when a hash function returns the same index for two different keys.
- [ ] separate chaining
	- [ ] When a collision occurs, separate chaining resolves it by maintaining a linked list or another data structure within each bucket. Instead of replacing the existing element with the new one, the new element is appended to the end of the linked list or data structure associated with that bucket.
- [ ] open addressing: linear probing
	- [ ] In open addressing, all elements are stored directly in the hash table itself, without using additional data structures like linked lists. When a collision occurs, instead of storing the colliding element in the same bucket, the algorithm scans through the hash table linearly (hence the term "linear probing") until it finds an empty slot to store the element.
- [ ] hash functions
	- [ ] This function is said to be deterministic. That means the hashing function must always return the same index when given the same key. This is important because we will need to hash the key again later to retrieve the stored value. We won’t be able to do this unless our hashing function behaves in a predictable and consistent way.
- [ ] how hashmaps are formed


Recipe for saving to a hash table:
- Take the key and plug it into the hash function, getting the hash code.
- Modulo that hash code by the length of the underlying array, getting an array index.
- Check if the array at that index is empty, if so, save the value (and the key) there.
- If the array is full at that index continue to the next possible position depending on your collision strategy.

Recipe for retrieving from a hash table:
- Take the key and plug it into the hash function, getting the hash code.
- Modulo that hash code by the length of the underlying array, getting an array index.
- Check if the array at that index has contents, if so, check the key saved there.
- If the key matches the one you're looking for, return the value.
- If the keys don't match, continue to the next position depending on your collision strategy.




## Algorithmic Complexity
### Asymptotic notation
- [ ] big omega and big o notation
- [ ] what is runtime
- [ ] adding runtimes
- [ ] - We use asymptotic notation to describe the runtime of a program. The three types of asymptotic notation are big Theta, big Omega, and big O.
- We use big Theta (Θ) to describe the runtime if the runtime of the program is the same in every case.
- The different common runtimes from fastest to slowest are: Θ(1), Θ(log N), Θ(N), Θ(N log N), Θ(N2), Θ(2N), Θ(N!).
- We use big Omega (Ω) to describe the best-case running time of a program.
- We use big O (O) to describe the worst-case running time of a program.


Certainly, here is a table that provides common algorithms and their time and space complexities for best-case, worst-case, and average-case scenarios. Keep in mind that these complexities are approximate, and they can vary depending on the specific implementation and input data:

| Algorithm                | Best-Case Time | Worst-Case Time | Average-Case Time | Space Complexity |
| ------------------------ | -------------- | --------------- | ----------------- | ---------------- |
| Linear Search            | O(1)           | O(n)            | O(n)              | O(1)             |
| Binary Search            | O(1)           | O(log n)        | O(log n)          | O(1)             |
| Bubble Sort              | O(n)           | O(n^2)          | O(n^2)            | O(1)             |
| Quick Sort               | O(n log n)     | O(n^2)          | O(n log n)        | O(log n)         |
| Merge Sort               | O(n log n)     | O(n log n)      | O(n log n)        | O(n)             |
| Insertion Sort           | O(n)           | O(n^2)          | O(n^2)            | O(1)             |
| Selection Sort           | O(n^2)         | O(n^2)          | O(n^2)            | O(1)             |
| Heap Sort                | O(n log n)     | O(n log n)      | O(n log n)        | O(1)             |
| Hash Table (average)     | -              | O(1)            | O(1)              | O(n)             |
| Breadth-First Search     | -              | O(V + E)        | O(V + E)          | O(V)             |
| Depth-First Search       | -              | O(V + E)        | O(V + E)          | O(V)             |
| Dijkstra's Algorithm     | O(V^2)         | O(V^2)          | O(V^2)            | O(V)             |
| Bellman-Ford Algorithm   | O(VE)          | O(VE)           | O(VE)             | O(V)             |
| Floyd-Warshall Algorithm | O(V^3)         | O(V^3)          | O(V^3)            | O(V^2)           |

Please note that these complexities provide a general sense of how these algorithms perform in different scenarios, but the actual performance may vary based on factors like the specific implementation, hardware, and input data. The complexities listed above represent typical cases and can differ in some real-world situations.

Certainly, here is a table that provides common data structures and their time and space complexities for various operations:

| Data Structure          | Insertion Time     | Deletion Time     | Search Time       | Space Complexity |
|------------------------|--------------------|-------------------|-------------------|------------------|
| Array                  | -                  | -                 | O(n)              | O(n)             |
| Dynamic Array (e.g., ArrayList) | O(1)*        | O(n)*             | O(n)              | O(n)             |
| Linked List            | O(1)               | O(1)              | O(n)              | O(n)             |
| Stack                  | O(1)               | O(1)              | O(n)              | O(n)             |
| Queue                  | O(1)               | O(1)              | O(n)              | O(n)             |
| Hash Table             | O(1)**            | O(1)**            | O(1)**            | O(n)             |
| Binary Search Tree     | O(log n)           | O(log n)          | O(log n)          | O(n)             |
| AVL Tree               | O(log n)           | O(log n)          | O(log n)          | O(n)             |
| Red-Black Tree         | O(log n)           | O(log n)          | O(log n)          | O(n)             |
| Skip List              | O(log n)           | O(log n)          | O(log n)          | O(n)             |
| B-Tree                 | O(log n)           | O(log n)          | O(log n)          | O(n)             |
| Trie                   | O(L)***            | O(L)***           | O(L)***           | O(ALPHABET_SIZE * L) |
| Heap (Binary, Fibonacci, etc.) | O(log n) | O(log n)          | O(n)              | O(n)             |

* Amortized time complexity.
** Assuming a good hash function.
*** L is the length of the key being inserted, deleted, or searched for.

Please note that the complexities listed above provide a general sense of how these data structures perform for various operations. The actual performance may vary based on factors like the specific implementation, hardware, and use case. Additionally, some data structures may have different complexities for specific operations, such as priority queue operations in a binary heap.
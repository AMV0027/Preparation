# Java Collections Documentation

---

## 1. List (Ordered Collection, Allows Duplicates)

### **1.1 ArrayList**

**Specialty:** A dynamically resizable array that provides fast random access.

**Code Sample:**

```java
ArrayList<Integer> list = new ArrayList<>();
list.add(10);
list.add(20);
System.out.println(list.get(1)); // 20
```

**Available Functions:**

- `add(element)`: Adds an element to the list.
- `get(index)`: Retrieves an element at the specified index.
- `set(index, element)`: Replaces an element at the given index.
- `remove(index)`: Removes an element at the given index.
- `contains(element)`: Checks if the list contains the given element.
- `size()`: Returns the number of elements in the list.
- `isEmpty()`: Checks if the list is empty.
- `clear()`: Removes all elements from the list.
- `indexOf(element)`: Returns the index of the first occurrence of the element.
- `lastIndexOf(element)`: Returns the index of the last occurrence of the element.
- `toArray()`: Converts the list into an array.

### **1.2 LinkedList**

**Specialty:** A doubly linked list that allows fast insertion and deletion.

**Code Sample:**

```java
LinkedList<String> list = new LinkedList<>();
list.add("A");
list.addFirst("Start");
list.addLast("End");
```

**Available Functions:**

- `add(element)`: Adds an element to the list.
- `addFirst(element)`: Adds an element to the beginning of the list.
- `addLast(element)`: Adds an element to the end of the list.
- `get(index)`: Retrieves an element at the specified index.
- `getFirst()`: Retrieves the first element.
- `getLast()`: Retrieves the last element.
- `remove(index)`: Removes an element at the given index.
- `removeFirst()`: Removes the first element.
- `removeLast()`: Removes the last element.
- `size()`: Returns the number of elements.
- `isEmpty()`: Checks if the list is empty.

### **1.3 Vector**

**Specialty:** A thread-safe dynamically resizable array.

**Code Sample:**

```java
Vector<Integer> vector = new Vector<>();
vector.add(100);
vector.add(200);
```

**Available Functions:**

- `add(element)`: Adds an element to the vector.
- `get(index)`: Retrieves an element at the specified index.
- `set(index, element)`: Replaces an element at the given index.
- `remove(index)`: Removes an element at the given index.
- `size()`: Returns the number of elements.
- `capacity()`: Returns the current capacity of the vector.
- `isEmpty()`: Checks if the vector is empty.
- `firstElement()`: Retrieves the first element.
- `lastElement()`: Retrieves the last element.

### **1.4 Stack**

**Specialty:** A Last In, First Out (LIFO) data structure.

**Code Sample:**

```java
Stack<Integer> stack = new Stack<>();
stack.push(10);
stack.push(20);
System.out.println(stack.pop()); // 20
```

**Available Functions:**

- `push(element)`: Adds an element to the stack.
- `pop()`: Removes and returns the top element.
- `peek()`: Retrieves the top element without removing it.
- `search(element)`: Searches for an element and returns its position.
- `empty()`: Checks if the stack is empty.

---

## 2. Queue (FIFO - First In, First Out)

### **2.1 LinkedList (Queue Implementation)**

**Specialty:** Implements a queue using a linked list.

**Code Sample:**

```java
Queue<Integer> queue = new LinkedList<>();
queue.add(1);
queue.add(2);
System.out.println(queue.poll()); // 1
```

**Available Functions:**

- `add(element)`: Inserts an element into the queue.
- `offer(element)`: Inserts an element, returning false if capacity restrictions apply.
- `poll()`: Retrieves and removes the head of the queue.
- `remove()`: Removes the head of the queue and throws an exception if empty.
- `peek()`: Retrieves but does not remove the head.
- `isEmpty()`: Checks if the queue is empty.
- `size()`: Returns the number of elements in the queue.

### **2.2 PriorityQueue**

**Specialty:** A queue that maintains elements in natural sorted order.

**Code Sample:**

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
pq.add(50);
pq.add(10);
System.out.println(pq.poll()); // 10
```

**Available Functions:**

- `add(element)`: Inserts an element maintaining natural order.
- `offer(element)`: Inserts an element, returning false if capacity restrictions apply.
- `poll()`: Retrieves and removes the smallest element.
- `remove()`: Removes the smallest element, throws an exception if empty.
- `peek()`: Retrieves but does not remove the smallest element.
- `isEmpty()`: Checks if the queue is empty.
- `size()`: Returns the number of elements.

---

## 3. Deque (Double-Ended Queue)

### **3.1 ArrayDeque**

**Specialty:** A faster alternative to Stack and LinkedList.

**Code Sample:**

```java
Deque<Integer> deque = new ArrayDeque<>();
deque.addFirst(10);
deque.addLast(20);
System.out.println(deque.pollFirst()); // 10
```

**Available Functions:**

- `addFirst(element)`: Adds an element to the front.
- `addLast(element)`: Adds an element to the back.
- `removeFirst()`: Removes and returns the first element.
- `removeLast()`: Removes and returns the last element.
- `getFirst()`: Retrieves the first element without removing it.
- `getLast()`: Retrieves the last element without removing it.
- `peekFirst()`: Retrieves but does not remove the first element.
- `peekLast()`: Retrieves but does not remove the last element.

---

## 4. Set (Unique Elements)

### **4.1 HashSet**

**Specialty:** A collection of unique elements with no defined order.

**Code Sample:**

```java
HashSet<Integer> set = new HashSet<>();
set.add(1);
set.add(2);
```

**Available Functions:**

- `add(element)`: Inserts an element if it is not already present.
- `remove(element)`: Removes an element if present.
- `contains(element)`: Checks if an element exists.
- `size()`: Returns the number of elements.
- `isEmpty()`: Checks if the set is empty.
- `clear()`: Removes all elements.

### **4.2 LinkedHashSet**

**Specialty:** Maintains elements in insertion order while ensuring uniqueness.

**Code Sample:**

```java
LinkedHashSet<Integer> set = new LinkedHashSet<>();
set.add(10);
set.add(20);
```

**Available Functions:**

- `add(element)`: Inserts an element if not already present.
- `remove(element)`: Removes an element if present.
- `contains(element)`: Checks if an element exists.
- `size()`: Returns the number of elements.
- `isEmpty()`: Checks if the set is empty.
- `clear()`: Removes all elements.

### **4.3 TreeSet**

**Specialty:** A set that stores elements in sorted order.

**Code Sample:**

```java
TreeSet<Integer> set = new TreeSet<>();
set.add(40);
set.add(10);
```

**Available Functions:**

- `add(element)`: Inserts an element while maintaining sorting.
- `remove(element)`: Removes an element if present.
- `first()`: Retrieves the smallest element.
- `last()`: Retrieves the largest element.
- `higher(element)`: Returns the smallest element greater than the given one.
- `lower(element)`: Returns the largest element smaller than the given one.
- `contains(element)`: Checks if an element exists.
- `size()`: Returns the number of elements.
- `isEmpty()`: Checks if the set is empty.

---

## 5. Map (Key-Value Pairs)

### **5.1 HashMap**

**Specialty:** A key-value pair collection with no specific order.

**Code Sample:**

```java
HashMap<Integer, String> map = new HashMap<>();
map.put(1, "One");
map.put(2, "Two");
```

**Available Functions:**

- `put(key, value)`: Adds a key-value pair.
- `get(key)`: Retrieves the value associated with the key.
- `remove(key)`: Removes the key-value pair if present.
- `containsKey(key)`: Checks if a key exists.
- `containsValue(value)`: Checks if a value exists.
- `size()`: Returns the number of key-value pairs.
- `isEmpty()`: Checks if the map is empty.
- `keySet()`: Returns a set of all keys.
- `values()`: Returns a collection of all values.

### **5.2 LinkedHashMap**

**Specialty:** Maintains key-value pairs in insertion order.

**Code Sample:**

```java
LinkedHashMap<Integer, String> map = new LinkedHashMap<>();
map.put(3, "Three");
map.put(1, "One");
```

**Available Functions:**

- `put(key, value)`: Adds a key-value pair while maintaining insertion order.
- `get(key)`: Retrieves the value associated with the key.
- `remove(key)`: Removes the key-value pair if present.
- `containsKey(key)`: Checks if a key exists.
- `containsValue(value)`: Checks if a value exists.
- `size()`: Returns the number of key-value pairs.
- `isEmpty()`: Checks if the map is empty.
- `keySet()`: Returns a set of all keys.
- `values()`: Returns a collection of all values.

### **5.3 TreeMap**

**Specialty:** A key-value map sorted by keys.

**Code Sample:**

```java
TreeMap<Integer, String> map = new TreeMap<>();
map.put(2, "Two");
map.put(1, "One");
```

**Available Functions:**

- `put(key, value)`: Adds a key-value pair in sorted order.
- `get(key)`: Retrieves the value associated with the key.
- `remove(key)`: Removes the key-value pair if present.
- `firstKey()`: Retrieves the smallest key.
- `lastKey()`: Retrieves the largest key.
- `higherKey(key)`: Returns the smallest key greater than the given one.
- `lowerKey(key)`: Returns the largest key smaller than the given one.
- `containsKey(key)`: Checks if a key exists.
- `size()`: Returns the number of key-value pairs.

---

---

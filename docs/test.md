## Advanced Python Problems

### 1. **Nested Loops and Matrix Generation**

Write a function `generate_matrix(n: int, m: int) -> list[list[int]]` that generates an `n × m` matrix where each element is the sum of its row and column indices.  
Return the matrix as a list of lists.

#### Example:

```python
matrix = generate_matrix(3, 3)
print(matrix)
# Expected Output:
# [[0, 1, 2], [1, 2, 3], [2, 3, 4]]
```

---

### 2. **Closure for Counter Function**

Create a closure `make_counter(start = 0)` that returns a tuple of two functions:

- `increment()`: increases the count by 1 and returns the current value.
- `decrement()`: decreases the count by 1 and returns the current value.

#### Example:

```python
increment, decrement = make_counter(10)
print(increment())  # Output: 11
print(decrement())  # Output: 10
```

---

### 3. **Deleting Elements and Shared References**

Consider the following scenario:

```python
a = [1, 2, 3]
b = a
del a[1]
print(b)
```

Explain and verify through code how modifying `a` affects `b`.

---

&nbsp;

&nbsp;

### 4. **In-Place List Modification**

Given a list of integers, write a function `remove_every_nth_element(lst: list[int], n: int)` that removes every n-th element from the list without creating a new list. Use the `del` keyword.

#### Example:

```python
mylist = [1, 2, 3, 4, 5, 6]
remove_every_nth_element(mylist, 2)
print(mylist)
# Expected Output: [1, 3, 5]
```

---

### 5. **Combining Closures and Decorators**

Write a decorator `track_execution()` that counts how many times a function has been executed. Use a closure inside the decorator to maintain the count.

#### Example:

```python
@track_execution
def say_hello():
    print("Hello")

say_hello()
say_hello()
# Expected Output:
# Hello
# Execution count: 1
# Hello
# Execution count: 2
```

---

### 6. **Recursive Function to Flatten Nested Lists**

Write a recursive function `flatten(mylist: list) -> list` that takes a deeply nested list (e.g., `[[1, [2, 3]], 4, [5, [6, 7]]]`) and returns a flattened list.

#### Example:

```python
nested_list = [[1, [2, 3]], 4, [5, [6, 7]]]
flat_list = flatten(nested_list)
print(flat_list)
# Expected Output: [1, 2, 3, 4, 5, 6, 7]
```

---

### 7. **Stateful Object with Closure**

Create a closure `make_stateful_object(initial_value: int)` that mimics an object with a private state. The closure should return a dictionary containing references to the three functions:

- `get_value()`: returns the current state.
- `set_value(new_value: int)`: updates the state.
- `reset()`: resets the state to the initial value.

#### Example:

```python
stateful = make_stateful_object(10)
print(stateful['get_value']())  # Output: 10
stateful['set_value'](20)
print(stateful['get_value']())  # Output: 20
stateful['reset']()
print(stateful['get_value']())  # Output: 10
```

---

### 8. **Dictionary Merging**

Write a function `merge_dicts(d1: dict[str, int], d2: dict[str, int]) -> dict[str, int]` that merges two dictionaries. If a key exists in both dictionaries, sum their values. Otherwise, keep the original value from the respective dictionary.

#### Example:

```python
d1 = {'a': 1, 'b': 2}
d2 = {'b': 3, 'c': 4}
merged = merge_dicts(d1, d2)
print(merged)
# Expected Output: {'a': 1, 'b': 5, 'c': 4}
```

---

### 9. **Palindrome Check**

Write a function `is_palindrome(s: str) -> bool` that checks whether a given string is a palindrome. The function should ignore case differences.

#### Example:

```python
print(is_palindrome("Madam"))  # Output: True
print(is_palindrome("Hello"))  # Output: False
```

---

### 10. **Prime Factorization**

Write a function `prime_factors(n: int) -> list[int]` that returns all prime factors of a given integer `n`.

#### Example:

```python
print(prime_factors(28))  # Output: [2, 2, 7]
```

---

### 11. **Matrix Transposition**

Write a function `transpose(matrix: list[list[int]]) -> list[list[int]]` that takes a 2D matrix and returns its transpose.

#### Example:

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
transposed = transpose(matrix)
print(transposed)
# Expected Output:
# [[1, 4, 7],
#  [2, 5, 8],
#  [3, 6, 9]]
```

### 12. **Minimum Coin Change**

Write a function `min_coin_change(coins: list[int], amount: int) -> int` that returns the minimum number of coins needed to make up the given amount. If it's not possible, return `-1`.
The argument `coins` is a list of integers, where each integer represents the denomination of coin you have available.

#### Example:

```python
print(min_coin_change([1, 5, 10, 25], 7))  # Output: 3
print(min_coin_change([1, 5, 10, 25], 6))   # Output: 2
print(min_coin_change([5, 10, 25], 6))   # Output: -1
```

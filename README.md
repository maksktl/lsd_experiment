# Part 1 

### Task 1: Easy

#### Task description:
Implement a function that takes a list of integers and returns the sum of all even numbers in the list.

##### **Function signature:**
```python
def sum_even_numbers(numbers: List[int]) -> int:
    pass
```
##### Tests:
```python
numbers = [1, 2, 3, 4, 5, 6]
assert sum_even_numbers(numbers) == 12
```

### Task 2: Medium

#### Task description:
Implement a function that takes a string and returns the reverse of the string.


##### **Function signature:**
```python
def reverse_string(s: str) -> str:
    pass
```
##### Tests:
```python
assert reverse_string("hello") == "olleh"
```

### Task 3: Difficult

#### Task description:
Implement a function that takes a list of dictionaries representing people and their birthdates, and returns the person with the earliest birthdate.

##### **Function signature:**
```python
def earliest_person(people: List[Dict[str, Union[str, int]]]) -> Dict[str, Union[str, int]]:
    pass
```
##### Tests:
```python
people = [
    {"name": "Alice", "birthdate": "1995-01-01"},
    {"name": "Bob", "birthdate": "1990-05-10"},
    {"name": "Charlie", "birthdate": "1993-03-15"},
]

assert earliest_person(people) == {"name": "Bob", "birthdate": "1990-05-10"}
```

### Task 4: Very Difficult

#### Task description:
Implement a function that takes a list of integers and returns the maximum sum that can be obtained by selecting a contiguous subsequence from the list such that no two elements in the subsequence are adjacent in the original list.

##### **Function signature:**
```python
def max_sum_no_adjacent(nums: List[int]) -> int:
    pass
```
##### Tests:
```python
assert max_sum_no_adjacent([1, 2, 3, 1]) == 4 # Explanation: select 2 and 1
assert max_sum_no_adjacent([2, 7, 9, 3, 1]) == 12 # Explanation: select 2, 9, and 1
```

# Part 2

### Task 1: Sort array

#### Task description:
Implement a function that takes two sorted arrays of integers and returns a new sorted array containing all the elements of the input arrays, without using any built-in sorting functions.

##### **Function signature:**
```python
def merge_sorted_arrays(arr1: List[int], arr2: List[int]) -> List[int]:
    pass
```
##### Tests:
```python
assert merge_sorted_arrays([1, 3, 5], [2, 4, 6]) == [1, 2, 3, 4, 5, 6]
assert merge_sorted_arrays([1, 2, 3], [4, 5, 6]) == [1, 2, 3, 4, 5, 6]
```

### Task 2: Shortest path

#### Task description:
Implement a function that takes a directed graph represented as an adjacency matrix and returns the length of the shortest path from the start node to the end node. If there is no path from the start node to the end node, the function should return -1.

##### **Function signature:**
```python
def shortest_path(adj_matrix: List[List[int]], start: int, end: int) -> int:
    pass
```
##### Tests:
```python
adj_matrix = [[0, 4, 0, 0, 0, 0, 0, 8, 0],
              [4, 0, 8, 0, 0, 0, 0, 11, 0],
              [0, 8, 0, 7, 0, 4, 0, 0, 2],
              [0, 0, 7, 0, 9, 14, 0, 0, 0],
              [0, 0, 0, 9, 0, 10, 0, 0, 0],
              [0, 0, 4, 14, 10, 0, 2, 0, 0],
              [0, 0, 0, 0, 0, 2, 0, 1, 6],
              [8, 11, 0, 0, 0, 0, 1, 0, 7],
              [0, 0, 2, 0, 0, 0, 6, 7, 0]]

assert shortest_path(adj_matrix, 0, 4) == 21
assert shortest_path(adj_matrix, 1, 5) == -1
```

### Task 3: Minimum path

#### Task description:
Implement a function that takes a list of n points in a 2D plane and returns the minimum length of a path that connects all the points exactly once and ends at the starting point. The path must be a closed polygonal chain, which means it starts and ends at the same point and does not intersect itself. The function should return -1 if it is impossible to connect all the points.

##### **Function signature:**
```python
from typing import List, Tuple

def minimum_path(points: List[Tuple[float, float]]) -> float:
    pass
```
##### Tests:
```python
points = [(0, 0), (1, 1), (2, 2), (3, 3), (4, 4)]

assert minimum_path(points) == 10.0

points = [(0, 0), (1, 1), (2, 2), (3, 3), (5, 5)]

assert minimum_path(points) == -1
```

### Task 4: Integral

#### Task description:
Implement a function that takes a one-dimensional function f(x), an interval [a, b], and an error tolerance epsilon, and returns the integral of the function f(x) over the interval [a, b] with an error no greater than epsilon. The function should use adaptive quadrature with recursive subdivision and a graph algorithm to achieve the required time complexity.

##### **Function signature:**
```python
from typing import Callable

def integrate(f: Callable[[float], float], a: float, b: float, eps: float) -> float:
    pass
```
##### Tests:
```python
import math

def f(x):
    return math.sin(x**2)

assert abs(integrate(f, 0, 1, 0.0001) - 0.3698) <= 0.0001
```



# Data structures and Dynamic Arrays
1.The specification 
2.What data can store
3.What operation are supported

## 1. Two interface 
### 1.1 The static sequence interface
- build(x): make new DS for items in x
- len(x): return new
- iter sequence(): output $x_0, x_1... x_n$ in the sequence order 
- get_at(i): return $x_i$ (index i)
- set_at(i): set $x_i$ to $x$ 

Key:  word RAM model of the Computation
-memory = array of w-bits word
-array =consecutive chunk of memory
=> array[i] = memory[address(array) + i]

Every get_at or set_at will be completed in the fixed time.

### 1.2 The static Array
- O(1) pre get_at
- O(n) pre build iter-sequence

### 1.3 The Dynamic sequence interface

- insert_at(x): make x the new $x_i$
- delete_at(x): shift $x_n\to x_{n-1}\to x_{n-2}...$

#### 1.3.1 Linked list
We store our items in branch of the items.
It is simple

### 1.4 Dynamic Arrays
It is efficient and included in many languages.
- Relax the size of the string we use.
- enforce size of the array size= $O(n)$
- maintain A[i] = $x_i$

- if n = size allocate new array of $\alpha$ siz
- n insert_last() from empty array

=> resize cost = $\theta(1+2+...)$ = $\theta(\sum_{i=1}^n 2^i)$


## 2. Amortization
operation takes $T(n)$ amortzed time
if any k operations take <= K*T(n) time
It performs well.

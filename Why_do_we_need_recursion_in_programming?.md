# What is Recursion and When Should We Use It?

<br>

<br>

## What is Recursion?

- If a function inside of its definition calls itself, that is recursion.

- Recursion happens when a function calls itself within its own definition.

- It calls itself over and over again until a base condition is met that breaks the loop.

<br>

### Recursive Function

1. base case
2. recursive call

<br>

### Base case (== ending point)

: In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems.

-> the function would theoretically repeat forever without it  == `stack overflow`

ex)

```python
def recursion(n):
    if n <= 1:
        return 1
    else:
        return n*recursion(n-1)
```

<br>

<br>

### Tail Recursion

A special form of recursion where the last operation of a function is a recursive call. The recursion may be optimized away by executing the call in the current stack frame and returning its result rather than creating a new stack frame.

<br>

#### Non-tail recursive function

ex) 

```python
def non_tail(n):
    if n == 0:
        return 1
    return n*non_tail(n-1)
```

The function is not tail recursive since the value returned by *non_tail(n-1)* is used in *non_tail(n)* and call to *non_tail(n-1)* is not the last thing done by *non_tail(n)* 

<br>

#### Tail recursive function

ex)

```python
def tail(n, a): 
  
    if (n == 0): 
        return a 
  
    return tail(n - 1, n * a) 
  
# A wrapper over tail(n,a) 
def fact(n): 
    return tail(n, 1) 
```

<br>

<br><br>

## When should we use recursion?

- If problem can be divided into multiple smaller version of the same problem, we can use the Recursive approach to solve that problem.

- It is especially good for working on things that have many possible branches and are too complex for an iterative approach.
- `Tree`  and  `graphs`  are another time when recursion is the best and easiest way to do traversal.

<br>

### Pros

1. can reduce `time complexity`
2. adds *clarity* and *reduces the time* needed to write and debug code
3. better at `tree traversal`

<br>

#### Cons

1. uses more memory
2. can be slow
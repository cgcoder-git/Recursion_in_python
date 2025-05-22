# Recursion in programming in python
Let’s take a deep dive into recursion — what it is, why it’s useful, 5 of the easiest examples, its benefits, and how to calculate time complexity using a recursion tree diagram.

## What is Recursion? 
"**Recursion** is a programming technique where a **function calls itself**",to solve smaller instances of a problem until it reaches a base case that can be solved directly.
You can think of it like breaking a big problem into smaller sub-problems that look similar to the original, solving the smallest version, and combining the results.

<img src="https://github.com/user-attachments/assets/19a1fbf8-32ed-40ee-a4e6-c6e31e6b712f" width="400">

Here we can see **recurse()** is being called inside **recurse()**, i.e. function is calling itself, but we can not let the function call itself infinite time, as this will fill the memory and crash occured, to prevent that we also use some condition to break it (**base condition**).
* in simple words "Imagine you're standing in a line and asking the person in front of you, "How many people are ahead of you?" That person asks the one in front of them, and so on. Eventually, someone at the front says "Zero." Each person adds 1 and passes the result back. That's recursion!".

# Types of Recursion:
1. Direct Recursion
2. Indirect Recursion
3. Head Recursion
4. Tail Recursion
5. Tree Recursion
6. Linear Recursion

### Direct Recursion:
In direct recursion, a function calls itself directly within its own definition. This means the function's code explicitly includes a call to the same function.
- **Example**
```python
def factorial(n):
    """
    Calculate the factorial of a number using recursion.
     """
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)
    
print(factorial(5))
# Output: 120
```

### Indirect Recurion:
In this recursion, there may be more than one functions and they are calling one another in a circular manner.
* **Example**
```python
""" indirect recursion"""
def even(n):
    if n == 0:
        return True
    else:
        return odd(n - 1)
    
def odd(n):
    if n == 0:
        return False
    else:
        return even(n - 1)
    
print(even(4))  # Output: True
print(odd(5))   # Output: True
```

### Head Recursion
The recursive call happens before other processing. recursive call is made first, and the actual work is done after the recursive call returns.
**Example**
```python
def head_recursion(s, i):
    if i >= len(s):
        return
    head_recursion(s, i + 1) # call 
    print(s[i], end="") # actual work 

string = "Hello"
i = 0
head_recursion(string,i)
#output : olleh
```

### Tail Recursion
The recursive call is the last statement. Nothing happens after the call.
**Example**
```python
def tail_recursion(s, i):
    if i < 0:
        return
    print(s[i], end="")
    tail_recursion(s, i - 1)

string = "Hello"
i = len(string)-1
tail_recursion(string,i)
```

### Tree Recursion
A recursive function is said to be tree-recursive if it makes more than one recursive call per invocation.
**Example**
```python
def fib(n):
    if n <= 1:
        return n
    return fib(n - 1) + fib(n - 2)

print(fib(5))  # Output: 5
```
**Calls made**
```python
             fib(4)
           /        \
      fib(3)        fib(2)
     /     \        /     \
 fib(2)   fib(1)  fib(1)  fib(0)
 /   \
fib(1) fib(0)

```

### Liner Recursion
A recursive function is linear if it makes at most one recursive call each time it executes, That means the call stack grows in a straight line — like a linked list, not a tree.
**Example**
```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)
factorial(4) # output: 24
```
**calls**
```python
factorial(4)
    → 4 * factorial(3)
        → 3 * factorial(2)
             → 2 * factorial(1)
                  → 1 * factorial(0)
                       → returns 1
```

**How it goes to stack**
- factorial of a number
<img width="488" alt="Screenshot 2025-05-22 at 12 32 00 AM" src="https://github.com/user-attachments/assets/b46a6c97-5769-4617-a989-fb36047be1ce" />

when return happends each results are taken from the stack and accumulate the final result.






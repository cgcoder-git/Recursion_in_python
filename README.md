# Recursion in programming in python
Let’s take a deep dive into recursion — what it is, why it’s useful, 5 of the easiest examples, its benefits, and how to calculate time complexity using a recursion tree diagram.

## What is Recursion? 
"**Recursion** is a programming technique where a **function calls itself**",to solve smaller instances of a problem until it reaches a base case that can be solved directly.
You can think of it like breaking a big problem into smaller sub-problems that look similar to the original, solving the smallest version, and combining the results.

<img src="https://github.com/user-attachments/assets/19a1fbf8-32ed-40ee-a4e6-c6e31e6b712f" width="400">

Here we can see **recurse()** is being called inside **recurse()**, i.e. function is calling itself, but we can not let the function call itself infinite time, as this will fill the memory and crash occured, to prevent that we also use some condition to break it (**base condition**).
in simple words "Imagine you're standing in a line and asking the person in front of you, "How many people are ahead of you?" That person asks the one in front of them, and so on. Eventually, someone at the front says "Zero." Each person adds 1 and passes the result back. That's recursion!".





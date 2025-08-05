# ENGR 102 Lab Topic 6 (individual)

## Activities
There are four deliverables for this individual assignment. Please submit the files described below to Gradescope. Check out the [Frequently Asked Questions](#frequently-asked-questions) below. **Please include the individual header in your ~.py files.**

1. [Howdy Whoop](#howdy-whoop)
2. [Computing Sums](#computing-sums)
3. [Juggler Sequence](#juggler-sequence)
4. [Co-balancing Numbers](#co-balancing-numbers)

## Howdy Whoop
Write a program named `howdy_whoop.py` that takes as input from the user two positive integers. Output the numbers `1` to `100`, each on its own line, unless the number is evenly divisible by one or both of the integers entered by the user. If the number is evenly divisible by the first integer, print `Howdy`. If it's evenly divisible by the second integer, print `Whoop`. If it's evenly divisible by both, print `Howdy Whoop`. Format your output as shown below.

Example output (using inputs `2` and `3`):
```
Enter an integer: 2
Enter another integer: 3
1
Howdy
Whoop
...
Whoop
Howdy
```


## Computing Sums
Write a program named `computing_sums.py` that takes as input from the user two integers and calculates the sum of all integers between them, inclusive. Do **NOT** use any containers like lists, tuples, sets, and dictionaries, or the `sum()` function. You **MUST** use a loop. Format your output as shown below.

Example output (using inputs `3` and `10`):
```
Enter an integer: 3
Enter another integer: 10
The sum of all integers from 3 to 10 is 52
```

Example output (using inputs `29` and `102`):
```
Enter an integer: 29
Enter another integer: 102
The sum of all integers from 29 to 102 is 4847
```


## Juggler Sequence
The [Juggler sequence](https://en.wikipedia.org/wiki/Juggler_sequence) produces a sequence of integers using the following procedure. Given a number `n`, if `n` is even then the next number is the floor of the square root of `n`. If `n` is odd, then the next number is the floor of `n^(3/2)`. The Juggler sequence ends when `n` reaches `1`. 

As an example, if you start with the number `7`, then the terms of the sequence will be: `7, 18, 4, 2, 1`.

Write a program named `juggler_sequence.py` that takes in a positive integer from the user, and computes the Juggler sequence, printing out all the numbers in the sequence, followed by a line stating how many iterations it took to reach the value `1`. Format your output as shown below.

Example output (using input `7`):
```
Enter a positive integer: 7
The Juggler sequence starting at 7 is:
7, 18, 4, 2, 1
It took 4 iterations to reach 1
```


## Co-balancing Numbers
A positive number `n` is a co-balancing number if the sum of numbers from `1` to `n` is equal to the sum of numbers `n+1` to `n+r` where `r` is a positive integer. 
For example, `14` is a co-balancing number with `r` of `6`. That means the numbers `1` through `14` sum to the same amount as the next six integers after `14` (`15` through `20`). In other words,

$$\underbrace{(1+2+3+...+13+14)}_{105}=\underbrace{(15+16+...+19+20)}\_{105}$$

Write a program named `cobalancing_numbers.py` that takes in an integer value `n` from the user and determines if it is a co-balancing number. If `n` is a co-balancing number, output the corresponding value of `r`. Do **NOT** use any containers like lists, tuples, sets, and dictionaries, or the `sum()` function. You **MUST** use a loop. Format your output as shown below.

Example output (using input `14`):
```
Enter a value for n: 14
14 is a co-balancing number with r=6
```

Example output (using input `102`):
```
Enter a value for n: 102
102 is not a co-balancing number
```


## Frequently Asked Questions
1. **Activity 3 (Juggler sequence) how do I tell if a number is odd or even?** If a number divided by 2 has no remainder, then it's even. Can you think of a way to check using `%`?

2. **Activity 3 how do I print the last number without a comma?** An easy way to prevent an extra comma is to print your final value after your loop. For example, the code below prints the first 4 values inside the loop, and the last value after the loop is done:

```python
num = 5
for i in range(num - 1):
    print(i + 1, end=", ")
print(num)
```
You can do something similar with a while loop:
```python
num = 5
while num > 1:
    print(num, end=", ")
    num -= 1
print(num)
```

3. **Activity 3 I tried using backspace (`\b`) and Gradescope labels it `\x08` instead. What's going on?** Gradescope displays the `\b` character as `\x08`. To get around using `\b`, you can use string concatenation or string formatting instead. For example:

```python
print("My sequence starting at", str(num) + " is:") # convert num to a string and concatenate
print(f"My sequence starting at {num} is:") # use an f-string to insert num in the {} placeholder
```
Both have the same output with no space between `num` and `:`.

Have a question you don't see here? Email your instructor!

Based upon Dr. Keyser’s Original<br/>
Revised Summer 2025 SNR

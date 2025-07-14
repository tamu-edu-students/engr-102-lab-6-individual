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


## Juggler Sequence


## Co-balancing Numbers


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

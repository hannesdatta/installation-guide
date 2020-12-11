<!-- This is a template. Please update the content while keeping this structure.
We provide examples in the comments below. Make sure to read our contribution
guide to learn how to submit your content to Tilburg Science Hub. -->

# Goal of the Building Block

Provide a brief overview of the issue to solve, or describe why this is a best practice.

Add any special requirements or attach a dummy data set if needed.


## Code
<!-- Provide your code in all the relevant languages and/or operating systems. -->

```python
# program to check if a number is prime or not

num = 333

# prime numbers are greater than 1
if num > 1:
   # check for factors
   for i in range(2,num):
       if (num % i) == 0:
           print(num,"is not a prime number.")
           print(i,"times",num//i,"is",num)
           break
   else:
       print(num,"is a prime number.")

# if num is less than or equal to 1, it is not prime
else:
   print(num,"is not a prime number.")
```


## Examples

Provide further examples to support the solution.


## Background

### Subheader 1

Explain when and why this problem usually occurs.

- Case 1

- Case 2

Clarify why it's important to fix the problem.

### Subheader 2 (Under the hood)

Demonstrate why the proposed solution is the best approach.


## Advanced use cases - "See also"

Illustrate advanced use cases and explain how to bring this to the next level.

Provide useful resources and link to "see also" articles.

## Keywords

Please provide up to 10 keywords for this Building Block.
Metadata should provide information on the role and usage of this Building Block.
<!-- For example: ‘devising and organizing the project’,
‘data collection’, ‘data analysis’ and ‘article writing’. -->

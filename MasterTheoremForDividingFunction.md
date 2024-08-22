# Master Theorem for Dividing Functions

## General Recurrence Relation

###  The general form of the recurrence relation for divide and conquer algorithms is:

$$
T(n) = aT\left(\frac{n}{b}\right) + f(n)
$$

where:

$$
a \geq 1
$$

$$
b > 1
$$

$$
f(n) = O\left(n^k \cdot \log^p n\right)
$$

## Key Values

### To apply the Master Theorem, we need to calculate two key values:

$$
\log_b a
$$

$$
k
$$

Based on these values, the theorem divides the analysis into three cases.

## Case 1

If 

$$
\log_b a > k
$$

then:

$$
T(n) = \Theta\left(n^{\log_b a}\right)
$$

$$
T(n) = \Theta\left(n^{\log_b a}\right)
$$

## Case 2

If 

$$
\log_b a = k
$$

then there are three subcases based on the value of \( p \):

----
1. If 

$$
p > -1
$$

   the time complexity is:

   $$
   T(n) = \Theta\left(n^k \cdot \log^{p+1} n\right)
   $$
   
----
2. If 

$$
p = -1
$$

   the time complexity is:

   $$
   T(n) = \Theta\left(n^k \cdot \log \log n\right)
   $$
   
----

3. If 

$$
p < -1
$$

   the time complexity is:

   $$ 
   T(n) = \Theta\left(n^k\right)
   $$

---

## Case 3

If 

$$
\log_b a < k
$$

then there are two subcases based on the value of \( p \):

---

1. If 

$$
p \geq 0
$$

   the time complexity is:

   $$
   T(n) = \Theta\left(n^k \cdot \log^p n\right)
   $$

---

2. If 

$$
p < 0
$$

   the time complexity is:

   $$
   T(n) = \Theta\left(n^k\right)
   $$

---

## Summary

### The Master Theorem simplifies the process of determining the time complexity for divide and conquer algorithms by providing a structured approach based on the relationship between:

$$
\log_b a
$$

and 

$$
k
$$

and the behavior of 

$$
f(n)
$$

in the recurrence relation.




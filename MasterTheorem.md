
# Master Theorem for Dividing Functions

The Master Theorem is used to determine the time complexity of divide and conquer algorithms. It provides a way to analyze the recurrence relation of such algorithms and deduce their time complexity in different cases.

## General Recurrence Relation

The general form of the recurrence relation for divide and conquer algorithms is:

$$
T(n) = aT\left(\frac{n}{b}\right) + f(n)
$$

where:
- \(a \geq 1\)
- \(b > 1\)
- \(f(n) = O\left(n^k \cdot \log^p n\right)\)

## Key Values

To apply the Master Theorem, we need to calculate two key values:

1. \( \log_b a \)
2. \( k \)

Based on these values, the theorem divides the analysis into three cases.

## Case 1: \( \log_b a > k \)

If \( \log_b a > k \), then:

$$
T(n) = \Theta\left(n^{\log_b a}\right)
$$

## Case 2: \( \log_b a = k \)

If \( \log_b a = k \), then there are three subcases based on the value of \( p \):

1. If \( p > -1 \), the time complexity is:
   $$
   T(n) = \Theta\left(n^k \cdot \log^{p+1} n\right)
   $$

2. If \( p = -1 \), the time complexity is:
   $$
   T(n) = \Theta\left(n^k \cdot \log \log n\right)
   $$

3. If \( p < -1 \), the time complexity is:
   $$
   T(n) = \Theta\left(n^k\right)
   $$

## Case 3: \( \log_b a < k \)

If \( \log_b a < k \), then there are two subcases based on the value of \( p \):

1. If \( p \geq 0 \), the time complexity is:
   $$
   T(n) = \Theta\left(n^k \cdot \log^p n\right)
   $$

2. If \( p < 0 \), the time complexity is:
   $$
   T(n) = \Theta\left(n^k\right)
   $$

## Summary

The Master Theorem simplifies the process of determining the time complexity for divide and conquer algorithms by providing a structured approach based on the relationship between \( \log_b a \) and \( k \), and the behavior of \( f(n) \) in the recurrence relation.

---

**Note:** This markdown is structured to capture the essence of the images you provided, formatted for easy readability and application in a GitHub markdown file.

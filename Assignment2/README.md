# Fuzzy Logic

This notebook demonstrates the basic principles of fuzzy logic, including the definition of fuzzy sets and various operations on them.

## Theory of Fuzzy Logic

Fuzzy logic is a form of many-valued logic in which the truth values of variables may be any real number between 0 and 1. It is employed to handle the concept of partial truth, where the truth value may range between completely true and completely false. This is in contrast to Boolean logic, where the truth values of variables may only be the integer values 0 or 1.

### Fuzzy Sets

A fuzzy set is a set containing elements that have varying degrees of membership. A fuzzy set is characterized by a membership function, which assigns to each element a degree of membership between 0 and 1.

Let A be a fuzzy set. The membership function of A is denoted by $`\mu_A(x)`$.

### Fuzzy Sets in this Notebook

In this notebook, we define two fuzzy sets, A ("Low Speed Limit") and B ("High Speed Limit"), with the following membership functions:

#### Fuzzy Set A: "Low Speed Limit"

$`\mu_A(x) = \begin{cases}
1 & \text{if } x < 30 \\
\frac{x-30}{50-30} & \text{if } 30 \leq x < 50 \\
\frac{x-50}{70-50} & \text{if } 50 \leq x < 70 \\
0 & \text{if } x \geq 70
\end{cases}`$

#### Fuzzy Set B: "High Speed Limit"

$`\mu_B(x) = \begin{cases}
0 & \text{if } x < 60 \\
\frac{x-60}{80-60} & \text{if } 60 \leq x < 80 \\
\frac{x-80}{100-80} & \text{if } 80 \leq x < 100 \\
1 & \text{if } x \geq 100
\end{cases}`$

## Operations on Fuzzy Sets

The notebook demonstrates the following operations on the fuzzy sets A and B:

### Union

The union of two fuzzy sets A and B is a fuzzy set C, where the membership value of each element is the maximum of the membership values in A and B.

$`\mu_{A \cup B}(x) = \max(\mu_A(x), \mu_B(x))`$

### Intersection

The intersection of two fuzzy sets A and B is a fuzzy set C, where the membership value of each element is the minimum of the membership values in A and B.

$`\mu_{A \cap B}(x) = \min(\mu_A(x), \mu_B(x))`$

### Complement

The complement of a fuzzy set A is a fuzzy set A', where the membership value of each element is 1 minus the membership value in A.

$`\mu_{A'}(x) = 1 - \mu_A(x)`$

### Difference

The difference between two fuzzy sets A and B is defined as:

$`\mu_{A - B}(x) = \max(0, \mu_A(x) - \mu_B(x))`$

### Fuzzy Relation

A fuzzy relation is a fuzzy set of ordered pairs. In this notebook, we define a fuzzy relation R between two fuzzy sets C ("Cold") and D ("Warm").

#### Fuzzy Set C: “Cold”

$`\mu_C(x) = \begin{cases}
0 & \text{if } x < -10 \\
\frac{x - (-10)}{0 - (-10)} & \text{if } -10 \leq x < 0 \\
1 & \text{if } 0 \leq x < 5 \\
0 & \text{if } x \geq 5
\end{cases}`$

#### Fuzzy Set D: “Warm”

$`\mu_D(x) = \begin{cases}
0 & \text{if } x < 25 \\
\frac{x - 25}{35 - 25} & \text{if } 25 \leq x < 35 \\
1 & \text{if } 35 \leq x < 40 \\
0 & \text{if } x \geq 40
\end{cases}`$

### Fuzzy Set Composition

The notebook also demonstrates fuzzy set composition using the Max-Min and Max-Product methods.

#### Max-Min Composition

$`(C \circ R)(y) = \max_x(\min(\mu_C(x), \mu_R(x, y)))`$

#### Max-Product Composition

$`(C \circ R)(y) = \max_x(\mu_C(x) \cdot \mu_R(x, y))`$

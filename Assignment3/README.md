# Fuzzy Numbers and Fuzzy Inference Systems

This notebook explores two key concepts in fuzzy logic: fuzzy numbers and the Mamdani fuzzy inference system.

## Part 1: Fuzzy Numbers

A fuzzy number is a fuzzy set that represents a number in a "fuzzy" way. It is used to model uncertainty or vagueness in numerical values. In this notebook, we represent the fuzzy number "Approximately equal to 4" using three different types of membership functions:

### 1. Trapezoidal Membership Function

A trapezoidal membership function is defined by four parameters ($a, b, c, d$) and has a flat top.

**Mathematical Expression:**

$`\mu(x) = \begin{cases}
0 & \text{if } x \leq a \\
\frac{x-a}{b-a} & \text{if } a < x \leq b \\
1 & \text{if } b < x \leq c \\
\frac{d-x}{d-c} & \text{if } c < x \leq d \\
0 & \text{if } x > d
\end{cases}`$

### 2. Triangular Membership Function

A triangular membership function is a special case of the trapezoidal function where $b = c$. It is defined by three parameters ($a, b, c$).

**Mathematical Expression:**

$`\mu(x) = \begin{cases}
0 & \text{if } x \leq a \\
\frac{x-a}{b-a} & \text{if } a < x \leq b \\
\frac{c-x}{c-b} & \text{if } b < x \leq c \\
0 & \text{if } x > c
\end{cases}`$

### 3. Gaussian Membership Function

A Gaussian membership function is defined by two parameters: the center $c$ and the standard deviation $\sigma$.

**Mathematical Expression:**

$`\mu(x) = e^{-\frac{(x-c)^2}{2\sigma^2}}`$

## Part 2: Mamdani Fuzzy Inference System

The second part of the notebook demonstrates the design of a Mamdani fuzzy inference system to control the fan speed of a furnace based on temperature.

### System Design

-   **Input Variable**: Temperature
-   **Output Variable**: Fan Speed

### Linguistic Variables and Fuzzy Sets

-   **Temperature**: "Risky", "Average", "Excellent"
-   **Fan Speed**: "Slow", "Moderate", "High"

### Fuzzy Rules

The system is based on a set of IF-THEN rules that map the input temperature to the output fan speed. For example:

1.  **Rule 1**: IF TEMPERATURE is "Risky", THEN FAN-SPEED is "Slow".
2.  **Rule 2**: IF TEMPERATURE is "Average", THEN FAN-SPEED is "Moderate".
3.  **Rule 3**: IF TEMPERATURE is "Excellent", THEN FAN-SPEED is "High".

### Fuzzification

The crisp input (temperature) is converted into fuzzy values by determining the degree of membership in each fuzzy set ("Risky", "Average", "Excellent").

### Rule Aggregation (Mamdani Model)

The Mamdani model is used to aggregate the outputs of the fuzzy rules. The output of each rule is a fuzzy set, and these fuzzy sets are combined using the max operator.

### Defuzzification (Centroid Method)

The aggregated fuzzy output is converted back to a crisp value (fan speed) using the centroid (or center of gravity) method. The centroid $z^*$ is calculated as:

$`z^* = \frac{\int z \cdot \mu(z) \, dz}{\int \mu(z) \, dz}`$

Day 1 placeholder — folder created.
1. What I Studied

Meaning of scalars, vectors, matrices, tensors
Difference between a row vector and a column vector
Matrix shape (m × n) and what it represents
Basic matrix operations: addition, subtraction, multiplication
Dot product and its geometric meaning
Matrix multiplication rules (important for M
Why linear algebra is the backbone of machine learning

2. Key Concepts in My Own Words
Scalar
A single number. Represented as 5, 2.3, -7, etc.
Vector
A list of numbers. Examples:
[1, 2, 3]

[0.5, -1.2, 4.7]

A vector has direction and magnitude.

Matrix

A 2D grid of numbers. Example:

[1 2 3]
[4 5 6]

Matrix Shape

Rows × Columns
Example: 2 × 3 matrix → 2 rows, 3 columns

Dot Product

Multiply corresponding elements and add them.

Example:
[1, 2, 3] ⋅ [4, 5, 6]
= 1×4 + 2×5 + 3×6 = 32

Matrix Multiplication Rule

If A is m × n and B is n × p,
then C = AB is m × p.

The inside numbers (n) must match.

3. Why This Matters in Machine Learning

Vectors represent data features

Matrices represent datasets

Almost every ML algorithm uses matrix operations:

Linear Regression → uses matrix inverse

Neural Networks → matrix multiplication in every layer

PCA → uses eigenvalues & eigenvectors

Gradient descent → uses vector calculus

Without linear algebra → ML looks like magic.
With linear algebra → ML becomes logical.

4. Small Example (Simple & Clear)

Dataset sample:

Age | Salary
20  | 30k
25  | 40k
30  | 50k


Vector of Ages = [20, 25, 30]
Matrix of data =

[20 30]
[25 40]
[30 50]


Linear model prediction:

Pred = XW


X → input matrix
W → weight vector

This is why matrix multiplication is the heart of ML.

5. Confidence Level (1–10):

6/10
(Will improve after more practice)


Date: 21 Nov 2025
Topic: Probability & Basic Statistics for Machine Learning (Day 1)
1. What I Studied

Introduction to Probability

Random Variables

Measures of Central Tendency:

Mean

Median

Mode

Measures of Spread:

Variance

Standard Deviation

Basic use of probability in ML models

2. Key Concepts in My Own Words
Probability

Probability measures how likely an event is to happen.
Value always lies between 0 and 1.

Examples:

P(rain) = 0 → Impossible

P(rain) = 1 → Guaranteed

P(rain) = 0.3 → 30% chance of rain

Random Variable

A variable whose value depends on the outcome of a random event.
Examples:

Toss a coin → random variable X = {0,1}

Roll a die → X = {1,2,3,4,5,6}

Two types:

Discrete random variable (countable outcomes)

Continuous random variable (infinite outcomes, e.g., height, weight)

Mean

Average of values.
Formula:

Mean
=
∑
𝑥
𝑖
𝑛
Mean=
n
∑x
i
	​

	​


Example:
[10, 20, 30] → mean = 60/3 = 20

Median

Middle value after sorting.
Resistant to outliers.

Example:
[3, 5, 100] → median = 5

Mode

The most common value in a dataset.
Useful in categorical data.

Example:
["red", "blue", "red", "green"] → mode = red

3. Variance & Standard Deviation
Variance

Measures how spread out the data is.
Higher variance → data is more scattered.

Formula:

𝜎
2
=
∑
(
𝑥
𝑖
−
𝜇
)
2
𝑛
σ
2
=
n
∑(x
i
	​

−μ)
2
	​

Standard Deviation (SD)

Square root of variance.
Gives spread in the same unit as the data.

𝜎
=
𝜎
2
σ=
σ
2
	​


Example (simple):
Dataset: [10, 20, 30]
Mean = 20
(10-20)² + (20-20)² + (30-20)² = 100 + 0 + 100 = 200
Variance = 200/3 ≈ 66.7
SD ≈ 8.16

4. Why These Concepts Matter in Machine Learning
✔️ Probability

Used in:

Naive Bayes

Logistic Regression

Bayesian Networks

Evaluation metrics

Uncertainty estimation

✔️ Mean/Median

Used in:

Data cleaning (handling missing values)

Feature engineering

✔️ Variance/Std

Used in:

Understanding data spread

Normalization & scaling

Gradient descent stability

Regularization concepts

Machine Learning = Mathematics + Probability + Linear Algebra.
Statistics is the foundation for understanding patterns + predictions.

5. Simple Example (Easy to Understand)

Dataset of student marks:

50, 60, 70, 80, 90


Mean = 70
Median = 70
Mode = None (all unique)
Variance = spread from the mean
SD = how much marks vary from 70

If SD is low → students' marks are similar
If SD is high → marks vary a lot

This idea appears everywhere in ML.

6. Confidence Level Today:

5/10
(Will increase after coding practice)

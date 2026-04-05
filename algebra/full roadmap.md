# ML Mathematics Roadmap — Complete Learning & Progress System

> **For:** B.Tech AI/DS student building a real foundation for ML — not tutorial fluency, but structural understanding.
> **Covers:** Linear Algebra (7 Milestones) · Probability & Statistics · Calculus
> **Style:** Just-in-time staging — each subject starts exactly when it unlocks something real
> **Total estimate:** 18–22 weeks at 2–3 hrs/day

---

## The Three Pillars of ML Mathematics

Before you touch a single formula, understand this clearly.

ML is not a single subject. It is a system built on **three mathematical pillars**. If any one is missing, your understanding collapses at a specific, predictable point. Not eventually — at a specific place.

| Pillar | What it gives ML | What breaks without it |
|---|---|---|
| **Linear Algebra** | Structure — data as vectors, models as matrices, transformations as linear maps | You cannot see what a model is doing. You press buttons and copy code. |
| **Probability & Statistics** | Uncertainty — how confident is a prediction, what does a loss function measure, how do you evaluate a model honestly | "Accuracy = 92%." You have no idea if that is good, bad, or meaningless. |
| **Calculus** | Learning — how models update, why gradient descent works, what backpropagation actually is | Gradient descent is a magic ritual. You tune hyperparameters blindly. |

You do not learn these in sequence. You do not finish one and start the next. You stage them — each one starts exactly when it becomes load-bearing for your ML work. That is the principle running through this entire roadmap.

---

## The Correct Learning Loop (Apply to Every Topic)

For every concept — whether it is dot products, Bayes' theorem, or the chain rule — use this exact loop:

```
1. Learn the concept          --> understand what it IS and WHY it exists
2. Solve by hand              --> do problems on paper, not on a computer
3. Code it from scratch       --> implement it without NumPy shortcuts first
4. Explain in plain English   --> if you cannot explain it simply, you do not understand it
5. Test with a fresh problem  --> one you have never seen before
```

If you skip step 2, your math is weak.
If you skip step 3, your implementation is fragile.
If you skip step 4, you are memorizing, not understanding.
If you skip step 5, you are fooling yourself.

All five steps. Every time.

---

## Master Timeline

```
Wk  | Linear Algebra (LA)         | Probability & Stats    | Calculus           | FCC ML
----+-----------------------------+------------------------+--------------------+-------------------
1   | M1: Vectors, geometric think| --                     | --                 | --
2   | M1: Span, projection, norm  | --                     | --                 | --
3   | M2: Matrices as machines    | B1: Core probability   | --                 | Intro + Regression
4   | M2: Systems, elimination    | B1: Bayes, RVs         | --                 | Linear Regression
5   | M3: Independence, span      | B2: Distributions      | --                 | Classification
6   | M3: Basis, rank, null space | B2: Gaussian, multi    | --                 | K-Means, Logistic
7   | M4: Orthogonality, proj.    | B3: MLE, MAP           | B1: Derivatives    | Trees, Ensembles
8   | M4: Least squares, Gram-Sch | B3: Bias-variance      | B1: Chain rule     | Dim. Reduction
9   | M5: Eigenvalues, eigenvect. | B4: Evaluation metrics | B2: Gradients      | Neural Networks
10  | M5: Diagonalization, PSD    | B4: Cross-validation   | B2: Partial derivs | Neural Networks
11  | M6: SVD full                | Full P&S review        | B3: Backprop math  | Deep Learning
12  | M6: PCA from scratch        | P&S Milestone 3        | B3: Comp. graphs   | Deep Learning
13  | M7: ML integration          | Review as needed       | B4: Hessians       | Advanced DL
14+ | All three active simultaneously -- Deep Learning integration phase
```

---

# PART I -- LINEAR ALGEBRA

## Why Linear Algebra Comes First

Linear algebra is the **structure** of ML. Before probability, before calculus, before any ML library -- you need to see data as vectors, models as matrices, and computations as linear transformations.

Every neural network forward pass is `Z = W @ X + b` -- a matrix multiplication. Every regression solution involves inverting or approximating a matrix. Every dimensionality reduction technique is a change of basis. Every attention mechanism in a transformer is a sequence of matrix multiplications.

This is not background knowledge. This is the language ML is written in.

---

## Milestone 1 -- Vector Thinking

### Introduction: What you are going to learn and why

You are going to learn to see vectors the right way -- not as lists of numbers, but as geometric objects with direction and magnitude that live in a space.

This matters for ML because everything in ML is a vector. A data point is a vector (its features are coordinates in feature space). A model's weight parameters are a vector. A gradient is a vector pointing in the direction of steepest loss increase. A word embedding is a vector in a 300-dimensional space. When you compute the similarity between two sentences in an NLP model, you are computing the cosine similarity between their embedding vectors. When a linear model makes a prediction, it computes a dot product.

Without understanding vectors geometrically -- not just algebraically -- every one of these operations is an opaque formula you memorize. With geometric understanding, they become obvious.

### Topics to Study

- Scalars vs vectors -- notation, meaning, dimension
- Vector addition and scalar multiplication -- what these do geometrically
- Linear combinations -- building new vectors from existing ones
- Span -- the set of all points reachable with linear combinations
- Norm and magnitude -- ||v|| = sqrt(v1^2 + v2^2 + ... + vn^2)
- Distance between vectors -- Euclidean distance as norm of difference
- Dot product -- a.b = sum(ai * bi) = ||a|| ||b|| cos(theta)
- Angle between vectors -- what the dot product tells you about alignment
- Projection of a onto b -- the component of a in the direction of b

### How to Study This

**Khan Academy:** Vectors unit (all videos). This is your intuition layer -- do not skip it.

**MIT 18.06:** Lectures 1-2. Use MIT for the geometric picture: why projections matter, what dot product is actually measuring, how vectors relate to linear systems.

**MML Book:** Sections 2.1-2.3. Read this after you have intuition from Khan and MIT. The book gives you formal structure.

### Implementation Milestone

Build these in Python -- **without NumPy shortcuts first**:

```python
# 1. Vector operations from scratch
def vec_add(a, b): ...          # element-wise addition
def scalar_mul(c, v): ...       # scale every component
def dot(a, b): ...              # sum of element-wise products
def norm(v): ...                # sqrt(sum of squares)
def cosine_sim(a, b): ...       # dot(a,b) / (norm(a) * norm(b))

# 2. Projection of a onto b
def project(a, b):
    # proj = (dot(a,b) / dot(b,b)) * b
    # rejection = a - proj
    ...

# 3. Linear combination checker
def can_form(target, vectors):
    # Can target be written as c1*v1 + c2*v2 + ... ?
    ...

# 4. Span visualizer (2D)
# Take two vectors, plot all reachable points with coefficients in [-2, 2]
# Show how the reachable set changes when vectors are parallel vs independent
```

After building from scratch, verify every function against NumPy. They should match to floating-point precision.

### Output: Vector Foundation Notebook

A Jupyter notebook containing:
- Theory notes in your own words (not copied text)
- 10 solved problems by hand (typed or photographed)
- All 4 code implementations above
- 2 visualizations: projection diagram, span visualization

### You Are Done When

- [ ] You can compute dot product and projection without hesitation
- [ ] You can explain what "span" means in plain English -- no textbook definitions
- [ ] You can solve vector problems by hand without looking anything up
- [ ] You can code vector operations without NumPy shortcuts
- [ ] You can answer: *Why does the dot product measure alignment between two vectors?*

---

## Milestone 2 -- Matrices as Machines

### Introduction: What you are going to learn and why

You are going to learn that a matrix is not a table of numbers -- it is a **transformation**. It takes a vector and moves it: stretches it, rotates it, squashes it, flips it, or projects it onto a smaller space.

This is the correct mental model, and it is the mental model that makes ML readable. Every neural network layer is a matrix transformation. The weight matrix W in a layer does not just "multiply" -- it changes the shape of the data, rotating and stretching it so that the next layer can operate on a more useful representation. If you understand what matrix multiplication does geometrically, you can reason about what layers are learning. Without this, you are blind to what your model is actually computing.

Gaussian elimination and the inverse are how you solve `Ax = b` -- the equation at the heart of linear regression, system identification, and most closed-form ML solutions.

### Topics to Study

- Matrices as rectangular arrays -- rows, columns, shapes, indexing
- Matrix addition and scalar multiplication
- **Matrix multiplication** -- the most important operation. Understand it three ways: (1) row-dot-column, (2) column combination view, (3) transformation composition
- Transpose -- (AB)^T = B^T A^T and the geometric meaning
- Identity matrix -- the "do nothing" transformation
- Inverse matrix -- the "undo" transformation, and when it exists
- Solving linear systems Ax = b
- Row operations -- swap, scale, add a multiple of one row to another
- Gaussian elimination and reduced row echelon form
- LU decomposition -- storing elimination as a factorization

### How to Study This

**Khan Academy:** Matrix multiplication, Inverse matrices, Solving systems with matrices.

**MIT 18.06:** Lectures 4-8. Strang's treatment of LU decomposition and the four subspaces begins here. The four subspaces section is not optional -- they appear in every subsequent topic.

**MML Book:** Sections 2.5-2.7. The mappings perspective connects matrices to the transformation idea.

### Implementation Milestone

```python
# 1. Matrix multiply from scratch -- no numpy.dot allowed
def matmul(A, B):
    # rows of A x columns of B
    # verify dimensions match before computing
    ...

# 2. Gaussian elimination
def gaussian_elim(A, b):
    # Build augmented matrix [A | b]
    # Forward elimination to row echelon form
    # Back substitution
    # Detect and report: unique / no solution / infinitely many
    ...

# 3. System solver with classification
def solve_system(A, b):
    # Use rank(A) vs rank([A|b]) vs n to classify
    # Return the solution or the appropriate message
    ...

# 4. Transformation visualizer
# Apply a 2x2 matrix to a grid of points in [-2,2] x [-2,2]
# Plot before (gray) and after (colored)
# Do this for: rotation, scaling, shear, projection onto x-axis
# The visual is the whole point -- if you cannot SEE the transformation, redo this
```

### Output: Matrix Systems Notebook

- Hand-solved examples (at least 5 systems of different types)
- Custom elimination code with test cases
- Transformation plots -- at least 4 different matrices visualized
- Written notes: what does the inverse actually do? Why is matrix multiplication not commutative?

### You Are Done When

- [ ] You can solve small systems manually without hesitation
- [ ] You can explain matrix multiplication geometrically -- not just row x column
- [ ] You understand why AB does not equal BA in general
- [ ] You can code Gaussian elimination without looking up each step
- [ ] You can answer: *What does multiplying by the inverse actually do to the transformation?*

---

## Milestone 3 -- Independence, Span, Basis, and Rank

### Introduction: What you are going to learn and why

You are going to learn the structural questions of linear algebra: which vectors are redundant? How many truly independent directions does a matrix contain? What information can this system express, and what information can it never produce?

This matters for ML because your data has structure that these concepts reveal. If two features in your dataset are linearly dependent -- one is a multiple of another -- your feature matrix is rank-deficient. The matrix (X^T X) in the linear regression normal equation becomes singular and uninvertible. The model breaks. Rank is not an abstract concept; it determines whether your problem is solvable.

The null space tells you what information a transformation destroys. In a neural network layer, vectors in the null space of the weight matrix produce zero output -- that is information that layer discards entirely. Understanding this is how you reason about information bottlenecks in deep networks.

### Topics to Study

- Linear independence -- formal definition and geometric meaning
- Linear dependence -- what makes a vector redundant
- Column space -- all vectors Ax can produce (lives in the output space)
- Row space -- span of the rows (lives in the input space)
- Null space -- all x such that Ax = 0 (what gets destroyed)
- Left null space -- all y such that A^T y = 0
- Basis -- a minimal spanning set for a space
- Dimension -- number of vectors in any basis for the space
- Rank -- number of independent columns (equals number of independent rows)
- Rank-nullity theorem: rank(A) + nullity(A) = n (number of columns)

### How to Study This

**MIT 18.06:** Lectures 7-11. Strang's four subspaces framework is the core of this milestone. The insight that every matrix has four subspaces -- coming in orthogonal complementary pairs -- is one of the deepest structural results in linear algebra.

**Khan Academy:** Linear independence, Null space and column space.

**MML Book:** Section 2.4 (Basis and Rank).

### Implementation Milestone

```python
# 1. Independence checker
def are_independent(vectors):
    # Stack vectors as columns of a matrix
    # Compute rank
    # If rank == number of vectors: independent
    ...

# 2. Basis extractor
def find_basis(vectors):
    # From a set of vectors (some may be dependent)
    # Return the minimal subset that spans the same space
    ...

# 3. Rank calculator via row reduction
def compute_rank(A):
    # Count pivots after row reduction
    ...

# 4. Null space solver
def null_space(A):
    # Find all x such that Ax = 0
    # Return a set of basis vectors for the null space
    ...

# 5. System classifier
def classify_system(A, b):
    # rank(A) vs rank([A|b]) vs number of unknowns
    # Return: "unique solution" / "no solution" / "infinitely many"
    ...
```

### Output: Subspaces and Rank Notebook

- Examples of independent and dependent sets with geometric explanation
- Rank calculations with interpretation
- Null space examples -- what does it mean for specific matrices?
- Summary table: conditions on rank for each type of solution

### You Are Done When

- [ ] You can look at a matrix and reason about its rank without full computation
- [ ] You understand why some systems have no solution -- geometrically
- [ ] You can explain null space as "what this transformation destroys"
- [ ] You can connect linear independence to feature redundancy in ML
- [ ] You can answer: *If rank(A) = 2 and A is 3x4, what is the dimension of the null space? Why?*

---

## Milestone 4 -- Orthogonality and Least Squares

### Introduction: What you are going to learn and why

**This is the milestone that directly unlocks ML.**

You are going to learn what happens when there is no exact solution to Ax = b -- which is almost always the case with real data. The answer is least squares: instead of finding an exact solution, find the **closest possible approximation**. That is the entire game of supervised learning, stated in one sentence.

When you run linear regression, you are computing the projection of the target vector y onto the column space of your feature matrix X. The residuals -- the prediction errors -- are the component of y that cannot be expressed using your features. The normal equation `beta = (X^T X)^{-1} X^T y` is the formula for this projection. This is not a formula to memorize; it is a geometric statement about finding the closest point in a subspace.

Gram-Schmidt and QR decomposition are how this is done in practice, more stably than inverting (X^T X).

### Topics to Study

- Orthogonal vectors -- dot product = 0
- Orthonormal vectors -- orthogonal + unit length
- Orthogonal complement -- the space perpendicular to a subspace
- Projections onto subspaces (not just single vectors)
- Gram-Schmidt process -- converting any basis to an orthonormal one
- QR decomposition -- A = QR, the result of Gram-Schmidt on A's columns
- Least squares -- minimizing ||Ax - b||^2 when no exact solution exists
- Normal equations -- A^T(Ax - b) = 0 leads to x = (A^T A)^{-1} A^T b
- Overdetermined systems -- more equations than unknowns
- Residual error -- the irreducible distance between y and its projection

### How to Study This

**MIT 18.06:** Lectures 14-17. Projection, least squares, Gram-Schmidt, QR. These four lectures are the most directly ML-relevant in the entire course.

**Khan Academy:** Orthogonal complements, Projections section.

**MML Book:** Sections 3.1-3.8 (Analytic Geometry -- norms, inner products, orthogonality, projections).

### Implementation Milestone

```python
# 1. Gram-Schmidt from scratch
def gram_schmidt(vectors):
    # Iteratively subtract projections onto previous orthonormal vectors
    # Return an orthonormal basis spanning the same space
    ...

# 2. Least squares regression via normal equation
def least_squares_normal(X, y):
    # beta = (X^T X)^{-1} X^T y
    # Add bias column (column of 1s) to X first
    ...

# 3. Compare three approaches on the same dataset
# a) Your normal equation implementation
# b) Simple gradient descent loop
# c) np.linalg.lstsq (uses SVD internally)
# Run on California Housing -- all three should give the same coefficients

# 4. Residual visualizer (2D case with one feature)
# Plot: data points, fitted line, vertical residual lines
# Show total squared error as a number

# 5. Overdetermined system experiment
# Create a system with 10 equations and 2 unknowns
# Show that no exact solution exists
# Show that least squares gives the closest approximation
```

### Output: Least Squares Notebook

- Gram-Schmidt implementation with step-by-step verification
- Regression from scratch with comparison against NumPy
- Residual plots with squared error displayed
- Written explanation: why does (X^T X)^{-1} X^T appear? (geometric, not algebraic)

### You Are Done When

- [ ] You can derive the logic of least squares from the projection formula
- [ ] You understand projection as "the closest point in the column space of X"
- [ ] You can explain residuals as "the part of y that no linear combination of features can express"
- [ ] You can build linear regression from scratch with no sklearn
- [ ] You can answer: *Why does (X^T X)^{-1} X^T appear in the normal equation?*

> **TRIGGER POINT:** After this milestone, begin the **FCC ML Course** and **Probability & Statistics Block 1** in parallel.

---

## Milestone 5 -- Eigenvalues and Eigenvectors

### Introduction: What you are going to learn and why

You are going to learn about the special directions of a matrix -- the directions it does not rotate, only scales. These are eigenvectors, and the scaling factors are eigenvalues.

Most vectors, when you apply a matrix to them, get rotated and stretched at the same time. Eigenvectors are special: the matrix only stretches or shrinks them, never rotates them. They are the "natural axes" of the transformation.

This matters enormously for ML. The covariance matrix of your data has eigenvectors -- those are the principal components in PCA, the directions of maximum variance. The Hessian matrix (matrix of second derivatives) of your loss function has eigenvectors -- those are the directions of maximum and minimum curvature of the loss landscape. A highly curved direction with a large eigenvalue means gradient descent will oscillate there. A flat direction with a small eigenvalue means gradient descent moves slowly. This is why batch normalization, careful weight initialization, and adaptive optimizers (Adam) exist: they are working around the eigenvalue structure of the Hessian.

### Topics to Study

- Eigenvectors and eigenvalues -- definition: Av = lambda * v
- Geometric interpretation -- eigenvectors are the "fixed directions" under A
- Characteristic equation -- det(A - lambda*I) = 0
- Finding eigenvectors -- solve (A - lambda*I)v = 0 for each eigenvalue
- Diagonalization -- A = P D P^{-1} when P has independent eigenvectors
- Symmetric matrices and the Spectral Theorem -- all eigenvalues real, eigenvectors orthogonal
- Positive semidefinite (PSD) matrices -- all eigenvalues >= 0; covariance matrices are always PSD
- Condition number -- lambda_max / lambda_min; high condition number means training instability

### How to Study This

**Khan Academy:** Eigenvalues and eigenvectors unit -- all videos.

**MIT 18.06:** Lectures 21-25. Eigenvalues, diagonalization, symmetric matrices, positive definite matrices. Do not skip lecture 25 on PSD matrices.

**MML Book:** Sections 4.1-4.4. The PSD section (Cholesky) connects directly to covariance matrices.

### Implementation Milestone

```python
# 1. Manual verification for 2x2 matrices
# Given A, lambda, v -- verify Av = lambda * v numerically

# 2. NumPy eigen computation with interpretation
import numpy as np
A = np.array([[3, 1], [1, 3]])
eigenvalues, eigenvectors = np.linalg.eig(A)
# For each eigenvector: visualize A*v and lambda*v -- show they are the same

# 3. Geometric visualization
# Plot a grid of unit vectors arranged in a circle
# Apply A to each one
# Show the result -- note that most get rotated AND stretched
# Highlight the eigenvectors -- they only scale, not rotate

# 4. Diagonalization demo
def diagonalize(A):
    # Return P, D such that A = P @ D @ inv(P)
    # Verify numerically
    ...

# 5. Repeated transformation experiment
# Apply A repeatedly (1, 5, 10, 50 times) to a random vector
# Plot the direction of the result at each step
# It converges to the dominant eigenvector -- this is power iteration
```

### Output: Eigen and Diagonalization Notebook

- Manual 2x2 examples with full hand derivation
- NumPy decomposition with visual verification
- Grid transformation plot with eigenvectors highlighted
- Diagonalization demo with A = P D P^{-1} verified
- Written note: why does the covariance matrix of data always have orthogonal eigenvectors?

### You Are Done When

- [ ] Eigenvectors feel geometric, not like formula outputs
- [ ] You can explain diagonalization as "finding the right coordinate system"
- [ ] You understand why symmetric matrices always have orthogonal eigenvectors
- [ ] You can connect condition number to gradient descent convergence speed
- [ ] You can answer: *Why does PCA need eigenvectors? What are they finding in the data?*

---

## Milestone 6 -- SVD and PCA

### Introduction: What you are going to learn and why

You are going to learn Singular Value Decomposition -- the generalization of eigendecomposition to all matrices, not just square ones. Every matrix A (any shape) can be written as A = U Sigma V^T. This is not a computational trick; it is a complete structural description of any linear transformation: rotate the input space (V^T), scale along coordinate axes (Sigma), rotate the output space (U).

PCA is one application: it finds the directions in your data that carry the most information (variance), so you can discard the rest. But SVD goes further. The singular values tell you the "effective rank" of a matrix -- how much of it is genuinely low-dimensional. This is the foundation of LoRA (Low-Rank Adaptation), the dominant technique for fine-tuning LLMs: weight update matrices are empirically low-rank, so you approximate them with a product of two small matrices. You built a presentation on LLM compression -- SVD is the mathematics underneath that work.

The Frobenius norm (used in L2 regularization on weights), the pseudoinverse (used by numpy.linalg.lstsq), and the condition number (used to diagnose training instability) all come from SVD.

### Topics to Study

- SVD definition -- A = U Sigma V^T for any m x n matrix
- U, Sigma, V^T -- geometric meaning: rotation, scale, rotation
- Singular values -- sigma_i = sqrt(eigenvalue of A^T A)
- Low-rank approximation (Eckart-Young theorem) -- best rank-k approx is A_k = U_k Sigma_k V_k^T
- Pseudoinverse -- A^+ = V Sigma^+ U^T, numerically stable least squares solution
- Frobenius norm -- ||A||_F = sqrt(sum of squared entries) = sqrt(sum of squared singular values)
- Spectral norm -- largest singular value; max amplification of any input vector
- Condition number -- sigma_max / sigma_min; high value means numerical instability
- PCA connection -- principal components = right singular vectors of the centered data matrix

### How to Study This

**MIT 18.06:** Lectures 29-31. SVD and principal component analysis.

**MML Book:** Sections 4.5-4.6 (SVD in depth) and Section 10.7 (PCA via SVD). Chapter 10 is the clearest treatment of PCA as a linear algebra problem.

### Implementation Milestone

```python
# 1. SVD on toy matrices -- study U, Sigma, V^T shapes and meanings
A = np.random.randn(4, 3)
U, s, Vt = np.linalg.svd(A, full_matrices=False)
# Verify: U @ np.diag(s) @ Vt == A (to floating point precision)
# Print: shapes of U, s, Vt; singular values; condition number

# 2. Low-rank approximation
def low_rank_approx(A, k):
    U, s, Vt = np.linalg.svd(A, full_matrices=False)
    return U[:, :k] @ np.diag(s[:k]) @ Vt[:k, :]
    # Compute Frobenius norm of error: ||A - A_k||_F

# 3. Image compression demo
# Load a grayscale image as a float matrix
# Reconstruct at k = 5, 20, 50, 100, 200
# Plot each reconstruction with its error and compression ratio
# Question: at what k does it become visually indistinguishable from original?

# 4. PCA from scratch -- complete implementation
def pca_from_scratch(X, n_components):
    # Step 1: center X (subtract column means)
    # Step 2: covariance matrix = (1/n) * X_centered^T @ X_centered
    # Step 3: eigendecomposition of covariance matrix
    # Step 4: sort eigenvectors by eigenvalue, descending
    # Step 5: project X_centered onto top-k eigenvectors
    ...

# Apply to Iris dataset (150 samples, 4 features --> 2 components)
# Color scatter plot by class label
# Verify projection matches sklearn.decomposition.PCA (up to sign flip)

# 5. Variance explained (scree plot)
# For each component: eigenvalue / sum(all eigenvalues)
# Plot: how much total variance is captured as you add more components
```

### Output: SVD and PCA Notebook

- SVD experiments with geometric interpretation written out
- Image compression demo with before/after plots at multiple k values
- PCA from scratch verified against sklearn
- Scree plot with variance explained
- Written answer: *Why is the first principal component the most important?*

### You Are Done When

- [ ] PCA feels like a geometric operation -- a change of basis -- not an algorithm
- [ ] You can explain SVD in plain language without notation
- [ ] You understand compression as singular value truncation
- [ ] You can connect Frobenius norm to weight regularization in neural networks
- [ ] You can answer: *If you keep only the top-2 singular values, what exactly are you discarding?*

---

## Milestone 7 -- ML Course Integration

### Introduction: What you are going to learn and why

This milestone is not a new math topic. It is the translation layer. The FCC ML course has been running in parallel since Milestone 4. Now, for every ML algorithm you encounter, your job is to trace it back to the linear algebra (and probability and calculus) it is built on.

This matters because completing a course and understanding a course are different things. If you can run a model but cannot explain the math underneath it, you have not learned the model -- you have learned to use a library. The entire purpose of the LA foundation is to make ML algorithms transparent, not magical.

The rule: for every FCC chapter, you produce one theory note connecting the algorithm to the math. You do not move past a chapter until you can write that note without notes.

### For Every ML Topic in FCC

```
linear regression     --> normal equation, projection, least squares (M4)
logistic regression   --> gradient descent, dot product, sigmoid (M1, M2 + Calculus)
k-means clustering    --> Euclidean distance, centroid as mean vector (M1)
PCA                   --> eigendecomposition, covariance matrix (M5, M6)
neural networks       --> matrix multiplication, chain rule (M2 + Calculus)
regularization        --> norms, Bayesian priors (M6 + Probability Block 3)
decision trees        --> information gain, entropy (Probability Block 1-2)
SVMs                  --> inner products, projections, margin maximization (M1, M4)
```

### Output: ML Course Notes + Implementations

For each FCC chapter, a one-page note containing:
1. What the model is doing in plain English
2. The matrix/vector operations involved
3. What the loss function is measuring (P&S connection)
4. One minimal from-scratch implementation

---

# PART II -- PROBABILITY & STATISTICS

## Why Probability & Statistics Starts at Milestone 4

You start P&S when you start FCC ML -- not before, not later. The trigger is Milestone 4 being complete and FCC ML beginning.

Here is specifically what breaks without probability in ML:

**Loss functions become meaningless.** Cross-entropy loss is the negative log-likelihood of a categorical distribution. MSE is the negative log-likelihood of a Gaussian. Without probability, these are arbitrary numbers you minimize because someone told you to.

**Model evaluation becomes dishonest.** 92% accuracy on a dataset where 92% of samples are class 0 means your model learned nothing -- it is just predicting the majority class. Precision, recall, F1, AUC-ROC all require probability to define properly.

**Regularization stays unexplained.** L2 regularization is MAP estimation with a Gaussian prior on weights. Without probability, it is a penalty term you add "to prevent overfitting" -- a ritual without understanding.

---

## P&S Block 1 -- Core Probability

### Introduction: What you are going to learn and why

You are going to learn the foundational rules of probability: how to combine probabilities, what conditional probability means, and Bayes' theorem -- the central equation of probabilistic ML.

This matters immediately when you start FCC ML, because the moment you train a classifier, it outputs probabilities. The loss function measures how wrong those probabilities are relative to the truth. Without understanding what a probability is -- not just a number between 0 and 1, but a statement about uncertainty -- you cannot understand what the training loop is actually doing.

### Topics to Study

- Sample spaces, events, probability axioms
- Joint P(A and B), marginal P(A), conditional P(A|B)
- Law of total probability
- Independence: P(A and B) = P(A) * P(B)
- **Bayes' theorem:** P(A|B) = P(B|A) * P(A) / P(B)
- Random variables -- discrete and continuous
- PMF (probability mass function) and PDF (probability density function)
- CDF (cumulative distribution function)
- Expectation E[X] and variance Var(X)

### Resources

**3Blue1Brown:** Watch "Bayes theorem" video before starting this block.

**Khan Academy:** Statistics and Probability unit -- all sections through conditional probability.

**MML Book:** Chapter 6, Sections 6.1-6.3.

### Implementation Milestone

Implement a **Naive Bayes spam classifier** from scratch. Given bag-of-words features:

```python
# Compute P(spam), P(not spam)
# For each word w: compute P(w | spam), P(w | not spam)
# For a new email: compute P(spam | words) using Bayes + conditional independence
# Compare accuracy against sklearn MultinomialNB
```

### You Are Done When

- [ ] You can apply Bayes' theorem to a concrete example without notes
- [ ] You understand the difference between P(A|B) and P(B|A)
- [ ] You understand what independence means for two features in a dataset
- [ ] Your Naive Bayes classifier runs and matches sklearn

---

## P&S Block 2 -- Distributions

### Introduction: What you are going to learn and why

You are going to learn the vocabulary of probabilistic ML: the distributions that appear over and over in every model and every loss function.

This matters because the choice of distribution determines the correct loss function. If your target variable is binary (spam/not spam), it follows a Bernoulli distribution, and the correct loss is binary cross-entropy. If your output is one of K classes, it follows a Categorical distribution, and the correct loss is cross-entropy. If your output is a continuous value with Gaussian noise, the correct loss is MSE. These are not arbitrary choices -- they are mathematically derived from the assumed distribution. Without knowing distributions, you apply loss functions as rules handed down from on high.

### Topics to Study

- Bernoulli and Binomial -- binary outcomes, binary classification
- Categorical -- multi-class labels; cross-entropy loss comes from this
- **Gaussian (Normal)** -- the most important distribution in ML: symmetric, defined by mu and sigma^2, Central Limit Theorem
- Multivariate Gaussian -- the covariance matrix is your M5 content (PSD, eigenvectors describe shape)
- How distribution choice determines loss function choice -- this is the key insight

### Implementation Milestone

```python
# Plot Gaussian PDF for different (mu, sigma) pairs
# Compute: P(X > 1.5), P(-1 < X < 1) for standard Gaussian
# Sample from a multivariate Gaussian and plot the 2D scatter
# Show how the covariance matrix's eigenvalues/eigenvectors control the shape
```

### You Are Done When

- [ ] You can describe when each distribution applies
- [ ] You can derive that Gaussian noise leads to MSE loss (not just assert it)
- [ ] You can connect multivariate Gaussian to the covariance matrix from M5

---

## P&S Block 3 -- Statistical Inference: The Math of Training

### Introduction: What you are going to learn and why

You are going to learn Maximum Likelihood Estimation (MLE) and Maximum A Posteriori (MAP) estimation -- the mathematical framework that training is an instance of.

This is the block where probability connects directly to what happens every time you call `.fit()`. Training a model with gradient descent on cross-entropy loss is computing an approximation to MLE for a categorical distribution. Adding L2 regularization to that training is computing MAP with a Gaussian prior on the weights. These are not analogies -- they are the same mathematical operation, stated in different notation. Understanding this means you can reason about regularization, loss function choices, and overfitting from first principles rather than as rules of thumb.

### Topics to Study

- **MLE:** theta_hat = argmax P(data | theta) -- find parameters that maximize data probability
- **MAP:** theta_hat = argmax P(data | theta) * P(theta) -- add a prior on parameters
- MAP with Gaussian prior = L2 regularization (prove this algebraically)
- MAP with Laplace prior = L1 regularization (prove this)
- Bias-variance tradeoff -- bias = systematic error, variance = sensitivity to training data
- Overfitting = high variance; underfitting = high bias
- Cross-validation -- why a single train/test split can be misleading

### Implementation Milestone

```python
# Dataset: 50 samples drawn from Gaussian(mu=2, sigma=1) + some noise

# 1. MLE estimate of mu: compute sample mean
# 2. MAP estimate with Gaussian prior mu ~ N(0, 1):
#    MAP_mu = (n * x_bar / sigma^2 + mu_prior / sigma_prior^2) / (n/sigma^2 + 1/sigma_prior^2)
# 3. Show on a plot how MAP pulls the estimate toward the prior mean
# 4. Show that as n -> infinity, MAP and MLE converge
```

### You Are Done When

- [ ] You can write the MLE objective for a Gaussian distribution
- [ ] You can show algebraically that MAP + Gaussian prior = L2 regularization
- [ ] You understand bias-variance as a real tradeoff, not just two bad things

---

## P&S Block 4 -- Model Evaluation

### Introduction: What you are going to learn and why

You are going to learn to evaluate models honestly. Training loss is not evaluation. Accuracy on a balanced test set is weak evaluation. Real evaluation requires understanding what you are actually measuring -- and most commonly used metrics are weaker than practitioners think.

This matters because model evaluation is how you know if you built something useful. A cancer screening model with 99% accuracy that always predicts "healthy" has killed patients. Understanding precision, recall, and the tradeoff between them means you can evaluate models for the actual task they need to perform, not for the metric that is easiest to maximize.

### Topics to Study

- Confusion matrix -- TP, TN, FP, FN (understand each geometrically)
- Precision = TP / (TP + FP) -- of all positive predictions, how many were correct?
- Recall = TP / (TP + FN) -- of all actual positives, how many did you catch?
- F1 = harmonic mean of precision and recall
- ROC curve -- performance at every possible decision threshold
- AUC -- area under the ROC curve; threshold-independent performance
- Cross-validation -- k-fold, stratified k-fold, when each is appropriate

### Implementation Milestone

```python
# Given: a trained binary classifier and a test set
# Build a FULL evaluation report from scratch -- numpy only, no sklearn.metrics

def evaluation_report(y_true, y_pred_prob, threshold=0.5):
    # Compute TP, TN, FP, FN from threshold
    # Compute precision, recall, F1
    # Plot ROC curve (sweep threshold from 0 to 1)
    # Compute AUC via trapezoidal rule
    ...
```

### You Are Done When

- [ ] You can compute all metrics from a raw confusion matrix
- [ ] You can explain when F1 is better than accuracy and exactly why
- [ ] You can interpret an ROC curve and explain what AUC measures
- [ ] Your evaluation report matches sklearn.metrics

---

# PART III -- CALCULUS

## Why Calculus Starts at Milestone 4-5

Do not start calculus because it is Week 7. Start calculus because **gradient descent has appeared in your ML work and you cannot answer the question: how is the model actually learning?** That is the trigger.

Here is specifically what breaks without calculus in ML:

**Backpropagation is a black box.** Backprop is the chain rule applied to a computational graph. Without the chain rule, you follow the algorithm without understanding it. You cannot debug it, modify it, or explain it.

**Training failures are mysterious.** Vanishing gradients, exploding gradients, learning rate sensitivity -- these are all properties of derivatives. Without calculus, you fight them with hyperparameter tuning and intuition borrowed from blog posts.

**Activation function choices are arbitrary.** ReLU replaced sigmoid not because it is "better" -- because its derivative is 1 for positive inputs (not near-zero), which prevents gradients from vanishing in deep networks. That is a calculus argument. Without it, activation functions are magic choices.

---

## Calculus Block 1 -- Derivatives

### Introduction: What you are going to learn and why

You are going to learn what a derivative is: the rate of change of a function at a point. The slope of the tangent line. The answer to "if I nudge this input slightly, how much does the output change?"

In ML, the input is a parameter (a weight), the output is the loss, and the derivative tells you in which direction to adjust the weight to decrease the loss. The gradient descent update -- theta = theta - alpha * gradient -- is three things: the gradient (calculus), the parameter vector (linear algebra), and the step size (a design choice). Without calculus, you cannot reason about any part of this update.

### Topics to Study

- What a derivative is: slope of tangent line, rate of change
- Notation: f'(x), dy/dx, partial d f / partial d x
- Power rule, product rule, quotient rule
- **Chain rule: d/dx[f(g(x))] = f'(g(x)) * g'(x)** -- the most important rule for ML
- Derivatives of ML functions: exp(x), log(x), sigmoid(x), ReLU(x), tanh(x)
- Critical points -- f'(x) = 0: local minima, local maxima, saddle points

### Resources

**3Blue1Brown:** Essence of Calculus series -- watch the full series before this block.

**Khan Academy:** Differential Calculus unit -- derivatives, chain rule.

**MML Book:** Chapter 5, Sections 5.1-5.2.

### Implementation Milestone

```python
# Implement gradient descent from scratch on f(x, y) = x^2 + 2y^2
# Gradient: [2x, 4y] -- compute this analytically, then verify numerically

def gradient_descent(f, grad_f, start, lr, steps):
    path = [start]
    pos = start.copy()
    for _ in range(steps):
        pos = pos - lr * grad_f(pos)
        path.append(pos.copy())
    return path

# Run with lr = 0.01 (too small), lr = 0.4 (good), lr = 1.1 (diverges)
# Plot the path taken on a contour plot of f for each learning rate
# The visual shows exactly why learning rate matters
```

### You Are Done When

- [ ] You can differentiate any composition of basic functions using the chain rule
- [ ] You know the derivatives of sigmoid, ReLU, and tanh
- [ ] You understand why ReLU's derivative prevents vanishing gradients
- [ ] Your gradient descent implementation converges and the path visualization is correct

---

## Calculus Block 2 -- Partial Derivatives and Gradients

### Introduction: What you are going to learn and why

A neural network has millions of parameters. The loss is a function of all of them simultaneously. A partial derivative asks: holding all other parameters fixed, how does the loss change when I nudge just this one? The gradient is the vector of all partial derivatives -- it points in the direction of steepest increase of the loss. Moving opposite to it decreases the loss.

This is the complete mathematical statement of gradient descent. The update rule theta = theta - alpha * gradient_L means: take a step in the direction that decreases L most steeply, with step size alpha.

### Topics to Study

- Partial derivative -- derivative with respect to one variable, others held fixed
- **Gradient vector** -- [partial L / partial theta_1, ..., partial L / partial theta_n]
- Directional derivative -- rate of change in arbitrary direction (dot product of gradient with direction; connects to M1)
- Why gradient descent uses -gradient: moving opposite to steepest ascent gives steepest descent
- Gradients of ML expressions: partial(W^T x) / partial W = x; partial(x^T A x) / partial x = 2Ax for symmetric A

### Implementation Milestone

```python
# Visualize the gradient field of f(x, y) = x^2 + 2y^2
# At each point on a grid: draw an arrow pointing in the gradient direction
# Overlay the gradient descent path from Block 1
# The arrows should point away from the origin; the path follows them backward
```

### You Are Done When

- [ ] You can compute partial derivatives for multivariate functions
- [ ] You understand geometrically why gradient descent uses -gradient
- [ ] You can derive the gradient of MSE loss with respect to the weight vector

---

## Calculus Block 3 -- Chain Rule in ML and Backpropagation

### Introduction: What you are going to learn and why

A neural network is a composite function: one function applied to another, applied to another, applied to another. Computing the gradient of the loss with respect to any weight requires the chain rule applied through every layer between that weight and the loss output. This is backpropagation.

Not an algorithm you memorize. A direct application of the chain rule from Block 1, applied to matrix multiplications and nonlinearities chained together.

The key insight: if Z = W @ X and the loss depends on Z, then partial L / partial X = W^T @ (partial L / partial Z). The transpose of the weight matrix appears not because of a rule -- because of the chain rule applied to matrix multiplication. This is a calculus result, not a pattern to memorize.

### Topics to Study

- Computational graphs -- neural networks as directed acyclic graphs
- Forward pass -- evaluate left to right: compute Z_1, A_1, Z_2, A_2, ...
- Backward pass -- apply chain rule right to left: compute gradients in reverse order
- Why W^T appears: if Z = WX, then partial L / partial X = W^T * (partial L / partial Z)
- Vanishing gradients: sigmoid derivative <= 0.25; after k layers this multiplies k times
- After 10 sigmoid layers: 0.25^10 = 9.5 * 10^{-7}. Gradients for early layers vanish.
- Exploding gradients: Jacobian norms > 1 multiplying repeatedly; gradient clipping as the fix

### Resources

**Andrej Karpathy -- micrograd:** Implement this. It is 150 lines of Python that build automatic differentiation from scratch. It is the best calculus exercise for ML that exists. Do this during Block 3.

**MML Book:** Chapter 5, Sections 5.3-5.6 (chain rule, automatic differentiation).

### Implementation Milestone

Implement **micrograd** from scratch. Build the Value class:

```python
class Value:
    def __init__(self, data, _children=(), _op=''):
        self.data = data
        self.grad = 0
        self._backward = lambda: None
        self._prev = set(_children)
        self._op = _op

    def __add__(self, other): ...   # forward + backward for addition
    def __mul__(self, other): ...   # forward + backward for multiply
    def tanh(self): ...             # forward + backward for tanh

    def backward(self):
        # Topological sort the computation graph
        # Call _backward() in reverse order
        ...
```

Train a tiny neural network on XOR using your micrograd. If it converges, you have implemented backpropagation correctly.

### You Are Done When

- [ ] You can walk through backprop on a 2-layer network, step by step, using chain rule
- [ ] You understand why W^T appears -- it is chain rule on matrix multiplication, not a rule to memorize
- [ ] You can explain vanishing gradients using sigmoid's derivative value
- [ ] Your micrograd implementation converges on XOR

---

## Calculus Block 4 -- Second-Order Methods and Optimization Geometry

### Introduction: What you are going to learn and why

The gradient tells you the direction and magnitude of steepest change. The Hessian matrix tells you the curvature -- how the gradient itself changes as you move. High curvature in a direction means the loss changes rapidly there; gradient descent must use a tiny step size to avoid overshooting. Low curvature means the surface is flat; gradient descent moves slowly.

The ratio of maximum to minimum curvature (the condition number of the Hessian) determines how difficult a loss surface is to optimize. A high condition number means some directions need tiny steps and other directions need large steps -- plain gradient descent cannot satisfy both at once. This is why adaptive optimizers (Adam, RMSProp) exist: they normalize the learning rate per parameter by the local curvature. Without understanding the Hessian, optimizers beyond vanilla SGD are unexplainable.

### Topics to Study

- Second derivative -- curvature: f''(x) > 0 means concave up (local minimum structure)
- **Hessian matrix** -- H = matrix of all second partial derivatives; always symmetric (Schwarz's theorem)
- Hessian eigenvalues = curvatures in principal directions (connects to M5)
- Condition number of Hessian = lambda_max / lambda_min -- determines convergence difficulty
- Convexity -- Hessian PSD everywhere: only one minimum; most neural network losses are non-convex
- Newton's method -- uses Hessian to correct step direction; fast near minimum but expensive

### Implementation Milestone

```python
# 1. Compute the Hessian of f(x, y) = x^4 - 2x^2*y + y^2 + 0.1*y^2 numerically
# Use finite differences: H[i,j] = (f(x + e_i + e_j) - f(x + e_i) - f(x + e_j) + f(x)) / e^2

# 2. Compute eigenvalues of the Hessian at several points
# Show that eigenvalues change across the surface

# 3. Train a small network (2 layers, 10 hidden units) on toy data
# At intervals during training, compute the approximate condition number of the loss Hessian
# Show how it changes as training progresses
```

### You Are Done When

- [ ] You can explain what the Hessian eigenvalues tell you about a loss surface
- [ ] You understand why high condition number causes training instability
- [ ] You can connect the Hessian to why BatchNorm, careful weight init, and Adam exist
- [ ] Your numerical Hessian matches the analytical Hessian on a test function

---

# PART IV -- DEEP LEARNING: THE INTEGRATION POINT

## Where All Three Pillars Converge

At deep learning, you are no longer learning one pillar at a time. Every concept requires all three simultaneously. Use this table as a diagnostic -- if any cell is unclear, you have a gap in that pillar.

| Deep Learning Concept | Linear Algebra | Probability & Stats | Calculus |
|---|---|---|---|
| Forward pass | Z = WX + b (matrix multiply) | -- | -- |
| Loss function | -- | Negative log-likelihood | Differentiable w.r.t. params |
| Backpropagation | W^T in gradient | -- | Chain rule on comp. graph |
| Attention mechanism | QK^T multiply, SVD intuition | Soft probability over tokens | Softmax gradient |
| Batch Normalization | -- | Mean, variance of activations | Gradient through normalization |
| Dropout | -- | Bernoulli sampling | Gradient through stochastic op |
| Weight initialization | Eigenvalues, condition number | Activation distribution | Gradient flow analysis |
| L2 Regularization | Frobenius norm of W | Gaussian prior (MAP) | Added gradient term |
| LoRA fine-tuning | SVD, rank of delta W | -- | Gradient through low-rank params |
| VAE | -- | KL divergence, reparameterization | Gradient through sampling |

---

# PART V -- DELIVERABLES AND PROGRESS TRACKING

## Notebooks to Build

| # | Notebook | Milestone | Contents |
|---|---|---|---|
| 1 | Vector Foundation Notebook | M1 | Theory notes, 10 hand problems, 4 code implementations, 2 visualizations |
| 2 | Matrix Systems Notebook | M2 | Hand-solved systems, elimination code, transformation plots |
| 3 | Subspaces and Rank Notebook | M3 | Independence checker, null space solver, system classifier |
| 4 | Least Squares Notebook | M4 | Gram-Schmidt, normal equation regression, residual visualization |
| 5 | Eigen and Diagonalization Notebook | M5 | Manual examples, geometric plots, diagonalization demo |
| 6 | SVD and PCA Notebook | M6 | Image compression, PCA from scratch, scree plot |
| 7 | ML Course Notes + Implementations | M7 | One theory page per FCC chapter, one from-scratch implementation |
| 8 | Probability Foundations Notebook | P&S B1-B2 | Bayes examples, distribution plots, Naive Bayes classifier |
| 9 | Inference and Evaluation Notebook | P&S B3-B4 | MLE vs MAP demo, full evaluation metrics |
| 10 | Calculus and Backprop Notebook | Calc B1-B4 | Gradient descent animation, micrograd, Hessian experiment |

## The Standard for Real Progress

**In math:** You can solve problems by hand. You can explain one concept in terms of another. Checkpoint questions answered without notes.

**In code:** You can implement without copy-pasting. You can test with small examples. You can compare against NumPy or sklearn. You can debug your own misunderstanding.

**In intuition:** You can visualize what is happening. You can tell a geometric story. You can explain why the formula exists -- not just what it computes.

If any one of these three is missing for a topic, your understanding of that topic is incomplete.

## Warning Signs

**Linear Algebra:**
- Can follow a derivation but not reproduce it --> weak at math
- Can implement with NumPy but not from scratch --> weak at implementation
- Understands the formula but cannot draw what it does --> weak at intuition

**Probability & Statistics:**
- FCC ML feels like "where did this formula come from?" --> started without P&S
- Finished a model, cannot explain what the loss measures --> no MLE understanding
- Reports only accuracy as a metric --> no evaluation knowledge

**Calculus:**
- Gradient descent "just works," no idea why --> calculus not started
- Backpropagation is a black box you follow --> chain rule not internalized
- Cannot explain vanishing gradients -- Block 1 incomplete

---

# PART VI -- RESOURCES REFERENCE

## Linear Algebra

| Resource | Purpose | How to Use |
|---|---|---|
| Khan Academy: Linear Algebra | Intuition and definitions | Use first for every topic -- build geometric picture before formulas |
| MIT 18.06 (Gilbert Strang) | Rigorous derivations, four subspaces | Use after intuition for depth and proof |
| MML Ch. 2-4 | ML-specific framing | Read after MIT to connect to algorithms |
| 3Blue1Brown: Essence of Linear Algebra | Deep geometric intuition | Watch full series during M1-M2 |

## Probability & Statistics

| Resource | Purpose | How to Use |
|---|---|---|
| Khan Academy: Statistics and Probability | Core concepts and practice | Definitions and practice problems |
| MML Ch. 6 | ML probability in paper notation | Read during P&S Blocks 2-3 |
| StatQuest (Josh Starmer) | Best intuition-first probability anywhere | Watch before each block |
| 3Blue1Brown: Bayes' Theorem | Single best Bayes explanation | Watch before Block 1 |

## Calculus

| Resource | Purpose | How to Use |
|---|---|---|
| Khan Academy: Differential Calculus | Derivatives and chain rule | Core Block 1-2 content |
| MML Ch. 5 (Vector Calculus) | Gradients and Jacobians in ML notation | Read during Blocks 2-3 |
| 3Blue1Brown: Essence of Calculus | Geometric intuition | Watch before Block 1 |
| Karpathy: micrograd | Backprop from scratch | Implement during Block 3 |

## ML Practice

| Resource | Purpose | When to Start |
|---|---|---|
| freeCodeCamp ML Course | Practical tools and workflows | After LA Milestone 4 |
| Karpathy: Neural Networks Zero to Hero | Connects all three pillars to modern DL | After LA M7 + P&S + Calc B1-3 |

---

*This document is a living reference. The week estimates are a framework -- the checkpoint questions are the real gates. Do not move forward until you can answer them without notes.*

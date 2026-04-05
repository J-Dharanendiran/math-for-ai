# Linear Algebra → Machine Learning: Complete Structured Roadmap

> **Who this is for:** A B.Tech AI/DS student going all-in on Linear Algebra with the goal of building a genuine mathematical foundation for ML — not just passing exams, but understanding *why* models work the way they do.
>
> **Resources in use:** Khan Academy Linear Algebra · MIT 18.06 (Gilbert Strang) · Mathematics for Machine Learning (MML, Deisenroth et al.) · freeCodeCamp ML Course
>
> **Total duration estimate:** 10–12 weeks (2–3 hrs/day)

---

## Why Are You Even Learning This?

Before touching a single formula, you need to answer this honestly: *why does an ML engineer need linear algebra?*

Here is the direct answer.

Every ML model — from a basic linear regression to a 70-billion parameter LLM — is fundamentally a sequence of linear algebraic operations. When you call `model.fit(X, y)` in sklearn, you are triggering matrix multiplications, eigendecompositions, and gradient computations under the hood. If you don't understand these, you are a button-presser. You can copy code. You cannot debug a broken model, explain why it underperforms, design a better architecture, or compress it for deployment.

Specifically:

**Neural networks are matrix multiplications.** A forward pass is literally `Z = W @ X + b`, applied layer after layer. Backpropagation is the chain rule applied to matrices — the gradient flowing backward is `W^T @ delta`. If you don't know what a matrix transpose does or why it appears here, you cannot reason about learning.

**Dimensionality reduction is linear algebra.** PCA, which underlies data preprocessing, feature extraction, and even parts of attention mechanisms in transformers, is an eigendecomposition of a covariance matrix. The "principal components" are eigenvectors. The "variance explained" is eigenvalues.

**Optimization is geometry in vector spaces.** Gradient descent moves a parameter vector in the direction of steepest descent in a loss landscape. The loss landscape is a surface in high-dimensional space. Understanding vectors, norms, and projections tells you *why* gradient descent works and *when* it fails (ill-conditioned matrices, saddle points).

**Data is a matrix.** Every dataset you will ever touch is a matrix: rows are samples, columns are features. Operations on datasets — centering, scaling, projecting, compressing — are matrix operations. Understanding rank, null space, and column space tells you what your data actually looks like structurally.

**Large Language Models are built on it.** The attention mechanism in transformers is: `Attention(Q, K, V) = softmax(QK^T / sqrt(d_k)) * V`. This is a sequence of matrix multiplications, a transpose, a dot product, and a scaling. SVD is used in LoRA (Low-Rank Adaptation), the dominant fine-tuning method for LLMs. You recently built a presentation on LLM compression — quantization and pruning both operate on weight matrices. Understanding the linear algebra makes that work non-trivial.

The bottom line: **linear algebra is the language that ML is written in.** Every other math topic (calculus, probability, statistics) sits on top of it. You learn this first, and you learn it properly.

---

## How to Use This Document

This roadmap has 5 phases. Each phase contains:

- **What you're learning** — the exact topics
- **Why each topic exists** — the ML motivation, not just the math
- **How it works internally** — the mechanism, not just the formula
- **Khan Academy reference** — which units/videos
- **MIT 18.06 reference** — which lectures
- **MML book reference** — which sections
- **Implementation milestone** — a concrete coding task you must complete before moving on
- **FCC ML sync point** — exactly when and how to integrate the freeCodeCamp ML course

---

## FCC ML Integration Strategy

This is important to understand upfront, because you asked specifically about this.

The freeCodeCamp ML course is a *practical* course — it teaches you how to use tools (sklearn, TensorFlow, etc.) to build models. The math roadmap here teaches you *why those tools work*. These are complementary, not redundant.

**The rule:** Start FCC ML at the beginning of Phase 2. Here is the full integration timeline:

| LA Phase | FCC ML Sections to Run Concurrently |
|---|---|
| Phase 1 (Vectors, Spaces) | Nothing yet. Pure math foundation first. |
| Phase 2 (Matrices, Systems) | FCC: Introduction to ML, Linear Regression |
| Phase 3 (Eigenvalues, PCA) | FCC: Classification, Logistic Regression, K-Means |
| Phase 4 (SVD, Norms) | FCC: Clustering, Dimensionality Reduction, Trees |
| Phase 5 (LA in ML) | FCC: Neural Networks, Deep Learning modules |

**Why not start FCC from day one?** Because Phase 1 is the vocabulary. If you start FCC without understanding vectors and vector spaces, you will use tools without knowing what they are operating on. Two weeks of pure math first pays dividends for everything after.

**How to run them together from Phase 2 onward:** Do LA in the morning (your deep focus session). Do FCC in the evening (lighter, practical, reinforces the theory you learned in the morning). They are scheduled to align: when you're learning matrix operations in LA, you're building linear regression in FCC — and you'll be able to see the exact math behind what sklearn is doing.

---

## Phase 1 — Vectors, Spaces, and Operations

**Duration:** Weeks 1–2  
**Difficulty:** Foundational (accessible, but don't rush it)

### What You're Learning

Vectors. Vector operations. Vector spaces. Linear combinations. Span. Basis. Linear independence.

### Why This Exists in ML

Everything in ML is a vector. A data point is a vector (its features are coordinates). A word in an embedding is a vector in high-dimensional space. A model's parameters are a vector. Gradients are vectors that point in a direction. A neural network layer maps one vector to another vector.

Without understanding what a vector *is* — not just as "an array of numbers" but as an object with direction and magnitude in a space — you are just shuffling numbers without knowing what they represent.

**Span and basis matter because:** Your dataset lives in some feature space. The basis of that space tells you the minimum number of independent directions needed to describe any point in it. PCA literally finds a new, better basis for your data. You cannot understand PCA without understanding basis and span.

**Linear independence matters because:** If two features in your dataset are linearly dependent (one is a linear combination of others), your feature matrix is rank-deficient. The matrix (AᵀA) in the normal equation for linear regression becomes singular — uninvertible — and the model breaks. This is why feature correlation is a real problem in ML, not just a statistical curiosity.

### How It Works Internally

A **vector space** is a set of objects (vectors) with two operations — addition and scalar multiplication — that satisfy 8 axioms. The key insight is: you don't need to think of vectors as arrows or coordinate pairs. Any set of objects that follows those rules is a vector space. Polynomials are vectors. Functions are vectors. This abstraction is what makes the framework so powerful.

A **linear combination** of vectors v₁, v₂, ..., vₙ with scalars c₁, c₂, ..., cₙ is: c₁v₁ + c₂v₂ + ... + cₙvₙ. The **span** of a set of vectors is the set of all possible linear combinations. If you can reach every point in the space, the vectors span the whole space.

A **basis** is a set of vectors that (1) spans the space and (2) is linearly independent (no vector is redundant — you can't build it from the others). The number of vectors in a basis is the **dimension** of the space.

**Linear independence check:** Vectors v₁, ..., vₙ are linearly independent if the only solution to c₁v₁ + ... + cₙvₙ = 0 is c₁ = c₂ = ... = cₙ = 0. If you can find other scalars that produce zero, one of the vectors is redundant.

### Resources

- **Khan Academy:** Vectors unit (all videos), Linear combinations and span, Linear independence
- **MIT 18.06:** Lecture 1 (The geometry of linear equations), Lecture 2 (Elimination with matrices), Lecture 3 (Matrix operations)
- **MML:** Chapter 2, Sections 2.1–2.4 (Linear Algebra, Vector Spaces, Linear Independence, Basis and Rank)

### Implementation Milestone 1

**Task:** Build a `Vector` class from scratch in pure Python (no NumPy).

```python
class Vector:
    def __init__(self, components: list):
        self.components = components
        self.dim = len(components)
    
    def __add__(self, other): ...         # element-wise addition
    def __mul__(self, scalar): ...        # scalar multiplication
    def dot(self, other): ...             # dot product: sum of element-wise products
    def magnitude(self): ...             # sqrt of sum of squares
    def normalize(self): ...             # divide by magnitude
    def is_orthogonal_to(self, other):   # dot product == 0
    
    def __repr__(self): ...
```

Then: write a function `are_linearly_independent(vectors: list[Vector]) -> bool` that checks independence by solving c₁v₁ + ... + cₙvₙ = 0 and checking if only the trivial solution exists.

Finally: verify all your results against NumPy. Every `.dot()` you wrote should match `np.dot()`. Every `.magnitude()` should match `np.linalg.norm()`.

**Why this task:** You can't fake understanding when you're writing the operations yourself. If you don't know why the dot product is computed the way it is, you'll get stuck. This is intentional.

**Checkpoint question before moving on:** Can you explain, in one sentence without formulas, why two orthogonal vectors are linearly independent? If not, re-read the span and linear independence material.

---

## Phase 2 — Matrices: Structure, Transformations, and Systems

**Duration:** Weeks 3–4  
**Difficulty:** Moderate (the conceptual density increases here)

### What You're Learning

Matrix multiplication. Transpose. Inverse. Rank. Null space. Column space. Row space. Gaussian elimination. LU decomposition.

### Why This Exists in ML

**Matrix multiplication is a forward pass.** In a neural network, every layer computes `Z = W @ X + b`. The weight matrix `W` transforms the input vector `X` into a new representation. Understanding what matrix multiplication *does geometrically* (it transforms vectors — rotates, stretches, projects them) tells you what a neural network layer is actually doing to your data.

**Rank tells you what your data can express.** The rank of a matrix is the number of linearly independent rows (or columns). If your feature matrix has rank less than the number of features, your data has redundancy — some features can be expressed as combinations of others. Low-rank matrices appear everywhere in ML: weight matrices in LLMs are approximated by low-rank matrices in LoRA precisely because they don't need full rank to capture the task-relevant information.

**The null space is where information is lost.** When you multiply Ax, vectors in the null space of A get mapped to zero — they disappear. In the context of a neural network layer, the null space of W represents input directions that produce no output. This is directly related to the problem of vanishing gradients and information bottlenecks.

**The column space is what the transformation can produce.** The output of a linear transformation Ax is always in the column space of A. If your target y is not in the column space of your feature matrix X, there is no exact solution to Xβ = y — which is why linear regression minimizes the distance from y to the column space (the "least squares" projection).

**Gaussian elimination is how systems are solved.** Every time you solve Ax = b, whether in linear regression, PDE solvers, or system identification, Gaussian elimination (or a variant) is running under the hood. LU decomposition is the factored form of Gaussian elimination that makes it efficient to solve multiple systems with the same A.

### How It Works Internally

**Matrix multiplication (A @ B):** The entry at row i, column j of the result is the dot product of row i of A with column j of B. This is the "row times column" view. But there is a better view: each column of the result (A @ B) is A applied to the corresponding column of B. Matrix multiplication is applying A to every column of B simultaneously.

**The Four Fundamental Subspaces (Strang's core idea):** For an m×n matrix A:
- **Column space C(A):** The span of the columns of A. Lives in ℝᵐ. Dimension = rank(A).
- **Null space N(A):** All x such that Ax = 0. Lives in ℝⁿ. Dimension = n - rank(A).
- **Row space C(Aᵀ):** The span of the rows of A. Lives in ℝⁿ. Dimension = rank(A).
- **Left null space N(Aᵀ):** All y such that Aᵀy = 0. Lives in ℝᵐ.

These four subspaces are the complete picture of what any matrix does.

**Why the rank-nullity theorem matters:** rank(A) + nullity(A) = n (number of columns). This tells you how much information any linear transformation preserves vs. loses.

**Gaussian elimination** reduces A to row echelon form by applying elementary row operations (swap rows, scale a row, add a multiple of one row to another). The pivots tell you the rank. The free variables (non-pivot columns) parameterize the null space.

**LU decomposition** writes A = LU where L is lower-triangular (with 1s on diagonal) and U is upper-triangular. This is just a way to store the elimination process. Solving Ax = b becomes: (1) solve Ly = b by forward substitution, (2) solve Ux = y by back substitution. Efficient for repeated solves with different b.

### Resources

- **Khan Academy:** Matrix multiplication, Inverse matrices, Solving systems with matrices
- **MIT 18.06:** Lectures 4–8 (LU decomposition, transposes, permutations, four subspaces)
- **MML:** Sections 2.5 (Linear Mappings), 2.6 (Basis Change), 2.7 (Linear Independence — continued), Chapter 2 summary

### Implementation Milestone 2 — Part A

**Task:** Implement Gaussian elimination and back-substitution from scratch.

```python
def gaussian_elimination(A: list[list[float]], b: list[float]) -> list[float]:
    """Solve Ax = b using Gaussian elimination with partial pivoting."""
    # Augmented matrix [A | b]
    # Forward elimination to row echelon form
    # Back substitution
    ...

def lu_decompose(A):
    """Return L, U such that A = L @ U"""
    ...
```

Test on at least three systems: one with a unique solution, one with no solution, one with infinite solutions. Your function should detect and report all three cases.

### Implementation Milestone 2 — Part B

**Task:** Implement linear regression via the normal equation, using only NumPy matrix operations (no sklearn).

The normal equation: **β = (XᵀX)⁻¹Xᵀy**

```python
import numpy as np

def linear_regression_normal_equation(X: np.ndarray, y: np.ndarray) -> np.ndarray:
    """
    X: (n_samples, n_features) — design matrix
    y: (n_samples,) — targets
    Returns: beta coefficients
    """
    # Add bias column (column of ones) to X
    # Compute X^T @ X
    # Compute its inverse using np.linalg.inv
    # Compute X^T @ y
    # Return the product
    ...
```

Use the California Housing dataset (5 features, ~20k samples). Compare your β against sklearn's `LinearRegression`. They should match to numerical precision.

**Why this task:** The normal equation is the closed-form solution to linear regression. It is a pure linear algebra expression. Implementing it forces you to understand that linear regression is not an algorithm — it is a matrix equation. The "algorithm" is just solving a system of linear equations.

**Checkpoint:** Can you explain why (XᵀX)⁻¹Xᵀ appears? Hint: the question is "what is the projection of y onto the column space of X?"

---

## Phase 3 — Eigenvalues, Eigenvectors, and Decompositions

**Duration:** Weeks 5–6  
**Difficulty:** High (this is where many students struggle — take your time)

### What You're Learning

Determinants. Eigenvalues and eigenvectors. Characteristic polynomial. Diagonalization. Symmetric matrices and their special properties. The spectral theorem. Positive (semi)definite matrices. Intuition for PCA. Introduction to SVD.

### Why This Exists in ML

This phase is arguably the most important for ML mathematics. Eigendecomposition underlies three of the most critical ideas in the field:

**Principal Component Analysis (PCA)** is an eigendecomposition. You compute the covariance matrix Σ of your data. Its eigenvectors are the principal components — the directions of maximum variance. Its eigenvalues tell you *how much* variance each direction captures. Projecting your data onto the top-k eigenvectors gives you the k-dimensional representation that preserves the most information. This is used in preprocessing, feature extraction, noise reduction, and visualization.

**Stability and convergence of optimization** depends on eigenvalues. The Hessian matrix of a loss function (second derivatives) is a symmetric matrix. Its eigenvalues determine the curvature of the loss landscape. If the ratio of the largest to smallest eigenvalue (the condition number) is large, gradient descent converges slowly and is numerically unstable. This is why batch normalization, weight initialization schemes, and adaptive optimizers (Adam) exist — they are all working around the eigenvalue structure of the Hessian.

**Covariance matrices are symmetric positive semidefinite.** This is not a coincidence. A covariance matrix Σ = XᵀX / n is always symmetric and always has non-negative eigenvalues. The eigenvectors of a covariance matrix are always orthogonal (due to the spectral theorem). This guarantees that PCA always produces an orthogonal basis.

**Markov chains and graph neural networks** use the dominant eigenvector. PageRank, the algorithm that built Google, is finding the dominant eigenvector of a transition matrix. Graph Laplacians in GNNs have spectra (eigenvalue distributions) that encode graph structure.

### How It Works Internally

**What an eigenvector is:** A vector v is an eigenvector of matrix A with eigenvalue λ if `Av = λv`. Geometrically: applying A to v only *scales* it (by λ) — it doesn't rotate it. Eigenvectors are the "special directions" of a transformation. Most vectors get rotated and stretched. Eigenvectors only get stretched.

**Finding eigenvalues:** Av = λv → Av - λv = 0 → (A - λI)v = 0. For a non-zero v to exist, the matrix (A - λI) must be singular (non-invertible), which means its determinant is zero. So you solve `det(A - λI) = 0`. This is the characteristic polynomial.

**Diagonalization:** If A has n linearly independent eigenvectors (columns of matrix P), then A = PDP⁻¹ where D is the diagonal matrix of eigenvalues. This decomposes the matrix into: change basis (P⁻¹), scale along each axis (D), change back (P). Powers of A become trivial: Aᵏ = PDᵏP⁻¹.

**Symmetric matrices are special (Spectral Theorem):** If A = Aᵀ, then (1) all eigenvalues are real, (2) eigenvectors for distinct eigenvalues are orthogonal, and (3) A can be diagonalized with an orthogonal matrix Q: A = QDQᵀ. Covariance matrices are always symmetric, so this always applies. Orthogonal eigenvectors mean the principal components are always perpendicular — no redundancy.

**Positive semidefinite (PSD):** A symmetric matrix A is PSD if xᵀAx ≥ 0 for all vectors x. This is equivalent to: all eigenvalues are ≥ 0. Covariance matrices are always PSD. PSD matrices are the "nice" matrices in ML — they define valid distances, valid kernels, and well-behaved loss surfaces.

### Resources

- **Khan Academy:** Determinants, Eigenvalues and eigenvectors (all videos in that unit)
- **MIT 18.06:** Lectures 21–25 (Eigenvalues/eigenvectors, diagonalization, differential equations, symmetric matrices, positive definite matrices)
- **MML:** Sections 4.1 (Determinants), 4.2 (Eigenvalues and Eigenvectors), 4.3 (Cholesky Decomposition), 4.4 (Eigendecomposition), 4.5 (SVD — first pass)

### FCC ML Sync Point — START FCC HERE (Phase 3)

At this point, begin these FCC sections *concurrently* with Phase 3:

- **Machine Learning with Python:** Introduction, supervised vs unsupervised overview
- **Classification algorithms:** k-NN, logistic regression
- **K-Means Clustering:** Pay specific attention — k-means assigns points to cluster centers. The notion of "distance from a center" is a Euclidean distance in the feature space. Understanding vectors and dot products makes this concrete.

When FCC covers PCA in preprocessing, you should already understand the math behind it from this phase. The goal is: every FCC model you implement, you should be able to trace back to the linear algebra.

### Implementation Milestone 3

**Task:** Implement PCA from scratch using only NumPy.

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris

def pca_from_scratch(X: np.ndarray, n_components: int) -> np.ndarray:
    """
    X: (n_samples, n_features) data matrix
    Returns: (n_samples, n_components) projected data
    
    Steps:
    1. Center X: subtract the mean of each feature
    2. Compute covariance matrix: (1/n) * X_centered^T @ X_centered
    3. Compute eigenvalues and eigenvectors of covariance matrix
    4. Sort eigenvectors by eigenvalue (descending)
    5. Project X_centered onto top-k eigenvectors
    """
    ...

# Load Iris (150 samples, 4 features, 3 classes)
X, y = load_iris(return_X_y=True)

# Run your PCA
X_projected = pca_from_scratch(X, n_components=2)

# Plot (color by class label)
plt.scatter(X_projected[:, 0], X_projected[:, 1], c=y, cmap='viridis')
plt.xlabel("PC1"); plt.ylabel("PC2")
plt.title("PCA from scratch — Iris dataset")
plt.savefig("pca_iris.png", dpi=150)

# Verification: compare against sklearn
from sklearn.decomposition import PCA
pca = PCA(n_components=2)
X_sk = pca.fit_transform(X)
print("Max diff from sklearn:", np.max(np.abs(np.abs(X_projected) - np.abs(X_sk))))
# (Note: sign flip is allowed — eigenvectors are defined up to sign)
```

**Variance explained:** After implementing, add a function that computes how much variance each principal component captures (eigenvalue / sum of all eigenvalues). Report what % of total variance the top-2 components capture for the Iris dataset.

**Checkpoint questions:**
1. Why do we center the data before computing the covariance matrix?
2. Why are the principal components orthogonal to each other?
3. If the first two PCs capture 95% of variance, what does the remaining 5% represent?

---

## Phase 4 — SVD, Norms, Orthogonality, and Projections

**Duration:** Weeks 7–8  
**Difficulty:** High (conceptually rich, deeply important)

### What You're Learning

Orthogonality and orthonormal bases. Projections and least squares (geometric view). Gram-Schmidt orthogonalization. QR decomposition. Matrix norms (Frobenius, spectral). Singular Value Decomposition (SVD) — full derivation and geometric interpretation. Pseudoinverse. Low-rank approximation.

### Why This Exists in ML

**SVD is the most important matrix decomposition in ML.** It generalizes eigendecomposition to *all* matrices (not just square ones). Every matrix A, regardless of shape, can be written as A = UΣVᵀ. This is not just a theoretical result — it has direct ML applications:

- **Dimensionality reduction:** Truncated SVD (keeping only the top-k singular values) gives the best rank-k approximation to A in terms of Frobenius norm. This is used in Latent Semantic Analysis (LSA) for text, in collaborative filtering for recommendation systems, and in data compression.
- **LoRA (Low-Rank Adaptation):** Fine-tuning LLMs by adding low-rank matrices ΔW = AB (where A is m×r and B is r×n, r << m,n) to frozen weight matrices. The motivation is that weight updates during fine-tuning are empirically low-rank. You decompose or approximate the update with SVD. You presented on this — now you can understand the math.
- **Pseudoinverse:** For overdetermined systems (more equations than unknowns), there's no exact solution to Ax = b. The pseudoinverse A⁺ = VΣ⁺Uᵀ gives the least-squares solution. This is what numpy's `lstsq` computes. It is more numerically stable than (AᵀA)⁻¹Aᵀ.
- **Condition number:** The condition number of A is σ_max / σ_min (ratio of largest to smallest singular value). A high condition number means the matrix is nearly singular — small perturbations in b produce large changes in the solution x. This is why ill-conditioned matrices cause numerical instability in training.
- **Matrix norms tell you how "large" a transformation is:** The spectral norm (largest singular value σ₁) is the maximum amplification any input vector can experience. The Frobenius norm sqrt(Σᵢⱼ Aᵢⱼ²) = sqrt(Σ σᵢ²) is used in regularization (weight decay is L2 regularization on the weight matrix).

**Projections are least squares.** When you solve a linear regression problem, you are projecting the target vector y onto the column space of X. The formula β = (XᵀX)⁻¹Xᵀy is the projection formula. Understanding projections geometrically means you understand why least squares works: it finds the closest point in the column space to y, where "closest" means minimum Euclidean distance.

### How It Works Internally

**Orthogonal projection:** The projection of vector y onto the column space of A is: ŷ = A(AᵀA)⁻¹Aᵀy. The matrix P = A(AᵀA)⁻¹Aᵀ is the projection matrix. Properties: P² = P (applying it twice does nothing — you're already projected), Pᵀ = P (symmetric). The residual (y - ŷ) is perpendicular to every column of A.

**Gram-Schmidt** takes any basis {v₁, ..., vₙ} and produces an orthonormal basis {u₁, ..., uₙ} by iteratively subtracting projections: u₁ = v₁/||v₁||, u₂ = (v₂ - proj_{u₁}(v₂)) / norm, etc.

**QR decomposition:** The result of Gram-Schmidt on the columns of A is A = QR, where Q has orthonormal columns and R is upper triangular. QR is the numerically preferred way to solve least squares: instead of forming XᵀX (which squares the condition number), you factor X = QR and solve Rβ = Qᵀy.

**SVD derivation:** For any matrix A (m×n):
- AᵀA is a symmetric n×n matrix → has real eigenvalues (σᵢ²) and orthonormal eigenvectors (columns of V).
- AAᵀ is a symmetric m×m matrix → has the same nonzero eigenvalues and orthonormal eigenvectors (columns of U).
- σᵢ = sqrt(eigenvalue of AᵀA) are the singular values.
- A = UΣVᵀ where U is m×m orthogonal, Σ is m×n diagonal (singular values on diagonal), Vᵀ is n×n orthogonal.

**Geometric interpretation of SVD:** Any linear transformation can be decomposed into three steps: (1) Vᵀ rotates the input, (2) Σ stretches along the coordinate axes, (3) U rotates again. It's rotation → stretch → rotation.

**Low-rank approximation (Eckart-Young theorem):** The best rank-k approximation to A (minimizing Frobenius norm of A - Aₖ) is Aₖ = U_k Σ_k V_kᵀ, where U_k, Σ_k, V_kᵀ are the first k columns/values/rows of the full SVD.

### Resources

- **Khan Academy:** Orthogonal complements, Projections (dot products and projections unit)
- **MIT 18.06:** Lectures 14–17 (Orthogonality, projections, least squares, Gram-Schmidt/QR), Lectures 29–31 (Singular Value Decomposition, principal component analysis)
- **MML:** Sections 3.1–3.8 (Analytic Geometry: norms, inner products, orthogonality, projections), Section 4.5–4.6 (SVD in depth), Section 10.7 (PCA via SVD)

### FCC ML Sync Point (Phase 4)

Run concurrently:
- **FCC: Clustering** (K-Means — now you can see that cluster assignments minimize intra-cluster variance, a geometric optimization)
- **FCC: Trees and Ensembles** (Random forests — note that feature importance is computed via how much each feature reduces impurity, which relates to variance concepts from SVD/PCA)
- Begin looking at any FCC neural networks module if available.

### Implementation Milestone 4

**Task:** Build an image compression tool using SVD.

```python
import numpy as np
import matplotlib.pyplot as plt
from PIL import Image

def compress_image_svd(image_path: str, k_values: list[int]) -> dict:
    """
    Load a grayscale image. Apply SVD. 
    Reconstruct at different rank-k approximations.
    Measure reconstruction error with Frobenius norm.
    """
    # Load image and convert to float array
    img = np.array(Image.open(image_path).convert('L'), dtype=float)
    
    # Full SVD
    U, s, Vt = np.linalg.svd(img, full_matrices=False)
    
    results = {}
    for k in k_values:
        # Reconstruct: use first k singular values/vectors
        img_k = U[:, :k] @ np.diag(s[:k]) @ Vt[:k, :]
        
        # Frobenius norm of error
        error = np.linalg.norm(img - img_k, 'fro')
        
        # Compression ratio: original stores m*n values
        # rank-k stores m*k + k + k*n = k*(m+n+1) values
        m, n = img.shape
        compression_ratio = (m * n) / (k * (m + n + 1))
        
        results[k] = {
            'image': img_k,
            'error': error,
            'variance_explained': np.sum(s[:k]**2) / np.sum(s**2),
            'compression_ratio': compression_ratio
        }
    
    return results

# Test with k = 5, 20, 50, 100, 200
results = compress_image_svd("your_image.jpg", k_values=[5, 20, 50, 100, 200])

# Plot reconstructions side by side
fig, axes = plt.subplots(1, len(results)+1, figsize=(18, 3))
# ... plot original and each reconstruction
```

**What to observe:** At what value of k does the image become visually indistinguishable from the original? What is the compression ratio at that point? What percentage of singular values (out of total) does that k represent? These observations directly connect to how LoRA works: the hypothesis is that weight updates are low-rank, meaning most singular values are near zero.

**Checkpoint:** Print the singular values of your image matrix. Do they decay quickly or slowly? What does a fast vs slow decay tell you about the structure of the image?

---

## Phase 5 — Linear Algebra Applied to Machine Learning

**Duration:** Weeks 9–10  
**Difficulty:** High (synthesis phase — ties everything together)

### What You're Learning

Jacobians and Hessians (matrix calculus). The chain rule in matrix form. Gradient descent as a vector operation. Backpropagation as matrix multiplication. The weight matrix structure of neural networks. Embeddings as vector spaces. Cosine similarity and inner product as similarity measures. Attention mechanism as a sequence of matrix operations.

### Why This Exists in ML

This phase does not introduce entirely new mathematical tools — it applies everything from Phases 1–4 to ML systems. After this phase, you should be able to look at any standard ML algorithm and identify the linear algebra operations it is performing.

**Gradient descent in matrix form:**  
Parameters θ are a vector. The loss L(θ) is a scalar function of θ. The gradient ∇L is a vector (same dimension as θ). The update rule is: θ ← θ - α∇L. This is a vector subtraction. In a neural network, θ is the concatenation of all weight matrices flattened. The gradient is computed via backpropagation.

**Backpropagation is matrix calculus:**  
The chain rule for matrices: if Z = W @ X, then ∂L/∂W = ∂L/∂Z @ Xᵀ and ∂L/∂X = Wᵀ @ ∂L/∂Z. Notice the transpose! Gradients flow backward through the transpose of the forward weight matrices. If you understand transposes and matrix multiplication, you understand why backprop works the way it does.

**Attention is matrix operations:**  
The scaled dot-product attention: `Attention(Q, K, V) = softmax(QKᵀ / √d_k) V`
- QKᵀ is a matrix multiplication producing similarity scores between queries and keys
- / √d_k is a scaling (divides by a scalar)
- softmax converts raw scores to a probability distribution (applied row-wise)
- multiply by V weights the values by attention probabilities
This entire mechanism is linear algebra with a nonlinearity (softmax) inserted.

**Embeddings are vectors in metric spaces:**  
A word embedding maps a discrete token to a continuous vector in ℝᵈ. Semantic similarity is measured by cosine similarity: cos(θ) = (u · v) / (||u|| ||v||). This is a normalized dot product — Phase 1 material. The fact that "king - man + woman ≈ queen" is a statement about linear structure in the embedding space.

### How It Works Internally

**The Jacobian:** For a vector-valued function f: ℝⁿ → ℝᵐ, the Jacobian J is an m×n matrix where Jᵢⱼ = ∂fᵢ/∂xⱼ. The gradient of a scalar function is a special case (m=1). The chain rule: if y = f(g(x)), then ∂y/∂x = (∂y/∂g)(∂g/∂x) — and these are matrix multiplications when y, g, x are vectors.

**Why the Hessian's eigenvalues control convergence:**  
The Hessian H = ∂²L/∂θ² is the Jacobian of the gradient. It is always symmetric (by Schwarz's theorem). Its eigenvalues are the curvatures along the principal directions. Where eigenvalues are large, the loss surface curves sharply — gradient descent takes tiny steps or oscillates. Where eigenvalues are small, the surface is flat — convergence is slow. The condition number κ = λ_max/λ_min determines convergence rate. This is why batch normalization helps: it conditions the Hessian.

**Numerical stability and why QR beats normal equations at scale:**  
Computing (XᵀX)⁻¹Xᵀy squares the condition number of X. If X has condition number κ, (XᵀX) has condition number κ². For large feature matrices, this causes catastrophic numerical error. QR decomposition solves the same problem with condition number κ. This is why sklearn's LinearRegression uses `np.linalg.lstsq` (which uses SVD internally) rather than the normal equation directly.

### Resources

- **MIT 18.06:** Lectures 27–28 (Positive definite matrices, similar matrices), Lecture 33 (Left and right inverses, pseudoinverse)
- **MML:** Chapter 5 (Vector Calculus — Jacobians, gradients), Chapter 6 (Probability — covariance matrices), Chapter 7 (Continuous Optimization — gradient descent, Hessians), Section 12.1 (Classification), Chapter 10 (Dimensionality Reduction via PCA — full treatment)
- **Supplemental:** Andrej Karpathy's "micrograd" (backprop from scratch, ~150 lines of Python)

### FCC ML Sync Point (Phase 5 — Full Overlap)

At this point, FCC and LA are deeply aligned:
- **FCC: Neural Networks** — you can now trace every forward pass as a matrix multiply and every backward pass as transposed matrix multiply
- **FCC: Deep Learning** — activation functions are applied element-wise to the result of linear transformations (Wx + b)
- Complete all remaining FCC modules here; the math gives you the "why" for every FCC concept you encounter

### Implementation Milestone 5 — Capstone

**Task:** Implement a 2-layer neural network entirely in NumPy. No PyTorch. No TensorFlow. No sklearn. Every operation must be traceable to a linear algebra concept.

```python
import numpy as np

class TwoLayerNet:
    def __init__(self, input_dim: int, hidden_dim: int, output_dim: int):
        # Xavier initialization: scale by sqrt(1/fan_in)
        self.W1 = np.random.randn(hidden_dim, input_dim) * np.sqrt(1.0 / input_dim)
        self.b1 = np.zeros((hidden_dim, 1))
        self.W2 = np.random.randn(output_dim, hidden_dim) * np.sqrt(1.0 / hidden_dim)
        self.b2 = np.zeros((output_dim, 1))
    
    def forward(self, X: np.ndarray) -> dict:
        """
        X: (input_dim, n_samples)
        Returns cache of intermediate values needed for backprop.
        
        Z1 = W1 @ X + b1      ← matrix multiply (Phase 2)
        A1 = sigmoid(Z1)       ← element-wise nonlinearity
        Z2 = W2 @ A1 + b2     ← matrix multiply (Phase 2)
        A2 = sigmoid(Z2)       ← output
        """
        ...
    
    def backward(self, X, y, cache: dict) -> dict:
        """
        Compute gradients via backpropagation.
        
        dZ2 = A2 - y                          ← output error
        dW2 = (1/m) * dZ2 @ A1^T             ← gradient w.r.t. W2 (Phase 4 — transpose!)
        db2 = (1/m) * sum(dZ2)
        
        dA1 = W2^T @ dZ2                      ← gradient flows back through W2 TRANSPOSE
        dZ1 = dA1 * sigmoid_derivative(Z1)
        dW1 = (1/m) * dZ1 @ X^T              ← gradient w.r.t. W1
        db1 = (1/m) * sum(dZ1)
        """
        ...
    
    def update(self, grads: dict, lr: float):
        """Gradient descent update: theta <- theta - lr * grad"""
        ...
    
    def train(self, X, y, lr=0.1, epochs=10000):
        losses = []
        for epoch in range(epochs):
            cache = self.forward(X)
            loss = self.compute_loss(cache['A2'], y)
            grads = self.backward(X, y, cache)
            self.update(grads, lr)
            if epoch % 1000 == 0:
                losses.append(loss)
                print(f"Epoch {epoch}, Loss: {loss:.4f}")
        return losses

# Train on XOR problem
X = np.array([[0,0],[0,1],[1,0],[1,1]]).T   # (2, 4)
y = np.array([[0,1,1,0]])                    # (1, 4)

net = TwoLayerNet(input_dim=2, hidden_dim=4, output_dim=1)
losses = net.train(X, y, lr=0.5, epochs=20000)

# Should converge to near-zero loss — XOR is learnable
print("Final predictions:", net.forward(X)['A2'])
# Expected: ~[0, 1, 1, 0]
```

**What every line maps to:**
- `W1 @ X + b1` → matrix multiply (Phase 2)
- `dW2 = dZ2 @ A1.T` → gradient via transpose (Phase 4, backprop)
- `W2.T @ dZ2` → gradient flowing backward through the transpose weight matrix
- Loss convergence curve → relates to Hessian eigenvalues and condition number (Phase 5 theory)

**After completing this:** you should be able to open the PyTorch source for `nn.Linear` and understand exactly what it is doing. The abstraction should be transparent to you.

---

## Parallel Tracks Summary

```
Week  |  Linear Algebra Phase         |  FCC ML Course
------+-------------------------------+----------------------------------
1     |  Phase 1: Vectors, Spaces     |  —
2     |  Phase 1: LA Independence     |  —
3     |  Phase 2: Matrices, Systems   |  Intro to ML, Regression
4     |  Phase 2: Normal Equation     |  Linear Regression, evaluation
5     |  Phase 3: Eigen, Symmetric    |  Classification, Logistic Reg.
6     |  Phase 3: PCA from scratch    |  K-Means, Clustering
7     |  Phase 4: SVD, Norms          |  Trees, Ensemble methods
8     |  Phase 4: Projections, QR     |  Dimensionality Reduction
9     |  Phase 5: Jacobians, Backprop |  Neural Networks
10    |  Phase 5: Capstone NN         |  Deep Learning, wrap-up
```

---

## Checkpoints: How to Know You're Ready to Move On

Do not move to the next phase until you can answer all questions in this section without looking anything up.

**After Phase 1:**
- What is the difference between the span of a set of vectors and a subspace?
- If vectors v₁ and v₂ are linearly dependent, what does that mean geometrically?
- Why does an orthogonal basis make computations easier?

**After Phase 2:**
- What are the four fundamental subspaces of a matrix? How are their dimensions related?
- If Ax = b has no solution, what does that mean geometrically about b and the column space of A?
- Why is the rank-nullity theorem useful? Give a concrete example.

**After Phase 3:**
- What does an eigenvector of a covariance matrix represent physically?
- Why are the eigenvectors of a symmetric matrix always orthogonal?
- If a matrix has condition number 10⁶, what problems does this cause for gradient descent?

**After Phase 4:**
- Why is the truncated SVD the best low-rank approximation?
- What is the pseudoinverse, and why is it more numerically stable than the normal equation?
- What does the Frobenius norm of a weight matrix measure in a neural network?

**After Phase 5:**
- Trace the full forward and backward pass of a linear layer, showing every matrix operation and its linear algebra meaning.
- Why does the gradient of a loss with respect to W involve Xᵀ?
- How does the attention mechanism in a transformer decompose into matrix operations?

---

## Common Mistakes to Avoid

**1. Memorizing formulas without understanding the geometry.**  
The formula A = UΣVᵀ is useless to you if you don't know what U, Σ, and V do geometrically. Always ask: what does this operation *do* to vectors?

**2. Skipping the proofs in MIT lectures.**  
Strang's proofs are not decoration. The proof that eigenvectors of symmetric matrices are orthogonal is exactly why PCA produces uncorrelated components. Watch the derivations, not just the results.

**3. Not connecting each LA concept to a specific ML operation.**  
Every section of this document tells you the ML connection. If you finish a phase and can't articulate why that math matters for a model you've actually used, review the "Why This Exists in ML" section.

**4. Using sklearn/PyTorch to verify before implementing manually.**  
The implementation milestones are in a specific order: build it yourself first, then verify against the library. Doing it the other way around removes the struggle that produces understanding.

**5. Treating FCC as "the main thing" and LA as supplementary.**  
FCC will make you a practitioner. LA will make you an engineer. You need both. But the math is the foundation — it does not serve the tools. The tools serve the math.

---

## Resources Quick Reference

| Resource | Best For | Access |
|---|---|---|
| Khan Academy: Linear Algebra | Intuition, visual understanding, gentle pacing | khanacademy.org |
| MIT 18.06 (Gilbert Strang) | Rigorous derivations, the four subspaces framework | YouTube / ocw.mit.edu |
| MML (Deisenroth et al.) | ML-specific framing, direct connection to algorithms | mml-book.github.io (free PDF) |
| freeCodeCamp ML | Practical implementation, sklearn/TF exposure | freecodecamp.org |
| Andrej Karpathy — micrograd | Backprop from scratch, ~150 lines | github.com/karpathy/micrograd |
| 3Blue1Brown — Essence of Linear Algebra | Geometric intuition before/during Phase 1–2 | YouTube |

---

*Generated as a structured learning reference. Revise the week estimates based on your actual pace — the implementation milestones are the real checkpoints, not the calendar.*

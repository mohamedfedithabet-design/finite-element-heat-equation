# Finite Element Method for the heat equation (Python)

Mini-project in numerical analysis at École Polytechnique de Tunisie (2026). I solve a steady heat-conduction problem with the **finite element method (MEF)** and compare the result with the exact solution.

**Stack:** Python, NumPy, SciPy (`quad`), SymPy, Matplotlib

## Notebooks

### 1. `01_heat_equation_1D_P2.ipynb`: 1D problem with P2 elements
- Problem: `-λ T''(x) = λ·T0·x² / L⁴` on `]0, L[`, with `T(0) = T(L) = 0`.
- Builds the **quadratic (P2) basis functions** τᵢ piecewise, for odd and even indices, on a mesh with step `h`.
- Assembles the load vector and the **stiffness matrix** by numerical integration, then solves the linear system.
- Computes the **exact solution** symbolically with SymPy (`dsolve`) and plots it against the FEM solution.
- Compares the two through the energy functional `J(u) = ½ a(u,u) − L(u)` and its relative error.

### 2. `02_heat_equation_radial_robin.ipynb`: radial problem with a Robin condition
- Problem in polar coordinates on `]R0, R1[`: Dirichlet condition `T(R0) = 0` and Robin condition `T'(R1) = −H·T(R1)`.
- Variational formulation and FEM solution of the radial problem.

## Run it

```bash
pip install numpy scipy sympy matplotlib jupyter
jupyter notebook
```

## Skills shown

Variational formulation, finite element discretization, numerical integration, symbolic vs numerical solutions, error analysis.

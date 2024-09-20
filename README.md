# AMG for solving Laplace's equation
Python implementations of AMG based on standard coarsening and direct interpolation, as well as on smoothed aggregation. [AMGLaplace](AMGLaplace.ipynb) is implemented with standard coarsening, while [AMGAggregation](AMGAggregation.ipynb) uses smoothed aggregation. The model problem solved with the codes is the two-dimensional Laplace's equation on a square 

$$\nabla^2 u(x,y) = 0,$$ 

with boundary conditions $u(x,H)=0$, $u(L,y)=0$, $u(0,y)=0$ and $u(x,0)=V(x)$. We choose $V(x)=\sin (2\pi x/L)$ to compare with the analytical solution 

$$u(x,y)=\frac{\sin \frac{2\pi x}{L} \sinh\frac{2\pi (H-y)}{L} }{\sinh\frac{2\pi H}{L}}.$$

The code uses Laplace's equation as a testbed, but it can actually be used for any matrix problem $A \textbf{u}=\textbf{f}$, only the matrix $A$ and vector $\textbf{f}$ have to be modified in the program. For more details check the PDF file. The following references were considered:

* K.Stüben, "Algebraic Multigrid (AMG): An Introduction with Applications", GMD, (1999).
* J. Volker, "Multigrid Methods", Weierstrass Institute, (2013).
* P. Vaněk, J. Mandel and M. Brezina, "Algebraic multigrid by smoothed aggregation for second and fourth order elliptic problems", *Computing* **56**, 179-196 (1996).



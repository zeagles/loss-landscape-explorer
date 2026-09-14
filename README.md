# Loss Landscape Explorer ❖

An interactive, web-based 3D visualizer for exploring optimization trajectories (SGDM vs. Adam) and real-time Hessian curvature analysis on a non-convex loss surface.

## 🚀 Live Demo
- [View Live Demo](https://zeagles.github.io/loss-landscape-explorer/)

## ✨ Key Features
- **3D Surface Visualization**: Interactive rendering of a non-convex loss function using Three.js and OrbitControls.
- **Real-Time Hessian Analysis**: Calculates Hessian matrices, eigenvalues ($\lambda_1, \lambda_2$), and eigenvectors on the fly.
- **Curvature Vectors**: Displays directional arrows representing maximum and minimum curvature at current optimizer positions.
- **Optimizer Comparison**: Side-by-side simulation of SGDM (Stochastic Gradient Descent with Momentum) and Adam.
- **Dynamic Parameters**: Tweak learning rate ($\eta$), momentum ($\gamma$), Adam $\beta_1$, and simulation speed in real time.
- **TeX Formulas**: Clean mathematical expression rendering via KaTeX.

## 📐 Loss Function & Math
The landscape is defined by the non-convex function with a saddle point at $(0, 0)$:

$$L(x, y) = x^2 - y^2 + 0.1 y^4$$

The Hessian matrix $H$ is computed dynamically:

$$H = \begin{pmatrix} \frac{\partial^2 L}{\partial x^2} & \frac{\partial^2 L}{\partial x \partial y} \\[4pt] \frac{\partial^2 L}{\partial y \partial x} & \frac{\partial^2 L}{\partial y^2} \end{pmatrix} = \begin{pmatrix} 2.0 & 0.0 \\ 0.0 & -2.0 + 1.2 y^2 \end{pmatrix}$$

## 🛠 Tech Stack
- **HTML5 / CSS3 / JavaScript** (Single-file application)
- **Three.js** (3D WebGL Rendering)
- **KaTeX** (TeX math rendering)

## 📄 License
MIT License

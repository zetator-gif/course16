## graph of \( T(t) = \sin(t) \)

We define the function:

$$
T(t) = \sin(t)
$$
### Python code to plot the function
```python
import numpy as np
import matplotlib.pyplot as plt

t = np.linspace(-2*np.pi, 2*np.pi, 400)
T = np.sin(t)

plt.plot(t, T)
plt.xlabel("t")
plt.ylabel("T(t)")
plt.title("Graph of T(t) = sin(t)")
plt.grid(True)
plt.show()
```

## attrition rate -simple

$$
 \dfrac{dX_R}{d_t} = -α_BX_B
$$

"Linear programming is actually an optimization technique used to get a
performance index (an objective function) to its maximum or minimum within the
constraints of resources or technology limitations."

$$
VTOL ⊂ V/STOL
$$

1002. **concise tetrahedron notation**

$$  
T = {P,Qx,Qy,Qz}
$$

refreshing the kernel from local jupyter cell while installing python packages from another cmd instance at the same time while notebook is running: 

```
import sys
!{sys.executable} -m pip install package_name
```

```
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d.art3d import Poly3DCollection

# Define the vertices of the tetrahedron
vertices = np.array([
    [1, 1, 1],   # Vertex P
    [-1, -1, 1], # Vertex Q1
    [-1, 1, -1], # Vertex Q2
    [1, -1, -1]  # Vertex Q3
])

# Define the faces of the tetrahedron
faces = [[vertices[j] for j in [0, 1, 2]],
         [vertices[j] for j in [0, 1, 3]],
         [vertices[j] for j in [0, 2, 3]],
         [vertices[j] for j in [1, 2, 3]]]

# Create a 3D plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Create a Poly3DCollection and add it to the plot
tetrahedron = Poly3DCollection(faces, alpha=.25, linewidths=1, edgecolors='r')
ax.add_collection3d(tetrahedron)

# Highlight edges from vertex P to Q1 and Q2
ax.plot([vertices[0][0], vertices[1][0]], [vertices[0][1], vertices[1][1]], [vertices[0][2], vertices[1][2]], color='blue', linewidth=2)
ax.plot([vertices[0][0], vertices[2][0]], [vertices[0][1], vertices[2][1]], [vertices[0][2], vertices[2][2]], color='green', linewidth=2)

# Annotate the angle α at vertex P
ax.text(vertices[0][0], vertices[0][1], vertices[0][2], 'α', fontsize=15, color='black')

# Set the limits and labels
ax.set_xlim([-2, 2])
ax.set_ylim([-2, 2])
ax.set_zlim([-2, 2])
ax.set_xlabel('X-axis')
ax.set_ylabel('Y-axis')
```

https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/sine-cosine-tangent/
<img width="594" height="600" alt="image" src="https://github.com/user-attachments/assets/db17251e-80f4-4231-89a4-f2316c4614c1" />

$$
T(t) =y\Leftarrow T^{-1}(y)=t
$$

1004. **tiny tetrahedral fluid element**
      • relating normal stresses on perpendicular faces to the stress on the inclined face
      


problem 1004. https://stackoverflow.com/questions/67482409/how-to-rotate-my-3d-plots-by-mouse-in-pycharm-professional

```python
import matplotlib.pyplot as plt
import matplotlib.patches as patches

fig, ax = plt.subplots(figsize=(6, 6))

# Ellipses
ellipse_A = patches.Ellipse((0.3, 0.8), width=0.4, height=0.2, edgecolor='black', facecolor='none')
ellipse_B = patches.Ellipse((0.3, 0.5), width=0.4, height=0.2, edgecolor='black', facecolor='none')
ellipse_C = patches.Ellipse((0.3, 0.2), width=0.4, height=0.2, edgecolor='black', facecolor='none')

ax.add_patch(ellipse_A)
ax.add_patch(ellipse_B)
ax.add_patch(ellipse_C)

# Points inside ellipses
ax.plot(0.3, 0.8, 'ko')  # x_0
ax.text(0.25, 0.82, r'$x_0$', fontsize=12)

ax.plot(0.3, 0.5, 'ko')  # g(x_0)
ax.text(0.25, 0.52, r'$g(x_0)$', fontsize=12)

ax.plot(0.3, 0.2, 'ko')  # y_0
ax.text(0.25, 0.22, r'$y_0 = f(g(x_0))$', fontsize=12)

# Labels A, B, C
ax.text(0.1, 0.9, 'A', fontsize=14, fontweight='bold')
ax.text(0.1, 0.6, 'B', fontsize=14, fontweight='bold')
ax.text(0.1, 0.3, 'C', fontsize=14, fontweight='bold')

# Arrows and text labels for functions
# Arrow x0 to g(x0)
ax.annotate('', xy=(0.3, 0.65), xytext=(0.3, 0.75), arrowprops=dict(arrowstyle='->'))
ax.text(0.33, 0.7, r'$g(x)$', fontsize=12)

# Arrow g(x0) to y0
ax.annotate('', xy=(0.3, 0.35), xytext=(0.3, 0.45), arrowprops=dict(arrowstyle='->'))
ax.text(0.33, 0.4, r'$f(x)$', fontsize=12)

# Arrow x0 to y0 (left side)
ax.annotate('', xy=(0.45, 0.3), xytext=(0.45, 0.75), arrowprops=dict(arrowstyle='->'))
ax.text(0.46, 0.55, r'$f \circ g(x)$', fontsize=12, rotation=90)

# Arrow top right (g*(y) o f*(y))
ax.annotate('', xy=(0.5, 0.78), xytext=(0.5, 0.52), arrowprops=dict(arrowstyle='->'))
ax.text(0.52, 0.65, r'$g^*(y) \circ f^*(y)$', fontsize=10, rotation=90)

# Hide axes
ax.axis('off')
ax.set_xlim(0, 0.7)
ax.set_ylim(0, 1)

plt.show()
```

<img width="500" height="494" alt="image" src="https://github.com/user-attachments/assets/12bf6ad0-f3ce-4946-93e6-41fa0b52ac06" />

## radicalization
inverse of exponentiation <br>
(“nth root of a”)

$$
\sqrt[n]{a}
$$



































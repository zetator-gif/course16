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







































```python
import numpy as np
import matplotlib.pyplot as plt

# Horizontal positions along the cylinder
x = np.linspace(0, 10, 100)

# Pressure is the same at all points on the same horizontal plane
pressure = np.ones_like(x) * 101325  # Pa (example: atmospheric pressure)

plt.figure(figsize=(6, 4))
plt.plot(x, pressure, label="Pressure along horizontal plane")
plt.scatter([2, 8], [101325, 101325], color='red', zorder=5,
            label="Two points on same horizontal plane")

plt.xlabel("Horizontal position along cylinder (x)")
plt.ylabel("Pressure (Pa)")
plt.title("Pressure at Two Points on the Same Horizontal Plane")
plt.legend()
plt.grid(True)
plt.tight_layout()
plt.show()
```
<img width="555" height="299" alt="image" src="https://github.com/user-attachments/assets/2dc984a9-5e89-4b33-9382-7b9ec04fffd8" />

```python
import numpy as np
import matplotlib.pyplot as plt

# Geometry
L = 10        # cylinder length
R = 1         # radius

# Cylinder surface
x = np.linspace(0, L, 120)
theta = np.linspace(0, 2*np.pi, 80)
X, T = np.meshgrid(x, theta)

Y = R * np.cos(T)
Z = R * np.sin(T)

# Choose ONE horizontal plane (constant height)
z_plane = 0.4

# Plot
fig = plt.figure(figsize=(9, 6))
ax = fig.add_subplot(111, projection='3d')

# Cylinder
ax.plot_surface(X, Y, Z, color='lightgray', alpha=0.6)

# Horizontal plane (pressure-equal plane)
Xp, Yp = np.meshgrid(np.linspace(0, L, 30),
                     np.linspace(-R, R, 30))
Zp = np.full_like(Xp, z_plane)

ax.plot_surface(Xp, Yp, Zp, color='blue', alpha=0.25)

# Two points on the SAME horizontal plane
ax.scatter(
    [2, 8],          # different x positions
    [0.6, -0.6],     # different circumferential positions
    [z_plane, z_plane],  # SAME HEIGHT
    color='red',
    s=80,
    label="Same horizontal plane → same pressure"
)

# Labels
ax.set_xlabel("x (along cylinder)")
ax.set_ylabel("y")
ax.set_zlabel("z (vertical)")
ax.set_title("Two Points on the Same Horizontal Plane in a Gas at Rest")

ax.legend()
ax.set_box_aspect((L, 2*R, 2*R))
plt.tight_layout()
plt.show()
```
<img width="489" height="387" alt="image" src="https://github.com/user-attachments/assets/aea17479-db21-47c2-ba96-7d6317fddc0b" />

$$
R_{specific}=\frac{Pv}{T}
$$

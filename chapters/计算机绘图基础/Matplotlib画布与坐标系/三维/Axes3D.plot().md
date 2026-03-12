# 感受matplotlib的Axes3D.plot()

### 渲染出多个点连成的直线

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0,10,50], [0,10,50], [0,10,50])   # ([x1,x2,x3],[y1,y2,y3],[z1,z2,z3]) 
ax.plot([0,10,50], [0,10,50], [0,10,50])      # ([x1,x2,x3],[y1,y2,y3],[z1,z2,z3])
# ax.scatter([0,10,50,100], [0,10,50,50], [0,10, 50,10])
# ax.plot([0,10,50,100], [0,10,50,50], [0,10, 50,10])

plt.show()
```
### 渲染出多个点连成的参数化曲线

```python
import numpy as np
import matplotlib.pyplot as plt

ax = plt.figure().add_subplot(111, projection='3d')

# Prepare arrays x, y, z
theta = np.linspace(-4 * np.pi, 4 * np.pi, 100)
z = np.linspace(-2, 2, 100)
r = z**2 + 1
x = r * np.sin(theta)
y = r * np.cos(theta)

ax.plot(x, y, z)

plt.show()
```

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [plot(xs, ys, *args, zdir='z', **kwargs)](https://matplotlib.org/stable/api/_as_gen/mpl_toolkits.mplot3d.axes3d.Axes3D.html#mpl_toolkits.mplot3d.axes3d.Axes3D.plot)


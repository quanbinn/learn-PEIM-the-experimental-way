# 感受matplotlib的Axes3D.plot_surface()

```python
import numpy as np
from matplotlib import pyplot as plt

ax = plt.figure().add_subplot(111, projection='3d')

X = np.array([[0, 1, 2, 3],
             [0, 1, 2, 3],
             [0, 1, 2, 3],
             [0, 1, 2, 3]]
            )
Y = np.array([[0, 0, 0, 0],
             [1, 1, 1, 1],
             [2, 2, 2, 2],
             [3, 3, 3, 3]]
            )
Z = np.array([[1.5, 1.5, 1.5, 1.5],
             [1.5, 1.5, 1.5, 1.5],
             [1.5, 3, 1.5, 1.5],
             [1.5, 1.5, 1.5, 10]]
            )

print(type(X))

# 绘出1.5(米)的水平面(平均身高男性眼眼睛瞳孔的高度)
ax.plot_surface(X, 
                Y, 
                Z
                ) 
     
plt.show()
```

```python
import numpy as np
from matplotlib import pyplot as plt

fig = plt.figure()
ax = fig.gca(projection='3d')

# print(type(X))
X=np.array([[1,2,3],
           [1,2,3]])
Y=np.array([[7,7,7],
           [8,8,10]])

# 绘出1.5(米)的水平面(平均身高男性眼眼睛瞳孔的高度)
ax.plot_surface(X, 
                Y, 
                Z=X*0+1.5
               ) 
     
plt.show()
```

```python
import matplotlib.pyplot as plt
from matplotlib import cm
import numpy as np

fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

X = np.arange(-5, 5, 0.25)
Y = np.arange(-5, 5, 0.25)
X, Y = np.meshgrid(X, Y)

R = np.sqrt(X**2 + Y**2)
Z = np.sin(R)

ax.plot_surface(X, Y, Z, rstride=1, cstride=1, cmap=cm.coolwarm, linewidth=0, antialiased=False)

plt.show()
```

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [plot_surface(X, Y, Z, *, norm=None, vmin=None, vmax=None, lightsource=None, **kwargs)](https://matplotlib.org/stable/api/_as_gen/mpl_toolkits.mplot3d.axes3d.Axes3D.html#mpl_toolkits.mplot3d.axes3d.Axes3D.plot_surface)
3. [Python 编程—list 与 numpy.ndarray](https://www.jianshu.com/p/f8e6a0a6399f)


# 感受matplotlib的Axes3D.scatter()

### 渲染出1个点

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0], [0], [0])				# ([x1,x2,x3,...],[y1,y2,y3,...],[z1,z2,z3,...]) 

plt.show()
```

### 渲染出2个点

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0,10], [0,10], [0,10])		# ([x1,x2,x3,...],[y1,y2,y3,...],[z1,z2,z3,...]) 

plt.show()
```

### 渲染出多个点

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0,10,50], [0,10,50], [0,10, 50])		# ([x1,x2,x3,...],[y1,y2,y3,...],[z1,z2,z3,...]) 
# ax.scatter([0,10,50,100], [0,10,50,50], [0,10, 50,10])

plt.show()
```

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [scatter(xs, ys, zs=0, zdir='z', s=20, c=None, depthshade=True, *args, data=None, **kwargs)](https://matplotlib.org/stable/api/_as_gen/mpl_toolkits.mplot3d.axes3d.Axes3D.html#mpl_toolkits.mplot3d.axes3d.Axes3D.scatter)


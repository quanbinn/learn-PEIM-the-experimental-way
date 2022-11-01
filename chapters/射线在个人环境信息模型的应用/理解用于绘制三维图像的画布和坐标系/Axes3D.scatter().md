# 感受matplotlib的Axes3D.scatter()

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

### 渲染出1个点
 
```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0], [0], [0])

plt.show()
```

### 渲染出2个点

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0,10], [0,10], [0,10])

plt.show()
```

### 渲染出多个点

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0,10,50], [0,10,50], [0,10, 50])
# ax.scatter([0,10,50,100], [0,10,50,50], [0,10, 50,10])

plt.show()
```

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [scatter(xs, ys, zs=0, zdir='z', s=20, c=None, depthshade=True, *args, data=None, **kwargs)](https://matplotlib.org/stable/api/_as_gen/mpl_toolkits.mplot3d.axes3d.Axes3D.html#mpl_toolkits.mplot3d.axes3d.Axes3D.scatter)


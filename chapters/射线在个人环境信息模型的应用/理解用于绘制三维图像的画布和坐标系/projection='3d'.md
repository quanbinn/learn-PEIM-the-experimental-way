# 感受matplotlib的projection='3d'

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

### 在三维空间中渲染出一个点
 
```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0], [0], [0])

plt.show()
```

### 在三维空间中渲染出两个点连成的直线

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.plot([0,10], [0,10], [0,10])

plt.show()
```

### 在三维空间中渲染出一个平点

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

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [**mpl_toolkits.mplot3d.axes3d.Axes3D**](https://matplotlib.org/stable/api/_as_gen/mpl_toolkits.mplot3d.axes3d.Axes3D.html#mpl_toolkits.mplot3d.axes3d.Axes3D)
3. [add_subplot(*args, **kwargs)](https://matplotlib.org/stable/api/figure_api.html#matplotlib.figure.Figure.add_subplot)
4. [python 画二维、三维点之间的线段实现方法](https://www.jb51.net/article/164754.htm)



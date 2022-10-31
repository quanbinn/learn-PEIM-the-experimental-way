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

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [**mpl_toolkits.mplot3d.axes3d.Axes3D**](https://matplotlib.org/stable/api/_as_gen/mpl_toolkits.mplot3d.axes3d.Axes3D.html#mpl_toolkits.mplot3d.axes3d.Axes3D)
3. [add_subplot(*args, **kwargs)](https://matplotlib.org/stable/api/figure_api.html#matplotlib.figure.Figure.add_subplot)
4. [python 画二维、三维点之间的线段实现方法](https://www.jb51.net/article/164754.htm)



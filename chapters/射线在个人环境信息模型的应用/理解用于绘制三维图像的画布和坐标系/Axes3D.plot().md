# 感受matplotlib的Axes3D.plot()

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

### 渲染出多个点连成的直线

```python
import matplotlib.pyplot as plt
import numpy as np

ax = plt.figure().add_subplot(111, projection='3d')
ax.scatter([0,10,50], [0,10,50], [0,10, 50])
ax.plot([0,10,50], [0,10,50], [0,10, 50])
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



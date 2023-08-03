# Code：绘出函数的图像

## 开始做实体实验

![](/images/使用最优化算法优化布局/使用目标函数求最小距离/到两个点的距离之和最短的点坐标/计算出特定点到两个已知点距离之和/1a1.png)

### 在线调试环境1

- 单击右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

### 在线调试环境2
- 单击右方的[Python Online Compiler](https://trinket.io/python3/a5bd54189b)，稍后在浏览器里会显示python的运行环境。
- 把下面的这段python代码拷贝到这个页面左侧的空白栏中， 然后单击上方的按键“Run”。


```python
import matplotlib.pyplot as plt
from matplotlib import cm
import numpy as np

fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

X = np.arange(0, 20, 0.25)				# the 2D coordinates of desired point C: x
Y = np.arange(0, 15, 0.25)				# the 2D coordinates of desired point C: y
X, Y = np.meshgrid(X, Y)				# the 2D coordinates of desired point C: [x,y]

d1 = np.sqrt((X-2)**2 + (Y-3)**2)		# the 2D coordinates of existing point A: [2,3]
d2 = np.sqrt((X-14)**2 + (Y-12)**2)		# the 2D coordinates of existing point B: [14,12]

Z = d1 + d2

ax.plot_surface(X, Y, Z, rstride=1, cstride=1, cmap=cm.coolwarm, linewidth=0, antialiased=False)

plt.show()
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.plot**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html)


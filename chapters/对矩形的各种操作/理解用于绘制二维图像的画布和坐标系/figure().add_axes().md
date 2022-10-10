# 感受matplotlib的figure().add_axes()

## 本质意义：在创建的矩形绘图区域内加上1个子矩形绘图区域（1个Axes对象）。

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

```python
import numpy as np
import matplotlib.pyplot as plt

#新建figure
fig = plt.figure()
#定义数据
x = [1, 2, 3, 4, 5, 6, 7]
y = [1, 7, 15, 24, 30, 50, 55]

#新建区域ax1
#figure的百分比,从figure 10%的位置开始绘制, 宽高是figure的80%
left, bottom, width, height = 0.1, 0.1, 0.8, 0.8
#获得绘制的句柄
ax1 = fig.add_axes([left, bottom, width, height])
ax1.plot(x, y,'r')
ax1.set_title('area1')
#新增区域ax2,嵌套在ax1内，看一看图中图是什么样，这就是与subplot的区别
left, bottom, width, height = 0.2, 0.6, 0.25, 0.25
#获得绘制的句柄
ax2 = fig.add_axes([left, bottom, width, height])
ax2.plot(x,y,'b')
ax2.set_title('area2')
plt.show()
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.figure**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.figure.html)
	- [**matplotlib.axes**](https://matplotlib.org/stable/api/axes_api.html#the-axes-class)
	- [**add_axes**](https://matplotlib.org/stable/api/figure_api.html#)
	- [**add_axes()——python绘图**](https://blog.csdn.net/qq_41011336/article/details/83017101)

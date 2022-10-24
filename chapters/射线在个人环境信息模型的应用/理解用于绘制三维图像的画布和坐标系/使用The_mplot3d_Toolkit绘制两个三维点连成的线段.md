# 使用The mplot3d Toolkit绘制两个三维点连成的线段

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

```python
from mpl_toolkits.mplot3d import axes3d
import matplotlib.pyplot as plt
 
# 打开画图窗口1，在三维空间中绘图
fig = plt.figure(1)
ax = fig.gca(projection='3d')
 
# 给出点（0，0，0）和（100，200，300）
x = [0, 100]
y = [0, 200]
z = [0, 300]
 
# 将数组中的前两个点进行连线
figure = ax.plot(x, y, z, c='r')
plt.show()
```

## 参考文献及资料

1. [The mplot3d Toolkit from matplotlib.org](https://matplotlib.org/stable/tutorials/toolkits/mplot3d.html)
2. [python 画二维、三维点之间的线段实现方法](https://www.jb51.net/article/164754.htm)



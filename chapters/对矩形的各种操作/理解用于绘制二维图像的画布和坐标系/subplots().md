# 感受matplotlib的subplots()

## 本质意义：

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

### fig, ax = plt.subplots()
### fig, axs = plt.subplots(2, 2)
 
```python
import matplotlib.pyplot as plt

# using the variable ax for single a Axes
fig, ax = plt.subplots()

# using the variable axs for multiple Axes
fig, axs = plt.subplots(2, 2)

# using tuple unpacking for multiple Axes
fig, (ax1, ax2) = plt.subplots(1, 2)
fig, ((ax1, ax2), (ax3, ax4)) = plt.subplots(2, 2)
```

```python
import matplotlib.pyplot as plt

def example_plot(ax):
    ax.plot([10, 1])
    ax.set_xlabel('x-label')
    ax.set_ylabel('y-label')
    ax.set_title('Title', fontsize=next(fontsizes))
    
fig, ax = plt.subplots()

example_plot(ax)
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.subplots**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.subplots.html)

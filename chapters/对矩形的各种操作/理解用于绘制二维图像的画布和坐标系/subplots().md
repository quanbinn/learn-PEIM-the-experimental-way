# 感受matplotlib的subplots()

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

```python
import matplotlib.pyplot as plt

f1=plt.figure()
plt.title("figure1")

f2=plt.figure()
plt.title("figure2")

f3=plt.figure(5)
plt.title("figure5")

f6=plt.figure(6,(4,4),100)
plt.title("figure6")

f7=plt.figure(7,None,None,'#FFD700','#FF0000')
plt.title("figure7")
plt.show()
```

```python
from matplotlib import pyplot as plt
import numpy as np

x = np.linspace(-np.pi, np.pi, 256)
y1 = np.sin(x)
y2 = np.cos(x)
 
fig1 = plt.figure(num='first')
fig1.suptitle('first figure')
plt.plot(x, y1)
 
fig2 = plt.figure(num='second')
fig2.suptitle('second figure')
plt.plot(x, y2)
 
plt.figure(num=1)  #plt.figure(num='first')
plt.plot(x, y2)
plt.show()
```

### fig, ax = plt.subplots()
### fig, axs = plt.subplots(2, 2)
 
```python
# using the variable ax for single a Axes
fig, ax = plt.subplots()

# using the variable axs for multiple Axes
fig, axs = plt.subplots(2, 2)

# using tuple unpacking for multiple Axes
fig, (ax1, ax2) = plt.subplots(1, 2)
fig, ((ax1, ax2), (ax3, ax4)) = plt.subplots(2, 2)
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.subplots**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.subplots.html)

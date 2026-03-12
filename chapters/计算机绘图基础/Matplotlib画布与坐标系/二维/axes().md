# 感受matplotlib的axes()

## 本质意义：创建一个包含了大多数图形元素：轴、记号、Line2D、文本、多边形等，并设置了坐标系的对象。 

```python
import matplotlib.pyplot as plt

# Creating a new full window Axes
plt.axes()

# Creating a new Axes with specified dimensions and a grey background
plt.axes((left, bottom, width, height), facecolor='grey')
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.axes**](https://matplotlib.org/stable/api/axes_api.html#the-axes-class)
	- [**matplotlib.pyplot.axes**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.axes.html)

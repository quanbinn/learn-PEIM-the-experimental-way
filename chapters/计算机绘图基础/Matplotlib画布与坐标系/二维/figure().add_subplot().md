# 感受matplotlib的figure().add_subplot()

## 本质意义：在当前的母矩形绘图区域中创建1个或多个子矩形绘图区域（其中包含1个或多个Axes对象）。

```python
import matplotlib.pyplot as plt

fig = plt.figure()

fig.add_subplot(231)
ax1 = fig.add_subplot(2, 3, 1)  # equivalent but more general

fig.add_subplot(232, frameon=False)  # subplot with no frame
fig.add_subplot(233, projection='polar')  # polar subplot
fig.add_subplot(234, sharex=ax1)  # subplot sharing x-axis with ax1
fig.add_subplot(235, facecolor="red")  # red subplot

ax1.remove()  # delete ax1 from the figure
fig.add_subplot(ax1)  # add ax1 back to the figure
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.figure**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.figure.html)
	- [**add_subplot()**](https://matplotlib.org/stable/api/figure_api.html#matplotlib.figure.Figure.add_subplot)

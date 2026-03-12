# 感受matplotlib的subplot()

## 本质意义： 在当前的母绘图区域中创建1个子矩形绘图区域（其中包含1个Axes对象）。

```python
import matplotlib.pyplot as plt
# plot a line, implicitly creating a subplot(111)
plt.plot([1, 2, 3])
# now create a subplot which represents the top plot of a grid
# with 2 rows and 1 column. Since this subplot will overlap the
# first, the plot (and its axes) previously created, will be removed
plt.subplot(211)
```

```python
import matplotlib.pyplot as plt

plt.subplot(221)

# equivalent but more general
ax1 = plt.subplot(2, 2, 1)

# add a subplot with no frame
ax2 = plt.subplot(222, frameon=False)

# add a polar subplot
plt.subplot(223, projection='polar')

# add a red subplot that shares the x-axis with ax1
plt.subplot(224, sharex=ax1, facecolor='red')

# delete ax2 from the figure
plt.delaxes(ax2)

# add ax2 to the figure again
plt.subplot(ax2)

# make the first axes "current" again
plt.subplot(221)
```

```python
import matplotlib.pyplot as plt

plt.subplot(2, 1, 1)
plt.plot(x1, y1, 'o-')
plt.title('A tale of 2 subplots')
plt.ylabel('Damped oscillation')

plt.subplot(2, 1, 2)
plt.plot(x2, y2, '.-')
plt.xlabel('time (s)')
plt.ylabel('Undamped')

plt.show()
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.subplot**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.subplot.html)
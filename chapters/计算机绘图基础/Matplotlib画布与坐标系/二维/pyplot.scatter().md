# 感受matplotlib的pyplot.scatter()

## 本质意义：在内存中准备好的点图形信息(1个或多个)，准备下一步把这些点图形信息显示在屏幕上。

### 在二维平面渲染出1个点

```python
import numpy as np
import matplotlib.pyplot as plt

plt.scatter(0,0)					# [x1,x2,x3,...],[y1,y2,y3,...]
plt.show()
```

### 在二维平面渲染出两个或多个点

```python
import numpy as np
import matplotlib.pyplot as plt

plt.scatter([0,5],[0,5])			# [x1,x2,x3,...],[y1,y2,y3,...]
# plt.scatter([0,5,10],[0,5,10])	
# plt.scatter([0,5,10,20],[0,5,10,5])

plt.show()
```

```python
import numpy as np
import matplotlib.pyplot as plt

# Fixing random state for reproducibility
np.random.seed(19680801)

N = 50
x = np.random.rand(N)
y = np.random.rand(N)
colors = np.random.rand(N)
area = (30 * np.random.rand(N))**2  # 0 to 15 point radii

plt.scatter(x, y, s=area, c=colors, alpha=0.5)
plt.show()
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.scatter**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.scatter.html)


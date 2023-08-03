# 在x轴方向上移动找到符合最小距离的坐标数值

## 开始做实体实验

![](/images/使用最优化算法优化布局/使用目标函数求最小距离/到两个点的距离之和最短的点坐标/在x轴方向上移动找到符合最小距离的坐标数值/1a1.jpg)

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

#### 在x轴方向，随着x依次变化一个固定的常数值，打印出每一次变化后的点距两个给定点的距离之和。

```python
import random
import math

x = float(input('input any number between 0 and 20: \n'))	  # x = random.uniform(0,20)
y = float(input('input any number between 0 and 15: \n'))	  # y = random.uniform(0,15)

p1 = [2,3]		# the 2D coordinates of existing point A
p2 = [14,12]	# the 2D coordinates of existing point B
p3 = [x,y]		# the 2D coordinates of desired point C

def sum_of_distances(p1,p2,p3):
	sum = math.sqrt((p3[0]-p1[0])**2 + (p3[1]-p1[1])**2) + math.sqrt((p3[0]-p2[0])**2 + (p3[1]-p2[1])**2)
	return sum

init_distances = sum_of_distances(p1, p2, p3)
print(init_distances)

for i in range(1,20):
    p3[0] = p3[0] - 1
    if sum_of_distances(p1, p2, p3) < init_distances:
        print(p3)
        print(sum_of_distances(p1, p2, p3))
```

#### 在x轴方向，随着x依次变化一个固定的常数值，如果在变化后的点距两个给定点的距离之和小于上一个点距两个给定点的距离之和，就打印出这个点坐标及其距离，反之，就不打印出来任何内容。

```python
import random
import math

x = float(input('input any number between 0 and 20: \n'))	  # x = random.uniform(0,20)
y = float(input('input any number between 0 and 15: \n'))	  # y = random.uniform(0,15)

p1 = [2,3]		# the 2D coordinates of existing point A
p2 = [14,12]	# the 2D coordinates of existing point B
p3 = [x,y]		# the 2D coordinates of desired point C

def sum_of_distances(p1,p2,p3):
	sum = math.sqrt((p3[0]-p1[0])**2 + (p3[1]-p1[1])**2) + math.sqrt((p3[0]-p2[0])**2 + (p3[1]-p2[1])**2)
	return sum

init_distances = sum_of_distances(p1, p2, p3)
print(init_distances)

for i in range(1,20):
	previous_distances = sum_of_distances(p1, p2, p3)
	p3[0] = p3[0] - 1
	moved_distances = sum_of_distances(p1, p2, p3)
	if moved_distances < previous_distances:
		print('At point ',p3,', the total distances is ',moved_distances)
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.plot**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html)


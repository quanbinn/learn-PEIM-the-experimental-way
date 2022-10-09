# 感受matplotlib的figure()

## 本质意义：创建一个空白的矩形图框，随后用plot()在内存中准备好所有的图形信息，最后调用show()把这些图形信息显示在屏幕上。

## 开始做实体实验

### 在线调试环境

- 单机右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

### 创建一个矩形区域

```python
import matplotlib.pyplot as plt

plt.figure(figsize=(20,6), facecolor='yellow')
plt.axis('equal')

plt.xlabel("X")
plt.ylabel("Y")
plt.title("Render a box in a rectanglar area")

class Rectangle_center:
    def __init__(self, xOfCenter, yOfCenter, width, height):
        self.xOfCenter = xOfCenter
        self.yOfCenter = yOfCenter
        self.x1 = xOfCenter - width / 2
        self.y1 = yOfCenter - height / 2
        self.x2 = xOfCenter + width / 2
        self.y2 = yOfCenter + height / 2
        self.width = width
        self.height = height        
    
    def getxofCenter(self): return self.getxofCenter
    def getyOfCenter(self): return self.yOfCenter
    def getx1(self): return self.x1
    def gety1(self): return self.y1
    def getx2(self): return self.x2
    def gety2(self): return self.y2
    def getWidth(self): return self.width
    def getHeight(self): return self.height

    def area(self):
        area = self.width * self.height
        return area

    def centralCoordinates(self):
        centralCoordinates = [self.xOfCenter, self.yOfCenter]
        return centralCoordinates
        
    def render(self):
        p1 = [self.x1, self.y1]
        p2 = [self.x2, self.y1] 
        p3 = [self.x2, self.y2]
        p4 = [self.x1, self.y2]

        plt.plot([p1[0], p2[0]],[p1[1], p2[1]],color="green")
        plt.plot([p2[0], p3[0]],[p2[1], p3[1]],color="green")
        plt.plot([p3[0], p4[0]],[p3[1], p4[1]],color="green")
        plt.plot([p4[0], p1[0]],[p4[1], p1[1]],color="green")   
        
rect1 = Rectangle_center(10,8,12,8)
rect1.render()

plt.show()
```

### 创建两个矩形区域

```python
import matplotlib.pyplot as plt

plt.figure(figsize=(20,6), facecolor='yellow')
plt.axis('equal')

plt.xlabel("X")
plt.ylabel("Y")
plt.title("Render a box in a rectanglar area of figure1")

class Rectangle_center:
    def __init__(self, xOfCenter, yOfCenter, width, height):
        self.xOfCenter = xOfCenter
        self.yOfCenter = yOfCenter
        self.x1 = xOfCenter - width / 2
        self.y1 = yOfCenter - height / 2
        self.x2 = xOfCenter + width / 2
        self.y2 = yOfCenter + height / 2
        self.width = width
        self.height = height        
    
    def getxofCenter(self): return self.getxofCenter
    def getyOfCenter(self): return self.yOfCenter
    def getx1(self): return self.x1
    def gety1(self): return self.y1
    def getx2(self): return self.x2
    def gety2(self): return self.y2
    def getWidth(self): return self.width
    def getHeight(self): return self.height

    def area(self):
        area = self.width * self.height
        return area

    def centralCoordinates(self):
        centralCoordinates = [self.xOfCenter, self.yOfCenter]
        return centralCoordinates
        
    def render(self):
        p1 = [self.x1, self.y1]
        p2 = [self.x2, self.y1] 
        p3 = [self.x2, self.y2]
        p4 = [self.x1, self.y2]

        plt.plot([p1[0], p2[0]],[p1[1], p2[1]],color="green")
        plt.plot([p2[0], p3[0]],[p2[1], p3[1]],color="green")
        plt.plot([p3[0], p4[0]],[p3[1], p4[1]],color="green")
        plt.plot([p4[0], p1[0]],[p4[1], p1[1]],color="green")   
        
rect1 = Rectangle_center(10,8,12,8)
rect1.render()

plt.figure(figsize=(20,6), facecolor='yellow')
plt.axis('equal')

plt.xlabel("X")
plt.ylabel("Y")
plt.title("Render a box in a rectanglar area of figure2")
        
rect2 = Rectangle_center(20,30,16,16)
rect2.render()

plt.show()
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.figure**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.figure.html)

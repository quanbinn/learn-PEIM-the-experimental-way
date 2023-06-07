# 两个矩形在X轴方向上的距离

## 开始做实体实验

![](/images/对矩形的各种操作/对两个或多个距形的运算/两个矩形在X轴方向上的距离/1a1.jpg)

### 在线调试环境

- 单击右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

```python
import matplotlib.pyplot as plt
plt.axis('equal')

class Rectangle_center:
    def __init__(self, xOfCenter, yOfCenter, length, width):
        self.xOfCenter = xOfCenter
        self.yOfCenter = yOfCenter
        self.x1 = xOfCenter - length / 2
        self.y1 = yOfCenter - width / 2
        self.x2 = xOfCenter + length / 2
        self.y2 = yOfCenter + width / 2
        self.length = length
        self.width = width        
    
    def getxofCenter(self): return self.getxofCenter
    def getyOfCenter(self): return self.yOfCenter
    def getx1(self): return self.x1
    def gety1(self): return self.y1
    def getx2(self): return self.x2
    def gety2(self): return self.y2
    def getlength(self): return self.length
    def getwidth(self): return self.width

    def area(self):
        area = self.length * self.width
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

def distance_of_edges_in_xaxis(rect1, rect2):
    x1 = rect1.centralCoordinates()[0]
    x2 = rect2.centralCoordinates()[0]
    dist_of_centralPoints_in_xaxis = abs(x2-x1)
    distance = dist_of_centralPoints_in_xaxis - (rect1.getlength()/2 + rect2.getlength()/2)
    return distance    
        
rect1 = Rectangle_center(0,0,10,10)
rect1.render()

rect2 = Rectangle_center(3,15,5,5)
rect2.render()   

print(distance_of_edges_in_xaxis(rect1, rect2))
```
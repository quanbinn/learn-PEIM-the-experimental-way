# 两个长方体在Y轴方向上的距离

## 开始做实体实验

![](/images![](/images/对长方体的各种操作/对两个或多个长方体的运算/两个长方体在Y轴方向上的距离/1a1.jpg)

### 在线调试环境

- 单击右方的[Jupyter Notebook](https://mybinder.org/v2/gh/ipython/ipython-in-depth/master?filepath=binder/Index.ipynb)，稍后在浏览器里会显示Jupyter Notebook的运行环境。
- 在File的第一个下拉菜单“New Notebook” 的右侧箭头处选择“Python 3”，然后会显示一个新的页面
- 把下面的这段python代码拷贝到这个页面“In [ ]:”右侧的空白栏中， 然后单击上方的按键“运行”。

```python
import matplotlib.pyplot as plt
plt.axis('equal')

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

def distance_of_edges_in_yaxis(rect1, rect2):
    y1 = rect1.centralCoordinates()[1]
    y2 = rect2.centralCoordinates()[1]
    dist_of_centralPoints_in_yaxis = abs(y2-y1)
    distance = dist_of_centralPoints_in_yaxis - (rect1.getHeight()/2 + rect2.getHeight()/2)
    return distance    
        
rect1 = Rectangle_center(0,0,10,10)
rect1.render()

rect2 = Rectangle_center(3,3,5,5)
rect2.render()   

print(distance_of_edges_in_yaxis(rect1, rect2))
```
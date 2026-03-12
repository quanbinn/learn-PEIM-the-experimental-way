# 感受matplotlib的pyplot.plot()

## 本质意义：在内存中准备好所有的线图形信息(1条或多条)，准备下一步把这些线图形信息显示在屏幕上。

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

        plt.plot([p1[0], p2[0]],[p1[1], p2[1]],color="green")			# [x1,x2,x3,...],[y1,y2,y3,...]
        plt.plot([p2[0], p3[0]],[p2[1], p3[1]],color="green")			# [x1,x2,x3,...],[y1,y2,y3,...]
        plt.plot([p3[0], p4[0]],[p3[1], p4[1]],color="green")			# [x1,x2,x3,...],[y1,y2,y3,...]
        plt.plot([p4[0], p1[0]],[p4[1], p1[1]],color="green")   		# [x1,x2,x3,...],[y1,y2,y3,...]	
        
rect1 = Rectangle_center(10,8,12,8)
rect1.render()

plt.show()
```

## 参考文献及资料

1. 维基百科
	- [Matplotlib](https://en.wikipedia.org/wiki/Matplotlib) | [Matplotlib库](https://en.wikipedia.org/wiki/Matplotlib)
	- [John D. Hunter](https://en.wikipedia.org/wiki/John_D._Hunter#Matplotlib)
	- [**matplotlib.pyplot.plot**](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html)


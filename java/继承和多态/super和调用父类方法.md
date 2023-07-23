super指代父类，可以用于调用父类中的普通方法和构造方法

### 调用父类的构造方法

```
super()或者super(arguments)
```
该语句必须出现在子类构造方法的第一行，这是显示调用父类构造方法的唯一形式
eg.
```
public Circle(double radius,String color,boolean filled) {
    super(color,filled);
    this.radius = radius;
}
```
### 构造方法链
在构造一个类的实例时，将会调用沿着继承链的所有父类的构造方法
## 调用父类的普通方法
super.method(arguments)

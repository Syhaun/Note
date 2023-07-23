一个对象的引用可以类型转换为对另外一个对象的引用，这称为对象转换

---
隐式转换

子类的实例引用给父类引用变量
eg：
```
Obiect o = new Student();
```

显示转换

实际为子类类型的父类实例引用给子类引用变量

```
Student b = (Student)o;
```
###instanceof
在尝试转化之前确保该对象是另外一个对象的实例
`a instanceof b`判断a是否b的实例 
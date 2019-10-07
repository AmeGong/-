## const形参和实参
当形参是const时，当用实参初始化形参时会忽略掉顶层const，换句话说，当形参有顶层const时，传给他变量对象或者非常量对象都是可以的。
## 引用类型的形参
### 引用类型为形参时，最好使用常量引用
使用引用而非常量引用会极大地限制函数所能接受地实参类型，有时回引起错误。
如下：
```
size_type find_char(string &s,char c,size_type &occurs);
这样地定义只能作用于string对象。类时下面地调用会发生编译错误。
find_char("Hello World",'o',ctr); //因为非const引用不能接受字面值常量
```

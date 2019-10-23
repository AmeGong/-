# 可调用对象
对于一个表达式，如果可以对其使用调用运算符，则称它为可调用的

可以向算法传递任何类别的可调用对象。
可调用对象有四种：函数，函数指针，lambda表达式，重载了函数调用运算符的类

lambda表达式表示一个可调用的代码单元，可以将其理解为一个未命名的内联函数。
一个lambda表达式具有如下形式
```
[capture list](parameter list)->return type {function body}
```
capture list（捕获列表）是一个lambda所在函数中定义的局部变量列表（通常为空）
return type、parameter list和function body和任何普通函数一样
lambda必须使用尾指返回来指定返回类型:->return type

我们可以忽略参数列表和返回类型，但必须永远包含捕获列表和函数体
```
auto f = [] {return 42};
```

## 向lambda传递参数
lambda不能使用默认参数
下面是一个带参数lambda的例子：
```
[](const string &a,const string &b) // 空捕获列表表明此lambda不使用它所在函数的任何局部变量
  {return a.size()<b.size();}
```

## 使用捕获列表
```
[sz](const string &a) //此lambda会捕获局部变量中的sz变量
  {return a.size()>=sz;}
```

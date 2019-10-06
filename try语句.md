## 异常处理
```
try{
  需要检测异常的语句
  if(出现异常){
    throw runtime_error("描述")  // 出现异常后，throw语句抛出一个异常类型，这里时runtime_error，后面的字符串用来初始化这个类
    }
}catch(runtime_error err){  //catch语句用来捕捉异常，然后进行处理异常。这里定义了一个异常err变量
  cout<<err.what()     //what()时异常类的一个方法，返回初始化的字符串
  
  }

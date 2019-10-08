命令行选项通过两个形参传递给main函数
```
int main(int argc,char *argv[]){...}
```
第二个形参argv是一个数组，他的元素指向c风格字符串的指针；第一个形参表示数组中字符串的数量。因为第二个形参是数组，所以main函数也可以定义成：
```
int main(int argc,char **argv){...}  //argv指向char *
```
当实参传递给mian函数后，argv的第一个元素指向程序的名字或者一个空字符串。

假定main函数位于可执行文件prog之内，我们可以向程序传递下面的选项：
```
prog -d -o ofile data0 //prog是可执行文件名，启动程序
```



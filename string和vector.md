string用来定义字符串。

string的初始化的方法：
string a(10,'s');//a为10个s字符组成的字符串.
string a("this is a string.") //直接初始化
string a = "this is a string." //赋值初始化

cin在读取时，遇到空格就停止，并且回自动忽略开头的空格
getline(cin,a) //getline的第一个参数是一个输入流，第二个时一个string对象，读并将其赋给a字符串，不包含换行符
string定义的字符串也可以用引索对每个元素进行访问

范围for：
for(auto letter:a){} //letter表示a字符串中的基础元素，并且进行迭代，与python相似

使用范围for修改字符串
for(auto &letter:a){letter = touppper(letter)}  //使用引用对a中的基础元素进行修改，toupper：将字符变为大写

a.size() //方法size（）返回一个size_type的类型，非负整数

vector与string类似
vector的push_back方法类似与python的append
与内置数组不同，vector数组可以直接比较数组，v1==v2可以判断vector是否相等。

## 构建string的其他方法
```
string s(cp,n) //s是cp指向的数组中前n个字符的拷贝
string s(s2,pos2) // s是string s2从下表pos2开始的字符的拷贝。
string s(s2,pos2,lens) //s是string s2从下标pos2开始len2个字符的拷贝
```
### substr操作
不带参数的substr默认返回字符串本身
```
string s2 = s.substr(pos1,pos2);
string s3 = s.substr(len) //创建s的前len个子字符串
```
### string支持通过下标进行增删
```
s.insert(pos,args) //在pos之前插入args指定的字符。pos可以是一个下标，也可以是一个迭代器。
                    下标：返回一个指向s的应用
                    迭代器：返回指向第一个插入字符的迭代器
s.erase(pos,len) //删除从pos开始的len个字符，若len省略则全部删除。
                   返回一个指向s的引用
s.append(args) //与push_back相似
s.replace(range,args) //删除s中range内的字符，替换尾args指定的字符。
                      range可以是一个下标和一个长度，或者是一对指向s的迭代器
                      返回的是指向s的应用
```                      
                 
### args的形式
```
str                 字符串str
b,e                 迭代器b和e指定的范围内的字符（b,e不能是指向e的迭代器）
str,pos,len         str中从pos开始最多len个字
cp,len              从cp指向的字符数组的前len个字符
cp                  cp指向的以空字符结尾的字符数组
n,c                 n个字符c
初始化列表           花括号包围的，以逗号分隔的字符列表
```

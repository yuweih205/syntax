对象指针：

访问对象一般是通过对象去访问对象的成员 公有的接口

通过对象指针去访问对象成员 

a->b = *(a).b 对象名.成员名

this指向当前对象自己的指针

前向引用声明 

动态申请内存 程序执行期间

静态申请内存 在编译期间



*ptr ptr是指针变量 存放的是数据的地址 *去访问这个地址



智能指针

unique_ptr 指向的地址只能由它指向 这是怎么确保实现的？可以用move

shared_ptr 

weak_ptr 可以复制该指针的地址



浅层复制  只复制指针的内容 而不动指针指向的内容 所以会出现重复释放

深层复制 不复制地址复制内容

移动构造 临时变量的地址转移给一个变量对象



c风格字符串 用字符数组存储字符串 char 末尾记得‘\0’

c++ 用string类 字符串常量 



继承和派生

多继承

析构函数不能被继承 构造函数可以

公有继承：可以访问public和protected成员函数 public对象 但不能从外部访问protected成员函数

私有继承：都只能在继承类间访问

保护继承：公有和保护成员函数都只能在继承类间访问和继承类的继承类

友员：可以访问私有和保护



用using语句继承基类构造函数 只能初始化从基类继承的成员

using B::B

不继承：派生类的构造函数还需要给基类构造函数传递参数 先继承基类传参  多继承的 初始化列表需要列出所有基类和初始化参数 调用顺序按继承时声明的顺序 

<br>
类的静态方法不需要实例化类 可以直接调用


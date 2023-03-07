# 教程 
* [C++教程](https://www.runoob.com/cplusplus/cpp-tutorial.html)
* [STL库](http://c.biancheng.net/stl/stl_basic/)
* [STL标准手册](http://www.cplusplus.com/reference/stl/)
* [C++常用头文件](https://blog.csdn.net/u012707739/article/details/76359238)

# 基础语法
## static和extern
* static 存储类指示编译器在程序的生命周期内保持局部变量的存在，而不需要在每次它进入和离开作用域时进行创建和销毁。因此，使用 static 修饰局部变量可以在函数调用之间保持局部变量的值。
* static 修饰符也可以应用于全局变量。当 static 修饰全局变量时，会使变量的作用域限制在声明它的文件内。在 C++ 中，当 static 用在类数据成员上时，会导致仅有一个该成员的副本被类的所有对象共享。
* extern 修饰符通常用于当有两个或多个文件共享相同的全局变量或函数的时候。
* static声明时可同时定义，extern声明和定义要分开。
## [生成随机数](https://blog.csdn.net/YF_Li123/article/details/75220786)
## 字符判断
* ASCII码：0为48， A为65，a为97
* isalpha()用来判断一个字符是否为字母，如果是字母则返回非零，否则返回零
* isalnum()用来判断一个字符是否为数字或者字母，也就是说判断一个字符是否属于a~z||A~Z||0~9，如果是数字或字母则返回非零，否则返回零
* islower()用来判断一个字符是否为小写字母，也就是是否属于a~z，如果是小写字母则返回非零，否则返回零
* isupper()和islower相反，用来判断一个字符是否为大写字母，如果是大写字母则返回非零，否则返回零
* isdigit()用来判断一个字符是否为数字
* tolower()把字符转换成小写字母,非字母字符不做出处理；toupper()将小写英文字母转换为大写英文字母
## 指针和引用
* [引用和指针区别](https://www.cnblogs.com/dolphin0520/archive/2011/04/03/2004869.html)
* 引用不能为空且只能初始化一次，更安全；指针更灵活。
* *&做参数可以改变指针本身，*做参数只能改变指针指向的内容（指针本身是传值参数）,[参见](https://blog.csdn.net/u010037542/article/details/105980430)
## [new和delete](https://www.cnblogs.com/hazir/p/new_and_delete.html)
## 数组
* [多维数组](https://www.runoob.com/cplusplus/cpp-dynamic-memory.html)
* [声明变长数组](https://blog.csdn.net/fanyun_01/article/details/77430682)
## [栈和堆的区别](https://www.cnblogs.com/lxmhhy/p/3559212.html)
## 输入
* [cin输入](https://www.runoob.com/note/50168)
* 连续多行输入（while(cin)）
  * https://cloud.tencent.com/developer/article/1036486
  * https://www.cnblogs.com/libbin/p/CinMultiLines.html
* 成对输入使用tuple，pair或定义struct
## void*用法
* 可以指向任意类型的指针，https://blog.csdn.net/JIEJINQUANIL/article/details/50001335
## [size_t含义](https://www.cxyzjd.com/article/yz930618/84785970)
## [前置++和后置++区别](https://blog.csdn.net/randyjiawenjie/article/details/6747720)
## [有符号数和无符号数转换](https://segmentfault.com/a/1190000021751193)
* 有符号数和无符号数，当无符号类型的所有值都能存在该带符号类型中，则无符号类型的运算对象将转换为带符号类型；如果不能，则带符号类型对象转换成无符号类型
## 类
* [类的继承和访问权限](https://blog.csdn.net/qq_43827595/article/details/104422068)
* [虚基类](https://blog.csdn.net/chlele0105/article/details/22654869)
* [虚函数](https://zhuanlan.zhihu.com/p/54145222)
## [模板](https://www.runoob.com/cplusplus/cpp-templates.html)

# STL使用
## [for(auto i : v)遍历容器元素](https://blog.csdn.net/qq_28087491/article/details/108171017)
## [string类](http://c.biancheng.net/view/400.html)
* 其中substr和erase的第二个参数为要截取或删除的子串的长度，不是索引
* string有front()、back()、push_back()、pop_back()操作，无push_front()、pop_front()操作；string的插入和删除使用[insert和erase函数](https://blog.csdn.net/pipixiu/article/details/52825728)
* string的插入和删除：参数均需要指定迭代器位置，不能只有要插入或删除的值；s.insert(p,t)->p迭代器，t值，插入在p之前，返回新元素的迭代器；s.erase(p)->删除迭代器p指定的元素，返回其后的迭代器
* set的插入和删除：insert不需要指定位置，参数直接为要插入的值；erase可以根据迭代器位置删除，也可以删除指定值（因为底层原理上set自己会排序、查找）
* [string转int](https://blog.csdn.net/caroline_wendy/article/details/29390573): int out = atoi(result.c_str())或int out = stoi(result)
* int转string使用to_string()函数
* string分割
  * https://www.jianshu.com/p/5876a9f49413
  * https://blog.csdn.net/Mary19920410/article/details/77372828
* [resize函数](https://blog.csdn.net/FreeCloud_InSky/article/details/47058597)，可以截断字符串，str.resize(数字)
## [find函数用法](https://blog.csdn.net/u014386899/article/details/108776009)
## [sort函数](https://www.cnblogs.com/alvinzh/p/6784862.html)
## [tuple用法](https://www.cnblogs.com/pandamohist/p/13630613.html)
## [容器在内存中的存储](https://blog.csdn.net/qq_28584889/article/details/117035106)
## [multimap用法](https://blog.csdn.net/believefym/article/details/1627874)
* 因存在重复key元素，所以不能通过下标操作符，即[key]来访问元素
* 访问单个元素可通过find函数（返回第一个与key匹配的值），或使用equal_range()、lower_bound()和 upper_bound()函数进行范围查找
## map排序
* 按key排序：默认就是按key升序排序，直接从begin到end打印即为按key升序排列结果，按key降序排列增加第三个参数greater<类型>，其他排序规则可自定义
* 按value排序:可以将key和value互换到新map，新map中为按原value排序结果，或将map中值存为pair类型，存入vector中，对vector自定义排序规则，使用sort函数排序（sort函数只能对线性的vector，list和deque排序）
* https://blog.csdn.net/iicy266/article/details/11906189
* https://www.delftstack.com/zh/howto/cpp/sort-map-by-value-in-cpp/
```
typedef pair<string, int> PAIR;
 
bool cmp_by_value(const PAIR& lhs, const PAIR& rhs) {
  return lhs.second < rhs.second;
}
 
struct CmpByValue {
  bool operator()(const PAIR& lhs, const PAIR& rhs) {
    return lhs.second < rhs.second;
  }
};
```
## 多主键排序
* 通过自定义sort的compare函数，对内容为struct的vector进行排序
* https://blog.csdn.net/pathuang68/article/details/7526381
* https://blog.csdn.net/qq_44654498/article/details/104502291
## 优先队列
* 底层数据结构为堆，默认大顶堆（less）（与一般自定义排序大于小于号方向相反，因为队首指向尾部，队尾指向头部）
* 三个参数，基本数据类型可只写第一个，涉及自定义排序方式时三个参数都要有
* https://blog.csdn.net/weixin_36888577/article/details/79937886
* https://blog.csdn.net/AAMahone/article/details/82787184
* priority_queue用top访问元素，queue用front和back访问元素
## [sort和优先队列自定义排序算法对比](https://blog.csdn.net/wwrzzu/article/details/106177818)
## vector去重
* [用set为vector去重](https://blog.csdn.net/cuglxw/article/details/78616418)
  * 先用vector初始化set（set<int> st(vec.begin(), vec.end())），然后用vec.assign重置vec（会替换原vec）
## 容器初始化
* map和vector未初始化时，若为基本数据类型，会默认初始化为零值，若为自定义类型，会自动初始化为定义好的默认值

# c++ 11&面向对象
## [右值引用](https://zhuanlan.zhihu.com/p/335994370，https://www.cnblogs.com/qicosmos/p/4283455.html)
## [const和constexpr](http://c.biancheng.net/view/7807.html)
## 函数指针和函数对象
* https://blog.csdn.net/duan19920101/article/details/50939326，https://www.runoob.com/w3cnote/cpp-func-pointer.html
* https://blog.csdn.net/try_again_later/article/details/81415110
## [lambda表达式](https://www.cnblogs.com/DswCnblog/p/5629165.html，https://www.cnblogs.com/gqtcgq/p/9939651.html)
* 按值捕获创建lambda时取值，默认为const参数，函数体内不可修改，加入mutable后函数体内可修改，但不会影响外部
* 按引用捕获调用时取值，是否可以修改依赖于此引用指向的是一个const类型还是一个非const类型，函数体内修改会影响外部
## [作用域和命名空间](https://www.cnblogs.com/hammerc/p/4024800.html)
## 智能指针
* https://www.cnblogs.com/lanxuezaipiao/p/4132096.html
* https://vivym.gitbooks.io/effective-modern-cpp-zh/content/SmartPointers/21-Prefer-std-make_unique-and-std-make_shared-to-direct-use-of-new.html

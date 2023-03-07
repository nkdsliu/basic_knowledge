# python基础知识
## [python教程](https://docs.python.org/zh-cn/3/tutorial/index.html)
## [python语法参考手册](https://docs.python.org/zh-cn/3/reference/index.html#reference-index)
## [python多行输入](https://blog.csdn.net/heshiip/article/details/86511406)
## [python可变对象和不可变对象](https://zhuanlan.zhihu.com/p/34395671)
可变对象改变时是创建了新的对象，改变了对象的引用，指向了新的地址；不可变对象改变时是直接在原地址修改（函数传参是传引用，函数内可变对象改变会影响全局，不可变对象改变不会影响全局）
## 与或非区分
* c++与或非&&，||，！
* python与或非and， or，not
* dataframe与或非&，|，~
## [Python遍历文件夹下所有文件及目录](https://blog.csdn.net/mighty13/article/details/77995857)
## [python多线程join用法](https://blog.csdn.net/whatday/article/details/124308427)
## [python下划线作用](https://zhuanlan.zhihu.com/p/36173202)
## [pdf逐页转图片](https://www.codeleading.com/article/43065377472/)
## [lambda, map, apply用法](https://zhuanlan.zhihu.com/p/42756654)
* [lambda for循环](https://www.cnblogs.com/liuq/p/6073855.html),[lambda表达式在执行的时候才会去寻找变量](https://www.cxyzjd.com/article/qq_43218657/102492599)
## python性能分析
### [profile性能分析](https://www.cnblogs.com/mikezhang/p/pythonprofile20170907.html)
* cProfile分析cpu使用情况（运行时间），memory_profiler分析内存使用情况
### [psutil](https://www.cnblogs.com/iamjianghao/p/11894623.html)
* Process实现[进程管理](https://www.cnblogs.com/zhuosanxun/p/15194175.html)，cpu_percent和memory_percent获取cpu和内存占用率
## [urllib request](https://www.runoob.com/python3/python-urllib.html)
* urlopen用于打开一个url，read()函数获取网页HTML实体代码
## [python划分训练集、验证集和测试集](https://blog.csdn.net/haoji007/article/details/106165488)
* 使用from sklearn.model_selection import train_test_split
## [字典获取key和value](https://blog.csdn.net/liuweiyuxiang/article/details/80561256)
## [计算文件md5](https://www.cnblogs.com/xiaodekaixin/p/11203857.html)
* [md5可用于校验文件是否相同](https://cloud.tencent.com/developer/article/1485440)
## [读取文件内容read，readline，readlines](https://blog.csdn.net/qq_37828488/article/details/100024924)
## dataframe和字典转换
* [dataframe转字典](https://blog.csdn.net/sinat_26811377/article/details/100065580)，my_dict = dict(zip(data['key'], data['value']))
* [字典转dataframe](https://blog.csdn.net/zx1245773445/article/details/103480750)，my_df = pd.DataFrame(my_dict, index=[0]).T
* [嵌套字典转dataframe](https://blog.csdn.net/xiuxiuxiu666/article/details/115404463)，my_df = pd.DataFrame.from_dict(my_dict).T
## [Pandas读取Excel日期数据的异常处理](https://bbs.huaweicloud.com/blogs/303768)
## [dataframe按列排序](https://blog.csdn.net/zn505119020/article/details/78315812)
* df.sort_values(by='sales', ascending=False) -> 按sales列降序排列，true为升序
## [dataframe获取每行索引](https://blog.csdn.net/xjb329859013/article/details/108401375)
* index_list = df.index.tolist() -> 获取所有索引组成的列表
* print(index_list[0]) -> 列表下标即为行号，通过行号获取对应行索引
## [获取内存和显存使用信息](https://www.codeleading.com/article/88515622463/)
## [python解析word](https://blog.csdn.net/qq_43350524/article/details/107857872)
* 使用docx库，按段落、表格或分块解析
## [判断目录是否存在，不存在则创建](https://blog.csdn.net/u013247765/article/details/79050947)
## [查看库安装位置](https://blog.csdn.net/C_chuxin/article/details/82960824)
* import后使用库名.__file__
* pip show 库名
## [Python中获取异常（Exception）信息](https://www.cnblogs.com/klchang/p/4635040.html)
```
import traceback
try： 
    xxx
except Exception as e:
    print('traceback.format_exc():\n%s' % traceback.format_exc())
```
## [pycharm添加命令行参数](https://blog.csdn.net/counte_rking/article/details/78837028)
## [yield用法](https://www.runoob.com/w3cnote/python-yield-used-analysis.html)
## [f-string格式化字符串](https://cloud.tencent.com/developer/article/1742486)
## python解析excel
* [使用xlrd](https://juejin.cn/post/6844903777825193992)
* [使用pandas](https://cloud.tencent.com/developer/article/1559513)
## [python解析pdf](http://www.ityouknow.com/python/2020/01/02/python-pdf-107.html)
## [join()方法](https://blog.csdn.net/doiido/article/details/43538833)
## windows下读取linux文件，open时要增加encoding='UTF-8'
## [python线程join和setDaemon方法](https://www.cnblogs.com/alan-babyblog/p/5325071.html)
* join方法主线程A中，创建子线程B，并在主线程A中调用了B.join()，那么主线程A会在调用的地方等待，直到子线程B完成操作后，才可以接着往下执行
* setDaemon方法把主线程A设置为守护线程，主线程A执行结束，不管子线程B是否完成,一并和主线程A退出
# [MongoDB](https://www.runoob.com/mongodb/mongodb-tutorial.html)
* WEB应用，可扩展、高性能、分布式文件存储的非关系型数据库
# [jupyter notebook使用argparse模块问题](https://zhuanlan.zhihu.com/p/145720581)
# [消息队列](https://cloud.tencent.com/developer/article/1006035)
* [topic和tag](https://blog.csdn.net/ye17186/article/details/89640286)
# [docker教程](https://yeasy.gitbook.io/docker_practice/)
* [docker引擎](https://www.itheima.com/news/20201130/154933.html)
* [docker客户端与服务器机制](https://www.sukun.xyz/docker%E5%AE%A2%E6%88%B7%E7%AB%AF%E4%B8%8E%E6%9C%8D%E5%8A%A1%E5%99%A8%E6%9C%BA%E5%88%B6/)
* [docker客户端与服务器通信方式](https://www.malaoshi.top/show_1EF5tUtWTr4X.html)
* [commit快照和dockerfile制作镜像](https://support.huaweicloud.com/swr_faq/swr_faq_0012.html)
# http
* [http参数类型](https://blog.csdn.net/madmk/article/details/97246761)
* [鉴权方式](https://juejin.cn/post/6844903927100473357), [token用法](https://support.huaweicloud.com/api-sis/sis_03_0058.html)
* [http表单](https://www.w3school.com.cn/html/html_forms.asp)

# Python 中不爽的地方


wp_id: 683
Status: publish
Date: 2017-11-11 11:16:00
Modified: 2020-05-16 11:52:09


# GIL

之前用多线程都是做一些IO密集的内容, 比如爬网页的时候开一个ThreadPool, 处理速度立马就翻了几倍. 所以一直没把GIL放在心上, 前几天要跑一些处理敏感词的数据, 大概要对几百万篇文章做正则匹配. 想都没想就用了多线程, 吃饭回来发现并没有跑完, 这才想起来正则匹配这种东西是CPU密集的, 用Python的线程并没有任何卵用. 这时候换成multiprocessing.Pool速度又飚起来了, 然而使用进程池终究还是不如线程池方便, 所有传入的函数必须是marshallable, 有时候还是不能直接替换的.

# 函数式编程

没有真正的闭包, 必须使用nonlocal关键词才能实现一些闭包的功能

也没有真正的lambda表达式, 自带的lambda表达式局限非常大

# 其他

bytes的格式化输出竟然是 b'xxx'
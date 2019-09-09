# -2019.9.9

一.switch穿透
二.一个以“.java”为后缀名的源文件，只能有一个与文件名相同的类，可以包含其他类
三.创建servlet实例是由servlet容器来完成的，且创建servlet实例是在初始化方法init()之前
四.共享数据的所有访问都必须使用synchronized加锁，所有访问一定要作为临界区，这样保证了所有的对共享数据的操作都通过对象锁的机制进行
五.标识符组成：英文、数字、下划线和$，数字不能做开头
六.hashmap和treemap都是线程不安全的
七.hashtable对整张表进行加锁、concurrenthashmap将hash表分为16桶，每次只对需要的桶进行加锁
八.list存放顺序可以重复内容、set不能存放重复内容内容 所有重复内容只能靠hashcode和equals两个方法区分、sortedset可以对集合中的数据进行排序
九.URL统一资源定位符：协议://主机:端口/路径
   协议：HTTP协议、主机：主机在因特网的域名、端口：默认为80、路径：文件路径
十.final类型的变量一定要初始化
十一.final变量，如果是基本数据类型，则其数值一旦初始化就不能被改变，如果是引用类型的变量，则对其初始化后，便不能再指向另一个对象，但是其里面的值是可以改变的，也就是说引用变量所指的对象中的内容是可以改变的
十二.8的八进制：010：逢8进1，最前面的0是为了和十进制作区分，也叫转义符
十三.unsigned是无符号数：两个操作数中有无符号数默认将两个数都当做unsigned进行处理
十四.java值传递，值传递拷贝的值用完后就会被释放，对原值没有任何影响，但是对于引用传递，拷贝的是对象的引用，和原值指向的同一块地址，即操作的是同一个对象；例如string str是值传递，操作之间互不影响，原值不变；但是char[] ch是数组，拷贝的是对象的引用，值发生变化，因此选B
十五.java访问权限有public、protected、private、default，default不能修饰变量
十六.native修饰方法，native修饰方法简单来说就是一个java方法调用一个非java代码的接口。定义native方法时，并不提供实现体，因为其实现体是用非java语言在外面实现的。native可以和任何修饰符连用，abstract除外。因为native暗示这个方法是有实现体的，而abstract却显示指明这个方法没有实现体
十七.构造函数可以是内联函数
十八.字节流：inputstream->fileinputstream、bufferedInputstream、datainputstream、objectinputstream
     字符流:reader:inputstreamreader(byte->char)、bufferedreader;writer:outputstreamwriter(char->byte)、bufferedwriter、printwriter
十九执行语句system.out.println(1+"10"+3+"2)=>11032
           system.out.println(1+2+"10"+3+"2)=>31032
           system.out.println(1+"10"+3+1+"2)=>110312
           如果在遇到string之前，int间使用"+"表示数值相加，但是在遇到第一个string后，后面就按string类型来了，变成字符串拼接
二十.statement对象用于执行不带参数的简单SQL语句、preparedstatement对象用于执行预编译的SQL语句、callablestatement对象用于执行对存储过程的调用
二十二.使用throw语句抛出、数组越界、指定URL不存在都会引发异常

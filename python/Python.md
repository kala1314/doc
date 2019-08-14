## Python

### 安装 

#### windows: [ 点击下载安装](<https://www.python.org/downloads/windows/>)

#### linux:

* Arch系列: 自带python3
* CentOS系列：[点击查看](<https://blog.csdn.net/Will_Pass/article/details/91948607>)

#### MacOS: 
* 推荐使用HomeBrew

  * 安装HomeBrew:

    ```shell
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

  * 安装Python3

    ```python
    brew install python3
    ```

    

###  简介

#### 用途：

> 主要方向： 前端、数据以及人工智能...

#### 基本语法

* 编码： 主要是针对这个脚本的编码，有的时候只能使用某一种编码。python3默认是utf-8， 一般不用管。 设置方法：

  ```python
  # -*-coding:utf-8 -*-
  ```

* 注释

  ```python
  # 单行注释用 # 
  # 我是一个单行注释
  
  # 多行注释  ''' '''
  '''
  我是第一行注释
  我是第二行注释
  '''
  ```

* 行与缩进

  ```python
  '''
  python中代码块是使用缩进来表示的， 其他大多数语言一般是{}表示，这就要求python的格式必须要符合规范，多一个空格或者少一个空格都会导致程序出现问题
  '''
  ```

* 变量 
  ```python
  '''
  Python 中的变量不需要声明。每个变量在使用前都必须赋值，变量赋值以后该变量才会被创建。
  等号（=）用来给变量赋值。
  等号（=）运算符左边是一个变量名,等号（=）运算符右边是存储在变量中的值。例如：
  '''
  a = 100
  b = "我是变量"
  ```

  


* 多行语句

  ```python
  # 有时候语句太行，写一行不容易观看，可以用 \ 来进行换行
  
  # 示例：
  a = 1 + 2 + 3 + 5 + \
  	6 + 7 + 8 + 9
  ```

* 输入和输出

  ```python
  # 输入 input
  number = input("请输入一个数： \n")
  ```

  ![输入](pic/input02.png)
  ```python
  # 输出 print
  # 上面输入了一个数，但是并没有打印出来（Mac好像会同时打印）
  print(number)
  ```
  ![输出](pic/print03.png)
### 运行Python

#### 交互式解释器

* windows: 命令提示符 输入 python 

  ![终端](pic/cmd01.png)

* linux/Mac:  同样，终端 python，对于2和3共存的可以 python3

#### 执行python文件

* 上面已经说了怎么在终端里面执行，但是终端有很大的缺点，无法保存。大多数时候都是写到文件里面，执行文件

* python脚本文件的拓展名是 .py 

* 执行示例：

  ![执行文件](pic/execfile04.png)



### 条件判断  if

#### 基本格式
* 基本格式

  ```python
    '''
  if 判断条件 :
      判断为真执行的语句
  else:
      判断不成立的执行语句
  '''
  ```

  <span style="color:red;">TIPS: if 后面的   ： 不要忘记，以及执行的语句需要缩进</span>

#### 简单的 if 示例


* 简单的 if 示例

  ```python
  if 5 > 1:
      print("5 大于 1")
  else:
      print("5 小于 1")
  ```
#### 多条件if
* 有时候一件事情的结果会很很多的结果，if...else就不能够非常准确的来进行判断，就有了 if...elif...else.. 

  ```python
  # 多条件判断基本格式
  if 条件：
  	执行语句
  elif 条件：
  	执行语句
  elif 条件：
  	执行语句
  else：
  	执行语句
  ```

  <span style="color:red">TIPS：elif 实际上就是 else if 的缩写， 可以有无数多个，看实际情况</span>

* 多条件判断示例：

  ```python
  if score == 100:
      print("厉害了，word哥")
  elif score > 80:
      print("你是最胖的")
  elif score >= 60:
      print("60分万岁")
  else:
      print("革命尚未成功，同志还需努力")
  ```

  
#### 嵌套if
* 嵌套if 有的时候需要在一个判断后的结果里面再次判断

  ```python
  # 基本格式
  if 判断条件:
      if 判断条件：
  else:
      执行语句
  ```

  <span style="color: red">TISP：缩进非常重要，注意缩进</span>

* 嵌套if 示例：

  ```python
  if score == 100：
  	if StuName == "小明"：
      	print("咋肥事，上次100，这次100，能不能进步一点")
      else:
          print("再接再厉，今晚加鸡腿")
  else:
      print("差点点就及格了")
  ```

  




### 循环

#### for循环

* 基本格式

  ```python
  for 变量 in 范围:
      执行语句
  ```

* 简单示例

  ```python
  for x in 1,2,3,4,5:
      print(x)
  
  # 执行结果： 1 2 3 4 5
  ```

* 内置函数 range()

  ```python
  # range() 可以用来生成整数列表， 比如1，2，3...100，但是是一个左闭右开的区间
  
  # 函数语法：
  range(起始数，终止数, 步长)
  
  # 示例：
  range(10, 100) # 生成10，11，12...99
  range(10,100,2) # 生成10 12 14...98
  range(100)      # 生成0，1，2，3...99
  ```



#### while 循环

* 基本格式

  ```python
  变量 = 变量值
  while 条件:
      执行语句
      变量数值变更
  ```

  

* 简单示例

  ```python
  a = 1
  while a < 10 :
      print(a)
      a += 1
  ```



### 条件与循环

##### 综合使用

  * 一般格式

    ```python
    for 变量 in 范围:
        if 判断条件:
            执行语句
    ```

  * 简单示例

    ```python
    for x in range(10):
        if x < 5:
            print("{} 小于5".format(x))
        else:
            print("{} 大于5".format(x))
    ```

#### break 和 continue

  * 用途： 在循环的过程中，遇到某种条件需要终止循环。

  * 简单示例

    ```python
    a = 1
    while a < 10:
        if a > 7:
            break
        else:
            print("这是第{}圈，还剩{}圈".format(a, 10-a))
            a += 1
       
    
    #----------------------------#
    break 是终止掉循环，continue是终止掉循环体内剩余的执行语句，直接进入一下轮循环
    for x in range(100):
        if x % 2 == 0:
            print("偶数")
        else:
            continue
    ```




### 运算符

#### 算数运算符

* 常见的加(\+) 减(-) 乘(*)  除(/)
* %  返回除法的余数
* ** 幂运算   x**2  <=> $x^2$
* // 整除（向下整除） 

#### 比较运算符
* 示例
  |    |     |
  | -- | --- |
  | == | 等于 |
  | != | 不等于 |
  | \> | 大于 |
  | \< | 小于 |
  | \>= | 大于等于 |
  | <= | 小于等于  |




#### 赋值运算符
* 示例：
  | =    | 等于   |                      |
  | ---- | ------ | -------------------- |
  | +=   | 加等于 | a += 1 <=> a = a + 1 |
  | -=   | 减等于 | a -= 1  <=> a = a -1 |
  | *=   |        |                      |
  | /=   |        |                      |
  | **=  |        |                      |
  | //=  |        |                      |



#### 位运算



#### 逻辑运算
* 示例：
  |   |    |
  | - | -- |
  | and | 并且|
  | or | 或者|
  | not | 非，如果为True,返回False,相反则返回True|


#### 成员运算
* 示例：
  |    |    |
  | -- | -- |
  | in | 在指定序列择True|
  | not in | 在指定序列没有择False|



### 基本数据类型

#### Number

* 数字又分为三种：
  * 整形int(整数)：1 ，2 ，3...
  * 浮点型float(小数)： 1.2 ，2.3...
  * 复数complex(实数和虚数构成)

* 方法函数
  * abs(x) ; 取x的绝对值
  * max(x)/min(x): 取x的最大最小值
  * mod(x): 取小数部分
  * pow(x,y): x的y次方
  * random(): 随机数 大于等于0，小于1



#### 字符串

* 单引号双引号或者三引号阔起来，即可创建一个字符串

* 字符串的运算：

   ```python
    # 1.字符串 + 字符串
    "Hello" + "world"  = "Hello world"
    
    # 2. 字符串 * 数字
    "Hello" * 2 = "HelloHello"
    
    # in/not in
    判断某个字符在不在字符串里面
   ```

* 切片

   ```python
    s = "Hello Python"
    # 获取第一个字母H
    s[0]   
    --> 字符串的索引是从0开始的，切片就是通过中括号里面的数字来进去取值。所以s[0]的结果就是H
    
    # 获取最后一个字母
    s[-1]
    --> 进行字符串切片时，也可以从后往前数，最后一个字符的索引是 -1
    
    # 获取第一个到第3个字符串： Hel
    s[0:3] <=> s[:3]
    --> 连续取值时可以用 ：表示， 如果：前后是起始位置就可以不用写具体的数：
    # 从第7个取到最后一个: Python
    s[6:]
    
    # 取Hello
    s[:5]
    --> 切片遵守左闭右开， s[:2] 是不包括第三个字符的
   ```

* 字符串的格式化

   ```python
    # python2 用的是c语言的格式化方法，虽然python3也可以用，但是python3 更建议使用 format()函数来进行格式化
    
    # 字符串的格式化通常使用的场景就是将变量用在字符串里面，比如：
    name = "考拉"
    age = 20
    print("大家好，我是{}，今年{}岁了。".format(name, age)) 
    --> 输出结果为： 大家好，我是考拉，今年20岁了。
    --> format()的使用方法就是在字符串里面用{}占位，字符串的引号后面紧跟.format(),按照占位符的顺序，一次将信息填入format的()里面
   ```

* 字符串常见的内置函数

  * find()/index(): 返回字符的索引 
  * len() ： 字符串的长度
  * lower() /upper() 转小写/大写
  * lstrip():  去掉字符串左边的空格或者执法仪字符
  * replace(old, new): 替换字符
  * split():  分割字符串



#### 列表List

* python中列表的出场率是非常高考的，十分灵活，什么数据类型都可以存

* 创建一个列表

   ```python
    first_list = [1, 2, "Python"]
   ```

* 获取列表的值

   ```python
    list1 = ['MacOS', 'Linux', 'Windows']
    # 获取linux:
    list1[1]
    -->列表的索引也是从0开始的， list1对应的值就是linux
     # 获取前两个
      list1[:2]
   ```

* 更改列表的值

   ```python
    list1 = ['MacOS', 'Linux', 'Windows']
    # 将第一个更改为Apple
    list1[0] = "Apple"
   ```

* 删除列表中的值

   ```python
    list1 = ['MacOS', 'Linux', 'Windows']
    # 删除windows
    del list1[2]
   ```

* 增加元素

   ```python
    list1 = ['MacOS', 'Linux']
    # 添加一个字符串： "我是新添加的"
    list1.append("我是新添加的")
   ```

   
    —>列表的增删查改都是可以与切片一起用的

* 方法函数

  * .append(): 往末尾添加元素
  * .count()     统计某个元素出现的次数
  * .index()      元素的索引
  * .reverse()   反转列表的元素



#### 元组tuple

* 和列表list类似，但是元组的元素是不能进行修改

* 创建一个元组

   ```python
    first_tup = (1, 2, "Google")
   ```





#### 字典

* 字典是另一种可变容器模型，且可存储任意类型对象。字典的每个键值(key=>value)对用冒号(**:**)分割，每个对之间用逗号(**,**)分割

* 创建字典

   ```python
    first_dict ={
      'apple':'MacOS/IOS',
      'google':"android",
      'mirosoft':'windows'
    }
   ```

* 获取字典的值

   ```python
    first_dict ={
      'apple':'MacOS/IOS',
      'google':"android",
      'mirosoft':'windows'
    }
    
    # 获取google的值
    first_dict['google']
   ```

* 修改字典的值
     ```python
      first_dict ={
        'apple':'MacOS/IOS',
        'google':"android",
        'mirosoft':'windows'
      }
      
      # 修改apple的值为 MacOS
      first_dict['apple'] = 'MacOS'
     ```

* 删除字典

     ```python
        # 删除某个键
        first_dict['apple']
        
        # 清空字典
        first_dict.clear()
        
        # 删除字典
        del first_dict
     ```

* 字典的注意事项

    * 1.字典的键是唯一的，如果同一个键加了两次，泽会保留后面的键
    * 2.字典的键是不能变的，其对应的值可以更改，且不能用列表来当键

* 方法函数

    * len() 长度

    * keys() 获取所有键

    * items() 查看所有的键值对

        

#### 集合set

* 集合是一个无序的 不重复的元素序列

* 创建集合可以用{} 或者 set(),如果是空集合则必须用 set()

   ```python
    first_set = set(1, 2, 3)
   ```

* 添加元素

   ```python
    first_set = set(1， 2， 3)
    # 添加一个10
    first_set.add(10)
    --> 或者用update
    first_set.update(10)
   ```

* 删除元素

   ```python
    first_set.remove(1)
    # discard()也可以移除元素，且如果没有该院送水不会报错
    first_set.discard(100)
    
    # clear() 清空所有元素
   ```

    

* 方法

  * len() 长度







### Other

#### if 循环运用

* 打印平行四边形

  ```java
  **********
   **********
    **********
  ```

  <!--for i in range(5): 
  	print(" "*i, end="")
  	print("**************") -->

* 打印三角形

  ```java
       *
      ***
     *****
  ```

  <!--for i in range(5):
  	for j in range(5 - i):
  		print(" ", end="")
        print("*"*(2* i - 1)) -->

* 九九乘法表

  ```shell
  1x1=1    
  1x2=2    2x2=4    
  1x3=3    2x3=6    3x3=9    
  1x4=4    2x4=8    3x4=12    4x4=16    
  1x5=5    2x5=10    3x5=15    4x5=20    5x5=25    
  ...
  ```
  <!--for i in range(1, 10):
    	for j in range(1, i+1):
        	print('{}x{}={}\t'.format(j, i, i*j), end='')
    	print() -->

* 菱形

  ```java
       *
      ***
     *****
      ***
       *
  ```

  

* 





### 函数def

* 函数的简单定义：

   ```python
    '''
    函数定义用 def 关键字
    基本语法：
    def 函数名(参数):
    	函数体
    '''
    def name():
      print('我是一个函数')
      
   ```

* 函数的调用

   ```python
       def plus(x, y):
         return x + y
       
       plus(1, 2)
       # 直接写上函数名就能调用了
   ```

   

* 匿名函数 

  * 不实用def 这样标准的形式来定义函数，而是用lambda表达式

  * 匿名函数格式： lambda 参数: 执行体

  * 示例：

     ```python
      # 两个数想加的函数
      def add(x, y):
        return x + y
      add(1, 2)
      # 匿名函数的形式
      print((lambda x, y: x + y)(1, 2))
     ```

    * ![001](pic/001.png)
  * 示例：

* 作用域

  * 什么是作用域： 作用域就是变量的可以使用的范围
  * 划分
    * 局部作用域(L)
    * 闭包函数外到函数 (E)
    * 全局作用域 (G)
    * 内建作用域(B)
  * 变量的查找规则：
    * L -> E -> G -> B,首先在自身作用域查找，找不到就一次向上作用域查找
  * 





### 闭包

* 在函数体中定义内部函数，并使用外部函数的变量，然后吧内部函数返回，那么这个内部函数就叫闭包



### 装饰器

* 什么是装饰器：装饰器就是一个闭包，把一个函数作为参数然后返回一个函数

* 在不修改原函数的情况下新增函数功能，够好的方式就是实用装饰器

   ```python
    # 在原函数 func()新增一行语句
    def func():
        print('我是原函数')
        
    # 装饰器仙新增
    def func1(func):
        def inner():
            print('我是新增的语句')
            func()
        return inner()
    
    func = func1(func)
   ```

* 复杂一点的

   ```python
    
    # 复杂一点的装饰器
    
    def info(name, age):
        print('{} 今年{} 岁'.format(name, age))
    
    
    # 这个函数有一个很明显的问题，年龄不可能为负数，但是这个函数并没有对年龄进行判断
    
    # 装饰器新增判断年龄
    
    def wrapper(info):
    
        def inner(name, age):
            if age < 0:
                age = 0
            return info(name, age)
        return inner
    
    info = wrapper(info)
   ```

* @ 装饰器

  ```python
   # 可以使用@ 将函数进行装饰
   # 实用方法： 在函数定义前，@原函数
  ```

  * ![002](pic/002.png)

* 通用的装饰器模板

   ```python
     def wrapper(func):
     
         def inner(*args, **kwargs):
     
             # 这里新增功能
     
             res = func(*args, **kwargs)
             return res
         return inner
     
     @wrapper
     def func(name):
         print('func这个函数可以传任何参数')
   ```

   

* 带参数的装饰器

   ```python
    # 重复执行函数
    def wrapper(count):
    
        def func1(func):
    
            def inner(*args, **kwargs):
                for i in range(count):
                    func(*args, **kwargs)
            return inner
        return func1
    
    @wrapper(5)
    def func():
        print('这个函数执行的次数是@后面的参数决定的')
    
    # 调用函数
    func()
   ```

  * 





### 迭代器生成器

* 可迭代对象

  * 可以直接作用与for循环的对象，统称( Iterable )
  * 可以直接作用域for 循环的数据类型：
    * 1、集合数据类型，如： list  tuple dict set String
    * 2、generator, 包含生成器和带yield的geberator function
    * 可以书踹死isinstance() 函数判断一个对象是否是 iterable 对象
  * 

* 生成器·

  * 列表生成式 ： 用来生成list的生成器

    ```python
    # 格式： 
    #变量名 = [生成变量 for  变量  变化范围 if 限制条件]
    # 生成 1 2 4 9 16 25 36 
    list1 = [x * x for x in range(1,7)]
        
    # 生成偶数列表
    list2 = [ x for x in range(11) if x %2 == 0]
        
    list3 = [m + n for m in "abc" for n in "123"]
    ```







### 模块

#### 什么是模块: 

* 为了方便事先把一些常见的功能、方法卸载一个文件里面，然后直接导入使用，就不用自己再去手动实现一遍

#### 模块的分类

* python内置模块
  * sys os time math ...
* 第三方模块
  * numpy pandas matplotlib ...
  

#### 模块安装

* pip

  ```shell
  # cmd 窗口 
  pip install 模块名 
  ```

  * [pip 不是内部和外部命令,点击查看](<https://blog.csdn.net/xueli1991/article/details/51914914>)

* pycharm

  ```shell
  import 模块名， ALT+ENTER 会提示 install  
  ```



#### 导入模块

* import     

  ```python
  import sys
  ```

  

* from  模块名 import 方法

  ```python
  from serialnum import webdriver
  ```



#### File模块
* 打开文件open

  ```python
  # 基本格式
  open(file,mode='r')
  
  # 简单示例
  a = open('a.txt', mode='r')
  
  '''
  mode 有 读 模式 r 
  写 w
  追加 w+
  读二进制 rb
  写二进制 wb
  '''
  ```

  

* file对象

  ```python
  
  file.readline()  # 读取一行
  file.readlines() # 全部读取
  file.write()
  ```

  

* 通用的文件写模板

  ```python
  # 读文件
  with open(文件, mode='模式') as f:
      f.write(内容)
  	f.close()
  ```

  

#### OS 模块

* OS：　os，语义为操作系统，所以肯定就是操作系统相关的功能了，可以处理文件和目录这些我们日常手动需要做的操作，就比如说：显示当前目录下所有文件/删除某个文件/获取文件大小……另外，os模块不受平台限制。

* 常用的方法：

  ```python
  # 获取系统名称
  os.name()  # nt 表示windows posix表linux
  
  # 返回指定目录下的所有文件和目录名
  os.listdir(指定路径)
  
  # 删除文件 
  os.remove(文件名)
  
  # 创建文件
  os.makedirs()
  
  # 更名
  os.rename()
  
  # 运行shell
  os.system() 
  
  # 判断是不是一个文件 
  os.path.isfile(名称)
  
  # 判断是不是一个目录
  os.path.isdir(路径)
  
  # 如果路径 path 存在，返回 True；如果路径 path 不存在，返回 False
  os.path.exists(path)
  
  ...
  ```

  ==方法比较多，用到什么就百度把==

* windows  清理垃圾文件Demo

  ```python
  import os
  
  '''
  需要清理的文件路径： D:\Test
  需要清理的文件： *.xlsx
  '''
  
  # windows 的路径需要 \\  或者 /
  
  locPath = 'D:\\Test'
  # locPath = 'D:/Test'
  
  # print(os.listdir(locPath))
  files = os.listdir(locPath)
  
  for f in files:
      if f.endswith(".xlsx"):
          # 组合文件绝对路径
          filename = os.path.join(locPath, f)
          os.remove(filename)
  ```

  



#### time 模块

* 时间的表示方式： 时间戳 、 时间元组、时间格式化

* 时间戳

  * 时间戳是指格林尼治时间1970年01月01日00时00分00秒(北京时间1970年01月01日08时00分00秒)起至现在的总秒数

  * 获取当前的时间戳

    ```python
    import time
    time.time()
    ```

* 时间元组

  * 时间元组：首先是一个元组类型，然后里面有9个元素，分别如下：
  * 

* 




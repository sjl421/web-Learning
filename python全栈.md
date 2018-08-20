# python全栈

标签（空格分隔）： python 全栈

[TOC]

---

python全栈教程，来自老男孩第三期

---
### python基础
#### python 分类

 - cython
 - jython
 - ironPython

#### python IDE
##### Pycharm


#### python 变量
变量命名：字母、数字、下划线，不能以数字开头，不能是关键字

```ipython
In [4]: a=1
```

#### python 数据类型

1、字符串
```ipython
In [12]: s='hello'

In [13]: ss="hello"

In [14]: sss='''
    ...: hello, i love python
    ...: '''
    
In [15]: s+ss+sss
Out[15]: 'hellohello\nhello, i love python\n'

In [16]: s*3
Out[16]: 'hellohellohello'
```

```ipython

In [37]: s="hello, python"

In [38]: s.capitalize() #首字母大写
Out[38]: 'Hello, python'

In [39]: s.casefold() #小写，支持多语言
Out[39]: 'hello, python'

In [40]: s.lower() #小写
Out[40]: 'hello, python'

In [42]: s.center(20) #字符串居中
Out[42]: '   hello, python    '

In [43]: s.center(20, '~')
Out[43]: '~~~hello, python~~~~'

In [45]: s.count('l') #字符串中的子序列出现的次数
Out[45]: 2

In [48]: s.count('t', 3)
Out[48]: 1

In [49]: s.count('t', 3, 5)
Out[49]: 0

In [50]: s.startswith('h') #是否以指定的字符串开头
Out[50]: True

In [51]: s.endswith('n') #是否以指定的字符串结尾
Out[51]: True

In [52]: s.find('ll') #在字符串中寻找子序列，找到了返回索引，找不到返回-1
Out[52]: 2

In [54]: s.index('ll') #在字符串中寻找子序列，找到了返回索引，找不到返回异常
Out[54]: 2

In [55]: s.isalnum() #判断字符串中是否是字母数字
Out[55]: False

In [57]: s.isalpha() #判断字符串中是否是字母
Out[57]: False

In [58]: s.isdecimal() #判断字符串中是否是小数
Out[58]: False

In [59]: s.isdigit() #判断字符串中是否是数字
Out[59]: False

In [60]: s.isidentifier() #判断字符串是否是有效的标识符
Out[60]: False

In [61]: s.islower() #判断字符串是否是小写的
Out[61]: True

In [62]: s.isnumeric() #判断字符串是否只有数字
Out[62]: False

In [63]: s.isprintable() #判断字符串中的字符是否是可打印的
Out[63]: True

In [64]: s.isspace() #判断是否是空白字符
Out[64]: False

In [66]: s.isupper() #判断字符串是否是大写的
Out[66]: False

In [73]: s='hello\tpython'

In [74]: s.expandtabs(2) #将tab用空格展开
Out[74]: 'hello python'

In [75]: s.expandtabs(3)
Out[75]: 'hello python'

In [76]: s.expandtabs(4)
Out[76]: 'hello   python'

In [84]: ' '.join(s) #将序列用指定字符拼接起来
Out[84]: 'h e l l o \t p y t h o n'

In [85]: s.ljust(30, '$') #左对齐
Out[85]: 'hello\tpython$$$$$$$$$$$$$$$$$$'

In [86]: s.rjust(30, '$') #右对齐
Out[86]: '$$$$$$$$$$$$$$$$$$hello\tpython'

In [87]: s.zfill(30) #右对齐，并用0填充
Out[87]: '000000000000000000hello\tpython'

In [88]: s='  hello, python     '

In [89]: s.strip() #去除字符集中的字符，默认空白字符
Out[89]: 'hello, python'

In [90]: s.lstrip() #去除左边字符集中的字符，默认空白字符
Out[90]: 'hello, python     '

In [91]: s.rstrip() #去除右边字符集中的字符，默认空白字符
Out[91]: '  hello, python'

In [1]: o = "aeiou"
In [2]: n = "12345"
In [3]: s="hcwebkashdfqwa"
In [5]: m=str.maketrans(o,n)
In [6]: s.translate(m) #按照字符转换表进行替换
Out[6]: 'hcw2bk1shdfqw1'

In [8]: s.partition('sh') # 将字符串按照指定部分分割成三份
Out[8]: ('hcwebka', 'sh', 'dfqwa')

In [9]: s.rpartition('sh') # 将字符串按照指定部分从右向前分割成三份
Out[9]: ('hcwebka', 'sh', 'dfqwa')

In [12]: s.split('h') # 按照指定的字符进行字符串分割
Out[12]: ['', 'cwebkas', 'dfqwa']

In [13]: s.rsplit('h') # 按照指定的字符从右进行字符串分割
Out[13]: ['', 'cwebkas', 'dfqwa']

In [14]: s="asdfkjhsa\nasuidhf\nuiewhfc\n"

In [15]: s.splitlines() #按照换行符进行分割
Out[15]: ['asdfkjhsa', 'asuidhf', 'uiewhfc']

In [17]: s.swapcase() # 大小写转换
Out[17]: 'ASDFKJHSA\nASUIDHF\nUIEWHFC\n'
```
字符串支持按照索引进行获取，索引从0开始。
```ipython
In [18]: s='hjsidfjkewfasdfasd'

In [19]: s[0]
Out[19]: 'h'

In [20]: s[1]
Out[20]: 'j'

In [21]: s[1:10]
Out[21]: 'jsidfjkew'

In [22]: s[:10]
Out[22]: 'hjsidfjkew'

In [23]: s[:]
Out[23]: 'hjsidfjkewfasdfasd'

In [24]: s[2:-1]
Out[24]: 'sidfjkewfasdfas'

In [25]: s[:-1]
Out[25]: 'hjsidfjkewfasdfas'

In [26]: s[-9:-1]
Out[26]: 'wfasdfas'
```

> 字符串是一个不可变对象,一旦创建就不可改变

字符串格式化：

    %[(name)][flags][width].[precision]typecode
    

 - (name)      可选，用于选择指定的key
 - flags    可选，可供选择的值有:
   - \+ 右对齐；正数前加正好，负数前加负号
   - \- 左对齐；正数前无符号，负数前加负号
   - 空格 右对齐；正数前加空格，负数前加负号
   - 0 右对齐；正数前无符号，负数前加负号；用0填充空白处
 - width       可选，占有宽度
 - .precision   可选，小数点后保留的位数
 - typecode    必选
   - s，获取传入对象的__str__方法的返回值，并将其格式化到指定位置
   - r，获取传入对象的__repr__方法的返回值，并将其格式化到指定位置
   - c，整数：将数字转换成其unicode对应的值，10进制范围为 0 <= i <= 1114111（py27则只支持0-255）；字符：将字符添加到指定位置
   - o，将整数转换成八进制表示，并将其格式化到指定位置
   - x，将整数转换成十六进制表示，并将其格式化到指定位置
   - d，将整数、浮点数转换成十进制表示，并将其格式化到指定位置
   - e，将整数、浮点数转换成科学计数法，并将其格式化到指定位置（小写e）
   - E，将整数、浮点数转换成科学计数法，并将其格式化到指定位置（大写E）
   - f， 将整数、浮点数转换成浮点数表示，并将其格式化到指定位置（默认保留小数点后6位）
   - F，同上
   - g，自动调整将整数、浮点数转换成 浮点型或科学计数法表示（超过6位数用科学计数法），并将其格式化到指定位置（如果是科学计数则是e；）
   - G，自动调整将整数、浮点数转换成 浮点型或科学计数法表示（超过6位数用科学计数法），并将其格式化到指定位置（如果是科学计数则是E；）
   - %，当字符串中存在格式化标志时，需要用 %%表示一个百分号

2、整型
在python3中所有的整型都是int，但是在python2中大的整数类型是long
```ipython
In [17]: a=10

In [18]: b=20

In [19]: a+b
Out[19]: 30

In [20]: a-b
Out[20]: -10

In [21]: a*b
Out[21]: 200

In [22]: a/b
Out[22]: 0.5

In [23]: a%b
Out[23]: 10

In [24]: a//b #地板除，结果为两数相除的商
Out[24]: 0
```

```ipython
In [17]: int?
Init signature: int(self, /, *args, **kwargs) 整型数据类型的工厂方法函数
Docstring:
int(x=0) -> integer
int(x, base=10) -> integer

In [22]: int('12')
Out[22]: 12

In [27]: int('01010101', base=2)
Out[27]: 85

In [29]: int('0o17263', base=8)
Out[29]: 7859

In [30]: int('0x1726f3', base=16)
Out[30]: 1517299

In [31]: a.bit_length?
Docstring:
int.bit_length() -> int 数字的二进制的位数长度(至少几位)

Number of bits necessary to represent self in binary.
>>> bin(37)
'0b100101'
>>> (37).bit_length()
6
Type:      builtin_function_or_method

In [32]: (1).bit_length()
Out[32]: 1

In [33]: (2).bit_length()
Out[33]: 2

In [34]: (3).bit_length()
Out[34]: 2

In [35]: (4).bit_length()
Out[35]: 3

In [36]: (5).bit_length()
Out[36]: 3
```
3、布尔类型
```ipython
In [4]: b=True

In [5]: b
Out[5]: True

In [6]: d=False

In [7]: d
Out[7]: False
```

#### python 数据结构
1、列表(list)

> 创建列表
```ipython
In [45]: l=[1,2,3,4,5,6,7]
```

> 读取列表元素
```ipython
In [47]: l[0]
Out[47]: 1

In [48]: l[1]
Out[48]: 2

In [49]: l[1:]
Out[49]: [2, 3, 4, 5, 6, 7]

In [50]: l[1:4]
Out[50]: [2, 3, 4]

In [51]: l[1:-1]
Out[51]: [2, 3, 4, 5, 6]

In [52]: l[:-1]
Out[52]: [1, 2, 3, 4, 5, 6]

In [53]: l[-3:-1]
Out[53]: [5, 6]

In [54]: l[0]='a'

In [55]: del l[-1]

In [56]: l
Out[56]: ['a', 2, 3, 4, 5, 6]

In [57]: 'a' in l
Out[57]: True
```
> 列表的常用方法

```ipython
In [61]: l
Out[61]: ['a', 2, 3, 4, 5, 6]

In [62]: l.append(10) #在列表尾部添加元素

In [64]: l.clear() #将列表清空

In [66]: l=[1,2,3]

In [67]: l.copy() #将列表copy，注意这里是浅copy
Out[67]: [1, 2, 3]

In [68]: l.count(1) #计算某元素的个数
Out[68]: 1

In [69]: l.extend([4,5,6]) #将可迭代对象中的元素全部添加到某列表中

In [72]: l.index(2) #返回某个元素的索引位置
Out[72]: 1

In [73]: l.insert(1, 'a') #在某个索引前插入值

In [75]: l.pop() #删除某索引处的元素，最后一个元素
Out[75]: 6

In [76]: l.remove('a') # 删除某个值

In [77]: l.sort() #排序，默认字典序

In [78]: l
Out[78]: [1, 2, 3, 4, 5]

In [79]: l.reverse() #元素反转

In [80]: l
Out[80]: [5, 4, 3, 2, 1]
```

2、元祖(tuple)
元祖中的元素不可被修改，同样用索引取值，支持切片
```ipython
In [1]: t=(1,2,3,4)

In [2]: t=(1,) #单元素元祖定义时加个","
```

元组的方法如下
```ipython
In [4]: t.count(1)
Out[4]: 1

In [5]: t.index(1)
Out[5]: 0
```

3、字典(dict)
字典是一系列键值对的无序集合，其中字典的key必须是可哈希的，value可以是任意值。

```ipython
In [6]: d1 = {"k1": "v1", "k2": "v2"}

In [7]: d1 = dict(k1="v1", k2="v2")

In [9]: d={1:1,'2':1,False:22, (1,3,4):14}

In [10]: d
Out[10]: {1: 1, '2': 1, False: 22, (1, 3, 4): 14}

In [11]: d[False]
Out[11]: 22

In [12]: d[(1,3,4)]
Out[12]: 14

In [13]: del d[1]
```
字典的常用方法：
```ipython
In [14]: d.keys() #返回所有的key
Out[14]: dict_keys(['2', False, (1, 3, 4)])

In [15]: d.values() #返回所有的value
Out[15]: dict_values([1, 22, 14])

In [16]: d.items() #返回所有的k,v对
Out[16]: dict_items([('2', 1), (False, 22), ((1, 3, 4), 14)])

In [17]: d.clear() #清空字典

In [18]: d.copy() #浅拷贝

In [19]: dict.fromkeys(["k1","k2", "k3"]) #将序列中的每一个作为key，创建字典
Out[19]: {'k1': None, 'k2': None, 'k3': None}

In [21]: d.get(1) #获取某个key的值，如果不存在，返回None或指定的值
Out[21]: '1'

In [23]: d.pop(1) #弹出某个key的值
Out[23]: '1'

In [24]: d.popitem() #随机弹出某一kvdui
Out[24]: (3, '3')

In [25]: d.setdefault('a', 'aa') #为字典设置值，但是如果已经存在，就不设置
Out[25]: 'aa'

In [26]: d
Out[26]: {2: '2', 'a': 'aa'}

In [28]: d.update({'aa':1,'bb':22}) #更新字典，已经存在的，将值更新，不存在的，直接设置

In [29]: d
Out[29]: {2: '2', 'a': 'aa', 'aa': 1, 'bb': 22}
```

4、集合(set)
由一系列不重复的，无序的可哈希的元素组成的元素集合

 - 元素是无序的
 - 元素不能重复
 - 元素必须是可哈希的
 
```ipython
In [30]: s={1,4,7,0,'a',(1,2)}
```

集合的常用方法：
```ipython
In [31]: s.add('b') #添加元素

In [32]: s.clear()  #清空集合

In [32]: s.copy() #对集合进行浅拷贝
Out[32]: {(1, 2), 0, 1, 4, 7, 'a', 'b'}

In [33]: s.pop() #随机弹出一个元素
Out[33]: 0

In [36]: s.remove(1) #移除集合中的某一个元素

In [38]: s.discard('1') #移除集合中的某一个元素,不存在也不会报错

In [57]: s.update({'a','b'}) #更新集合
```

集合操作
```ipython
In [39]: s1={1,2,3,4,5,6,7}

In [40]: s2={2,3,5,7,8,90}

# 交集
In [41]: s1 & s2
Out[41]: {2, 3, 5, 7}

In [42]: s1.intersection(s2)
Out[42]: {2, 3, 5, 7}

# 并集
In [43]: s1 | s2
Out[43]: {1, 2, 3, 4, 5, 6, 7, 8, 90}

In [44]: s1.union(s2)
Out[44]: {1, 2, 3, 4, 5, 6, 7, 8, 90}

# 差集
In [45]: s1 - s2
Out[45]: {1, 4, 6}

In [46]: s1.difference(s2)
Out[46]: {1, 4, 6}

# 补集
In [47]: s1 ^ s2
Out[47]: {1, 4, 6, 8, 90}

In [48]: s1.symmetric_difference(s2)
Out[48]: {1, 4, 6, 8, 90}

In [49]: s1.isdisjoint(s2) #两个集合是否有交集
Out[49]: False

In [50]: s1.isdisjoint({})
Out[50]: True

In [55]: s1.issuperset({1,2,3,4,5,6,7,8}) #判断某集合是否是另一集合的超集
Out[55]: False

In [56]: s1.issubset({1,2,3,4,5,6,7,8}) #判断某集合是否是另一集合的子集
Out[56]: True
```

5、不可变集合(frozenset)
```ipython
In [61]: s=frozenset([1,2,3,4])

In [62]: s
Out[62]: frozenset({1, 2, 3, 4})
```

#### python 内置函数
![内置函数列表][1]
1、`len`
```ipython
In [27]: len('12321')
Out[27]: 5

In [28]: len('你好')
Out[28]: 2

In [29]: len([1,2,3,4,5])
Out[29]: 5
```

2、`range`
> 在python2中range返回的是列表，在python3中返回的是一个可迭代的range对象。

```ipython
In [31]: range(10)
Out[31]: range(0, 10)

In [32]: range(1,10)
Out[32]: range(1, 10)

In [33]: range(1,10, 2)
Out[33]: range(1, 10, 2)
```
3、`sorted`
排序，默认按照字典序，支持自定义的方式
自定义比较结果

 - -1 小于
 - 0 等于
 - 1 大于

4、`format`

    [[fill]align][sign][#][0][width][,][.precision][type]
    

 - fill 【可选】空白处填充的字符
 - align 【可选】对齐方式（需配合width使用）
   - <，内容左对齐
   - >，内容右对齐(默认)
   - ＝，内容右对齐，将符号放置在填充字符的左侧，且只对数字类型有效。即使：符号+填充物+数字
   - ^，内容居中
 - sign 【可选】有无符号数字
   - +，正号加正，负号加负；
   - -，正号不变，负号加负；
   - 空格 ，正号空格，负号加负；
 - # 【可选】对于二进制、八进制、十六进制，如果加上#，会显示 0b/0o/0x，否则不显示
 - ，【可选】为数字添加分隔符，如：1,000,000
 - width 【可选】格式化位所占宽度
 - precision 【可选】小数位保留精度
 - type 【可选】格式化类型
   - 传入” 字符串类型 “的参数
     - s，格式化字符串类型数据
     - 空白，未指定类型，则默认是None，同s
   - 传入“ 整数类型 ”的参数
     - b，将10进制整数自动转换成2进制表示然后格式化
     - c，将10进制整数自动转换为其对应的unicode字符
     - d，十进制整数o，将10进制整数自动转换成8进制表示然后格式化；
     - x，将10进制整数自动转换成16进制表示然后格式化（小写x）
     - X，将10进制整数自动转换成16进制表示然后格式化（大写X）
   - 传入“ 浮点型或小数类型 ”的参数
     - e， 转换为科学计数法（小写e）表示，然后格式化；
     - E， 转换为科学计数法（大写E）表示，然后格式化;
     - f ， 转换为浮点型（默认小数点后保留6位）表示，然后格式化；
     - F， 转换为浮点型（默认小数点后保留6位）表示，然后格式化；
     - g， 自动在e和f中切换
     - G， 自动在E和F中切换
     - %，显示百分比（默认显示小数点后6位）   
5、`all`
对序列中的每一个元素做布尔运算，如果所有的都为True，则最终的结果为True，空序列的结果是True

6、`any`
对序列中的每一个元素做布尔运算，只要有一个为True，则最终的结果为True

7、`bin`
将十进制转为二进制

8、`bytes`
转换为字节

9、`callable`
判断是否是可调用的

10、`chr`
返回对应的ascii表的字符

11、`dir`
显示对象的属性和方法列表

12、`divmod`
返回两数相除的商和余数

13、`getattr`
14、`setattr`
15、`hash`
返回不可变对象的hash值

16、`hex`
将十进制转为十六进制

17、`oct`
将十进制转为八进制

18、`isinstance`
判断某对象是否为某类的实例

19、`locals`
返回当前作用域的局部变量字典

20、`globals`
返回全局变量字典

21、`max`
返回最大值，支持按照自定义函数进行判断

22、`min`
返回最小值，支持按照自定义函数进行判断

23、`zip`
函数用于将可迭代的对象作为参数，将对象中对应的元素打包成一个个元组，然后返回由这些元组组成的列表。

24、`ord`
与chr相反

25、`reversed`
将序列反转

26、`round`
四舍五入

27、`slice`
slice(start, stop[, step])，返回一个切片对象

28、`sum`
对可迭代序列进行求和

29、`type`
返回对象的类型

30、`vars`
如果没有传参，等价于lcoals(), 如果有传参，等价于object.__dict__

31、`__import__`
导入一个模块


#### python 运算符

> +、-、\*、/、%、\*\*、//
> in
> \>、\>=、<、<=、==、!=、<>
> not、and、or
> =、+=、-=、*=、/=、%=、//=、\*\*=

#### python 条件语句

    if condition:
        #条件成立时
        
    if condition:
        #条件成立时
    else:
        #条件不成立时
        
    if condition1:
        #条件1成立时
    elif condition2:
        #条件2成立时
    else:
        #以上条件均不成立时
        
```python
num = 10
if num > 0 and num < 10:
    print('num less than 10')
elif num >= 10 and num < 20:
    print('num less than 20')
else:
    print('num more than 20')
```
    
`pass`表示什么都不做
```python
if True:
    pass
```

#### python 循环
1、for 循环

    for var in var_list:
        # do something

2、while循环

    while condition：
        # do something
        
## while循环要特别注意退出条件 ##

举例：
```python
n = 1
while n < 11:
    print(n)
    n = n + 1
```

#### python 函数

    def funcName(parameter):
        '''
        文档注释
        '''
        #body
        #函数体
        
函数返回值：
> 在python的函数中，return语句不是必须的，如果没有，会默认返回None
> return语句后可以跟多个值，多个值会作为一个元祖返回
     
函数的参数：
1、普通形参

    def func(a,b):
        #body
        
    func(1,2)
    func(b=2, a=1)
    func(1, b=2)#关键字参数必须在位置参数后面
     
2、默认参数

    def f(a,b=None,c=None):
        #body
        
    f(1)
    f(1,2)
    f(1,2,3)

3、参数组

    def f(a, *args):
        "不定长参数，args会存储成一个列表"
        #body
        
    f(1,2)
    f(1,2,3,4)
    f(1,2,3,4,5,6)
    f(1,*[1,2,3,4])//
    
    def f(a, **kwargs):
        "不定长参数，keargs会存储成一个字典"
        #body
        
    f(1)
    f(1,a=1,b=2)
    f(1,a=1,b=2,c=4)
    f(1, **{a=1,b=2,c=4})//
    
4、匿名函数

    lambda para: #表达式
    eg:
    x = lambda a: a**2
    x(10)
    
5、函数式编程

 - 函数内部不用变量保存状态，不修改变量
 - 函数即变量，函数可以做为函数的参数，也可以作为返回值


尾调用优化
在函数的最后一步(不是最后一行)进入下一步递归,这种不需要保存上一步状态，直接进入下一层(普通的递归需要保存上一步的状态)
```python

def bar():
    print('bar')

def foo():    
    return bar()
    
foo()
```

高阶函数：
满足1：参数中包含函数，2：返回值中包含函数，就是所谓的高阶函数

`map`
用指定的操作处理序列中的每一个元素，得到的结果是一个列表，该列表元素个数及位置与原来一样
```ipython
In [1]: map?
Init signature: map(self, /, *args, **kwargs)
Docstring:
map(func, *iterables) --> map object

Make an iterator that computes the function using arguments from
each of the iterables.  Stops when the shortest iterable is exhausted.
Type:           type
```

`reduce`
将序列的首元素和次元素做指定的操作，得到的元素作为新的首元素，继续该操作直到得到最终的结果
```ipython
In [2]: reduce?
Docstring:
reduce(function, sequence[, initial]) -> value

Apply a function of two arguments cumulatively to the items of a sequence,
from left to right, so as to reduce the sequence to a single value.
For example, reduce(lambda x, y: x+y, [1, 2, 3, 4, 5]) calculates
((((1+2)+3)+4)+5).  If initial is present, it is placed before the items
of the sequence in the calculation, and serves as a default when the
sequence is empty.
Type:      builtin_function_or_method
```
> 注意reduce函数在python3中被移到了functools模块中

`filter`
用指定操作遍历序列的每一个元素，如果是True则留下来，如果是FALSE则过滤掉
```ipython
In [3]: filter?
Init signature: filter(self, /, *args, **kwargs)
Docstring:
filter(function or None, iterable) --> filter object

Return an iterator yielding those items of iterable for which function(item)
is true. If function is None, return the items that are true.
Type:           type
```

#### 函数递归

> 递归必须要有一个退出条件,否则会导致死循环直到内存占尽

```python
def f(n):
    if n = 0 or n = 1:
        return 1
    else:
        return f(n-1)*n
        
f(10)
```

#### python 作用域
1、全局变量
全局变量在全局生效
2、局部变量
在子程序中定义，只在子程序中生效

变量的查找顺序：首先查找局部变量，如果找不到，则查找全局变量

`global`
如果想要在局部直接操作全局变量，则需要用global修饰变量
```python
name = 'sjl'
def out():
    name = 'sjl421'
    def in():
        global name
        name = 'sjl_421' #直接将全局的name修改了
        print(name)
    in()
    print(name)
    
print(name) #sjl
out() #sjl421
print(name)#sjl_421
```
`nonlocal`
如果想要在局部操作上一级变量，则需要用nonlocal修饰变量
```python
name = 'sjl'
def out():
    name = 'sjl421'
    def in():
        nonlocal name
        name = 'sjl_421' #直接将上级的name修改了
    in()
    print(name)
    
print(name) #sjl
out() #sjl_421
print(name) #sjl
```

#### python文件操作

    #文件处理的步骤
    # 1. 打开文件
    f_handler = open(file_name)#以系统默认编码打开
    # 2. 处理文件
    f_handler.read()
    # 3. 关闭文件
    f_handler.close()
    
文件打开模式：

 - r 只读
 - w 只写，如果文件存在，会将文件内容清空，如果不存在，会新建文件
 - a 追加
 - r+ 打开可读写的文件，该文件必须存在。 
 - w+ 打开可读写文件，若文件存在则文件长度清为零，即该文件内容会消失。若文件不存在则建立该文件。
 - a+ 以附加方式打开可读写的文件。若文件不存在，则会建立该文件，如果文件存在，写入的数据会被加到文件尾后，即文件原先的内容会被保留。 
 - rb 二进制读
 - wb 二进制写
 - ab 二进制追加
 
> 注意以b的方式打开文件时，文件的编码不需要指定
> 在Linux平台，文件默认就是二进制的
 

常用方法：
1、`readable`
是否可读
2、`readline`
读取一行
3、`readlines`
读取所有行
4、`read`
从光标当前位置读取后面所有内容
5、`write`
往文件中写内容
6、`writelines`
以列表的形式往文件中写内容
7、`flush`
将缓冲区内容立即写入文件
8、`seek`
移动光标，默认从文件开头进行移动，seek支持一下三种模式：

 - 0 0代表从文件开头算起，
 - 1 1代表开始从当前位置开始算起，
 - 2 2代表从文件末尾开始算起。
 
> 注意，模式为2时，移动偏移量要设置成负值才能正确的移动


9、`tell`
返回光标当前所在位置
10、`truncate`
文件截取，注意必须是位于写模式


with语句块
会自动关闭文件句柄
    with open(filename) as f:
        # do something
        
举例：寻找文件最后一行
```python

file_name = ""
f = open(file_name, 'rb')
for i in f:
    offset = -10
    while True:
        f.seek(offset, 2)
        data = f.readlines()
        if len(data) > 1:
            print('最后一行是%s'%data[-1])
            break
            
        offset *= 2


f.close()

```
    
#### 迭代器和生成器
**迭代器协议**：对象必须提供一个next方法，执行该方法要么返回迭代中的下一项，要么就引起一个StopIteration异常，以终止迭代 （只能往后走不能往前退）

实现了迭代器协议的对象就是可迭代对象(包含__iter__()方法)

> for循环的本质就是对一个可迭代对象(或者可以转换为可迭代对象的对象，也就是包含__iter__方法)进行遍历。for循环就是基于迭代器协议实现统一的可以遍历所有对象的方法。

> next()方法等价于obj.__next__(), 

**生成器**:可以理解为一种数据类型，这种类型自动实现了迭代器协议，所以生成器就是可迭代对象。

 1. 函数内存在yield语句，该函数就是生成器类型，可以存在多个yield语句
 2. 生成器表达式，类似于列表推导式，见下面

#### 装饰器
本质就是函数，为其他函数实现附加功能

原则：
1、不修改被修饰函数的源代码
2、不修改被修饰函数的调用方式

    #装饰器语法糖，相当于myFunc=wrapper(myFunc)
    @wrapper
    def myFunc(*args, **kwargs):
        pass
        
    def wrapper(func):
        #外部闭包环境
        def innerWrapper(*args, **kwargs):
            #函数嵌套，内部函数被返回
            res = func(*args, **kwargs)
            return res
        return innerWrapper
        
    myFunc(......)#调用
    
    
带参装饰器：

    @wrapper(para="some_value")
    def myFunc(*args, **kwargs):
        pass
        
    def func_wrapper(para=value):
        def wrapper(func):
            #外部闭包环境
            def innerWrapper(*args, **kwargs):
                #函数嵌套，内部函数被返回
                res = func(*args, **kwargs)
                return res
            return innerWrapper
        return wrapper
    myFunc(......)#调用

**闭包**：闭包是由函数及其相关的引用环境组合而成的实体(即：闭包=函数+引用环境),
按照命令式语言的规则，ExFunc函数只是返回了内嵌函数InsFunc的地址，在执行InsFunc函数时将会由于在其作用域内找不到sum变量而出 错。而在函数式语言中，当内嵌函数体内引用到体外的变量时，将会把定义时涉及到的引用环境和函数体打包成一个整体（闭包）返回。

    def outer():
    
        # 外部函数的作用域
        def inner():
            # body
            
        # 将内部函数返回，内部函数会保留当前作用域的环境，形成闭包
        return inner
        
序列解压：

```ipython
In [1]: a, *_, c = [1,2,3,4]

In [2]: a
Out[2]: 1

In [3]: c
Out[3]: 4

In [4]: a, b, *c = [1,2,3,4]

In [5]: a
Out[5]: 1

In [6]: b
Out[6]: 2

In [7]: c
Out[7]: [3, 4]
```

装饰器举例：
```python

user_list=[
    {'name':'sjl','passwd':'123'},
    {'name':'sjl421','passwd':'123'},
    {'name':'songjl','passwd':'123'},
    {'name':'sjl_421','passwd':'123'},
]

current_user={'username':None,'login':False}

def auth_deco(func):
    def wrapper(*args,**kwargs):
        if current_user['username'] and current_user['login']:
            res=func(*args,**kwargs)
            return res
        username=input('用户名: ').strip()
        passwd=input('密码: ').strip()

        for index,user_dic in enumerate(user_list):
            if username == user_dic['name'] and passwd == user_dic['passwd']:
                current_user['username']=username

                current_user['login']=True
                res=func(*args,**kwargs)
                return res
                break
        else:
            print('用户名或者密码错误,重新登录')

    return wrapper

@auth_deco
def index():
    print('欢迎来到主页面')
            
```



#### 推导式

1、列表推导式

    [ v for v in some_iter]
    # 结合三元表达式
    [ v for v in some_iter if condition ]
    
2、字典推导式

    { K:v for k in some_iter}

3、生成器表达式

    ( v for v in some_iter )


#### python 对象拷贝
**浅拷**贝：`copy.copy`，拷贝父对象，不会拷贝对象的内部的子对象。
![此处输入图片的描述][2]

**深拷贝**：`copy.deepcopy`，完全拷贝了父对象及其子对象。
![此处输入图片的描述][3]


#### python 模块

在python中，一个py文件就是一个模块。
模块的导入

    import module

或者

    from module import (class|const|function)
    
> - 注意import导入时会把脚本执行

> - from方式导入时同样会将脚本执行

> - 导入模块时默认从sys.path从按照顺序查找，如果模块不再sys.path中，则需要将模块添加到sys.path中

`__name__`
当脚本直接被执行时，`__name__`的值是`__main__`，当脚本被作为模块导入时，__name__的值为作为模块的路径名
```python
if __name__ == "__main__":
    # body
```

`__file__`
当前文件的文件名(注意打印的仅仅是文件名)

#### python 常用模块
1、`time`



 - `time.time()`  #从1970年1月1号到现在的秒数
 - `time.localtime()` #当前时间的struct_time对象
 - `time.gmtime()` #当前时间的struct_time对象(UTC时间)
 - `time.mktime(struct_time)` #将一个struct_time对象转化为时间戳
 - `time.strftime(time_format, struct_time)` #将struct_time对象转化为指定格式的时间字符串
   - %Y  Year with century as a decimal number.
   - %m  Month as a decimal number [01,12].
   - %d  Day of the month as a decimal number [01,31].
   - %H  Hour (24-hour clock) as a decimal number [00,23].
   - %M  Minute as a decimal number [00,59].
   - %S  Second as a decimal number [00,61].
   - %z  Time zone offset from UTC.
   - %a  Locale's abbreviated weekday name.
   - %A  Locale's full weekday name.
   - %b  Locale's abbreviated month name.
   - %B  Locale's full month name.
   - %c  Locale's appropriate date and time representation.
   - %I  Hour (12-hour clock) as a decimal number [01,12].
   - %p  Locale's equivalent of either AM or PM.
 - `time.strptime(string, format)` #将指定格式的时间字符串转化为struct_time对象

2、`random`

 - random.random() #返回[0,1)的浮点数
 - random.randint(a, b) #返回[a，b]之间的整数
 - random.randrange(a,b) #返回[a,b)之间的整数
 - random.choice(list) #返回list的一个随机元素
 - random.sample(set, num) #从一个元素集合中取num个样品
 - random.uniform(a,b) #返回a,b之间的一个随机数
 - random.shuffle(list) #将一个元素集合打乱顺序

生成随机验证码：
```python

def v_code():
    ret = ""
    for i in range(5):
        num = random.randint(0,9)
        alf = chr(random.randint(65,122))
        ret += str(random.choice([num, alf]))

    return ret
```
 

3、`os`

 - `os.getcwd()` #获取当前工作目录，即python脚本执行目录
 - `os.chdir()` #改变工作目录
 - `os.curdir` #返回当前工作目录('.')
 - `os.pardir` #返回当前目录的父目录('..')
 - `os.makedirs()` #递归创建目录
 - `os.removedirs()` #递归删除目录
 - `os.mkdir()` #创建单级目录
 - `os.rmdir()` #删除单级目录
 - `os.listdir()` #列出指定目录下的所有文件和子目录
 - `os.remove()` #删除一个文件
 - `os.rename()` #重命名文件/目录
 - `os.stat()` #获取文件/目录信息
 - `os.sep` #操作系统特定的路径分隔符
 - `os.linesep` #操作系统特定的行分割符
 - `os.pathsep` #操作系统特定的分割文件路径的字符串
 - `os.name` #输出字符串指示当前使用平台
 - `os.system()` #运行shell命令
 - `os.environ` #获取系统环境变量
 - `os.path.split()` #将path分割成目录和文件名的元祖
 - `os.path.abspath` #返回绝对路径
 - `os.path.dirname` #返回path的目录
 - `os.path.basename` #返回path最后的文件名
 - `os.path.exists()` #判断path是否存在
 - `os.path.isabs()` #判断path是否是绝对路径
 - `os.path.isfile()` #判断路径是否是文件
 - `os.path.isdir()` #判断路径是否是目录
 - `os.path.join()` #将多个路径组合后返回
 - `os.path.getatime()` #获取路径的最后访问时间
 - `os.path.getmtime()` #获取路径的最后修改时间

4、`sys`

 - sys.argv #命令行参数，第一个元素是程序本身
 - sys.exit() #退出程序
 - sys.version #获取python解释程序的版本信息
 - sys.maxint #最大的int值
 - sys.path #模块搜索路径,初始化时使用PYTHONPATH环境变量的值
 - sys.platform #返回操作系统平台名称
 - sys.stdin #标准输入
 - sys.stdout #标准输出
 - sys.stderr #标准错误

5、`json`

 - `json.loads` # 将一个json字符串转为python对象
 - `json.dumps` # 将一个python对象转为json字符串
 - `json.load` # 从文件中将json数据转为python对象
 - `json.dump` # 将python对象转为json格式并持久化到一个文件中

6、`pickle`
 - `pickle.loads` # 将一个pickle字符串转为python对象
 - `pickle.dumps` # 将一个python对象转为pickle字符串
 - `pickle.load` # 从文件中将pickle数据转为python对象
 - `pickle.dump` # 将python对象转为pickle格式并持久化到一个文件中
 
7、`shelve`

 - `shelve.open` #打开一个持久化存储的字典(会生成三个文本)

8、`xml`
导入xml模块`import xml.etree.ElementTree as ET`，

    1. 解析
    tree = ET.parse(file_name)
    2. 获取根节点
    root_node = tree.getroot()
    3. 属性和方法
    root_node.tag #标签名
    root_node.attrib #属性字典
    root_node.text #获取节点文本
    root_node.set(key, value) #设置属性值
    root_node.write(file_name) #将xml内容写至文件
    root_node.findall(node_name) #查找节点
    root_node.remove(node) #移除节点
    4. 遍历节点
    for sub_node in root_node:
        print sub_node
    #只遍历指定名称的节点    
    for sub_node in root_node.iter("node_name"):
        print sub_node
    5. 创建一个xml文档
    root = ET.Element("node_name") #根元素
    ET.SubElement(root, "node_name") # 子元素
    et = ET.ElementTree(root) # 文档对象
    et.write(file_name) #保存文档对象
    ET.dump(root) #打印生成的格式

9、`re`

元字符

 - `.` 匹配除了`\n`之外的所有单字符
 - `^` 匹配以内容开头
 - `$` 匹配以内容结尾
 - `*` 匹配任意个前面的字符
 - `+` 匹配至少1个前面的字符
 - `?` 匹配0个或1个前面的字符
 - `{n}` 匹配n个前面的字符
 - `{n,m}` 匹配至少n个，至多m个
 - `[]` 匹配中括号字符集中的一个，`-`表示范围，`^`表示字符集取反，`\`表示转义，其它字符均原样匹配
 - `[^]` 匹配中括号字符集外的一个
 - `\` 对特殊的元字符进行转义
 - `pattern|pattern` 模式1或模式2
 - `()` 模式分组
 - `(pattern)` 普通分组
 - `(?P<name>pattern)` 名称分组
 - `(?:pattern)` 去掉分组优先级，默认按照分组匹配并返回结果
 
特殊字符集
 - `\d` 匹配任何十进制数
 - `\D` 匹配任何非数字字符
 - `\s` 匹配任何空白字符，包括`\t\n\r\f\v`
 - `\S` 匹配任何非空白字符
 - `\w` 匹配任何字母数字字符
 - `\W` 匹配任何非字母数字字符
 - `\b` 匹配一个特殊字符边界
 - r'' 原生字符串，不对字符串里面的内容进行转义
 
re模块的常用方法
 - `re.findall` 在字符串中按照模式进行查找，会查找全部
 - `re.search` 在字符串中按照模式进行查找，找到即返回
 - `re.match` 在字符串中按照模式进行查找，只匹配开头
 - `re.split` 对字符串按照模式进行分割
 - `re.sub` 对字符串用指定模式进行替换
 - `re.subn` 对字符串用指定模式进行替换,返回匹配后内容和匹配次数的元祖
 - `re.compile` 将模式编译为类型对象
 - `finditer` 同findall，返回一个迭代器
 
    
10、`logging`

日志级别:
debug < info < warning < error < critical

> 默认级别为warning

日志配置

    logging.basicConfig(
        level, #日志级别
        filename, #日志文件名
        filemode, #日志打印模式
        datefmt, #日期格式
        format, #日志格式
        
    )
    
    format格式化字符串：
        %(levelno)s: 打印日志级别的数值
        %(levelname)s: 打印日志级别名称
        %(pathname)s: 打印当前执行程序的路径，其实就是sys.argv[0]
        %(filename)s: 打印当前执行程序名
        %(funcName)s: 打印日志的当前函数
        %(lineno)d: 打印日志的当前行号
        %(asctime)s: 打印日志的时间
        %(thread)d: 打印线程ID
        %(threadName)s: 打印线程名称
        %(process)d: 打印进程ID
        %(message)s: 打印日志信息

logger方式打印日志        
    #生成logger对象,默认是root
    logger = logging.getLogger() 
    #设置logger级别
    logger.setLevel()
    #设置打印格式
    fm=logging.Formatter(formatter)
    #设置输出文件打印
    f=logging.FileHandler()
    #设置屏幕输出打印
    s=logging.StreamHandler()
    #配置格式
    f.setFormatter(fm)
    s.setFormatter(fm)
    #将打印句柄添加到logger
    logger.addHandler(f)
    logger.addHandler(s)
    
    #打印日志
    logger.info()
    logger.warning()
    logger.error()
    logger.debug()
    
> 如果一个子logger对象打印，同时父对象也进行了打印，则子对象会将父对象同时打印    

11、configparser

    #ini配置文件格式
    [section1]
    key1=value1
    key2=value2
    key3=value3
    key4=value4
    
操作配置文件
    #创建一个config对象
    cfg=configparse.ConfigParser()
    #读取配置文件
    cfg.read()
    #配置
    cfg['section'] = {key1:value1, key2:value2}
    #写入文件
    cfg.write(fh)
    #常用方法
    cfg.sections() #所有的section
    cfg.items() #某个section的所有配置项
    cfg.get() #获取某个section某配置项的值
    cfg.add_section() #添加一个section
    cfg.remove_section() #移除一个section
    cfg.remove_option() #从某个section中移除一个配置项
    cfg.set() #在某个section中添加一个配置项
    

12、`hashlib`

 - `hashlib.md5()` md5算法
 - `hashlib.sha1()` sha1算法
 - `hashlib.sha256()` sha256算法
 
加密过程
    1. 选择算法
    md5 = hashlib.md5() #可以设定特定的秘钥
    2. 更新
    md5.update()
    3. 生成md5值
    md5.hexdigest()


#### python 包
用来组织python的模块，是一个带钩子(`__init__.py`)的文件夹

`__init__.py`: 


#### python 面向对象编程
**类**:类是一个抽象的概念，是把一类具有相同特征和方法的事物整合在一起
**对象**:基于类而创建的一个具体的事物

    class ClassName(object):
        def __init__(self, *args, **kwargs):
            #初始化
        def method(self):
            #函数体
    
day24-03

  [1]: http://chuantu.biz/t6/354/1533745102x-1376440240.png
  [2]: https://s15.postimg.cc/enh7t3f9n/image.png
  [3]: https://s15.postimg.cc/xtuevsirf/image.png

# 内容1

## 使用anaconda搭建python的环境（跳过第一章，去网络上搜索anaconda3的教程）

conda安装：http://www.anaconda.com/download/  

根据自己的操作系统，下载安装。  

### **Conda环境管理**  

**列举环境**：conda info --envs  

**创建环境**: conda create -n py27 python=2.7.12  

**环境切换**：activate env_name  

**退出环境**: deactivte env_name  

### **Conda包管理**  

**安装anaconda发行版中所有的包:**

conda install anaconda  

**为某个环境安装包:**

conda install -n env_name jupyter  

**查看已经安装的package:**

conda list  

**指定查看某环境下安装的package:**

conda list -n env_name  

**查找包:** 

conda search numpy  

**更新包:**  

conda update matplotlib  

conda update anaconda  

**卸载包:**  

conda remove numpy

## 完成系统变量的设置，通过在命令行输入python3检验一下python3有没有装成功。

test：  win+R ---> cmd ---> python3

## 解释什么是变量，变量命名规则。

**什么是变量**：变量的概念基本上和初中代数的方程变量是一致的，只是在计算机程序中，变量不仅可以是数字，还可以是任意数据类型。  
**变量命名规则**：  
（1）变量名只能包含字母、 数字和下划线。 变量名可以字母或下划线打头， 但不能以数字打头， 例如， 可将变量命名为message_1， 但不能将其命名为1_message。  
（2）变量名不能包含空格， 但可使用下划线来分隔其中的单词。 例如， 变量名greeting_message可行， 但变量名greeting message会引发错误。  
（3）不要将Python关键字和函数名用作变量名， 即不要使用Python保留用于特殊用途的单词。python中的保留字可以通过以下方法查询：
```python
import keyword
print(keyword.kwlist)
```
（4）变量名应既简短又具有描述性。 例如， name比n好， student_name比s_n好， name_length比length_of_persons_name好。  
（5）慎用小写字母l和大写字母O， 因为它们可能被人错看成数字1和0。  
最近在网上看到一个很好的查变量命名的网站：https://unbug.github.io/codelf/  


## 了解字符串这一数据类型，通过书和搜索整理字符串的方法，包括大小写的转换，合并字符串，删除空白等（strip()）(第二章)


```python
MyStr = 'hello, my name is Leeway'
#首字母大写
print(MyStr.title()) # Hello, My Name Is Leeway
#字符串改为全部大写
print(MyStr.upper()) #HELLO, MY NAME IS LEEWAY
#字符串改为全部小写
print(MyStr.lower()) #hello, my name is leeway
#拼接字符串
last_name = 'Hou'
MyStr += ' ' + last_name
print(MyStr)
#在字符串中添加换行符
print('hello,\nmy\nname\nis\nLeeway')
#换到下一行， 并在下一行开头添加一个制表符
print('hello,\n\tmy\n\tname\n\tis\n\thLeeway')
#删除字符串开头与末尾多余的空白
MyStr =  '     ' + MyStr + '     '
print(MyStr)
print(MyStr.strip())

```

    Hello, My Name Is Leeway
    HELLO, MY NAME IS LEEWAY
    hello, my name is leeway
    hello, my name is Leeway Hou
    hello,
    my
    name
    is
    Leeway
    hello,
    	my
    	name
    	is
    	hLeeway
         hello, my name is Leeway Hou     
    hello, my name is Leeway Hou
    

## 了解基本的转义字符和格式化字符，并整理成文字或者代码。(第二章)


```python
'''字符串格式化
      %c	 格式化字符及其ASCII码  
      %s	 格式化字符串
      %d	 格式化整数
      %u	 格式化无符号整型
      %o	 格式化无符号八进制数
      %x	 格式化无符号十六进制数
      %X	 格式化无符号十六进制数（大写）
      %f	 格式化浮点数字，可指定小数点后的精度
      %e	 用科学计数法格式化浮点数
      %E	 作用同%e，用科学计数法格式化浮点数
      %g	 根据值的大小决定使用%f活%e
      %G	 作用同%g，根据值的大小决定使用%f活%e
      %p	 用十六进制数格式化变量的地址
'''
print('%c %c %c' % (97,98,99))  #a b c
print('%s' % '3+2') # 3+2
print('%d' % 5.321) # 5
print('%o' % 10) # 12
n = 10
print('My print is %d' % n)
print('My print is %r' % n) #如果我们并不知道自己要打印的是什么类型的信息，这时可以用%r来表示

'''转义字符
      \'	  单引号
      \"	  双引号
      \a	  发出系统响铃声
      \b	  退格符
      \n	  换行符
      \t	  横向制表符
      \v	  纵向制表符
      \r	  回车符
      \f	  换页符
      \o	  八进制数代表的字符
      \x	  十六进制数代表的字符
      \000	  终止符，\000后的字符串全部忽略

'''

```

    a b c
    3+2
    5
    12
    My print is 10
    My print is 10
    

## 了解数字类型，整数和浮点数。(第二章)


```python
# 整数
print(2+3)
print(3-2)
print(3*4)
print(3/2)
print(3**2)
print(3**4)
print(3-2*5)
#浮点数
print(0.1+0.1)
print(0.1*3) #0.30000000000000004 暂时忽略多余的小数位数即可
```

    5
    1
    12
    1.5
    9
    81
    -7
    0.2
    0.30000000000000004
    

## 如何添加注释(第二章)


```python
# 注释用井号（# ） 标识
'''
多行注释
'''
```




    '\n多行注释\n'



# 内容2

## 了解列表数据类型。(第三章)


```python
LuckyNum = [1,4,5,9,'None']
print(LuckyNum)   #[1, 4, 5, 9]
print(LuckyNum[2])  #5
print(LuckyNum[4].lower()) #none
print(list("hello")) #将字符串转换为列表
```

    [1, 4, 5, 9, 'None']
    5
    none
    

## 完成列表的增删查改（增加，删除，查找，修改）。


```python
LuckyNum = [1,4,5,9,'None']

#增
LuckyNum.append('10')   #将元素附加到列表末尾
print(LuckyNum) #[1, 4, 5, 9, 'None', '10']
LuckyNum.insert(1,3)  #在列表的任何位置添加新元素
print(LuckyNum) #[1, 3, 4, 5, 9, 'None', '10']

#删
del LuckyNum[0]    #根据索引删除任何位置处的列表元素
print(LuckyNum)   #[3, 4, 5, 9, 'None', '10']
poped_Num = LuckyNum.pop()  #删除列表末尾的元素， 并让你能够接着使用它
print(LuckyNum)    #[3, 4, 5, 9, 'None']
print(poped_Num)   #'10'
LuckyNum.pop(0)   #使用pop() 来删除列表中任何位置的元素， 只需在括号中指定要删除的元素的索引即可
print(LuckyNum)   #[4, 5, 9, 'None']
LuckyNum.remove(4)   #根据值删除元素 且只删除第一个指定的值
print(LuckyNum)  #[5, 9, 'None']

#查
#四种方式：in、not in、count、index前两种方法是保留字，后两种方式是列表的方法。
a_list = ['a','b','c','hello']
print('a' in a_list)   #True
print('a' not in a_list) #False
print(a_list.count('a')) #1
print(a_list.index('a'))  #0

#改
x = [1,2,3,4,5]
x[1]=0
print(x)  #[1, 0, 3, 4, 5]
```

    [1, 4, 5, 9, 'None', '10']
    [1, 3, 4, 5, 9, 'None', '10']
    [3, 4, 5, 9, 'None', '10']
    [3, 4, 5, 9, 'None']
    10
    [4, 5, 9, 'None']
    [5, 9, 'None']
    True
    False
    1
    0
    [1, 0, 3, 4, 5]
    

## 了解列表的排序，比较sorted和sort两个函数。(第三章)


```python
NewList = [1,4,2,7,3,6,2,9,12,66,24]
print(sorted(NewList))  #调用函数sorted() 后， 列表元素的排列顺序并没有变
print(NewList)  #[1, 4, 2, 7, 3, 6, 2, 9, 12, 66, 24]
NewList.sort()   #永久性地修改了列表元素的排列顺序
print(NewList) 
```

    [1, 2, 2, 3, 4, 6, 7, 9, 12, 24, 66]
    [1, 4, 2, 7, 3, 6, 2, 9, 12, 66, 24]
    [1, 2, 2, 3, 4, 6, 7, 9, 12, 24, 66]
    

## 了解列表的方法，sort(),reverse()等。(附加题：了解sort()函数里的key参数，并实现一个列表的排序[[“a”,1],[“b”,0],[“c”,3]],要求变成[[“b”,0],[“a”,1],[“c”,3]])。(第三章)


```python
NewList = [1,4,2,7,3,6,2,9,12,66,24]
NewList.sort() 
print(NewList)   #[1, 2, 2, 3, 4, 6, 7, 9, 12, 24, 66]
NewList.reverse()   # 永久性地修改列表元素的排列顺序
print(NewList)  #[66, 24, 12, 9, 7, 6, 4, 3, 2, 2, 1]
print(len(NewList))  #11   列表的长度
print("This is a test string from Leeway".split())   #['This', 'is', 'a', 'test', 'string', 'from', 'Leeway']

# key：用列表元素的某个属性或函数进行作为关键字，有默认值，迭代集合中的一项;
# sort(key=None, reverse=False)
L = [["a",1],["b",0],["c",3]]
L.sort(key = lambda x:x[1])
print(L)    #[['b', 0], ['a', 1], ['c', 3]]
'''
在排序之前，Lt里的所有元素都会执行key的函数，这里指的就是lambda函数，
计算出值之后，赋值给key，然后sort()是针对key进行排序，然后再根据这个key对应的值替换到排好序的L里。
'''
```

    [1, 2, 2, 3, 4, 6, 7, 9, 12, 24, 66]
    [66, 24, 12, 9, 7, 6, 4, 3, 2, 2, 1]
    11
    ['This', 'is', 'a', 'test', 'string', 'from', 'Leeway']
    [['b', 0], ['a', 1], ['c', 3]]
    

## 了解循环，实现简单的遍历列表


```python
Colors = ['red','pink','green','blue']
for i in Colors:
    print(i)
```

    red
    pink
    green
    blue
    

## 了解range函数，并实现创建列表，解析列表。(第四章)


```python
# range() 可以生成一系列的数字
for i in range(1,5):   #前闭后开
    print(i)   
    
print(list(range(1,6)))   #[1, 2, 3, 4, 5]
print(list(range(2,11,2)))  #[2, 4, 6, 8, 10]

#使用函数range() 几乎能够创建任何需要的数字集
squares = []
for value in range(1,11):
    square = value**2
    squares.append(square)
print(squares)    #[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
print(max(squares)) #100
print(min(squares))  #1
print(sum(squares))  #385

#前面介绍的生成列表squares 的方式包含三四行代码， 而列表解析让你只需编写一行代码就能生成这样的列表。 
squares = [value**2 for value in range(1,11)]
print(squares)  #[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

    1
    2
    3
    4
    [1, 2, 3, 4, 5]
    [2, 4, 6, 8, 10]
    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    100
    1
    385
    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
    

## 了解切片并使用切片。(第四章)


```python
squares = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
print(squares[0:3])  #[1, 4, 9]
print(squares[1:4]) #[4, 9, 16]
print(squares[:4]) #[1, 4, 9, 16]
print(squares[4:]) #[25, 36, 49, 64, 81, 100]
print(squares[-4:]) #[49, 64, 81, 100]
```

    [1, 4, 9]
    [4, 9, 16]
    [1, 4, 9, 16]
    [25, 36, 49, 64, 81, 100]
    [49, 64, 81, 100]
    


```python

```

# Python

Version: 3.9.4

[官网](https://www.python.org/)

[下载](https://www.python.org/downloads/)

[文档](https://docs.python.org/3/)

## 安装

### Windows

### Linux

1. 源码安装
    - `wegt https://www.python.org/ftp/python/version/Python-version.tgz` **version**:对应版本
    - `tar xzvf Python-version.tgz` **version**:对应版本
    - 安装依赖，[文档地址](https://devguide.python.org/setup/#install-dependencies)
    - `sudo apt-get build-dep python3.9`
    - `./configure --enable-optimizations --prefix=/home/user/Desktop/Environment/Python`
    - `nproc`
    - `make -j4`
    - `make install`
    - `sudo ln -s ~/Desktop/Environment/Python/bin/python3 /usr/bin/python`
    - `sudo ln -s ~/Desktop/Environment/Python/bin/pip3 /usr/bin/pip`

### Mac

## PIP

1. 修改阿里源
    - windows系统,路径: `%HOMEPATH%/pip/pip.ini`
    - Linux系统: `vim ~/.pip/pip.conf`

```ini
[global]
index-url = https://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
```

2. 安装包
    - `pip install package`: 最新版本
    - `pip install package==version`: 指定版本
    - `pip install package>=version`: 最小版本

3. 升级包
    - `pip install --upgrade package`

4. 搜索包
    - `pip search package`

5. 卸载
    - `pip uninstall package`

6. 依赖包
    - `pip freeze > requirement.txt`: 导出
    - `pip install -r requirement.txt`: 导入

## IDE

### Pycharm

[下载](https://www.jetbrains.com/pycharm/download/)

#### 重置插件

插件仓库地址:https://plugins.zhile.io

插件: IDE Eval Reset

## 基本语法和使用

### 变量

命名规范：字母，数字，下划线,不能以数字开头

### 数据类型

1. 数字
    - int
    - float
    - complex

2. 字符串(str)

3. 布尔(True、False)

4. 列表(list)

5. 元组(set)
   - 元组是不可修改的，元组用”()”标识，内部元素用逗号隔开,只有一个元素时后面需要","

6. 字典(dict)

7. 集合(set)
   - 无序
   - 不重复

### 注释

1. 单行注释

```python
# 单行注释
```

2. 多行注释

```python
"""
多行注释
"""
```

## 字符串

### 基础用法

### 方法

#### title()

单词首字母大写，以空格分割

```python
message = "hello world"
print(message)
print(message.title())
```

#### upper()

字符串大写

```python
message = "hello world"
print(message)
print(message.upper())
```

#### lower()

字符串小写

```python
message = "HELLO WORLD"
print(message)
print(message.lower())
```

#### rstrip()

删除右边空格

```python
message = "hello world "
print(message)
print(message.rstrip())
```

#### lstrip()

删除左边的空格

```python
message = " hello world"
print(message)
print(message.lstrip())
```

#### strip()

删除两边的空格

```python
message = " hello world "
print(message)
print(message.strip())
```

## 数字

### 基础用法

### 方法

## 列表

### 基本用法

#### 创建

用 []表示列表

```python
messages = [0, 1, 2, 3, 4, 5]
```

#### 访问

通过元素索引访问元素值

```python
messages = [0, 1, 2, 3, 4, 5]
print(messages[0])
print(messages[1])
print(messages[2])
print(messages[-1])
```

#### 修改

通过元素索引修改元素值

```python
messages = [0, 1, 2, 3, 4, 5]
messages[0] = 10
print(messages)
```

#### 遍历

循环遍历列表元素

```python
messages = [0, 1, 2, 3, 4, 5]
for i in messages:
    print(messages)
```

#### 创建数字列表

使用range()、list()函数创建

```python
messages = list(range(10))
print(messages)
```

列表推导式

```python
messages = [i for i in range(0, 10, 1)]
print(messages)
```

#### 切片

切片[**起始索引**:**结束索引**:**步长**​]

```python
messages = list(range(10))
print(messages[0:2:1])
```

#### 复制

使用切片复制列表

```python
messages = [0, 1, 2, 3, 4, 5]
list1 = messages[:]
list2 = messages[:]
print(messages)
print(list1)
print(list2)
messages.append(6)
list1.append(7)
list2.append(8)
print(messages)
print(list1)
print(list2)
```

### 方法

#### append()

在列表尾部添加元素

```python
messages = [0, 1, 2, 3, 4, 5]
print(messages)
messages.append(6)
print(messages)
```

#### insert()

在指定索引位置插入元素

```python
messages = [0, 1, 2, 3, 4, 5]
print(messages)
messages.insert(1, 6)
print(messages)
```

#### pop()

未指定元素索引，从列表尾部删除元素并返回该元素

```python
messages = [0, 1, 2, 3, 4, 5]
print(messages)
print(messages.pop())
print(messages)
```

指定元素索引，从列表中删除该元素并返回

```python
messages = [0, 1, 2, 3, 4, 5]
print(messages)
print(messages.pop(3))
print(messages)
```

#### del()

删除指定索引元素，如未指定索引，则删除整个列表

```python
messages = [0, 1, 2, 3, 3, 4, 5]
print(messages)
del messages[1]
print(messages)
del messages
```

#### remove()

删除指定值元素,有多个相同元素时只删除第一个指定值

```python
messages = [0, 1, 2, 3, 3, 4, 5]
print(messages)
messages.remove(3)
print(messages)
```

#### sort()

永久排序列表，修改原列表

reverse=True为倒序

```python
messages = [4, 1, 2, 0, 3, 5]
print(messages)
messages.sort(reverse=False)
print(messages)
```

#### sorted()

临时排序列表，不修改原列表

reverse=True为倒序

```python
messages = [4, 1, 2, 0, 3, 5]
print(messages)
print(sorted(messages, reverse=False))
print(messages)
```

#### reverse()

反转列表,永久修改列表

```python
messages = [0, 1, 2, 3, 4, 5]
print(messages)
messages.reverse()
print(messages)
```

#### index()

获取对应元素第一次出现的索引值

```python
messages = [0, 1, 1, 2, 3, 4, 5]
messages.index(2)
```

extend()

合并列表

```python
messages = [0, 1, 2, 3, 4, 5]
messages.extend([6, 7, 8, 9, 10])
```

count()

统计对应元素值出现的次数

```python
messages = [0, 1, 1, 2, 3, 4, 5]
messages.count(1)
```

#### len()

获取列表长度

```python
messages = [0, 1, 2, 3, 4, 5]
print(len(messages))
```

#### max()

数字列表中的最大值

```python
messages = [0, 1, 2, 3, 4, 5]
print(max(messages))
```

#### min()

数字列表中的最小值

```python
messages = [0, 1, 2, 3, 4, 5]
print(min(messages))
```

#### sum()

对数字列表求和

```python
messages = [0, 1, 2, 3, 4, 5]
print(sum(messages))
```

## 元组

### 基本用法

#### 创建

使用()表示元组，只有一个元素时，该元素后必须有,

```python
messages = (0,)
```

#### 访问

```

```

#### 元组定义后不能修改

### 方法

## 字典

## 集合

## 函数

## 类

基本用法

```python
class Person(object):
    count = 0
    flag = None

    def __init__(self):
        self.name = '类的属性'

    def __str__(self):
        return self.name
```

## 输入

## 输出

## 条件

## 循环

## 异常

## 文件

## 测试

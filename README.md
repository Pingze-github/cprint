# cprint
A Python package for formatting output of complex data structures. Work well with un-English.

一个Python包，用于格式化输出复杂数据结构（元组、集合、列表、字典及其嵌套）。尤其用于显示中文。

## Installation
EN: Just put the "cprint.py" into your dir ".../Python/Lib", or in your project.

ZH:将“cprint.py”放入Python安装目录".../Python/Lib"，或者项目文件夹中。

## Usage
```
from cprint import cprint
cprint(obj1)
```
## Features
EN:
1. Use indentation to show the structure of object.
2. Print coded character as its character instead of its code.
ZH:
1. 使用缩进来表现对象的组成结构。
2. 打印编码字符（Unicode/UTF-8/GBK）时，打印可读的字符，而非字符编码。

## Example
#### Test Code
```
obj1 = {
    'data':[
        {
        'data_id':'1',
        'content':'西红柿'
        },
        {
        'data_id':'2',
        'content':'胡萝卜'
        }
    ],
    'name':'蔬菜',
    'id':1,
}
print(obj1)
print('\n')
from pprint import pprint
pprint(obj1)
print('\n')
from cprint import cprint
cprint(obj1)
```
#### Output
```
{'data': [{'content': '\xe8\xa5\xbf\xe7\xba\xa2\xe6\x9f\xbf', 'data_id': '1'}, {'content': '\xe8\x83\xa1\xe8\x90\x9d\xe5\x8d\x9c', 'data_id': '2'}], 'name': '\xe8\x94\xac\xe8\x8f\x9c', 'id': 1}

{'data': [{'content': '\xe8\xa5\xbf\xe7\xba\xa2\xe6\x9f\xbf', 'data_id': '1'},
          {'content': '\xe8\x83\xa1\xe8\x90\x9d\xe5\x8d\x9c', 'data_id': '2'}],
 'id': 1,
 'name': '\xe8\x94\xac\xe8\x8f\x9c'}

{
    data: [
        {
            content: 西红柿,
            data_id: 1
        },
        {
            content: 胡萝卜,
            data_id: 2
        }
    ],
    name: 蔬菜,
    id: 1
}
```
```

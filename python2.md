lambda
```
python
mult3 = filter(lambda x: x % 3 == 0, [1, 2, 3, 4, 5, 6, 7, 8, 9])
```
>sets mult3 to [3, 6, 9], those elements of the original list that are multiples of 3. This is shorter (and, one could argue, clearer) than
```
def filterfunc(x):
    return x % 3 == 0
mult3 = filter(filterfunc, [1, 2, 3, 4, 5, 6, 7, 8, 9])
```
>same in list comprehension
```
mult3 = [x for x in [1, 2, 3, 4, 5, 6, 7, 8, 9] if x % 3 == 0]
```
>执行语句from M import *会将M中定义的所有对象绑定到当前作用域，而不是M本身

>程序使用完文件后，请一定记得关闭文件，否则写入的内容可能部分或全部丢失。

>open(fn, 'w')：fn是一个表示文件名的字符串。创建一个文件用来写入数据，返回文件句柄。

>open(fn, 'r')：fn是一个表示文件名的字符串。打开一个已有文件读取数据，返回文件句柄。

>open(fn, 'a')：fn是一个表示文件名的字符串。打开一个已有文件用来追加数据，返回文件句柄。

>fh.read()：返回一个字符串，其中包含与文件句柄fh相关的文件中的内容。

>fh.readline()：返回与文件句柄fh相关的文件中的下一行。

>fh.readlines()：返回一个列表，列表中的每个元素都是与文件句柄fh相关的文件中的一行。

>fh.write(s)：将字符串s写入与文件句柄fh相关的文件末尾。

>fh.writeLines(S)：S是个字符串序列。将S中的每个元素作为一个单独的行写入与文件句柄fh相关的文件。

>fh.close()：关闭与文件句柄fh相关的文件。

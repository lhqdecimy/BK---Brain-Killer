## BK - Brain Killer
这是一个类似brainfuck的编程语言。

这个语言解释器的核心是一个长度为65536（2^16），单位为字节的初始化为0的数组和一个指向数组开头的指针，以及一个用来保存指针值的栈。

基本语法：
- +：将指针指向的字节加1。
- -：将当前字节减1。
- ,: 从标准输入中读取一个字符到当前字节。
- .：从标准输出中写入当前字节。
- <: 将指针向左移动一个字节。
- \>：将指针向右移动一个字节。
- =: 将指针的地址设为当前4个字节所表示的地址。
- []：while循环，循环条件是当前字节。
- ()：if语句， 条件是当前字节。
- {: 将当前指针压入栈中，保存指针值。
- }: 将栈中的值弹出，改变指针的值。

另外，输入数字，代表执行后面的+-><那么多遍。

示例代码：

输入两个数，输出和：
```
,48->,[-<+>]<.[-]
```
这里的48是'0'的字符编码

运行结果：
```
输入 12
输出 3
```

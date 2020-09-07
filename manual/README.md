# SeaTable 脚本编程手册

SeaTable 脚本使用 Javascript 语言编写。一个脚本一般用于表格中数据的处理。脚本可以在用户的浏览器中或者后台运行。(目前仅支持在用户的浏览器中运行)

脚本执行器提供了几个对象供你使用:

1. base 对象。通过 base 对象可以操作表格中的数据。
2. output 对象。用于输出结果。

SeaTable 脚本中用到的一些对象的数据结构:

* [数据结构](data-structure.md)

编程参考:

* [base](base.md)
* [output](output.md)
* [utilities](utils.md)

## 例子

可以通过这个链接找到一些容易理解的例子[https://github.com/seatable/seatable-scripts-cn/tree/master/examples](https://github.com/seatable/seatable-scripts/tree/master/examples)

具体如下

* [get-incremental.js](https://github.com/seatable/seatable-scripts/tree/master/examples/get-incremental.js): 从一个累计列计算出增量数据
* [auto-add-rows.js](https://github.com/seatable/seatable-scripts/tree/master/examples/auto-add-rows.js): 自动往一个记账表中添加每月重复的项目。
- 1、**将c 语言文件编译成exec可执行文件,直接将生成的可执行文件拖入终端回车即可执行**

```
clang -o abc abc.c //-o abc 的意思是指定输出的可执行文件是abc
或者
clang abc.c // 不指定输出文件，会默认生成一个 a.out 可执行文件

```

- 2、**将c 文件编译生成 .o 目标文件**
```
clang -c -o 输出文件名 abc.c // -c 的意思是编译成 .o 文件，-o 输出文件名 是指定 .o 输出文件名
或者
clang -c abc.c // 不指定输出，默认会生成和 .c 同名的 .o 文件
```

- 3、**查看文件类型**
```
file name // 查看指定文件的类型
```

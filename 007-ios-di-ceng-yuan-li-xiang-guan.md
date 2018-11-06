##一、 1个NSObject 对象占用多少内存？

####1、 Objective-c 的本质

我们平时写的Objective-c 代码，底层实现其实都是C\C++ 代码的.
![](/assets/oc代码本质.png)

所以Objective-c 的面向对象都是基于C\C++ 的数据结构实现的.

<br>
**思考:**
Objectic-c 的对象\类主要是基于C\C++ 的什么数据结构事项的呢?<br>
**答案:**
结构体



---
<br>
<br>



####2、 将我们编写的OC的代码转换成C\C++ 语言

将我们平时编写的Objective-c 文件转换成C\C++语言的文件,主要要用到Clang 编译器.

```
cd   xxx.main.m     // 切换到 main.m 所在文件路径
clang -rewrite-objc main.m main.cpp // 将main.m(oc文件) 转换为C++ 文件(main.cpp)
```
为什么我们不将OC的代码直接转换成C语言的文件呢? 因为OC是由C\C++共通实现的,因此里面有C和C++是实现的代码, 而且C++ 是兼容C的,因此我们将OC的文件直接转换成C++的文件



<br>
虽然上面的命令可以将OC的代码转换成C++的文件, 但是不推荐这样用, 应为编译器将OC代码装换成C++语言的文件时还是要看平台的, 不同的平台, 转换出来的C++文件其实是由差异的, 即不同平台支持的C++代码是由差异的, 比如: windows\ MAC \ iOS , 特别是最终C++ 代码转换成对应平台的汇编语言时, 是由很大差异的.

**正确的做法:**

```
xcrun -sdk iphoneos clang -arch arm64 -rewrite-objc main.m -o main-arm64.cpp
//xcrun -sdk iphoneos 表示是指定 使用 Xcode 的 ios SDK  的方式
//clang -arch arm64 表示指定clang的arm64位编译器
```
![](/assets/Snip20181107_7.png)

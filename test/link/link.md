## 超链接

1. 行内形式

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.

[相对路径](../README.md)

2. 参考形式

[google][1]

[baidu][2]

[1]: https://www.google.com/
[2]: https://www.baidu.com/

3. 自动形式

<https://www.google.com/>

4. 页内跳转链接

>一篇很长的文章，要是没有目录的话。阅读起来十分不便。页内跳转就能很好的解决这个问题。

>[锚点链接实践](锚点链接.md)

>- [github上的一个md文件的目录](https://github.com/CyC2018/CS-Notes/blob/master/docs/notes/Java%20%E5%9F%BA%E7%A1%80.md)

[页面跳转test](#test)



999. 参考
>- <http://wow.kuapp.com/markdown/#link>
>- <https://www.jianshu.com/p/ab539e9a7955>


# test

* [一、数据类型](#一数据类型)
    * [基本类型](#基本类型)
    * [包装类型](#包装类型)
    * [缓存池](#缓存池)
* [二、String](#二string)
    * [概览](#概览)
   
* [三、运算](#三运算)



# 一、数据类型

## 基本类型

- byte/8
- char/16
- short/16
- int/32
- float/32
- long/64
- double/64
- boolean/\~

boolean 只有两个值：true、false，可以使用 1 bit 来存储，但是具体大小没有明确规定。JVM 会在编译时期将 boolean 类型的数据转换为 int，使用 1 来表示 true，0 表示 false。JVM 并不支持 boolean 数组，而是使用 byte 数组来表示 int 数组来表示。

- [Primitive Data Types](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)
- [The Java® Virtual Machine Specification](https://docs.oracle.com/javase/specs/jvms/se8/jvms8.pdf)

## 包装类型

基本类型都有对应的包装类型，基本类型与其对应的包装类型之间的赋值使用自动装箱与拆箱完成。

```java
Integer x = 2;     // 装箱
int y = x;         // 拆箱
```

## 缓存池

new Integer(123) 与 Integer.valueOf(123) 的区别在于：

- new Integer(123) 每次都会新建一个对象；
- Integer.valueOf(123) 会使用缓存池中的对象，多次调用会取得同一个对象的引用。


valueOf() 方法的实现比较简单，就是先判断值是否在缓存池中，如果在的话就直接返回缓存池的内容。

```java
public static Integer valueOf(int i) {
    if (i >= IntegerCache.low && i <= IntegerCache.high)
        return IntegerCache.cache[i + (-IntegerCache.low)];
    return new Integer(i);
}
```

# 二、string
## 概览

xxxxxxx

# 三、运算

# 1
abadfj
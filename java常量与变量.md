# java常量与变量
### 常量
#### 声明常量
语法格式：
>final 数据类型 常量名称[=常量值]

中括号中的内容可以没有  
常量名称通常使用大写字母，虽然java中有`const`，但是并没有正式使用。  
必须要对常量进行初始化，否则会编译错误。  
### 变量
#### 声明变量
声明一个变量时，编译程序会在内存单元里开辟一块足以容纳此变量的的内存空间给它。而内存空间的大小和数据类型有关，和变量值无关。  
#### 变量的作用域
* 成员变量：在类体中定义，作用域为整个类。
* 局部变量：在方法体或者代码块中定义，作用域为方法体内或者代码块内。
* java方法体中作用范围时禁止嵌套的，c++则可以。如以下代码是错误的：  

``` java
 public int fun(){
 int a;
 {
    int a;//即使是其他数据类型也是错的
 } 
}
```

而c++则没问题
``` c++
 int fun(){
 int a;
 {
    int a;
 } 
}
```
**但是**，java类与方法中变量作用域可以嵌套。注意是类与方法。如下：
``` java
public class StreamInTest {
    String str;
    public static void main(String[] args) {
        String str;//正确
    }
}
```
``` java
public class StreamInTest {
    String str;
    {
       String str;//错误 
    }
}
```
# java程序概述
* 如果将一个类声明为public，那么文件名称必须和此类名相同。
* 一个java文件中，至多只有一个public类。
* `public static void main(String args[])`是java程序的运行起点。main()方法前面必须加上pulic static void三个标识符。public代表公有方法，static代表是一个静态方法，也就是在创建类的对象时仍然可以使用，void代表函数返回值的类型为空，也就是没有返回值。
* 在c++中，在类之外的函数就叫`函数`，在类中的函数叫做`成员函数`，而不叫方法。
* 在java程序中，函数称作`方法`，不叫函数是因为方法和对象有关（除静态方法），一般不说`调用某个方法`而是`调用某对象的某方法`，而函数和对象无关。
* 在使用变量之前必须声明它的数据类型。
* System.out是指标准输出。
*  main方法不一定包含在public类中，比如用eclipse的话，把main写在一个不是公共类的类中，依然可以运行，只不过运行时得在运行配置中指定到这个程序，因为eclipse默认到public的类中去找main函数
*  在eclipse中，虽然没有共有类的时候也能输出，但是控制台会报错。
## java类、包、文件概念
在java项目中，存在大量的类，难免存在类的名称相同的情况，比如“矩形”和“三角形”工程中都可能有相同的面积类。为了解决此问题，便引入包的概念。将同名的类放在不同的包中，在调用类的时候加上包名，就可以区别同名的类。  
在Eclipse中，创建一个项目之后会默认在工程目录下创建一个src文件夹，创建类的时候如果填写了包名，则会在src下生成一个以包名为名称的文件夹，java文件放在此文件夹下  
在java中，一个java文件有且仅有一个公有（public）类及其他非公有类（可以没有）。
## java标识符
java的包，类，方法，参数，变量，常量的名称可由任意顺序的字母，数字，下划线，美元符号组成，但不能以数字开头，也不能时java的关键字。
## java关键字

    abstract class    extends implements null      strictfp     true
    assert   const    false   import     package   super        try
    boolean  continue final   instanceof private   switch       void
    break    default  finally int        protected synchronized volatile
    byte     do       float   interface  public    this         while
    case     double   for     long       return    throw
    catch    else     goto    native     short     throws
    char     enum     if      new        static    transient

## java注释
* 单行注释：`//注释内容`，eclipse快捷键`ctrl+/`注释本行
* 多行注释：`/*注释内容*/`,eclipse快捷键`ctrl+shift+/`注释所选区域，`alt+shift+j`添加注释。
## java变量
1.变量的声明
`数据类型 变量名=数值或表达式;`分号不能少。如：
0>int a=0;

2.声明多个变量并赋值
>int a=0,b=1,c=2;




## Java 组成与语法结构
### 类

- **程序的基本单位**
- 包含**共同特征实体**集合
---

### 主方法

```java
public static void main(String[] args)
{

}
```
---

### 关键字

| 关键字          | 说明           | 关键字          | 说明     |
| :----------- | :----------- | :----------- | :----- |
| abstract     |              | int          |        |
| assert       |              | interface    |        |
| **boolean**  |              | long         |        |
| **break**    | 提前跳出         | native       |        |
| **byte**     | 字节类型         | **new**      | 新建实例对象 |
| case         |              | **package**  |        |
| catch        |              | private      |        |
| **char**     | 字符类型         | protected    |        |
| **class**    | 声明类          | **public**   |        |
| const        |              | **return**   |        |
| **continue** | 回到开始处        | **short**    |        |
| default      |              | **static**   |        |
| do           |              | strictfp     |        |
| **double**   | 双精度浮点        | super        |        |
| **else**     |              | **switch**   | 分支     |
| enum         |              | synchronized |        |
| extends      |              | this         |        |
| **final**    | 不可改变最终属性（常量） | throw        |        |
| finally      |              | throws       |        |
| **for**      |              | transient    |        |
| goto         |              | **try**      |        |
| **if**       |              | **var**      | 局部变量   |
| implements   |              | **void**     |        |
| **import**   |              | **while**    |        |
| instanceof   |              |              |        |

---

### 标识符

- 为类、方法等内容指定的名称
- 由一个或多个字母数字下划线和 $ 组成，字符间无空格、可由几个单词组成
  ```java
a,B,Name,$table
```
- 类名的单词首字母大写
```java
Class ScienceFictionFilms
```
- 变量或者方法首个单词的字母小写，其余字母大写
```java
usrName
```
- 常量的所有字母大写，可以用_连接
- 第一个字符不可以是数字

---

### 注释

- 单行注释：//
- 多行注释：/**/
- 文档注释

```java
public class Main {  
    /**    主方法，程序的入口  
     * @param args-主方法参数  
     */  
    public static void main(String[] args)  
    {  
        System.out.println("Hello World");  
    }  
}
```

>[!warning]
>可读性第一，效率第二，**注释占代码总量的20%-50%**

---
文档注释的标签语法：

| 文档注释的标签  | 解释                        |
| -------- | ------------------------- |
| @version | 版本                        |
| @since   | 最早出现在那个版本                 |
| @author  | 作者                        |
| @see     | 参考其他说明文档的连接               |
| @link    | 参考其他的说明文档，可以嵌入注释为特殊词汇生成链接 |
| @param   | 描述方法的参数                   |
| @return  | 描述方法的返回值                  |
| @throws  | 描述方法的异常和抛出异常的条件           |

>[!tips]
>单行注释写在上方或右侧
>多行注释位置同上，但是最好不要写在代码里
>文档注释必须写在代码上方

---

## **变量与常量**

**声明**
- 向程序表明变量的类型和名称

### **变量**


>**声明变量**
- 数据类型 变量标识符;
- 数据类型 变量标识符1,变量标识符2 , ... , 变量标识符n
>**赋值**
- 数据类型 变量标识符 = 变量值;
- 数据类型 变量标识符1= 变量值1， 数据类型 变量标识符2= 变量值2;
- 数据类型 变量标识符1,变量标识符2；
  变量标识符1 = 变量值1；
  变量标识符2 = 变量值2；

### **常量**
>**声明**
- final 数据类型 常量标识符;
>**赋值**
-  final 数据类型 常量标识符 = 常量值;
- final 数据类型 常量标识符1 = 常量值1，final 数据类型 常量标识符2 = 常量值2;
- 如果已经对一个常量赋值，那么无法再修改这个常量的值。


## 输入和输出
### 输出字符
- print() -不会自动换行
  
```java
System.out.print("Hello");  
System.out.print("World");
/*输出结果为：
HelloWorld
*/
```

可以在后面加上“\n”实现换行

- print() -可以自动换行
  
```java
System.out.println("Hello");  
System.out.println("World");
/*输出结果为：
Hello
World
*/
```

- 格式化输出：printf()方法
```java
printf(String format, Object...args)
System.out.printf("120 + 132的结果是: %d\n",120+132);// 数字用转换符%d  
System.out.printf("pi取两位小数为：%.2f\n",3.141592653589793);// 小数用转换符%.xf(x代表保留几位小数)
/*输出结果为：
120 + 132的结果是: 252
pi取两位小数为：3.14
*/
```

### 控制台输入
- import
  导入本类所在包之外的类，包括项目里的包中的类
- 导入后可以调用
```java
import java.util.Date;  
import java.util.Scanner;  
import com.mr.util.ImageUtil;

import java.util.*;//一次性把包中所有类都导入
```

>[!warning]
>"*"只可以替代**类**名，不能替代**包**名。
>```java
>import java.awt.*;
>import java.awt.event.*;

---

- Scanner
```java
import java.util.Scanner;

```


| 方法名        | 返回类型   | 说明                        |
| ---------- | ------ | ------------------------- |
| next()     | String | 查找并返回这个Scanner类获取的下一个完整标记 |
| nextLine() | String | 扫描一个值并返回String类型          |
| close()    | void   | 关闭这个Scanner类              |
>[!tips]
>nextLine()扫描第一个字符到换行符的内容，next()、nextInt()扫描的是第一个字符开始到这段内容结束。

```java

```

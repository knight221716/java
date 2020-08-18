### 运算符

注意：

整数操作只能得到整数，要想得到小数，必须有浮点数参与运算。

```java
public class HelloWorld {
    public static void main (String[] args){
        int a = 10;
        int b = 3;
        System.out.println(a/b);  // 输出结果3
        System.out.println(a%b);  // 输出结果1
    }
}
```

byte类型，short类型和char类型将被提升到int类型，不管是否有其他类型参与运算

整个表达式的类型自动提升到与表达式中最高等级的操作数相同的类型

等级顺序：byte,short,char --> int --> long --> float --> double

##### tip

正是由于上述原因，所以在程序开发中我们很少使用byte或者short类型定义整数。也很少会使用char类型定义字符，而使用字符串类型，更不会使用char类型做算术运算。

### ++   --

```
public class HelloWorld {
    public static void main (String[] args){
        int x = 10;
        int y = x++;   // 赋值运算，++在后边，所以是使用x原来的值赋值给y，x本身自增1
        System.out.println("x:" + x + ", y:" + y);  // x:11，y:10
    }
}
```

```
public class HelloWorld {
    public static void main (String[] args){
        int m = 10;
        int n = ++m;   // 赋值运算，++在前边，所以是使用m自增后的值赋值给n，m本身自增1
        System.out.println("m:" + m + ", m:" + m); // m:11，m:11
    }
}
```

```
public class HelloWorld {
    public static void main (String[] args){
        int x = 10;
        int y = x++ + x++ + x++;
        System.out.println(y);
    }
}
```

### 逻辑运算符

与、或、异或、非

&    |    ^    !

短路与、短路或

$$    ||

逻辑与&，无论左边真假，右边都要执行。

短路与&&，如果左边为真，右边执行；如果左边为假，右边不执行。

逻辑或|，无论左边真假，右边都要执行。

短路或||，如果左边为假，右边执行；如果左边为真，右边不执行。

### 三元运算符

```
关系表达式 ? 表达式1 : 表达式2;
```

### 数据输入

```java
import java.util.Scanner;

public class HelloWorld {
    public static void main (String[] args){
        Scanner sc = new Scanner(System.in);  // 创建Scanner对象 sc 表示变量名，其他的都是不可变的
        int x = sc.nextInt();  // 表示将键盘录入的值作为int返回
        System.out.println("x:"+x);
    }
}
```

### if

```
if (关系表达式){
    语句体1
}else if(关系表达式){
    语句体2
}else{
    语句体3
}
```

```java
import java.util.Scanner;

public class HelloWorld{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入一个整数");
        int x = sc.nextInt();
        if (x%2==0){
            System.out.println("偶数");
        }else {
            System.out.println("奇数");
        }
    }
}
```
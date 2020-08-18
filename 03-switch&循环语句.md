### switch

```
switch (表达式){
    case 1:
        语句体1;
        break;
    case 2:
        语句体2;
        break;
    default:
        语句体;
        break;
}
```

### for

```java
public class HelloWorld{
    public static void main(String[] args){
//        输出0-5
        for (int i=0;i<=5;i++){
            System.out.println(i);
        }
//        输出5-0
        for (int i=5;i>=0;i--){
            System.out.println(i);
        }
    }
}
```

### for循环求和

```
public class HelloWorld{
    public static void main(String[] args){
        int sum = 0;
        for (int i=1;i<=100;i++){
            sum = sum+i;   // 求和
        }
        System.out.println(sum);
    }
}
```

### while循环

```
while (条件判断语句){
    循环体语句;
    条件控制语句;(i++);
}
```

### do while循环

```
do{
    循环体语句;
    条件控制语句;
}while(条件判断语句);
```

### 跳出循环

break跳出循环，结束循环

continue跳出本次循环，继续下次循环

### Random

```
import java.util.Random;

public class HelloWorld{
    public static void main(String[] args){
        Random r = new Random();
        System.out.println(r.nextInt(100));
    }
}
```
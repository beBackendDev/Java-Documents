# **Java Core** 

## About Java:
Phải download **Java Development Kit (JDK)** và phải có **Intergrated Development Enviroment (IDE)** 


## 1. Variable:
Biến được khai báo có thể có giá trị hoặc không có giá trị truyền vào:

`int username; //declare without value`

`String username = "dev Thoai"; //declare with value be assigned`

## 2. User input:
Java thực hiện lấy thông tin đầu vào của người dùng thông qua thư viện Scanner và nó thực hiện lấy giá trị thông qua các method như: `.nextLine(), .nextInt(), .nextDouble() ...`

example: 

<!-- Code minh họa--->
```
 import java.ulti.Scanner;//khai báo thư viện Scanner 

 Scanner scanner = new Scanner(System.in);//khởi tạo scanner

 String name;

 System.out.println("Vui lòng nhập tên của bạn");
 name = scanner.nextLine();
 System.out.println("Tên của bạn là: " + name);

 scanner.close(); 
```

## 3. Arithmetic:
Phép toán thông thường, tham khảo thêm: [Java Arithmetic Operators](https://www.geeksforgeeks.org/java/java-arithmetic-operators-with-examples/).

## 4. If Statements:
Thực hiện khối câu lệnh bên trong if nếu điều kiện if thỏa mãn
``` 
    if(condition){
        condition true
        //execute statements
    }   
    else{
        condition false
        //execute statements
    }
```

## 5. Random Number:
Thực hiện khởi tạo một số ngẫu nhiêu trong khoảng a- b;

example: 

```
import java.ulti.Random;

Random random = new Random();
int number ;
number = random.nextInt(); //thực hiện lấy số ngẫu nhiên từ -2 billion cho tới 2 billion
number1 = random.nextInt(a, b);// random trong khoảng từ a- b
```

## 6. Math class:
Một vài hàm có sẵn để tính toán như căn bậc 2, trị tuyệt đối, số Pi ... 

vd: `pow(), sqrt(), Pi, E, abs()`

Bạn có thể tham khảo thêm một số hàm toán học có sẵn tại [GeeksforGeeks](https://www.geeksforgeeks.org/java/java-math-class/).

## 7. Printf:
>    **printf()**  là phương thức được sử dụng cho format của ouput

Xem thêm tại đây: [format output](https://www.geeksforgeeks.org/java/formatted-output-in-java/)

## 8. Nested If Statements:
```
if(condition){
    if(condition){
//statement
    }
    else{
//statement

    }
}
    else{
//statement

    }
```

## 9. Ternary Operator:
```
    //ternary operator ? = return 1 of 2 values if a condition is true.
    // variable = (condition)?ifTrue: ifFalse;
    int become = 30000;
    double taxRate = (income >= 40000) ? 0.25: 0.15;
    System.out.println( taxRate);
```

## 10. String methods: 
Xem thêm : [Java String methods](https://www.geeksforgeeks.org/java/java-string-methods/).

## 11. Substrings: 
Xem thêm : [Java SubString methods](https://www.geeksforgeeks.org/java/substring-in-java/).

## 12. Enhanced Switches:
Syntax:
```
switch(Var){
    case valueOfVar -> {statements};
    case valueOfVar -> {statements};
    case valueOfVar -> {statements};
    case valueOfVar -> {statements};
    default -> {statements}
}
```
## 13. Logical Operators:

## 14. While loops:
while loops will repeat some code forever while some condition remain true.

`while (condition){statements};`
## 14. For loops:
For loops execute some code a **CERTAIN amount of times**.

## 15. break & continue:
**break** = break out of a loop( STOP)

**continue** = skip current interaction of a loop( SKIP)

## 16. Nested Loops:
A loop inside another loop used often with matrices or DS&A.

## 17. Methods( Function):
Method is **a block of reusable code** that is executed when called ().

## 18. Variable scope:

## 19. Array:
- This contain many variables that have same data_type.
Syntax: 

`data_type[] var_name= {value1, value2,..., valueN}`

- If you just declare and dont assgign value in, you have to allocate memory for array:

`data_type[] var_name = new data_type[numOfValue];`

- If you wanna find position of each value you can try lieanr search, like count by length and when each value equal which value you find -> return it. If array have same value( over two same value) you have to return sub array( which save same value you want to find).
- And in here have new content `varargs` stand for `variable arguments` . Like `array`, work with `varargs` like with array but with `array` you must assign value before pass into function, `varargs` you dont need do that, this will be assigned when process executed. 
## 20. 2D array:

## 21. OOP( Object-Oriented Programming):
* `Object` is a entity that holds data( attributes) and can perform     actions (methods). Its a reference data type.
    
* We have some concepts in Object:

    * **Constructor**: this is a special method to initialize objects. You can pass arguments to a constructor and set up initial values.

    ```
    public class Student{
        String name;
        int age;
        String address;

        Student(){
            //this is default constructor
        }

        //this is Parameterized constructor
        Student(String name, int age, String address){
            this.name = name;
            this.age = age;
            this.address = address;
        }
    }
    ```
    **Note:** Constructor will executed when Object initialized:
    
        ```
        Student std = new Student()//default constructor will execute
        ```

    * **Overloaded Constructors:** Same like overloaded methods.

    * **Array of Objects**:

    * **static**:
Chủ yếu được dùng để quản lý bộ nhớ, chúng ta có thể áp dụng static với các biến, phương thức và các khối lồng nhau. `static` có vai trò quan trọng trong Java, đặc biệt trong quản lý tài nguyên và hiệu suất chương trình. Vậy `static` trong Java là gì?
    
    `static` trong Java được sử dụng để xác định rằng một thành viên của lớp ( biến hoặc phương thức) thuộc về chính lớp đó, thay vì đối tượng ( instance) của lớp. Điều này có nghĩa là thành viên `static` có thể truy cập được mà không cần phải khởi tạo đối tượng.
    
    ![alt text](image.png)

Như vậy, đối với`static` chúng ta có những khái niệm liên quan như:
* **Static Variable:** 
    * Khi một biến được khai báo với từ khóa là `static` thì biến đó được gọi là biến static( biến tĩnh).
    * Việc cấp phát bộ nhớ cho biến `static` chỉ được thực hiện 1 lần khi class được nạp vào bộ nhớ. Giá trị mặc định khi biến `static` và `non-static` được khai báo là như nhau.
    * Biến `static` có thể được sử dụng làm thuộc tính chung, để dùng chung dữ liệu cho tất cả `objects` hoặc (instances) của lớp đó và giúp cho chương trình tiết kiệm bộ nhớ hơn.
    * Nếu một biến có cả `static` và `final` thì biến đó được gọi là ` hằng số` và được quy ước là viết hoa toàn bộ tên biến và được nối với nhau bằng kí tự ` _ ` nếu có nhiều từ nối lại.

    ```
    public static final PI = 3.14; 
    public static final SECRET_KEY = "devThoai110503"; 
    ```  

    * Trong `interface` mặc định một biến sẽ được khai báo là `public static final`.

Vd:
`public static String name = "dev Thoai";`
* **Static Method:** Tương tự như `static variable`, một method được khai báo với key là `static` thì method đó là method tĩnh( static).

Vd:
```
public static void changeWebsite(String website){
    MyWebsite.WEBSITE = website;
}
```
* **Static Block:** Được sử dụng để khởi tạo thành viên static.
* **Static Class:** Một class có thể được đặt là `static` khi nó là một `nested class`. Một `nested static class` có thể được truy cập mà không cần một `object` của một `outer class` ( Lớp bên ngoài).

## 22. Tính chất của OOP:
Object-Oriented Programming( OOP) là một khái niệm quang trọng trong xuyên suốt lập trình, hầu như trong xuyên suốt bất kì Project nào đó thì đều có sự góp mặt của OOP. OOP có 4 tính chất cơ bản.
    ![alt text](image-1.png)
* **Kế thừa( Inheritance)**: Là một lớp kế thừa toàn bộ các attributes và methods của lớp cha thông quan từ khóa `exxtend`
    * **super:**
    * **method overriding:** Khi lớp con( subclass) cung cấp hành vi của method của chính nó để ghi đè lên method đã được định nghĩa ở lớp cha để thay đổi hành vi của method. Cho phép code được tái sử dụng với một hành vi chi tiết được đưa vào.
* **Trừu tượng( Abstraction)**: 
    * Used to define abstract classes and methods. Abstraction is a process of **hidding implementation details** and **showing only the essential features**. 
    * Abstract classes  CANT be instantiated directly.
    * Can contain `'abstract'` methods( which must be implemented).
    * Can contain `'concrete'` methods (which are inherited).

    ví dụ:
```
public abstract class Shape{
    abstract double area(); //ABSTRACT

    void display(){//CONCRETE
        System.out.println("This is a shape.");
    }
}
```

**Sự khác nhau giữa Interface và Abstraction:**

* **Interface:** 
    * Interface is a `blueprint` for a class that specifies a set of abstract methods that implementing classes MUST define. Supports multiple inheritance- like behavior.
    * Khác với abstract, interface sử dụng từ khóa implement cho subclass

* **Đóng gói( Encapsulation)**:
* **Đa hình( Polymorphism)**:
    * `PolyMorphism` được định nghĩa là đa hình( Poly = Many, Morph = Shape).
    * Objects can identify as other objects.
    * Objects can be treated as objetcs of a common superclass.
    
    ví dụ:

Ta có lớp Vehicle và các lớp kế thừa( Abstract) hoặc Interface nó như: `Car`, `Boat`, `Bike`. Và PolyMorphism được hiểu đơn giản là 
## 23. 

--------------------TEMPLATE--------------------
# This is a Heading h1
## This is a Heading h2
###### This is a Heading h6

## Emphasis

*This text will be italic*  
_This will also be italic_

**This text will be bold**  
__This will also be bold__

_You **can** combine them_

## Lists

### Unordered

* Item 1
* Item 2
* Item 2a
* Item 2b
    * Item 3a
    * Item 3b

### Ordered

1. Item 1
2. Item 2
3. Item 3
    1. Item 3a
    2. Item 3b

## Images

![This is an alt text.](/image/sample.webp "This is a sample image.")

## Links

You may be using [Markdown Live Preview](https://markdownlivepreview.com/).

## Blockquotes

> Markdown is a lightweight markup language with plain-text-formatting syntax, created in 2004 by John Gruber with Aaron Swartz.
>
>> Markdown is often used to format readme files, for writing messages in online discussion forums, and to create rich text using a plain text editor.

## Tables

| Left columns  | Right columns |
| ------------- |:-------------:|
| left foo      | right foo     |
| left bar      | right bar     |
| left baz      | right baz     |

## Blocks of code

```
let message = 'Hello world';
alert(message);
```

## Inline code

This web site is using `markedjs/marked`.

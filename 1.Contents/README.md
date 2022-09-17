### VISUAL C# AND VISUAL STUDIO INTRO
#### 1. Welcome to C#
#### 2. Working with variables, operators, and expressions 变量、运算符、表达式
##### 2.1 Declare a variable 声明一个变量
> Text is a set to be deleted
##### 2.2 Declare a variable and give it an initial value 声明一个变量并赋予一个初始值
> Text is a set to be deleted
##### 2.3 Change the value of a variable 改变一个变量的值
> Text is a set to be deleted
##### 2.4 Generate a string representation of the value in a variable 将用`字符串`代表的值->`变量`代表的值
> 
##### 2.5 Convert a `string` to an `int/double` 
> Using `System.Int32.Parse` or `System.Double.Parse`
> 
> 简言之 `int.Parse`and `double.Parse`
> ```C#
> string strPI = "3.14159";
> string strThirdteen = "13";
> double dPI = double.Parse(strPI);
> int thirdteen = int.Parse(strThirdteen);
> ```
##### 2.6 Override the precedence of an operator 覆盖运算符的优先级
> compute the value inside of the bracket
> ```C#
> (1 + 2) * 3
> ```
##### 2.7 Assign the same value to several variables 给多个变量赋相同的值
> the value is passed from right to left 赋值方向👈👈👈
> ```C#
> int myInt4, myInt3, myInt2, myInt1, myInt0;
> myInt4 = myInt3 = myInt2 = myInt1 = myInt0 = 10;
> ```
##### 2.8 Increment or decrement a variables 增加或减少一个变量
> using `++` or `--`
> 
> e.g. `count++`

#### 3. Writing methods and applying scope 书写方法✍️、应用范围
##### 3.1 Declare a method 声明一种方式
> write inside the class
> ```C#
> [return type] [method name] (data_type value1, data_type value2)
> {
>   /**/
> }
> ```
> e.g:
> ```C#
> int addValue (int topFace, int bottomFace) 
> {
>   /**/
> }
> ```

##### 3.2 Return a value from within a method 从方法从回传一个值
> use keyword `return`
> ```C#
> int addValue (int topFace, int bottomFace) 
> {
>   return topFace + bottomFace;
> }
> ```
> even though you dont have to include a `return` at the end of a `void` function, it is suggested to do so, since every method is supposed to be return something. `void` method `return` void.
> ```C#
> public void Method()
> {
>   //something supposed to be return
>   return;
> }
> ```

##### 3.3 Return multiple values from within a method 在一个方法中回传多个值
> return multiple values as a tuple 以多元组的形式回传多个值
> ```C#
> (int min, int max) FindMinMax(int[] input)
> {
>   //finding min and max
>   return (min, max);
> }
> ```
> The returned multiple values function can be used like this: 回传多个值的函数能被这样使用
> ```C#
> var input = new[] {-9, 0, 67,100};
> var (minimum, maximum) = FindMinMax(input);
> ```

##### 3.4 Return from a method before the end of the method 在一个方法结束前回传一个方法
> block ends at where `return` is 
> ```C#
> void PrintSomething()
> {
>   Console.WriteLine("0"); // √
>   Console.WriteLine("1"); // √
>   return;
>   Console.WriteLine("2"); // ✖️
> }
> ```
##### 3.5 define an expression bodied method 定义一种表达式bodied方法
> 简言之 replace`{}` and `return` with `=>`
> ```C#
> double CalculateStrength(double strengthtoWeight, int weight)
> {
>   return strengthtoWeight * weight
> }
> ```
> it will be like 
> ```C#
> double CalculateStrength(double strengthtoWeight, int weight) => strengthtoWeight * weight
> ```
##### 3.6 call a method call 一个方法
> be like `methodName(args0, args1, args2, ...);`
> ```C#
> addValues(1, 1);
> ```
##### 3.7 Use the Generate Method Stub Wizard 方法存根向导
##### 3.8 Create a nested method (method in method) 创建一个nested 
> obviously there is a method `strength` inside the method `CalculateStrength`
> ```C#
> long CalculateStrength(string input)
> {
>   /**/
>   long strength(int dataValue)
>   {
>     if (dataValue == 1)
>     {
>       return 1;
>     } 
>     else
>     {
>       return dataValue * strength(dataValue - 1);
>     }
>   }
> }
> ```
##### 3.9 display the debug toolbar 展示debug🔧
> View -> Toolbar - Debug

##### 3.10 Step into a method 
##### 3.11 Step out of a method 
##### 3.12 Specify an optional parameter to a method 为方法指定可选参数
> ```C#
> void optMethod(int first, double second 1.0, string third ="Hello")
> {
>   /**/
> }
> ```
##### 3.13 Pass a method argument as a named 传递一个method arg作为命名
> Since you already have some default argument, you don't have to assign it again...
> ```C#
> optMethod(second: 1.0, third:"Hello");
> ```
> you can skip assign the value for `second`

#### 4. Using decision statements 决策语句
##### 4.1 `==`，`!=` determine equivalent
> ```C#
> thisYear == 2022
> ```
##### 4.2 `>`，`>=`, `<`, `<=` compare the value of two expressions 对比两个表达式的数值
> ```C#
> bool flag = 2 > 1;
> ```

##### 4.3 Declare a Boolean variable 声明一个布尔运算变量
> ```C#
> bool isOdd;
> ```

##### 4.4 `AND` 
> use `&&`
> ```C#
> inRange = (lo <= number) && (number <= hi);
> ```

##### 4.5 `or` 
> use `||`
> ```C#
> outOfRange = (number < lo) || (hi < number);
> ```
##### 4.6 `if` statement `if`声明
> in short(not recommend): ❌
> ```C#
> if (inRange)
>   process();
> ```
> in short(not recommend): ✔️
> ```C#
> if (inRange)
> {
>   process;
> }
> ```

##### 4.7 `switch` statement `switch`声明
> which is like a gate, which controls the output
> ```C#
> int choice;
> switch(choice)
> {
>     case 0:
>         //do some jobs(if choice== 0)
>         break;
>     case 1:
>         //do some jobs(if choice== 1)
>         break;
>     default:
>         //do some jobs(if (choice !== 0 && choice !== 1))
>         break;
> }
> ```
> tips: always remember to leave `default` value


#### 5. Using compound assignment and iteration statements 使用复合赋值与迭代语句
##### 5.1 What the hell is compound assignment? 什么是复合赋值？
> it is a shortcut for arithmetic operation and assignment 算数🧮操作和赋值的捷径
> ```C#
> variable += 1; //equivalent to variable = variable + 1;
> variable -= 1; //equivalent to variable = variable - 1;
> variable *= 1; //equivalent to variable = variable * 1;
> variable /= 1; //equivalent to variable = variable / 1;
> ```
> if there are multiple variables on the right hand side.Dont recommend using this shortcut

##### 5.2 `while`loop
> `while` something is `true`, do some jobs
> ```C#
> int i = 0;
> while(i < 10)
> {
>   Console.WriteLine(i);
>   i++; //dont forget to increment the condition!
> }
> ```

##### 5.3 `for`loop `for` 循环♻️
> ```C#
> for (int i = 0; i < 10; i++)
> {
>   Console.WriteLine(i);
> }
> ```
> you can also iterate backward and increment base on value bigger than 1 向后➖以及➕大于1的值
> for (int i = 10; i > 0; i--)
> {
>   //do some jobs
> }
> for (i = 0; i < 10; i+=2)
> {
>   //do some jobs
> }

##### 5.4 `do-while`loop `do-while` 循环♻️
> the difference between `do-while` loop and `while` loop is that: `do-while` loop iterate at least once.
> ```C#
> int i = 0;
> do
> {
>   Console.WriteLine(i);
>   i++;
> }
> while(i < 10);
> ```

#### 6. Managing errors and exceptions 管理错误与异常
##### 6.1 Catch a specific exception 捕捉特定异常
> if you want to catch specific exception, you have to specify the type of exception 
> ```C#
> try
> {
>   //do some jobs...
> }
> catch(FormatException fEx)
> {
>   //do some jobs...
> }
> ```
##### 6.2 Use `checked` to prevent overflow 防止溢出
> this is very handy in arithmetic computation for it prevent overflow 在算术🧮计算中防止溢出
> ```C#
> int number = Int32.MaxValue; //看不懂🤷‍♂️
> checked {number++}; // in this case, the overflow error will be caught 在这个情况下溢出的cuo wucuowu
> ```
##### 6.3 Throw an exception 抛出一个异常
> use `throw` keyword 使用`throw`关键词
> ```C#
> throw new FormatException(source);
> ```
##### 6.4 Ensure code will always run even though with an exception 确保代码运行即便出现异常
> this is very handy 
> ```C#
> try
> {
>   //do some jobs...
> }
> finally 
> {
>   //this part will be running no matter there is an exception above or not 
> }
> ```


### THE C# OBJECT MODEL 对象模型
#### 7. Creating and managing classes and objects 创建与管理类、与对象
##### 7.1 Declare a `class` 声明一个类
> ```C#
> class className
> {
>   //...  
> }
> ```

##### 7.2 Declare a `constructor` 声明一个构造器
> write a method its name is the same as the name of the class, and it has no return type
> ```C#
> class Point
> {
>   //..place the field at here
>   public Point(int x, int y)
>   {
>       //...
>   }
> }
> ```

##### 7.3 Call a `constructor` call一个构造器
> Use the new keyword and specify the constructor with appropriate set of parameters
> ```C#
> Point origin = new Point(10, 10);
> ```

##### 7.4 Declare a `static` method 声明一个静态方式
> Use the `static` keyword; a `static` method is that you can call this method without initializing an instance of this class. 静态方法意味着你可以call这个方法而无需初始化这个类的实例instance
> ```C#
> class Point
> {
>   //...
>   public static int ObjectCount()
>   {
>       //...
>   }
> }
> ```

##### 7.5 Call a `static` method call一个静态方法
> call a `static` method, e.g.[ClassName].[staticMethodName]
> ```C#
> int pointCreatedSoFar = Point.ObjectCount();
> ```

##### 7.6 Declare and acess a `static` field
> ```C#
> class Point
> { 
>   //...
>   public static int ObjectCount;
> }
> ```
> and you can acess the static field by invoke directly
> ```C#
> int num = Point.ObjectCount;
> ```

##### 7.7 Declare a `const` field
> `const` is a constant value 是一个constant 类型值
> ```C#
> class Math
> {
>   //...
>   public const double PI = 3.14159;
> }
> ```

#### 8. Understanding values and references 了解🫡值与引用
##### 8.1 copy a value type variable 复制一个值类型变量
> when you copy value type
> ```C#
> int i = 13;
> int copyi = i;
> i++; //above change won't affect `copyi`
> ```

##### 8.2 copy a reference type variable 复制一个引用类型的变量, reference type variable which dont store the actual value, rather the reference of the value
> when you copy a reference type, you actually copied the `reference` of the variable 
> ```C#
> Curve arcCrv = new Curve();
> Curve crv = arcCrv;
> arcCrv.translate(); // not only translate `arcCrv` but also `crv`
> ```

##### 8.3 declare a variable that can hold a value type or the `null` value 声明一个变量持有 值的类型或者 `null`值
> use `？` modifier
> ```C#
> int? i = null;
> ```

##### 8.4 pass a argument to a `ref` parameter 传递一个args 到`ref`参数
> the keyword `ref` simply implies that the change will affect itself
> ```C#
> static void doIncrement(ref int number)
> {
>   number++
> }
> int i = 42;
> doIncrement(ref i)  //i was incremented 
> ```
> although the function `doIncrement` is a `void` function which returns nothing, we should keep eye on `ref` keyword. in this case, the `i` was incremented. 空函数回传🈳，存在关键词`ref`，使 `i` 增加

##### 8.5 pass an argument to an `out` parameter 传递一个argument 到一个`out`参数
> it is very similar to ref keyword 

#### 9. Creating value types with enumerations and structures 通过枚举、结构创建值的类型
#### 10. Using arrays 阵列
#### 11. Understanding parameter arrays 参数阵列
#### 12. Working with inheritance 继承
#### 13. Creating interfaces and defining abstract classes 创建接口与定义抽象类
#### 14. Using garbage collection and resource management 垃圾回收♻️与资源管理

### EXTENSIBLE TYPES WITH C#
#### 15. Implementing properties to access fields 实现属性以访问字段
#### 16. Using indexers 使用索引器
#### 17. Introducing generics 范型
#### 18. Using collections 使用集合 
#### 19. Enumerating collections 枚举集合
#### 20. Decoupling application logic and handling events 解耦应用逻辑和事件处理
#### 21. Querying in-memory data by using query expressions 使用查询表达式查询内存中的数据
#### 22. Operator overloading 运算符重载

### BUILDING UNIVERSAL WINDOWS PLATFORM APPLICATIONS WITH C#
#### 23. Improving throughput by using tasks 通过使用任务提高吞吐量
#### 24. Improving response time by performing asynchronous operations 通过执行异步操作缩短响应时间
#### 25. Implementing the user interface for a Universal Windows Platform app 实现通用Windows平台应用的用户界面
#### 26. Displaying and searching for data in a universal Windows Platform app 在通用windows 平台应用中显示和查询数据
#### 27. Accessing a remote database from a universal Windows Platform app 从通用Windows 平台应用访问远程数据库

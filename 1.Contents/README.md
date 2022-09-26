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
> it is very similar to `ref` keyword, the way to perceive this is that wherever you see `out` 
> it is a decoration for output, you have to prepare something for output.
> ```C#
> using System.Linq;
> static void duplicateTenTimes(int i, out List<int> duplicatedList)
> {
>     duplicatedList = Enumerable.Repeat(i, 10).ToList();
> }
> List<int>tenDuplicate = new List<int>();
> duplicateTenTimes(10, out tenDuplicate); //at this point, the `tenDuplicate` has 10 copies of 10.
> ```
##### 8.6 Box and unbox a value 📦一个值
> `box` is a way of wrapping anything to a generic type, in this case we use `object`
> ```C#
> object o = 42;  
> ```
> retrospectively, you can see `unbox` as way casting the generic type to specific type 
> int i = (int)o;  
  
##### 8.8 cast an object safely 安全地铸造一个对象
> 1. first choice, use `is` keyword to check if the cast success 
> ```C#
> WrappedInt wi = new WrappedInt();
> //...
> object o = wi;
> if (o is WrappedInt temp)
> {
>   //...  
> }  
> ```
> 2. second choice, use `as` to perform the cast, and check if it is `null`
> ```C#
> WrappedInt wi = new WrappedInt();
> //...
> object o = wi;
> WrappedInt temp = o as WrappedInt;
> if (temp != null)
> {
>    //...
> }
> ```

#### 9. Creating value types with enumerations and structures 通过枚举、结构创建值的类型
bear in mind, the biggest difference between `struct` and `class` is that: **Structs are value type whereas Classes are reference type.** `struct`：值类型、`class`：参考类型
##### 9.1 declare an enumeration 声明一个枚举
> use the `enum` keyword => name of this `enum` => enumeration **literal** name
> ```C#
> enum Fruits{🍉，🥭，🍎，🍌，🍐，🥝}；  
> ```  
##### 9.2 declare a enumeration variable 声明一个枚举变量
> ```C#
> Fruits tropicalFruit;  
> ``` 
##### 9.3 declare a enumeration variable 赋一个枚举变量 一个值
> ```C#
> tropicalFruit = 🥭;  // error! the compiler cant detect what `🥭` is semantically
> tropicalFruit = Fruits.🥭;  // √
> ``` 

##### 9.4 declare a structure type 声明一个结构类型
> use the keyword `struct` => the name of the `struct` => the body of the `struct`(the constructors, methods, and fields).[similar to class]
> ```C#
> struct Point3d
> {
>   internal double _x, _y, _z;
>   public Point3d(double x, double y, double z)
>   {
>       this._x = x;
>       this._y = y;
>       this._z = z;  
>   }  
> }  
> ```

##### 9.5 declare a structure variable 声明一个结构化变量
> ```C#
> Point3d pt;  
> ```
  
##### 9.6 initialize a stucture variable to a value 初始化一个结构化变量并赋值
> similar to `class`
> ```C#
> Point3d = new Point3d(0, 1, 2);  
> ```  
#### 10. Using arrays 阵列
> what is the biggest difference between `Array` and `List`? `Array` is fixed size once it is initialized.`List` is dynamic, you can either `add` or`remove`items from it. 
>   
##### 10.1 declare an array variable 声明一个 `array` 变量
> [data_type][name_of_array];
> ```C# 
> bool [] flags;
> ``` 
##### 10.2 **create an instance** of an array **创建**数组的**实例**
> when you create an instance, you have to explicitly define the amount of the array. 当你创建一个实例，需要明确地定义数组的数量
> ```C#  
> bool [] flags = new bool[10];
> ``` 
##### 10.3 initialize the elements of an array to specific values 初始化元素数组声明值 
> when you initialize the array, you have to assign specific values 初始化数组🔢，赋特定的值
> ```C#   
> int [] numPI = {3, 1, 4, 1, 5, 9};
> ```  
  
##### 10.4 find how many elements in an array 找到数组中元素的数量
> use `Length` property
> ```C#  
> int[] numPI = {3, 1, 4, 1, 5, 9};
> int numPIAmount = numPI.Length; // here we got 6
> ```  
  
##### 10.5 access a single array element 访问数组中的一个单一元素
> use the `[]` to access particular element 访问特定元素
> ```C#   
> int num = numPIAmount[2]; // we got 4
> ```  
##### 10.6 loop over an array 循环一个数组
> use `for` loop or `foreach` loop
> ```C#   
> bool [] flags = {true, false, true, false};
> for (int i = 0; i < flags.Length; i++)
> {
>     Console.WriteLine(flags[i]);  
> }                              
> foreach (bool flag in flags)
> {
>     Console.WriteLine(flag);  
> }
> ```  
##### 10.7 declare a **multidimensional array** variable 初始化元素数组声明值
> declare a **multidimensional array** variable 声明一个**多维数组**变量
> ```C#   
> use this `[,]`
> int [,] table;  
> table = new int[4, 6]; //initialize an 4*6 array
> ```  
##### 10.8 declare a **jagged array** variable
> use this `[][]`
> ```C#
> int[][] items;
> items = new int[4][];
> items[0] = new int[3];
> items[1] = new int[10];
> items[2] = new int[40];
> items[3] = new int[25];
> ```
the difference between _multidimensional array_ and _jagged array_ is that the 
_multidimensional array_ is like a **square** with anything aligned.
_jagged array_ is like zig-zag no symmetric shape.
> ```C#
> public class ArrayHolder
> {
>     int[,] multi
> }
> ```
the difference between **multidimensional array** and **jagged array** is that 
**multidimensional array** is like a `square` with all element aligned.
**jagged array** is like zig-zag `non-symmetric shape`.
> ```C#
> public class ArrayHolder
> {
>     int[,] = multiDimArray = {{1,2,3,4},
>                               {5,6,7,0},
>                               {8,0,0,0},
>                               {9,0,0,0},  
>                              };
>     int[][] jaggedArray = { new int[] {1,2,3,4},
>                             new int[] {5,6,7},
>                             new int[] {8},
>                             new int[] {9}
>                           };
> }   
> ```  
  
#### 11. Understanding parameter arrays 参数阵列
> By using the `params` keyword, we can specify a method parameter that takes a variable number of argument. 使用 关键词`params` 声明一个方法参数
> however, the parameter type must be a single-dimensional array.
> ```C#
> public class MyClass
> {
>     public static void IntParams(params int[] list) //with `params` keyword, the length of array can be dynamic
>     {
>         for (int i = 0; i < list.Length; i++)
>         {
>             Console.Write(list[i] + " ");    
>         }
>         Console.WriteLine();  
>     }
>     public static void objParams(params object[] list)
>     {
>         for (int i = 0; i < list.Length; i++)
>         {
>             Console.Write(list[i] + " ");  
>         }
>         Console.WriteLine();    
>     }
>     
>     static void Main()
>     {
>         //output: 1 2 3 4
>         IntParams(1, 2, 3, 4);
>
>         //output: 1 a test
>         objParams(1, 'a', "test");
>
>         //output: a blank line
>         objParams();
>         
>         //output: 5 6 7 8 9
>         int[] myIntArray = {5, 6, 7, 8, 9};
>
>         //output: 2 b best again
>         object[] myObjArray = {2, 'b', "best", "again" };
>         
>         //output: error!!! no output!!!
>         IntParams(myObjArray); //this cannot be compiled
>           
>         //output: System.Int32[]
>         ObjParams(myIntArray); //no error, the entire integer array become the 1st element of the params array.
>     }  
> }  
> ``` 
> /*
> 
> Output:
>     1 2 3 4
>     1 a test
>
>     5 6 7 8 9
>     2 b best again
>     System.Int32[]  
> */
>

#### 12. Working with inheritance 继承
##### 12.1 createa derived class from a base class 从基类创建派生类
> use the colon `:`
> ```C#
> class BaseClass
> {
>     public BaseClass(int x, int y)
>     {
>         //ctor...    
>     }    
> }
> class DerivedClass : BaseClass
> {
>         public DerivedClass(int x, int y) : base(x, y)
>         {
>         }
>         //if you want to inherit the constructor from the BaseClass,
>         //then you dont need to write the code here, leave it blank  
> }  
> ```
##### 12.2 declare a `virtual` method in the `base` class and `override` it in the `derived` class 在基类中声明一个虚拟方法 并且 在衍生类中重写
> remember:
> `virtual` in the `base` class
> `override` in the `derived` class 
> ```C#
> class Mammal 
> {
>     public virtual void Breathe()
>     {
>     }
> }
> class Monkey: Mammal
> {
>     public override void Breathe()
>     {
>         //override the breathe method rather than using the general breathe **覆盖方法**而不使用**通用**
>     }
>         //...
> }
> ```
##### 12.3 define an extension method for a type 为一种类型定义一个`扩展方法` 
> what is `extension method`❓ 
> it is the `.` method you use everyday. like `.Select()`, `.ToString()`, `.OrderBy()`.
>  
> in summary, the `extension method` is a **static method** which `extends` some sort of method invoked by the dot `.`
>  
> for example, we can write our own `countStringLength` method by decorating the **variable** with `this`.
>  
> what is `this` keyword❓
>  
> the `this` keyword refers to the **current instance of the class** and it is also a modifier of the first parameter of an extension method.
> ```C#
> namespace ExtensionMethods
> {
>     static class Util
>     {
>         public static int Negate(this int i)
>         {
>                 return -i;  
>         }  
>     }  
> }  
> ```
> as you can see `this String str` is decorated with `this`, which means the variable can be the current instance of the class!!
> ```C#  
> Using ExtensionMethods; //bring the Extension method here
> //...
> int ten = 10;
> int nine = ten.Negate(); //we can use `.Negate()` method without writing this method inside a class!!
> ```  

#### 13. Creating interfaces and defining abstract classes 创建接口与定义抽象类
##### the concept of `interface` is a little bit similar to `.header` file in C++, which is **a must for such class to implement it**
##### 13.1 declare an interface 声明一个界面
> use `interface` keyword
> ```C#
> interface IDemo
> {
>     string GetName();
>         string GetDescription();  
> }  
> ```
##### 13.2 Implement an interface 实现一个界面
> implement the class to fulfill interface **explicitly** 实现一个类以明确地实现接口
> ```C#
> class Test : IDemo
> {
>     public string IDemo.GetName()
>     {
>         //...  
>     }
>     public string IDemo.GetDescription()
>     {
>         //...  
>     }  
> }
> ```
> implement the class to fulfill interface **implicitly** 实现类以含蓄地实现接口
> ```C#
> class Test : IDemo
> {
>     public string GetName()
>     {
>         //...  
>     }
>     public string GetDescription()
>     {
>         //...  
>     }  
> }  
> ```
##### 13.3 `abstract` class which **can only be a base class** 抽象类只能成为基类
> use the abstract keyword. **you cannot create an instance from an abstract class**
> then, what is the point to create an `abstract` class? ❓
> it means to be **a template**. for instance, you define a class call `Felidae`, but `Felidae` should be treated as a family of mammals! There is no such instance of `Felidae` 一个模版，例如，定义一个**Felidae**类，但是**Felidae** 不能被当作**mammals**的族，不能出现`Felidae`这样的**实例**
> ```C#
> abstract class Felidae
> {
>     //...
>     public virtual void Sound();  
> }  
> public class Cat : Felidae
> {
>     //...
>     public override void Sound();
>     {
>         Console.WriteLine("Meow");  
>     }  
> }
> ```
##### 13.4 a `sealed` class that `cannot be a base class `
> sealed class Horse 
> {
>     //...  
> }  

#### 14. Using garbage collection and resource management 垃圾回收♻️与资源管理
##### 14.1 Write a destructor
> use the `~` prefix. the method of destructor cannot have access modifier!(like `public`)
> ```C#
> class Example
> {
>     //...
>     ~Example()
>     {
>     }  
> }  
> ```
##### 14.2 call the destructor is invalid 
> you cannot call a destructor, only the garbage collector can call a destructor.
##### 14.3 ❌ force garbage collection(not recommended) 
> ```C#
> GC.Collect
> ```
##### 14.4 release a resource at a known point in time 在已知⌚️释放资源
> ⚠️ cons: this is at the risk of resource leaks if an exception interrupts the execution 如果异常中断执行则存在资源泄漏的风险
> how to do it? => write a **disposal method** (a method that disposes of a resource) and **call it explicitly** from the program 写一个**处理方法**
> (处理资源的方法),显式调用它
> ```C#
> class TextReader
> {
>     //...
>     public virtual void Close()
>     {
>         //write the disposal method here  
>     }
> }
> class Example
> {
>     void Use()
>     {
>         TextReader reader = ...;
>  
>         reader.Close(); //call it explicitly to dispose a resource call显式处理一个资源  
>     }  
> }  
> ```
##### 14.5 support exception-safe disposal in a class 在类中支持异常-安全🔐处理
> that said, to implement the `IDisposable` interface
> ```C#
> class SafeResource : IDisposable
> {
>         //...
>     public void Dispose()
>     {
>     //Dispose resource here  
>     }  
> }  
> ```
##### 14.6 implement exception-safe disposal for an object that implements the `IDisposable` interface 实现 异常-安全🔐 处理 对象实施 `IDisposable`接口
> 🌟 this is the recommended option in garbage collection 垃圾收集
  
### EXTENSIBLE TYPES WITH C# C#的扩展类型
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

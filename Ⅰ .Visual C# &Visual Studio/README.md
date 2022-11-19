### VISUAL C# AND VISUAL STUDIO INTRO

#### 1. Welcome to C#



#### 2. Working with variables, operators, and expressions //变量、运算符、表达式

##### 2.1 Declare a variable //声明一个变量
> Text is a set to be deleted

##### 2.2 Declare a variable and give it an initial value //声明一个变量并赋予一个初始值
> Text is a set to be deleted

##### 2.3 Change the value of a variable //改变一个变量的值
> Text is a set to be deleted

##### 2.4 Generate a string representation of the value in a variable //将用`字符串`代表的值->`变量`代表的值
##### primitive data types
| Data type数据类型 | Description描述 | Size(bits)大小 | Range范围 | Sample Usage用例 |
|-----------|-------------|------------|-------|--------------|
| _int_     | Whole numbers(integers) | 32         | $-2^{31}$ through $2^{31}-1$ | `int count; count = 42;`
| _long_    | Whole numbers(bigger range) | 64         | $-2^{63}$ through $2^{63}-1$ | `long wait; wait = 42L;` |
| _float_   | Floating-point numbers | 32         | $-3.4 \times 10^{-38}$ through $3.4 \times 10^{38}$ | `float away; away = 0.42F;` |
| _double_  | Double-precision(more accurate) | 64         | $\pm 5.0 \times 10^{-324}$ through $\pm 1.7 \times 10^{308}$ | `double trouble; touble = 0.42;` |
| _decimal_ | Monetary values | 128        | 28 significant figures | `decimal coin; coin = 0.42M;` |
| _string_  | Sequence of characters | 16 bits per character | Not applicable | `string vest; vest = "forty two";` |
| _char_    | Single character | 16         | 0 through $2^{16}-1$ | `char grill; grill = 'x';` |
| _bool_    | Boolean | 8          | True or false | `bool teeth; teeth = false;` |

##### 2.5 Convert a `string` to an `int/double` //将 `string`转换为 `int/double`
> Using `System.Int32.Parse` or `System.Double.Parse`
> 
> 简言之 `int.Parse`and `double.Parse`
> ```C#
> string strPI = "3.14159";
> string strThirdteen = "13";
> double dPI = double.Parse(strPI);
> int thirdteen = int.Parse(strThirdteen);
> ```

##### 2.6 Override the precedence of an operator //覆盖运算符的优先级
> compute the value inside of the bracket //优先计算括号里的内容
> ```C#
> (1 + 2) * 3
> ```

##### 2.7 Assign the same value to several variables //给多个变量赋相同的值
> the value is passed from right to left 赋值方向👈👈👈
> ```C#
> int myInt4, myInt3, myInt2, myInt1, myInt0;
> myInt4 = myInt3 = myInt2 = myInt1 = myInt0 = 10;
> ```

##### 2.8 Increment or decrement a variables //增加或减少一个变量
> using `++` or `--`
> 
> e.g. `count++`



#### 3. Writing methods and applying scope //书写方法✍️、应用范围
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

##### 3.2 Return a value from within a method //从方法从回传一个值
> use keyword `return`
> ```C#
> int addValue (int topFace, int bottomFace) 
> {
>   return topFace + bottomFace;
> }
> ```
> even though you dont have to include a `return` at the end of a `void` function, it is suggested to do so, since every method is supposed to be return something. `void` method `return` void. 虽然在 `void` 函数结束后 不需要包含一个 `return`，还是建议这么做，因为每个方法都会回传 something，`void`方法 回传 void 
> ```C#
> public void Method()
> {
>   //something supposed to be return
>   return;
> }
> ```

##### 3.3 Return multiple values from within a method //在一个方法中回传多个值
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

##### 3.4 Return from a method before the end of the method //在一个方法结束前回传一个方法
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

##### 3.5 define an expression bodied method //定义一种表达式bodied方法
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
##### 3.6 call a method //call 一个方法
> be like `methodName(args0, args1, args2, ...);`
> ```C#
> addValues(1, 1);
> ```

##### 3.7 Use the Generate Method Stub Wizard //方法存根向导
##### 3.8 Create a nested method (method in method) //创建一个nested 
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

##### 3.9 display the debug toolbar //展示debug🔧
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
> ```C#
> for (int i = 10; i > 0; i--)
> {
>   //do some jobs
> }
> for (i = 0; i < 10; i+=2)
> {
>   //do some jobs
> }
> ```

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
> `static` sequence interface: the number of item does not change but the actual items might 
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
  
##### 8.8 cast an object safely //安全地铸造一个对象
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



#### 9. Creating value types with enumerations and structures //通过枚举、结构创建值的类型
bear in mind, the biggest difference between `struct` and `class` is that: **Structs are value type whereas Classes are reference type.** `struct`：值类型、`class`：参考类型

##### 9.1 declare an enumeration //声明一个枚举
> use the `enum` keyword => name of this `enum` => enumeration **literal** name
> ```C#
> enum Fruits{🍉，🥭，🍎，🍌，🍐，🥝}；  
> ```  

##### 9.2 declare a enumeration variable //声明一个枚举变量
> ```C#
> Fruits tropicalFruit;  
> ``` 

##### 9.3 declare a enumeration variable //赋一个枚举变量 一个值
> ```C#
> tropicalFruit = 🥭;  // error! the compiler cant detect what `🥭` is semantically
> tropicalFruit = Fruits.🥭;  // √
> ``` 

##### 9.4 declare a structure type //声明一个结构类型
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

##### 9.5 declare a structure variable //声明一个结构化变量
> ```C#
> Point3d pt;  
> ```
  
##### 9.6 initialize a stucture variable to a value //初始化一个结构化变量并赋值
> similar to `class`
> ```C#
> Point3d = new Point3d(0, 1, 2);  
> ```  



#### 10. Using arrays //阵列
> what is the biggest difference between `Array` and `List`? `Array` is fixed size once it is initialized.`List` is dynamic, you can either `add` or`remove`items from it. 
>

##### 10.1 declare an array variable //声明一个 `array` 变量
> [data_type][name_of_array];
> ```C# 
> bool [] flags;
> ``` 

##### 10.2 **create an instance** of an array //**创建**数组的**实例**
> when you create an instance, you have to explicitly define the amount of the array. 当你创建一个实例，需要明确地定义数组的数量
> ```C#  
> bool [] flags = new bool[10];
> ```

##### 10.3 initialize the elements of an array to specific values //初始化元素数组声明值 
> when you initialize the array, you have to assign specific values 初始化数组🔢，赋特定的值
> ```C#   
> int [] numPI = {3, 1, 4, 1, 5, 9};
> ```  
  
##### 10.4 find how many elements in an array //找到数组中元素的数量
> use `Length` property
> ```C#  
> int[] numPI = {3, 1, 4, 1, 5, 9};
> int numPIAmount = numPI.Length; // here we got 6
> ```  
  
##### 10.5 access a single array element //访问数组中的一个单一元素
> use the `[]` to access particular element 访问特定元素
> ```C#   
> int num = numPIAmount[2]; // we got 4
> ```

##### 10.6 loop over an array //循环一个数组
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

##### 13.3 `abstract` class which **can only be a base class** //抽象类只能成为基类
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



#### 14. Using garbage collection and resource management //垃圾回收♻️与资源管理
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

##### 14.2 call the destructor is invalid //不能call一个destructor
> you cannot call a destructor, only the garbage collector can call a destructor. 只有垃圾回收♻️才能call 一个destructor
##### 14.3 ❌ force garbage collection(not recommended) //不建议 强制垃圾垃圾回收
> ```C#
> GC.Collect
> ```

##### 14.4 release a resource at a known point in time //在已知⌚️释放资源
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

##### 14.5 support exception-safe disposal in a class //在类中支持异常-安全🔐处理
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
> 🌟 this is the recommended option in garbage collection 垃圾收集的建议选项
> how to do it? => create the object in a `using` statement 在 `using` 声明中创建一个对象
> ```C#
> using(SafeResource resource = new SafeResource())
> {
>     // use SafeResource here
>     // ...  
> }   
> ```  
  
### EXTENSIBLE TYPES WITH C# C#的扩展类型



#### 15. Implementing properties to access fields 实现属性以访问字段
> big picture: the design of property in C# is to inherit the `get()` and `set()` method in C++, but in an efficient, elegant and safe way.
##### 15.1 declare a read/write `property` for a structure or class 为structure 或 class 声明一个 读/写 `属性` 
> define the `type` of that property with `get` and `set`
> `get`: able to read
> `set`: able to write 
> ```C#
> struct ScreenPosition
> {
>         //...
>     public int X
>     {
>         get { ... } // or get => ...
>         set { ... } // or set => ... 
>     }
>     //...  
> }  
> ```

> property with only `get` keyword is **read-only**
> property with only `set` keyword is **write-only**
  
##### 15.2 declare a property in an `interface` 在 `interface` 中声明一个属性
> write down the `get` and `set`
> ```C#
> interface IScreenPosition
> {
>     int X { get; set; };
>     int Y { get; set; };  
> }  
> ```
> the class implemented the interface will look like this: 类实施的接口：
> ```C#
> struct ScreenPosition : IScreenPosition
> {
>     private int _x;
>     private int _y;
>     public int X
>     {     
>         //read
>         get => this._x;
>         //write
>         set => this._x = value;
>     }
>     public int Y
>     {
>         //read
>         get => this._y;
>         //write
>         set => this._y = value;
>     }
> }
> ```  

##### 15.3 Create an automatic property 创建一个自动属性
> in the class or structure that contains the property, define the property with empty get and set accessors 在类或结构中包含属性，通过空的 `get`和 `set`附件定义属性
> this is very handy feature!
> ```C#
> public class Customer
> {
>     public int Id { get; set; }
>     public string FirstName { get; set; }
>     public string LastName { get; set; }  
> }
> ```
> now this class can be used as a sort of data container!!
> ```C#  
> var customerBob = new Customer
> {
>     Id = 1,
>     FirstName = "Bob",
>     LastName = "Smith"  
> }
> var customerDavid = new Customer
> {
>     Id = 3,
>     FirstName = "David",
>     LastName = "Rutten"  
> }  
> ```  



#### 16. Using indexers 使用索引器
> 🌟 big scope: what is the purpose of using indexer?
> it aims to **deconstruct the integer to binary value**(`1/0` and `true/false`)which is very flexible!
> 📌 fact: what are **integer**, **binary**, **hex**, etc?
> we use `decimal system`十进制 in our life, e.g. "i am `29` years old", however the `hex`, `binary` are another form of representing numbers
> `hexadecimal`十六进制 is 16-base. `binary`二进制 is 2-base.

##### 16.1 specify an integer value using **binary** or **hexadecimal** notation 
> `0b0` for **binary** values prefixes.
> `0x0` for **hexadecimal** values prefixes.
> include `_` separator to make values easier to read.
> ```C#
> unit moreBinData = 0b0_11110000_01011010_11001100_00001111;
> unit moreHexData = 0x0_F0_5A_CC_0F;  
> ```  

##### 16.2 display an integer value as its binary or hexadecimal representation 以 **二进制** 或 **十六进制** 显示整数类型值
> use the `Convert.ToString()` method, and specify 2(for binary) or 16(for hexadecimal) as the number base.
> ```C#
> unit moreHexData = 0x0_F0_5A_CC_0F;
> Console.WriteLine($"{moreHexData, 2}")  
> // display 0b0_11110000_01011010_11001100_00001111
> // therefore the value of `0b0_11110000_01011010_11001100_00001111` and `0x0_F0_5A_CC_0F` are the same yet in different base.
> ``` 

##### 16.3 create an indexer for a class or structure 为一个类或者结构创建一个索引器
> use the keyword `this` and **square bracket** `[]`
> ```C#
> struct RawInt
> {
>     //...
>     public bool this [ int index ]
>     {
>         get { ... }
>         set { ... }  
>     }
>     //...  
> }
> ```

##### 16.4 define an indexer in an interface and implement it 定义一个索引器在 接口 中并 实施 它
> define it: 定义ta
> ```C#
> interface IRawInt
> {
>         bool this [ int index ] { get; set; }
> }
> ```

> implicitly implement it: 含蓄地实施ta
> ```C#
> struct RawInt : IRawInt
> {
>     //...
>     public bool this [ int index ]
>     {
>         get { ... }
>         set { ... }  
>     }
>     //...  
> }  
> ```

> explicitly implement it: 明确地实施ta
> ```C#
> struct RawInt : IRawInt
> {
>     //...
>     bool IRawInt.this [ int index ]
>     {
>         get { ... }
>         set { ... }  
>     }
>     //...  
> }  
> ```



#### 17. Introducing generics 范型

##### 17.1 Instantiate an object by using a generic type 通过使用范型实例化一个对象
> when you see `<>` , it means this is used in generic type `<>` 意味着在范型中使用
> ```C#
> Queue<int> myQueue1 = new Queue<int>();
> Queue<double> myQueue2 = new Queue<double>();
> Queue<string> myQueue3 = new Queue<string>();
> List<int> myList1 = new List<int>();
> List<double> myList2 = new List<double>();
> List<string> myList3 = new List<string>();
> ```
> as you can see, the `Queue` can contain `int`, `double`, and `string` etc. that is the design of `Queue` and `List`
> 🌟 `T` was used to notate **generic** type 标记 范型
> ```C#
> public class Queue<T> : IEnumerable<T>, ICollection, IEnumerable
> {
>     //...  
> }
> public class List<T> : IList<T>, ICollection<T>, IList, ICollection, IReadOnlyList<T>, IReadOnlyCollection<T>, IEnumerable<T>, IEnumerable
> {
>     //...  
> }
> ```
  
##### 17.2 create a new generic type 创建一个新的范型 
##### 17.3 🌟**Restrict** the **type** that can be substituted for the **generic** type parameter 限制能被 替换成 范型的参数
> it means that if you want to use this generic formwork, the data-type you set my implement something 意味着如果想要使用这个 范型，
> the following means the `T` in the `Tree` must implement `IComparable<T>`
> ```C#
> public class Tree<T> where T : IComparable<T>
> {
>         //...  
> }  
> ```

##### 17.4 define a generic method 定义一个 范型方法
> put`<T>` before the `()`
> ```C#  
> static void InsertIntoTree<T>(Tree<T> tree, params T[] data)
> {
>     //...  
> }
> ```  
  
##### 17.5 invoke a generic method 范型 方法
> to put the data type you use to replace the `T`
> ```C#
> InsertIntoTree<char>(charTree, `Z`, `X`);
> ```  
##### 17.6 define a **covariant** interface 定义一个 **协变** 接口
> specify the `out` qualifier for covariant type parameter. Reference the covariant type parameters only as the return types from methods and not as
> the types for method parameters: `协变` 类型参数。从 ☑️方法 中参考协变类型参数，而不是❌方法参数 
> ```C#
> interface IRetrieveWrapper <out T>
> {
>         T GetData();  
> }  
> ```

##### 17.7 define a **contravariant** interface 定义一个 **逆变** 接口
> specify the `in` qualifier for covariant type parameters. Reference the **contravariant** type parameters only as the types of method parameters and not as return types:
> ```C#  
> public interface IComparer<in T>
> {
>         int Compare(T x, T y);  
> }    
> ```
> A note on `T`. here the `T` is literal symbol of `Generic`. what really does represent `Generic` is `< >`, see the following example:
> ```C#
> public class Tree<T>
> {
>         //...  
> }
> public class Tree<TItem>
> {
>         //...  
> }  
> ```
they work as the same in functionality no matter use `T` or `TItem`. I personally prefer `T` for simplicity.



#### 18. Using collections 使用集合
> the frequently used collections in C# are：
##### 18.1 create a new collection 创建一个新集合
> use `List<T>` as an example 
> ```C#
> List<PlayingCard> cards = new List<PlayingCard>();
> ```

##### 18.2 add an item to a collection 添加一个物件到集合中
> `List<T>` use `Add`
> `HashSet<T>` use `Add`
> `Dictionary<T, T>` use `Insert`
> `Queue<T>` use `Enqueue`
> `Stack<T>` use `Push`
> ```C#
> HashSet<string> employee = new HashSet<string>();
> employee.Add("John");
> LinkedList<int> data = new LinkedList<int>();
> data.AddFirst(101);
> Stack<int> numbers = new Stack<int>();
> numbers.Push(99);
> ```

##### 18.3 remove an item from a collection 从一个集合中移除一个物件
> `Remove` is used in `List<T>`, HashSet<T>, Dictionary<T, T>
> `Dequeue` is used in `Queue<T>`
> `Pop` is used in `Stack<T>`
> ```C#
> HashSet<string> employees = new HashSet<string>();
> //...
> employees.Remove("John");
>   
> LinkedList<int> data = new LinkedList<int>();
> //...
> data.Remove(101); 
> 
> Stack<int> numbers = new Stack<int>();
> //...
> int item = numbers.Pop(); // pop a item from a stack
> ```

##### 18.4 find the number of elements in a collection 
> /*the two same elements wont allowed to appear in **collection** */
> use `Count`
> ```C#
> List<PlayingCard> cards = new List<PlayingCard>();
> //...
> int noOfCards = cards.Count;
> ```

##### 18.5 locate an item in a collection 在集合中定位一个物件
> _array notation_ is used in _dictionary-oriented collections_
> `Find` is used in _lists_
> ```C#
> Dictionary<string, int> ages = new Dictionary<string, int>();
> ages.<"Wang", 29>;
> int wangsAge = ages["Wang"]
> ```
> in case there is a class named `Person` 
> ```C#
> public class Person  
> {
>     public int ID { get; set; }
>     public string Name { get; set; }
>     public double Height { get; set; }  
> }
> ```

> find the info in a list by `Find` using `System.Linq`
> ```C#
> List<Person> personnel = new List<Person>();
> Person Simon = new Person{ ID = 3, Name = "Kobe Bryant", Height = 6'6' };
> personnel.Add(Simon);
> Person match = Personnel.Find(p => p.ID == 3); // there you go, you find Kobe by searching ID == 3
> ```

##### ⚠️⚠️⚠️ Note: The `Stack<T>`, `Queue<T>`, and `HashSet<T>` collection classes **DO NOT** support searching, although you can test for membership of an item in a hash set by using the `Contains` method.

##### 18.6 iterate through the elements of a collection 迭代集合中的元素
> use `for` or `foreach` statement to do so 
> ```C#
> LinkedList<int> numbers = new LinkedList<int>();
> //...
> for (LinkListNode<int> node = numbers.First; node != null; node = node.Next)  
> {   
>     int number = node.Value;
>     Console.WriteLine(number);  
> }
> //...
> foreach (int number in numbers)
> {
>     Console.WriteLine(number);  
> }  
> ```  



#### 19. Enumerating collections 枚举集合
##### 19.1 make class enumerable which support the `foreach` construct 使类可枚举并支持 `foreach` 构造
> implement the `IEnumerable` interface and provide a `GetEnumerable` method that return an IEnumerator object
> ```C#
> public class Tree<T> :  IEnumerable<T>
> {
>     //...
>     IEnumerable<T> GetEnumerable()
>     {
>     //...  
>     }  
>   
> }
> ```

##### 19.2 implement an enumerator without using an iterator 实施一个枚举器 without使用 一个迭代器
> define a enumerator class that implements the `IEnumerator` interface, and that provide the `Current` property and the `MoveNext` method (and optionally the `Reset` method).
> ```C#
> public class TreeEnumerator<T> : IEnumerator<T>
> {
>     //...
>     T Current
>     {
>         get
>         {
>         //...
>         }
>     }
>     bool MoveNext()
>     {
>          //...
>     }
> }
> ```

##### 19.3 define an enumerator by using an iterator 使用迭代器定义一个 遍历器
> implement the enumerator to indicate which items should be returned (using the `yield` statement) and in which order
> ```C#
> IEnumerator<TItem> GetEnumerator()
> {
>     for (...)
>     {
>         yield return ...  
>     }
> }  
> ```


  
#### 20. Decoupling application logic and handling events 解耦应用逻辑和事件处理
#### Delegate and Event 委托与事件
##### delegate 
> 🌟 `delegate` is literally an agent which can be seen as **delegate** of function 函数的委托
> 🌟 `delegate` is a pointer to method 方法的
##### 20.1 declare a **delegate** type 
> put the delegate ahead the decoration of the function.
> ```C#
> delegate void myDelegate();  
> ```  
##### 20.2 create an instance of a delegate with initialization 通过初始化 创建一个委托的实例
> 🔭 bigger picture: why do we need delegate? 为什么需要委托？
> bc sometime we dont know which method we should use, imagine **delegate is a variable of method** rather than value 应该使用什么方法.
> ```C#
> //two methods defined
> public double Add(double lhs, double rhs) => lhs + rhs;
> public double Substract (double lhs, double rhs) => lhs - rhs;
> 
> //declare an delegate whose parameter must match those you want to use
> public double ArithmeticOperation (double lhs, double rhs);
>   
> //initialization
> ArithmeticOperation operation;
> bool flag = false;
> 
> //now the method operation is decided by the boolean value
> public void AutoSelectOperation()
> {
>     if(flag)
>     {
>        operation = Add;  
>     }
>     else
>     {
>        operation = Substract;  
>     }  
> }  
>  
> // use the delegate method
> double result = operation(10, 3)//since flag = false, the operation points to substract, so the result = 7  
> ```
  
##### 20.3 declare an event 
//to do 
  


#### 21. Querying in-memory data by using query expressions 使用查询表达式查询内存中的数据
##### the following examples use a class called `Address` with 3 properties: `CompanyName`, `City`, `Country`
##### 21.1 **select** specified fields from an enumerable collection
> use `Select` method with lambda expression 
> ```C#
> using System.Linq;
> //Linq way of doing
> var customerFirstNames = customers.Select(cust => cust.FirstName)
> ```  
  
> use `select` and `from`
> //SQL way of doing
> ```C#
> var customerFirstNames = from cust in customers
>                                                 select cust.FirstName;  
> ```
  
##### 21.2 **filter** rows from an enumerable collection 从可遍历集合中过滤行
> use the `where` method with lambda expression.
> ```C#
> using System.Linq;
> //Linq way of doing 
> var usCompanies = addresses.Where(addr => 
>                                                     String.Equals(addr.Country,"United States"))
>                                                     .Select(usComp => usComp.CompanyName);  
> ```

> Use `where`
> ```C#
> //SQL way of doing 
> var usCompanies = from a in addresses
>                   where String.Equals(a.Country, "United States")
>                   select a.CompanyName;  
> ```
  
##### 21.3 enumerate data in a specified order 在特定的顺序下列举数据
> Use the `OrderBy` method with lambda expression. lambda表达式的`OrderBy`方法
> ```C#
> using System.Linq;
> //linq way of doing 
> //sort the list in light of CompanyName then select the names  
> var companyNames = addresses.OrderBy(addr => addr.CompanyName)
>                                                           .Select(comp => comp.CompanyName);  
> ```

> Use `orderby`
> ```C#
> //SQL way of doing 
> var companyNames = from a in addresses
>                    orderby a.CompanyName
>                    select a.CompanyName;
>   
> ```  
##### Lambda 表达式是一种可以替代委托实例的匿名方法。编译器会立即将Lambda表达式转换为以下两种形式之一：
- 一个委托实例
- 一个类型为Expression<TDelegate> 的表达式🌲。该表达式🌲将Lambda表达式内部的代码表现为一个可遍历的对象模型

##### 21.4 **group** data by the values in a field 
> use the `GroupBy` method with lambda expression
> ```C#
> using System.Linq;
> //linq way of doing
> var companiesGroupedByCountry = addresses.GroupBy(addres => addrs.Country);
> ```
  
> use `group by`
> ```C#
> //SQL way of doing
> var companiesGroupedByCountry = from a in addresses
>                                                                 group a by a.Country;  
> ```  
  
##### 21.5 **join** data held in two different collections **join** 两个不同集合中的数据
> use the `Join` method, specifying the collection with which to join, the join criteria, and the fields for the result
> ```C#
> using System.Linq;
> //linq way of doing   
> var countriesAndCustomers = customers.Select(c => new { c.FirstName, c.LastName, c.CompanyName})
>                                                                           .Join(addresses, custs => custs.CompanyName,
>                                                                           addrs => addrs.CompanyName,  
>                                                                           (custs, addrs) => new {custs.FirstName, custs.LastName, addrs.Country});
> ```

  
##### 21.6 force immediate generation of the results for a LINQ query 强迫LINQ query立即生成结果
> use `ToList()` and `ToArray()` to generate a list or an array 
> ```C#
> var allEmployees = from e in empTree.ToList<Employee>()
>                                    select e;  
> ```
  
#### 22. Operator overloading 运算符重载
##### 🔭🔭 big picture: operator overloading is to mimic arithmetic operation between instances, see following example to demonstrate all. 模拟实例之间的算术运算
> ```C#
> class Complex 
> {
>     public int Real { get; set; } //the real part of complex num
>     public int Imaginary { get; set; } //the imaginary part of complex num
>     
>       
>     //add the constructor, this constructor takes two *int* parameters and uses them to populate the *Real* and *Imaginary* properties 添加构造器，该构造器将两个 **int** 参数 
>     public Complex (int real, int imaginary)
>     {
>         this.Real = real;
>         this.Imaginary = imaginary;
>     }
>     
>       
>     //Override the ToString method 覆盖ToString 方法
>     //...
>     public override string ToString()
>     {
>         return $({this.Real} + {this.Imaginary}i);
>     }
>     
>       
>     //add the overloaded + operator to the complex class 添加重载 + 运算符到 复杂 类
>     //...
>     public static Complex operator + (Complex lhs, Complex rhs)
>     {
>         return new Complex (lhs.Real + rhs.Real, lhs.Imaginary + rhs.Imaginary); 
>     }
>     
>     
>     //add the overloaded - operator to the complex class 添加重载 - 运算符到 复杂 类
>     //...
>     public static Complex operator - (Complex lhs, Complex rhs)
>     {
>         return new Complex (lhs.Real - rhs.Real, lhs.Imaginary - rhs.Imaginary);  
>     }
>
>     
>     //add the == and != operators to the Complex class 添加 == 与 != 运算符到 复杂 类
>     public static bool operator == (Complex lhs, Complex rhs)
>     {
>         return lhs.Equals(rhs);
>     }
>     // can be written as ⬇️  
>     public static bool operator == (Complex lhs, Complex rhs) => lhs.Equals(rhs);
>       
>     public static bool operator != (Complex lhs, Complex rhs)
>     {
>         return !(lhs.Equals(rhs));
>     }
>     // can be written as ⬇️
>     public static bool operator != (Complex lhs, Complex rhs) => !(lhs.Equals(rhs));
>       
>  
>     
>     //implement * operator and /operator 实施* 运算符 与 /运算符
>     //...
>     public static Complex operator *(Complex lhs, Complex rhs)
>     {
>         return new Complex (lhs.Real * rhs.Real - lhs.Imaginary * rhs.Imaginary,
>                             lhs.Imaginary * rhs.Real + lhs.Real * rhs.Imaginary);  
>     }
>     
>     public static Complex operator /(Complex lhs, Complex rhs)
>     {
>         int realElement = (lhs.Real * rhs.Real + lhs.Imaginary * rhs.Imaginary) / 
>                           (rhs.Real * rhs.Real + rhs.Imaginary * rhs.Imaginary);
>         int imaginaryElement = (lhs.Imaginary + rhs.Real - lhs.Real * rhs.Imaginary) /
>                                (rhs.Real * rhs.Real + rhs.Imaginary * rhs.Imaginary);
>         return new Complex(realElement, imaginaryElement);  
>     }
>     
>     //
>     static void doWork()
>     {
>         Complex first = new Comlex(10, 4);
>         Complex second = new Complex(5, 2);
>           
>         Console.WriteLine ($"first is {first}");
>         Console.WrireLine ($"second is {second}");
>         
>         Complex temp = first + second;
>         Console.WriteLine ($"Add: result is {temp}");
>  
>         temp = first - second;
>         Console.WriteLine($"Substract: result is {temp}");
>           
>         temp = first * second;
>         Console.WriteLine($"Multiply: result is {temp}");
>           
>         temp = first / second;
>         Console.WriteLine($"Divide: result is {temp}");    
>     }
>     
>     //override the `Equals` method
>     public override bool Equals(object obj)
>     {
>         if (obj is Complex)
>         {
>             Complex compare = (Complex)obj;
>             return (this.Real == compare.Real) && (this.Imaginary == compare.Imaginary);  
>         }
>         else
>         {
>             return false;  
>         }
>     }
>     // `int` TO => `Complex instance` can be implicit 隐式转换
>     public static implicit operator Complex(int from) => new Complex(from);
>     // `Complex instance` TO => `int` has to be explicit 显式转换
>     public static explicit operator int (Complex complex) => complex.Real;
> }
> 
having everything set up, we can take advantage of the `overloaded` operator
> ```C#
> Complex first = new Complex(10, 4);
> Complex second = new Complex(5, 2);
> Complex temp = first + second //since the `+` is overloaded for Complex class, this operation is valid 
> //since the `==` is overloaded for Complex class
> //the two instance can be compared under the way defined above
> if (temp==first)
> {
>     Console.WriteLine("Comparison: temp == first");  
> }  
> else
> {
>     Console.WriteLine("Comparison: temp!= first");  
> }
> //since from `complex instance` TO=> `int` is implicitly overloaded, this operation is valid 
> temp += 2;
> Console.WriteLine($"Value after adding 2: temp = {temp}");
>  
> //since from `int` TO => `complex instance`, this operation is valid
> int tempInt = (int)temp; //use `(int)` to unbox explicitly
> Console.WriteLine($"Int value after conversion: tempInt == {tempInt}");  
> ```

### BUILDING UNIVERSAL WINDOWS PLATFORM APPLICATIONS WITH C#
#### 23. Improving throughput by using tasks 通过使用任务提高吞吐量
> ##### 23.1. create a task and run it 创建一个任务并运行
> 📌 use the `Task` class and suppose there is a void method 
> ```C#
> private void doWork()
> {
>         //the task runs this code when it is started ...  
> }  
> ``` 
  
> a.create and `Run` the task in a single step 在单一步骤创建 并运行任务
> ```C#
> Task task = Task.Run(() => doWork());
> ```
> b.reference the method and `Start` it 
> ```C#
> Task task = new Task(doWork); task.Start();
> ```

  
> ##### 23.2. **Wait** for a task to finish
> use `Wait` 使用⌛️
> ```C#
> Task task = ...;
> //...
> task.Wait();  
> ```
  
> Use `await`(only legal in `async` method) 在异步方法中才合法 
> ```C#
> await task;
> ```  
  
> ##### 23.3. **Wait** for **all** tasks to finish 等待⌛️任务结束
> Use `WaitAll` method 使用 `WaitAll` 方法
> ```C#
> Task task1 = ...;
> Task task2 = ...;
> Task task3 = ...;
> Task task4 = ...;
> //...
> Task WaitAll(task1, task2, task3, task4);
> ```  

  
> ##### 23.4. Continue a task after last task finished 在最后的任务结束 后继续一个任务
> Use `ContinueWith`
> ```C#
> Task task = new Task(doWork);
> task.ContinueWith(doMoreWork, TaskContinuationOptions.NotOnFaulted);
> ```
  
##### 23.5 **Parallel** Computing 平行计算
> Use `Parallel.For` or `Parallel.ForEach` to iterate parallely
> ```C#
> private void performLoopProcessing(int x)
> {
>         // perform loop processing  
> }
> //...
> Parallel.For(0, 100, performLoopProcessing);
> ```

> use `Parallel.Invoke` to perform concurrent method with multiple tasks `Parallel.Invoke` 执行同时发生的方法 多任务👥
> ```C#
> Parallel.Invoke(doWork, doMoreWork, doYetMoreWork);  
> ```

##### 23.6 **handle exceptions** raised by one or more tasks 处理例外 
> ```C#
> //1. catch the aggregate exception
> try 
> {
>     Task task = Task.Run(...)  
> }
> catch (AggregateException ae)
> {
>     ae.Handle(handleException); 
> }  
> //2. Check which bunch of exceptions are in aggregate exceptions
> private bool handleException(Exception e)
> {
>     if(e is TaskCanceledException)
>     {
>         //...
>         return true;  
>     }
>     else
>     {
>         return false;  
>     }  
> }  
> ```


##### 23.7. Enable cancellation in a task
> a. create a `CancellationTokenSource` object 
> b. put `CancellationToken` in method
> c. call `ThrowIfCancellationRequested` to throw `OperationCanceledException`
> d. terminate this task
> ```C#
> private void generateGraphData(..., CancellationToken token)
> {
>     //...
>     token.ThrowIfCancellationRequested();
> }  
> ```


#### 24. Improving response time by performing asynchronous operations 通过执行异步操作缩短响应时间
#### Problem ❓ and Solution 🔨
#### the problem ❓: 
##### suppose that you define a method called `slowMethod()` which is invoked by a UI event, e.g. displays a message in a _TextBox_ control on the screen. 
if you invoke `slowMethod()` method from a piece of **UI code** e.g. _Click_ event handler for a button control, the **UI** will become unresponsive until the method runs through one by one.
  
> ```C#
> private void slowMethod()
> {
>     doFirstLongRunningOperation();
>     doSecondLongRunningOperation();
>     doThirdLongRunningOperation();
>     message.Text = "Processing Completed"
> }
> private void doFirstLongRunningOperation()
> {
>     //...
> }
> private void doSecondLongRunningOperation()
> {
>     //...
> }
> private void doThirdLongRunningOperation()
> {
>     //...
> }
> ```

#### the solution
#### 1⃣️: implement with `Task t` 👎
##### make the _slowMethod_ method more responsive by using a _Task_ object to run the _doFirstLongRunningOperation_ method and define continuations for the same _Task_ that run the _doSecondLongRunningOperation_ and _doThirdLongRunningOperation_ methods in turn 
> ```C#
> private void slowMethod()
> {
>     Task task = new Task(doFirstLongRunningOperation);
>     task.ContinueWith(doSecondLongRunningOperation);
>     task.ContinueWith(doThirdLongRunningOperation);
>     task.Start();
>     message.Text = "Processing Completed"; //When does this message appear?
> }
> private void doFirstLongRunningOperation()
> {
>     //...  
> }
> private void doSecondLongRunningOperation(Task t)
> {
>     //...  
> }  
> private void doThirdLongRunningOperation(Task t)
> {
>     //...  
> }  
> ```

❌the following problem is that the `message.Text` does not wait for `Task t` end, the message pop up right after `task.Start()` or we can say while the `"Processing Completed"` is being performed.


#### 2⃣️ implement `Task` with `wait`
> ```C#
> private void slowMethod()
> {
>     Task task = new Task(doFirstLongRunningOperation);
>     task.ContinueWith(doSecondLongRunningOperation);
>     task.ContinueWith(doThirdLongRunningOperation);
>     task.Start();
>     task.Wait();  
>     message.Text = "Processing Completed";  
> }
> ```  
❌the call to `Wait()` method blocks the thread executing the `slowMethod()` method and make using `Task` in the first place meaningless
⚠️⚠️⚠️ gp you should _never_ call the _Wait_ method directly in the UI thread. 

  
##### 3⃣️ implement `Task` with defined continuation 
> ```C#
> private void slowMethod()
> {
>     Task task = new Task(doFirstLongRunningOperation);
>     task.ContinueWith(doSecondLongRunningOperation);
>     task.ContinueWith(doThirdLongRunningOperation);
>     task.ContinueWith((t) => message.Text = "Processing Complete");
>     task.Start();  
> }  
> ```
  
❌run code in Debug mode, you will find that the final continuation generates a _System.Exception_ "the application call an interface that was marshaled for a different thread."
  
  
##### 4⃣️display the message required by the _slowMethod_ from a continuation, and use `Dispatcher`.😯👌
> ```C#
> private void slowMethod()
> {
>     Task task = new Task(doFirstLongRunningOperation);
>     task.ContinueWith(doSecondLongRunningOperation);
>     task.ContinueWith(doThirdLongRunningOperation);
>     task.ContinueWith((t) => this.Dispatcher.RunAsync(CoreDispatcherPriority).Normal,
>     () => message.text = "Processing Complete");
>     task.Start();
> }
> ```
❌messy and difficult to maintain, have a delegate (the continuation) specifying another delegate(the code to be run by _RunAsync_) 
the `_Dispatcher_` object is a component of the UI infrastructure, and you can send it requests to perform work on the UI thread by calling its `_RunAsyn_` method


The solution 🔨🔨🔨
the keyword `async` and `await` in C# is to enable you to define and call methods that can run asynchronously. you dont have to concern with specifying continuations or scheduling code to run on _Dispatcher_ objects to ensure that data is manipulated on the correct thread.

async:

does ✔️: 
specify that the code in the method can be divided into one or more continuations, when these continuations run, they execute on the same thread as the original method call.
does not ❌: 
the _async_ modifier does not signify that a method runs asynchronously on a seperate thread.

await: 
does ✔️: 
does not ❌: 
  
##### the _slowMethod_ method implemented as an asynchronous method with the _async_ modifier and _await_ operators
> ```C#
> private async void slowMethod()
> {
>     await doFirstLongRunningOperation();
>     await doSecondLongRunningOperation();
>     await doThirdLongRunningOperation();
>     message.Text = "Processing Complete";
> }
> ``` 



#### 25. Implementing the user interface for a Universal Windows Platform app 实现通用Windows平台应用的用户界面
#### 26. Displaying and searching for data in a universal Windows Platform app 在通用windows 平台应用中显示和查询数据
#### 27. Accessing a remote database from a universal Windows Platform app 从通用Windows 平台应用访问远程数据库

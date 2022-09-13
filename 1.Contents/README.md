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
> 
> ```

#### 3. Writing methods and applying scope 书写方法✍️、应用范围
#### 4. Using decision statements 决策语句
#### 5. Using compound assignment and iteration statements 复合赋值与迭代语句
#### 6. Managing errors and exceptions 管理错误与异常

### THE C# OBJECT MODEL
#### 7. Creating and managing classes and objects 创建与管理类、与对象
#### 8. Understanding values and references 了解🫡值与引用
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

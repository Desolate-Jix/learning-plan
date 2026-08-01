# Java / Python / C# 基础语法对照

> 建立日期：2026-08-01（新西兰时间）  
> 用途：在学习 Python 和 C# 时，以已经使用过的 Java 为参照，快速检查相同概念在三种语言中的写法。

## 一、整体差异

| 项目 | Java | Python | C# |
|---|---|---|---|
| 类型系统 | 静态类型 | 动态类型 | 静态类型 |
| 编译检查 | 较严格 | 很多问题在运行时暴露 | 较严格 |
| 代码块 | `{}` | 缩进 | `{}` |
| 语句结尾 | 通常需要 `;` | 不需要 `;` | 通常需要 `;` |
| 命名习惯 | `camelCase` | `snake_case` | 变量常用 `camelCase`，公开成员常用 `PascalCase` |
| 常见用途 | 企业后端、Android、算法 | 自动化、数据、AI、后端 | .NET 后端、桌面、Unity |

---

## 二、变量与基本类型

### Java

```java
int age = 24;
double height = 1.67;
String name = "Jix";
boolean isStudent = true;
```

### Python

```python
age = 24
height = 1.67
name = "Jix"
is_student = True
```

### C#

```csharp
int age = 24;
double height = 1.67;
string name = "Jix";
bool isStudent = true;
```

### 快速对照

| 概念 | Java | Python | C# |
|---|---|---|---|
| 整数 | `int` | `int` | `int` |
| 小数 | `double` | `float` | `double` |
| 字符串 | `String` | `str` | `string` |
| 布尔值 | `boolean` | `bool` | `bool` |
| 真 | `true` | `True` | `true` |
| 假 | `false` | `False` | `false` |
| 空值 | `null` | `None` | `null` |

Python 变量可以在运行时改变类型：

```python
value = 10
value = "hello"
```

Java 和 C# 的变量类型确定后通常不能随意改变：

```java
int value = 10;
// value = "hello"; // 编译错误
```

```csharp
int value = 10;
// value = "hello"; // 编译错误
```

C# 的 `var` 只是让编译器推断类型，不是动态类型：

```csharp
var age = 24; // 推断为 int
// age = "hello"; // 仍然是编译错误
```

---

## 三、输出

### Java

```java
System.out.println("Hello");
System.out.print("Hello");
```

### Python

```python
print("Hello")
```

### C#

```csharp
Console.WriteLine("Hello");
Console.Write("Hello");
```

---

## 四、字符串插值与拼接

### Java

```java
String name = "Jix";
int age = 24;
System.out.println("Hello, " + name + ". You are " + age + ".");
```

### Python

```python
name = "Jix"
age = 24
print(f"Hello, {name}. You are {age}.")
```

### C#

```csharp
string name = "Jix";
int age = 24;
Console.WriteLine($"Hello, {name}. You are {age}.");
```

记忆：

```text
Python：f"...{变量}..."
C#：    $"...{变量}..."
Java：  通常使用 + 拼接，或使用格式化方法
```

---

## 五、用户输入

### Java

```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
System.out.print("Enter your name: ");
String name = scanner.nextLine();
```

### Python

```python
name = input("Enter your name: ")
```

### C#

```csharp
Console.Write("Enter your name: ");
string name = Console.ReadLine();
```

三种语言读取控制台输入时，最常见的原始结果都是字符串。

---

## 六、字符串转换为数字

### Java

```java
int age = Integer.parseInt("24");
double price = Double.parseDouble("19.9");
String text = String.valueOf(123);
```

### Python

```python
age = int("24")
price = float("19.9")
text = str(123)
```

### C#

```csharp
int age = int.Parse("24");
double price = double.Parse("19.9");
string text = 123.ToString();
```

### 更安全的转换

C#：

```csharp
bool success = int.TryParse(input, out int age);
```

Java 常见做法是捕获异常：

```java
try {
    int age = Integer.parseInt(input);
} catch (NumberFormatException e) {
    System.out.println("Invalid number");
}
```

Python 常见做法也是捕获异常：

```python
try:
    age = int(text)
except ValueError:
    print("Invalid number")
```

重要提醒：

```python
bool("no")
```

结果是 `True`，因为非空字符串都是真值。布尔输入应显式比较：

```python
answer = input("yes/no: ").strip().lower()
is_student = answer == "yes"
```

---

## 七、条件判断

### Java

```java
if (age < 18) {
    System.out.println("Minor");
} else if (age < 65) {
    System.out.println("Adult");
} else {
    System.out.println("Senior");
}
```

### Python

```python
if age < 18:
    print("Minor")
elif age < 65:
    print("Adult")
else:
    print("Senior")
```

### C#

```csharp
if (age < 18)
{
    Console.WriteLine("Minor");
}
else if (age < 65)
{
    Console.WriteLine("Adult");
}
else
{
    Console.WriteLine("Senior");
}
```

Python 使用缩进表示代码块，通常每一级使用 4 个空格。

---

## 八、比较和逻辑运算符

| 含义 | Java | Python | C# |
|---|---|---|---|
| 等于 | `==` | `==` | `==` |
| 不等于 | `!=` | `!=` | `!=` |
| 并且 | `&&` | `and` | `&&` |
| 或者 | `\|\|` | `or` | `\|\|` |
| 取反 | `!` | `not` | `!` |

Python 支持连续比较：

```python
if 18 <= age < 65:
    print("Adult")
```

对应 Java / C#：

```java
if (age >= 18 && age < 65) {
    System.out.println("Adult");
}
```

```csharp
if (age >= 18 && age < 65)
{
    Console.WriteLine("Adult");
}
```

判断布尔变量时，三种语言都可以直接判断：

```java
if (isStudent) { }
```

```python
if is_student:
    pass
```

```csharp
if (isStudent) { }
```

---

## 九、字符串常用操作

| 操作 | Java | Python | C# |
|---|---|---|---|
| 去除两端空白 | `text.trim()` | `text.strip()` | `text.Trim()` |
| 转小写 | `text.toLowerCase()` | `text.lower()` | `text.ToLower()` |
| 转大写 | `text.toUpperCase()` | `text.upper()` | `text.ToUpper()` |
| 是否以某内容开头 | `text.startsWith("a")` | `text.startswith("a")` | `text.StartsWith("a")` |
| 是否以某内容结尾 | `text.endsWith("a")` | `text.endswith("a")` | `text.EndsWith("a")` |
| 是否包含 | `text.contains("a")` | `"a" in text` | `text.Contains("a")` |
| 字符串长度 | `text.length()` | `len(text)` | `text.Length` |

命名规律：

```text
Java：  多为 camelCase，例如 toLowerCase()
Python：多为 snake_case，例如 startswith()、is_student
C#：    公共方法多为 PascalCase，例如 ToLower()、StartsWith()
```

---

## 十、空值判断

### Java

```java
if (result == null) {
    System.out.println("No result");
}
```

### Python

```python
if result is None:
    print("No result")
```

### C#

```csharp
if (result == null)
{
    Console.WriteLine("No result");
}
```

Python 推荐使用 `is None` 和 `is not None`，而不是 `== None`。

---

## 十一、同一个健身房价格程序的三种写法

规则：

```text
年龄小于 18：15 元
否则如果是学生：20 元
否则：30 元
```

### Java

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = Integer.parseInt(scanner.nextLine());

        System.out.print("Are you a student? yes/no: ");
        String answer = scanner.nextLine().trim().toLowerCase();
        boolean isStudent = answer.equals("yes");

        int price;

        if (age < 18) {
            price = 15;
        } else if (isStudent) {
            price = 20;
        } else {
            price = 30;
        }

        System.out.println("Your membership price is $" + price + ".");
    }
}
```

### Python

```python
age = int(input("Enter your age: "))
answer = input("Are you a student? yes/no: ").strip().lower()
is_student = answer == "yes"

if age < 18:
    price = 15
elif is_student:
    price = 20
else:
    price = 30

print(f"Your membership price is ${price}.")
```

### C#

```csharp
Console.Write("Enter your age: ");
int age = int.Parse(Console.ReadLine());

Console.Write("Are you a student? yes/no: ");
string answer = Console.ReadLine().Trim().ToLower();
bool isStudent = answer == "yes";

int price;

if (age < 18)
{
    price = 15;
}
else if (isStudent)
{
    price = 20;
}
else
{
    price = 30;
}

Console.WriteLine($"Your membership price is ${price}.");
```

---

## 十二、快速检查表

### 从 Java 切换到 Python

- `String` 改成 `str`，但通常不写类型声明；
- `boolean` 改成 `bool`，值写作 `True / False`；
- `null` 改成 `None`；
- `&& / || / !` 改成 `and / or / not`；
- `else if` 改成 `elif`；
- 删除 `{}` 和 `;`，改用冒号与缩进；
- `System.out.println()` 改成 `print()`；
- `Scanner` 改成 `input()`；
- `Integer.parseInt()` 改成 `int()`；
- 字符串内容比较直接用 `==`。

### 从 Java 切换到 C#

- `String` 常写成 `string`；
- `boolean` 改成 `bool`；
- `System.out.println()` 改成 `Console.WriteLine()`；
- `Scanner.nextLine()` 改成 `Console.ReadLine()`；
- `Integer.parseInt()` 改成 `int.Parse()` 或 `int.TryParse()`；
- 字符串插值使用 `$"...{变量}..."`；
- 条件语法、花括号、分号和逻辑运算符与 Java 基本相同；
- C# 字符串方法通常以大写字母开头，例如 `Trim()`、`ToLower()`。

## 本页后续补充顺序

```text
下一次：for、while、range、函数、return
之后：数组 / list、tuple、切片、Dictionary / dict、HashSet / set
再之后：class、构造方法、异常、文件与 async / await
```

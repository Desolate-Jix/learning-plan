# 每日知识与错题复习笔记

> 这份文档用于保存每天真正学到的知识，而不只是记录“做了哪道题”。以后每次反馈后，继续在这里追加：知识点、提问、语法错误、原始代码、代码审查、改进写法和复习题。

## 使用方法

复习某一天时，按以下顺序阅读：

1. 先看“今日结论”，回忆当天解决了什么问题；
2. 再看“知识点与案例”，确认自己是否真的理解；
3. 查看“语法错误记录”，避免重复犯错；
4. 对照“我的代码”和“改进写法”；
5. 最后闭卷回答“复习检查题”。

---

# Day 1｜2026-07-13｜Java 字符串、循环与第一道 LeetCode

## 1. 今日结果

- **题目：** [1768. Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
- **中文：** 交替合并字符串
- **结果：** Accepted，108 / 108 测试通过
- **掌握等级：** B——主要解题思路由自己提出，在 Java 语法提示下完成
- **自己的核心思路：**
  1. 同时读取两个字符串当前位置的字符；
  2. 按 `word1`、`word2` 的顺序拼接；
  3. 一个字符串先结束后，再追加另一个字符串剩余的字符。

这个思路是正确的。当天的主要困难不是算法，而是 Java 语法、循环边界和字符串操作还不熟练。

---

## 2. 知识点与具体案例

### 2.1 变量：声明、初始化、赋值不是同一件事

#### 声明并初始化

```java
int a = 0;
String word = "";
```

含义：创建变量，并给它一个初始值。

#### 后续赋值

```java
a = 1;
word = word + "a";
```

含义：变量已经存在，现在把新值保存进去。

#### 当天问到的问题

下面为什么不行？

```java
String word = word + "a";
```

因为 Java 会先计算等号右边：

```java
word + "a"
```

但此时左边正在创建的 `word` 还没有完成初始化，右边无法使用它。

正确写法：

```java
String word = "";
word = word + "a";
```

可以把它理解为：必须先准备一个盒子，才能读取盒子里的旧内容并放入新内容。

---

### 2.2 `=` 和比较运算符的区别

#### `=`：赋值

```java
int a = 0;
```

表示把 `0` 保存到变量 `a`。

#### `<`、`<=`、`>`、`>=`：比较

```java
a < word1.length()
```

这不是创建变量，而是在得到一个布尔值：

```text
true 或 false
```

所以当天这句不成立：

```java
int a <= word1.length();
```

`int a` 表示“声明整数变量”，但 `<=` 表示“比较”，二者不能这样连在一起。

比较条件应该放在 `if`、`for` 或 `while` 中：

```java
if (a < word1.length()) {
    // 只有条件为 true 才执行
}
```

---

### 2.3 `if`：判断一次，决定一段代码要不要执行

基本格式：

```java
if (条件) {
    条件成立时执行的代码;
}
```

案例：

```java
if (word1.length() > word2.length()) {
    System.out.println("word1 更长");
}
```

`if` 本身不会重复执行。它只是到达这里时检查一次条件。

当天代码中，外层写过：

```java
if (a <= word1.length() && b <= word2.length()) {
    for (...) {
        ...
    }
}
```

这里的外层 `if` 没有必要，因为 `a`、`b` 都从 `0` 开始，而且题目保证字符串非空；真正负责决定是否继续重复的是内部循环。

一句话区分：

- `if`：要不要做一次；
- `for` / `while`：要不要继续重复做。

---

### 2.4 `for`：适合下标遍历或已知重复规律

固定格式：

```java
for (初始化; 继续条件; 每轮更新) {
    循环体;
}
```

案例：打印字符串中的每个字符：

```java
String word = "abc";

for (int i = 0; i < word.length(); i++) {
    System.out.println(word.charAt(i));
}
```

执行过程：

| 轮次 | `i` | 条件 `i < 3` | 读取字符 |
|---|---:|---|---|
| 1 | 0 | true | `a` |
| 2 | 1 | true | `b` |
| 3 | 2 | true | `c` |
| 4 | 3 | false | 结束 |

当天曾写过：

```java
for (a = 0, b = 0; a <= word1.length, b <= word2.length; a++, b++)
```

这里有三个问题：

1. 字符串长度应写成 `length()`；
2. 条件区不能用逗号表达“同时成立”，应使用 `&&`；
3. 下标通常应使用 `< length()`，不能访问下标 `length()`。

正确结构示例：

```java
for (a = 0, b = 0;
     a < word1.length() && b < word2.length();
     a++, b++) {
    // 使用 a 和 b
}
```

`for` 的初始化区和更新区可以用逗号同时处理多个变量，但中间的条件区最终必须是一个 `true` 或 `false` 的布尔表达式。

---

### 2.5 `while`：只要条件成立，就继续重复

基本格式：

```java
while (条件) {
    循环体;
    更新变量;
}
```

这道题的参考写法：

```java
int i = 0;

while (i < word1.length() && i < word2.length()) {
    // 读取两个字符串的第 i 个字符
    i++;
}
```

适合这道题的原因：我们不知道哪个字符串先结束，只需要表达“两个字符串都还有字符时继续”。

`for` 和 `while` 都能完成这道题，重点不是谁绝对更好，而是哪一种能把逻辑写得更清楚。

---

### 2.6 `&&` 和 `||`

#### `&&`：两个条件都必须成立

```java
i < word1.length() && i < word2.length()
```

含义：只有两个字符串在下标 `i` 都还有字符，才进入循环。

#### `||`：至少一个条件成立

```java
i < word1.length() || i < word2.length()
```

含义：只要任意一个字符串还有字符，就继续。

当天曾在循环条件中使用逗号：

```java
a < word1.length(), b < word2.length()
```

Java 的循环条件不能用逗号连接两个判断，应根据语义选择 `&&` 或 `||`。

---

### 2.7 字符串的 `length()`

Java 字符串使用方法：

```java
word.length()
```

Java 数组使用字段：

```java
nums.length
```

需要记住：

```text
String：length()
数组：length
```

当天出现过：

```java
word1.length
```

编译器把 `length` 当成了一个不存在的变量，所以出现：

```text
cannot find symbol: variable length
```

---

### 2.8 下标为什么必须小于长度

字符串：

```text
word = "abc"
长度 = 3
```

合法下标：

```text
0 -> a
1 -> b
2 -> c
```

不存在下标 `3`。

因此正确条件通常是：

```java
i < word.length()
```

下面虽然与 `< length()` 等价，但更绕：

```java
i <= word.length() - 1
```

下面会越界：

```java
i <= word.length()
```

因为当 `i == word.length()` 时，再调用 `charAt(i)` 会访问不存在的位置。

---

### 2.9 `charAt(i)`：取得字符串指定下标的字符

```java
String word = "abc";

char first = word.charAt(0);  // 'a'
char second = word.charAt(1); // 'b'
```

当天曾误写：

```java
chatAt(a)
```

正确拼写：

```java
charAt(a)
```

返回值类型是 `char`，例如 `'a'`，不是完整的 `String`。

---

### 2.10 `return`：把方法结果交还给调用者

方法声明：

```java
public String mergeAlternately(String word1, String word2)
```

这里的 `String` 表示：这个方法承诺最后返回一个字符串。

所以结束前必须写：

```java
return word;
```

否则会出现：

```text
missing return statement
```

可以理解为：调用者执行下面代码时正在等待结果。

```java
String result = mergeAlternately("abc", "pqr");
```

没有 `return`，Java 就不知道该把什么放进 `result`。

---

### 2.11 `String` 拼接和 `StringBuilder`

#### 当天自己的写法

```java
String word = "";
word = word + "a";
word = word + "b";
```

这个写法是合法的，也能得到 `"ab"`。

但是 Java 的 `String` 不可修改。每一次 `word + 新内容` 都需要创建新的字符串，并复制之前的内容。

循环次数很少时问题不大；字符串较长时，会产生较多临时对象和重复复制。

#### 更适合循环拼接的写法

```java
StringBuilder result = new StringBuilder();
result.append('a');
result.append('b');

return result.toString();
```

`StringBuilder` 像一个可以继续扩展的字符容器，`append()` 会在其中追加内容。

提前指定容量：

```java
StringBuilder result = new StringBuilder(word1.length() + word2.length());
```

因为最终结果长度一定等于两个字符串长度之和，这样通常可以减少内部扩容。

---

### 2.12 `substring()`：取得一段字符串

```java
String word = "pqrs";
String rest = word.substring(2, 4);
```

结果：

```text
"rs"
```

范围规则：

```text
包含起点，不包含终点
[start, end)
```

这道题中：

```java
result.append(word1.substring(i, word1.length()));
result.append(word2.substring(i, word2.length()));
```

如果某个字符串已经刚好结束，例如 `i == word1.length()`，那么：

```java
word1.substring(i, word1.length())
```

会得到空字符串 `""`，追加空字符串不会改变结果，因此不需要再分别判断谁更长。

也可以简写：

```java
word1.substring(i)
```

表示从 `i` 一直到结尾。

---

### 2.13 编译错误、运行错误和答案错误

#### 编译错误 Compile Error

代码不符合 Java 语法，程序还没有开始运行。

案例：

```java
word1.length
chatAt(a)
```

#### 运行错误 Runtime Error

代码能编译，但执行过程中崩溃。

案例：

```java
word.charAt(word.length())
```

可能导致下标越界。

#### 答案错误 Wrong Answer

程序能正常执行，但输出与题目预期不一致。

当天先集中解决编译错误，再检查循环边界和输出，最终 Accepted。

---

## 3. 当天语法错误记录

| 当时的写法 / 错误 | 错误原因 | 正确或推荐写法 |
|---|---|---|
| `int a <= word1.length;` | 声明变量时不能使用比较符；String 的长度还漏了括号 | `int a = 0;`，比较写进条件：`a < word1.length()` |
| `int b <= word2.length;` | 同上 | `int b = 0;` |
| `word1.length` | `String` 没有名为 `length` 的变量 | `word1.length()` |
| `a <= word1.length()` | 当 `a == length()` 时，`charAt(a)` 会越界 | `a < word1.length()` |
| `a < ... , b < ...` | 循环条件需要一个布尔表达式，逗号不能表示“并且” | `a < ... && b < ...` |
| `chatAt(a)` | 方法名拼写错误 | `charAt(a)` |
| `String word = word + ...` | 右侧先读取了尚未初始化的 `word` | 先写 `String word = "";`，再拼接 |
| 赋值语句后漏写 `;` | Java 语句通常以分号结束 | `word = word + ...;` |
| 方法结束前没有返回值 | 方法声明返回 `String`，但没有交回结果 | `return word;` |
| 外层 `if` 包住整个 `for` | 不一定编译失败，但逻辑冗余，循环自身已经有继续条件 | 删除外层 `if`，让循环负责重复控制 |

### 读懂当天报错信息

```text
';' expected
```

表示编译器期待看到分号，通常检查当前行或上一行结尾。

```text
not a statement
```

表示这一段不构成合法 Java 语句，例如把比较表达式放在不允许的位置。

```text
cannot find symbol
```

表示 Java 找不到对应的变量、方法或类，常见原因是拼写错误、漏括号或变量尚未声明。

```text
missing return statement
```

表示一个有返回类型的方法，并非所有执行路径都会返回结果。

---

## 4. 当天最终 Accepted 的代码

```java
class Solution {
    public String mergeAlternately(String word1, String word2) {
        int a = 0;
        int b = 0;
        String word = "";

        if (a <= word1.length() && b <= word2.length()) {
            for (a = 0, b = 0;
                 a <= word1.length() - 1 && b <= word2.length() - 1;
                 a++, b++) {
                word = word + word1.charAt(a) + word2.charAt(b);
            }

            if (word1.length() > word2.length()) {
                for (int n = word1.length() - word2.length();
                     n > 0;
                     n--, a++) {
                    word = word + word1.charAt(a);
                }
            }

            if (word2.length() > word1.length()) {
                for (int n = word2.length() - word1.length();
                     n > 0;
                     n--, b++) {
                    word = word + word2.charAt(b);
                }
            }
        }

        return word;
    }
}
```

> 上面只调整了换行和缩进，保留当天实际通过测试的逻辑。

---

## 5. 对自己代码的审查

### 5.1 做得好的地方

1. **核心算法思路正确。** 能想到先交替遍历，再处理剩余字符。
2. **正确保留了下标位置。** 主循环结束后，`a`、`b` 正好指向尚未处理的位置。
3. **考虑了三种情况。** 两个字符串等长、`word1` 更长、`word2` 更长。
4. **经过报错逐步调试。** 没有直接复制完整答案，而是从编译失败修到 108 / 108。
5. **最终代码可以正确覆盖题目测试。**

### 5.2 可以改进的地方

#### 改进 1：外层 `if` 是多余的

```java
if (a <= word1.length() && b <= word2.length()) {
    ...
}
```

`a`、`b` 初始化为 `0`，题目字符串长度至少为 `1`，该条件一定成立。即使允许空字符串，也可以让循环自己判断是否进入。

#### 改进 2：两个同步下标可以只使用一个

主循环中 `a` 和 `b` 总是一起增加：

```java
a++, b++
```

因此可以只用一个 `i` 同时访问两个字符串。

#### 改进 3：边界表达可以更直观

当前：

```java
a <= word1.length() - 1
```

推荐：

```java
a < word1.length()
```

两者在这里含义相同，但后者是更常见、更不容易写错的下标边界。

#### 改进 4：循环中反复使用字符串 `+`

```java
word = word + ...;
```

由于 `String` 不可修改，每次都要创建并复制新字符串。随着结果增长，累计复制成本可能达到平方级。

- 当前实现：解题步骤本身是线性遍历，但循环中的反复字符串拼接可能让实际总成本接近 `O((n + m)^2)`；
- `StringBuilder` 实现：整体可以稳定保持为 `O(n + m)`。

题目长度最多只有 100，所以当前写法仍能通过，但面试中应优先使用 `StringBuilder`。

#### 改进 5：处理剩余字符可以更简单

当前分别计算两个字符串的长度差，再写两个 `for`。

可以在共同部分结束后直接追加：

```java
result.append(word1.substring(i));
result.append(word2.substring(i));
```

已经结束的字符串会贡献空字符串，仍然安全。

#### 改进 6：变量名可以更清楚

```java
a, b, word
```

可以改成：

```java
i, result
```

或在双下标场景中使用：

```java
index1, index2, result
```

---

## 6. 当天学到的更好写法

### 6.1 `StringBuilder + while + substring` 版本

```java
class Solution {
    public String mergeAlternately(String word1, String word2) {
        int i = 0;
        int length1 = word1.length();
        int length2 = word2.length();

        StringBuilder result = new StringBuilder(length1 + length2);

        while (i < length1 && i < length2) {
            result.append(word1.charAt(i));
            result.append(word2.charAt(i));
            i++;
        }

        result.append(word1.substring(i, length1));
        result.append(word2.substring(i, length2));

        return result.toString();
    }
}
```

### 6.2 逐段理解

```java
int i = 0;
```

两个字符串使用相同下标，因为共同部分中每轮都各取一个字符。

```java
StringBuilder result = new StringBuilder(length1 + length2);
```

结果总长度已知，提前设置容量。

```java
while (i < length1 && i < length2)
```

两个字符串都还有字符时，继续交替加入。

```java
result.append(word1.charAt(i));
result.append(word2.charAt(i));
```

按照题目要求，先 `word1`，再 `word2`。

```java
i++;
```

进入下一个下标。

```java
result.append(word1.substring(i, length1));
result.append(word2.substring(i, length2));
```

共同部分结束后，把两边的剩余部分都尝试追加。没有剩余部分的一方会追加空字符串。

```java
return result.toString();
```

方法要求返回 `String`，所以把 `StringBuilder` 转成字符串。

---

## 7. 两种实现对比

| 对比项 | 当天自己的版本 | 改进版本 |
|---|---|---|
| 核心思路 | 共同部分 + 单独处理剩余字符 | 共同部分 + `substring` 追加剩余字符 |
| 下标 | `a`、`b` 两个同步下标 | `i` 一个下标 |
| 拼接 | 循环中使用 `String +` | 使用 `StringBuilder.append()` |
| 循环结构 | 主 `for` + 两个剩余 `for` + 外层 `if` | 一个 `while` + 两次 `substring` |
| 可读性 | 可以理解，但分支与变量较多 | 更短、更直接 |
| 时间成本 | 反复复制旧字符串，最坏可接近平方级 | `O(n + m)` |
| 是否正确 | 正确，108 / 108 | 正确 |

重要结论：

> 自己的算法方向并没有错。改进版本主要减少冗余，并选择了更适合循环拼接的数据结构。

---

## 8. 关于 LeetCode 的 `0 ms` 与排名

参考代码显示 `0 ms`，自己的提交显示过 `9 ms`。这不能直接证明两段代码真实速度相差九倍，因为单次结果会受 JVM 预热、服务器负载、测试机器和测量粒度影响。

判断算法时优先看：

1. 时间复杂度；
2. 空间复杂度；
3. 是否创建大量临时对象；
4. 代码是否清晰、边界是否可靠。

这里参考写法的真正优势是 `StringBuilder` 和更简洁的剩余字符处理，而不是页面上某一次显示的 `0 ms`。

---

## 9. 闭卷复习检查题

先不看答案，尝试自己回答。

### 问题 1

为什么字符串使用 `length()`，数组使用 `.length`？

### 问题 2

为什么循环访问字符串时通常写：

```java
i < word.length()
```

而不是：

```java
i <= word.length()
```

### 问题 3

`if`、`for`、`while` 分别适合做什么？

### 问题 4

下面为什么错误？

```java
String result = result + "a";
```

### 问题 5

`&&` 和 `||` 有什么区别？

### 问题 6

为什么循环拼接字符串时通常推荐 `StringBuilder`？

### 问题 7

`substring(2, 5)` 包含哪些下标？

### 问题 8

`public String method()` 为什么必须返回一个字符串？

### 问题 9

请从空白写出下面结构：

```text
创建下标
创建 StringBuilder
两个字符串都还有字符时交替 append
追加两边剩余字符串
返回 String
```

<details>
<summary>点击查看简要答案</summary>

1. `String.length()` 是方法；数组的 `length` 是字段。
2. 长度为 `n` 时，合法下标是 `0` 到 `n - 1`，下标 `n` 已越界。
3. `if` 判断一次；`for` 适合按下标或明确规律重复；`while` 适合在条件成立期间继续。
4. 右侧先使用了尚未完成初始化的 `result`。
5. `&&` 要求两边都成立；`||` 只要求至少一边成立。
6. `String` 不可修改，反复 `+` 会创建并复制新字符串；`StringBuilder` 可以持续追加。
7. 包含下标 `2、3、4`，不包含 `5`。
8. 返回类型是方法对调用者的承诺，必须把对应类型的结果交回去。
9. 参考本页“当天学到的更好写法”，然后再次关闭答案重写。

</details>

---

## 10. Day 1 复习状态

- [x] 自己提出基本算法思路
- [x] 修复编译错误并 Accepted
- [x] 理解变量初始化和 `return`
- [x] 理解 `String.length()`、`charAt()` 和合法下标
- [x] 初步理解 `if`、`for`、`while`
- [x] 看懂 `StringBuilder + while + substring` 写法
- [ ] 隔天不看参考代码，独立重写改进版
- [ ] 能用自己的话解释为什么 `StringBuilder` 更合适

---

# 后续每日记录模板

## Day N｜YYYY-MM-DD｜主题

### 1. 今日结果

- 题目 / 学习主题：
- 完成结果：
- 掌握等级：
- 核心思路：

### 2. 知识点与案例

### 3. 当天提问与回答

### 4. 语法 / 逻辑错误记录

| 错误写法 | 报错或表现 | 原因 | 正确写法 |
|---|---|---|---|

### 5. 当天自己的代码

```java

```

### 6. 代码审查

- 做得好的地方：
- 可以改进的地方：
- 时间复杂度：
- 空间复杂度：

### 7. 当天学到的改进写法

```java

```

### 8. 两种写法对比

### 9. 闭卷复习检查题

### 10. 下一次复习要求

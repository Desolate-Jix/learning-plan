# Day 2｜Can Place Flowers：边界、状态更新与代码块

## 结果

- 题目：[605. Can Place Flowers](https://leetcode.com/problems/can-place-flowers/)
- 结果：Accepted，130 / 130
- 掌握等级：B
- 最终思路：分别处理长度为 1、首位、中间位置和末位；每次种花后立即把对应位置改成 `1`。

## 自己最终通过的代码

```java
class Solution {
    public boolean canPlaceFlowers(int[] flowerbed, int n) {
        int l = flowerbed.length;
        int counter = 0;

        if (l == 1 && flowerbed[0] == 0) {
            counter++;
        }

        if (l > 1) {
            if (flowerbed[0] == 0 && flowerbed[1] == 0) {
                counter++;
                flowerbed[0] = 1;
            }

            for (int i = 1; i < l - 1; i++) {
                if (flowerbed[i - 1] == 0
                        && flowerbed[i] == 0
                        && flowerbed[i + 1] == 0) {
                    flowerbed[i] = 1;
                    counter++;
                }
            }

            if (flowerbed[l - 1] == 0 && flowerbed[l - 2] == 0) {
                flowerbed[l - 1] = 1;
                counter++;
            }
        }

        return n <= counter;
    }
}
```

> 仅统一缩进，保留实际 Accepted 的逻辑。

## 调试过程与错误记录

| 问题 | 根本原因 | 修正方式 |
|---|---|---|
| 用数组长度和已有花数量推算最大可种数 | 能否种花取决于 `0/1` 的具体排列，不只取决于总数量 | 逐个位置检查左、当前、右三个位置 |
| `f;powerbed` | 变量名拼写错误，并意外插入分号 | 改为 `flowerbed` |
| `flowerbed[i] = 0` | `=` 是赋值，不是比较 | 使用 `flowerbed[i] == 0` |
| 访问 `flowerbed[i + 1]` 时出现越界 | 循环让 `i` 到达最后一个下标，导致访问下标 `length` | 中间循环限定为 `i < l - 1` |
| 长度为 1 时访问 `flowerbed[1]` | 只有下标 0，没有下标 1 | 单独处理 `l == 1`，其余逻辑放入 `l > 1` |
| `counter++` 即使条件不成立也执行 | `if` 后没有大括号，Java 只控制紧接着的一条语句 | 用 `{}` 把状态更新和计数放在同一个代码块中 |

## 今天最重要的知识

### 1. 数组边界

数组长度为 `l` 时：

```text
合法下标：0 到 l - 1
```

访问 `i + 1` 时必须保证：

```java
i < l - 1
```

访问 `i - 1` 时必须保证：

```java
i > 0
```

### 2. Java 不看缩进，只看大括号

```java
if (condition)
    action1();
action2();
```

只有 `action1()` 受 `if` 控制，`action2()` 每次都会执行。

```java
if (condition) {
    action1();
    action2();
}
```

两条语句才都受条件控制。

### 3. 做出选择后要更新状态

种花后必须执行：

```java
flowerbed[i] = 1;
```

否则检查下一个位置时，不知道刚才已经种过花，可能在相邻位置重复种植。

## Reviewer 点评

### 做得好的地方

- 能根据 Wrong Answer 的反例放弃错误的“总数量公式”；
- 能把首位、中间、末位拆开处理；
- 遇到 Runtime Error 后理解了 `i + 1` 的数组边界；
- 修复没有大括号导致的计数错误；
- 最终覆盖全部 130 个测试用例。

### 可以改进

当前写法正确，但分支较多。更通用的写法可以在一个循环中定义：

```java
boolean leftEmpty = i == 0 || flowerbed[i - 1] == 0;
boolean rightEmpty = i == flowerbed.length - 1 || flowerbed[i + 1] == 0;
```

然后统一判断。当前阶段不要求立即改写，因为你自己的首、中、末分段版本更容易理解。

## 复杂度

- 时间复杂度：`O(n)`
- 除输入数组外额外空间：`O(1)`

## 复习检查题

1. 长度为 `7` 的数组最后一个合法下标是什么？
2. 为什么 `i < l` 时不能无条件访问 `flowerbed[i + 1]`？
3. `=` 和 `==` 的区别是什么？
4. 为什么种花后要立刻把当前位置改成 `1`？
5. 为什么 Java 代码缩进正确，仍可能因为缺少 `{}` 出错？

## 后续复习

- [x] 根据具体排列逐个判断能否种花
- [x] 修复首尾数组边界
- [x] 理解 `if` 大括号对代码块范围的影响
- [x] Accepted，130 / 130
- [ ] 三天内用统一边界条件的单循环版本重写一次

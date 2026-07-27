# 面试学习进度

> 本页只保存总体进度、当前规则和每日笔记索引。详细长期安排见 `WEEKDAY_4H_STUDY_PLAN.md`；每天的知识点、代码、错误和 Reviewer 点评只写入当天唯一的 `daily/YYYY-MM-DD.md`。

## 仓库核心文件

- [LeetCode 75 白名单与完成状态](./LEETCODE_75_CHECKLIST.md)
- [工作日四小时综合学习计划](./WEEKDAY_4H_STUDY_PLAN.md)
- [截至 2026-09-22 的路线图](./ROADMAP_TO_2026-09-22.md)

## 2026-07-27 当前状态

- **当前正式进度：** 13 / 75
- **剩余：** 62 题
- **当前日期：** 2026-07-27（周一，新西兰时间）
- **目标截止：** 2026-09-22
- **理想完成第一遍：** 2026-09-08
- **缓冲完成线：** 2026-09-11
- **刷题语言：** Java
- **工作日学习时间：** 每天约 4 小时
- **周六、周日：** 固定休息
- 当前计入的 13 道题全部属于 LeetCode 75。

## 今日任务进度｜2026-07-27

### LeetCode A｜已完成

[1456. Maximum Number of Vowels in a Substring of Given Length](https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/)

- **结果：** Accepted，107 / 107；
- **难度：** Medium；
- **主题：** 固定长度滑动窗口；
- **自己的实现：**
  - 先统计第一个长度为 `k` 的窗口；
  - 后续把 `i` 作为新窗口起点；
  - 离开字符为 `s.charAt(i - 1)`；
  - 进入字符为 `s.charAt(i + k - 1)`；
  - 循环条件为 `i + k <= n`，允许最后一个窗口的右边界正好到达字符串长度；
- **调试过程：**
  - `contains()` 不能直接接收 `char`，改用 `indexOf(char) != -1`；
  - 暴力版本最初使用 `<`，漏掉最后一个合法窗口，应使用 `<=`；
  - 滑动窗口版本最初把进入下标写成 `i + k + 1`，造成越界；正确下标为 `i + k - 1`；
- **复杂度：** `O(n)` 时间，`O(1)` 额外空间；
- **掌握等级：** B+。

### LeetCode B｜待完成

[2215. Find the Difference of Two Arrays](https://leetcode.com/problems/find-the-difference-of-two-arrays/)

- **状态：** 尚未 Accepted，不计入进度；
- **主题：** HashSet、自动去重、`add()`、`contains()`、嵌套 `List`；
- 完成后今日进度将达到 **14 / 75**。

### 计算机基础｜45 分钟

```text
关系模型、主键、外键、ER、1NF / 2NF / 3NF
```

使用 `Student / Course / Enrollment` 三张表画出多对多关系，并口述主键与外键的区别、规范化为什么能减少重复。

### Python｜60 分钟

```text
变量、int / float / str / bool、True / False、if / elif / else
```

使用 Java 作参照，完成 `python_basics_day1.py`，测试三个条件分支。

详细步骤见：[2026-07-27 当天笔记](./daily/2026-07-27.md)。

## 新的固定周计划

```text
周一：LeetCode × 2 + 计算机基础 + Python
周二：LeetCode × 2 + 计算机基础 + 项目表达
周三：LeetCode × 2 + 计算机基础 + Python
周四：LeetCode × 2 + 计算机基础 + 项目表达
周五：LeetCode × 2 + 计算机基础 + C#
周六、周日：休息
```

### 每天四小时分配

```text
LeetCode 75：135 分钟
计算机基础：45 分钟
Python / C# / 项目表达：60 分钟
```

求职扫描、简历定制和投递不计入四小时，由本人另行安排。

## 每天两道题规则

1. 默认安排“一道较难 + 一道较轻”；
2. 如果第一题接近 2 小时，第二题只要求读题、手算、识别模式和写代码骨架；
3. 第二题下一工作日优先继续，未 Accepted 不计入进度；
4. Easy 独立思考 20～25 分钟，Medium 35～45 分钟；
5. 超时后依次使用：小提示 → 思路提示 → 完整题解；
6. 每周计划 10 道，最低有效目标 9 道 Accepted；
7. 周末不补题，不增加到三题。

## 计算机基础路线

每天 45 分钟，固定顺序：

```text
数据库 → 并发 → 计算机网络 → 操作系统
```

时间安排：

- 7月27日－8月7日：数据库；
- 8月10日－8月21日：并发；
- 8月24日－9月4日：计算机网络；
- 9月7日－9月11日：操作系统；
- 9月14日－9月22日：混合复习与口述。

## Python / C# / 项目表达

### Python 与 C#

- 周一：Python 新概念，对照 Java；
- 周三：Python 练习和 GUI Agent / FastAPI 代码阅读；
- 周五：C# 对照 Java；
- Python 优先于 C#；
- Python 基础稳定后再进入 FastAPI；
- 暂不同时学习 ASP.NET Core。

主题顺序：

```text
变量与类型
→ 条件判断
→ 循环与函数
→ 字符串与集合
→ dict / set、Dictionary / HashSet
→ 类与对象
→ 异常、模块、文件
→ async / await
→ FastAPI 入门
```

### 项目与面试表达

- 周二：GUI Agent 技术表达；
- 周四：行为面试、英文问答和模拟面试；
- 最终形成项目 30 秒、2 分钟、5 分钟三套讲法。

## LeetCode 进度线

| 工作周 | 理想累计 | 最低累计 |
|---|---:|---:|
| 7月27日－7月31日 | 22 / 75 | 21 / 75 |
| 8月3日－8月7日 | 32 / 75 | 30 / 75 |
| 8月10日－8月14日 | 42 / 75 | 39 / 75 |
| 8月17日－8月21日 | 52 / 75 | 48 / 75 |
| 8月24日－8月28日 | 62 / 75 | 57 / 75 |
| 8月31日－9月4日 | 72 / 75 | 66 / 75 |
| 9月7日－9月11日 | 75 / 75 | 75 / 75 |

## 每日笔记索引

| 日期 | 内容 | 当天结果 |
|---|---|---|
| [2026-07-13](./daily/2026-07-13.md) | Java 字符串、循环、Merge Strings Alternately | 1 道新题 Accepted |
| [2026-07-14](./daily/2026-07-14.md) | StringBuilder、ArrayList、数组边界 | 2 道新题 Accepted + 1 次复刷 |
| [2026-07-15](./daily/2026-07-15.md) | 同方向双指针、隐藏测试调试 | Is Subsequence Accepted |
| [2026-07-16](./daily/2026-07-16.md) | 左右双指针、字符数组、`indexOf()` | Reverse Vowels Accepted |
| [2026-07-17](./daily/2026-07-17.md) | 快慢双指针、原地修改 | Move Zeroes Accepted |
| [2026-07-18](./daily/2026-07-18.md) | 暴力优化、双指针与贪心 | Container With Most Water Accepted |
| [2026-07-20](./daily/2026-07-20.md) | 前缀和、最高海拔、中心下标 | 两道 Easy 均 Accepted |
| [2026-07-22](./daily/2026-07-22.md) | 字符串公因子、字符串 API、数学 GCD | GCD of Strings Accepted |
| [2026-07-24](./daily/2026-07-24.md) | 前缀乘积、后缀乘积、状态复用 | Product of Array Except Self Accepted |
| [2026-07-25](./daily/2026-07-25.md) | 固定长度滑动窗口、整数除法 | Maximum Average Subarray I Accepted |
| [2026-07-27](./daily/2026-07-27.md) | 滑动窗口、HashSet、数据库基础、Python 入门 | 题目 A Accepted；题目 B 待完成 |

## 已完成的 13 道官方题

1. [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
2. [Greatest Common Divisor of Strings](https://leetcode.com/problems/greatest-common-divisor-of-strings/)
3. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)
4. [Can Place Flowers](https://leetcode.com/problems/can-place-flowers/)
5. [Is Subsequence](https://leetcode.com/problems/is-subsequence/)
6. [Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)
7. [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
8. [Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
9. [Find the Highest Altitude](https://leetcode.com/problems/find-the-highest-altitude/)
10. [Find Pivot Index](https://leetcode.com/problems/find-pivot-index/)
11. [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
12. [Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)
13. [Maximum Number of Vowels in a Substring of Given Length](https://leetcode.com/problems/maximum-number-of-vowels-in-a-substring-of-given-length/)

完整勾选状态以 [LEETCODE_75_CHECKLIST.md](./LEETCODE_75_CHECKLIST.md) 为准。

## 当前掌握情况

- Is Subsequence：A；
- Reverse Vowels：算法独立性 A-，代码简洁度 B；
- Container With Most Water：B+；
- Find the Highest Altitude：B+；
- Product of Array Except Self：B+；
- Maximum Average Subarray I：B+；
- Maximum Number of Vowels in a Substring of Given Length：B+；
- 其余已完成题当前主要为 B；
- Find Pivot Index 已 Accepted，但仍需从 `O(n²)` 优化为 `O(n)`。

## 近期复习

- [ ] 用“进入下标 `i`、离开下标 `i-k`”的常见写法闭卷重写 Maximum Number of Vowels；
- [ ] 用 `windowSum / maxWindowSum` 闭卷重写 Maximum Average Subarray I；
- [ ] 用更清楚的 `leftProduct / rightProduct` 命名重写 Product of Array Except Self；
- [ ] 闭卷写出 GCD of Strings 的拼接一致性 + 长度最大公约数版本；
- [ ] 用 `totalSum + leftSum` 把 Pivot Index 重写为 `O(n)`；
- [ ] 用显式 `write / scan` 重写 Move Zeroes；
- [ ] 用 `left/right/maxArea` 重写 Container With Most Water。

复刷不重复计入 75 题进度。

## 每次生成“今日任务”的检查流程

1. 检查新西兰当前日期；
2. 读取本页和 `LEETCODE_75_CHECKLIST.md`；
3. 先处理上一工作日顺延题；
4. 选择一难一轻两道白名单未完成题；
5. 同时安排当天 45 分钟计算机基础；
6. 根据星期安排 Python、C# 或项目表达；
7. 创建或更新当天唯一的 `daily/YYYY-MM-DD.md`；
8. Accepted 后同步白名单、总体进度和当天笔记。

# 面试学习进度

> 本页只保存总体进度、当前目标和每日笔记索引。每天的知识点、代码、错误与 Reviewer 点评只保存在当天唯一的日期文件中。

## 仓库结构

```text
STUDY_PROGRESS.md                 # 当前进度与索引
ROADMAP_TO_2026-09-22.md          # 截止 9 月 22 日的总体路线
daily/
  2026-07-13.md                   # Day 1 当天唯一笔记
  2026-07-14.md                   # Day 2 当天唯一笔记
  2026-07-15.md                   # Day 3 当天唯一笔记
  2026-07-16.md                   # Day 4 当天唯一笔记
```

## 每日笔记规则

- 每个自然日只允许一个笔记文件：`daily/YYYY-MM-DD.md`；
- 当天做多道题时，全部追加到同一个日期文件；
- 每次反馈后同时更新当天日期文件和本页进度；
- 总体路线只有在截止日期或学习节奏明显变化时才更新。

## 当前目标

- **截止日期：** 2026-09-22
- **每天学习时间：** 通常约 2 小时；疲劳日可以缩短到 60～75 分钟
- **刷题语言：** Java
- **主线：** LeetCode 75
- **完整路线图：** [2026-09-22 刷题路线图](./ROADMAP_TO_2026-09-22.md)

## 每日笔记索引

| 日期 | 内容 | 当天结果 |
|---|---|---|
| [2026-07-13](./daily/2026-07-13.md) | Java 字符串、循环、Merge Strings Alternately | 1 道新题 Accepted |
| [2026-07-14](./daily/2026-07-14.md) | StringBuilder 复刷、ArrayList、线性扫描、数组边界 | 2 道新题 Accepted + 1 次复刷 |
| [2026-07-15](./daily/2026-07-15.md) | 同方向双指针、字符串边界、隐藏测试调试 | Is Subsequence Accepted；最终修复独立完成 |
| [2026-07-16](./daily/2026-07-16.md) | 左右双指针、字符数组、`indexOf()`、交换元素 | Reverse Vowels Accepted，480 / 480 |

## 当前进度

- **LeetCode 75：** 5 / 75
- **已完成题目：**
  1. [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
  2. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)
  3. [Can Place Flowers](https://leetcode.com/problems/can-place-flowers/)
  4. [Is Subsequence](https://leetcode.com/problems/is-subsequence/)
  5. [Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)
- **掌握等级：** 前三题 B；Is Subsequence 为 A；Reverse Vowels 的算法独立性为 A-、代码简洁度为 B
- **当前阶段：** 双指针；已经接触同方向双指针和左右双指针
- **本周目标：** 2026-07-19 前再完成 2 道 LeetCode 75 新题

## Day 4 完成情况｜2026-07-16

- **题目：** Reverse Vowels of a String
- **结果：** Accepted，480 / 480
- **核心算法：** 字符串转字符数组；左右下标寻找元音；交换后向中间移动
- **独立成果：** 自己完成整体算法，并指出内部使用 `if` 也能正确工作，只是每次外层循环最多移动一步
- **主要收获：**
  - 左右“指针”本质上是两个整数下标；
  - `String.toCharArray()` 与 `new String(char[])`；
  - `char` 和 `String` 的区别；
  - `indexOf()` 找不到时返回 `-1`；
  - 辅助方法不能直接读取另一个方法中的局部变量；
  - 右指针应使用 `right--`；
  - 左右双指针停止条件应为 `left < right`，不能只判断 `left != right`；
  - 内部使用 `if` 和内部使用 `while` 都可以保持 `O(n)`。
- **详细记录：** [Day 4 当天笔记](./daily/2026-07-16.md)

## 当前已掌握 / 初步接触

- 字符串下标、`length()`、`charAt()`、`substring()`；
- `StringBuilder`、`append()`、`toString()`；
- 变量初始化、作用域、`return`；
- `if`、`for`、`while` 的基本职责；
- 数组与 List 的区别；
- `List<Boolean>`、`ArrayList<>()`、`add/get/set/size`；
- 基本类型和包装类型；
- 数组边界与首尾特殊情况；
- Java 大括号决定代码块范围；
- 修改数组状态解决相邻约束问题；
- 同方向双指针；
- 左右双指针；
- `toCharArray()`、字符交换、`new String(char[])`；
- `indexOf()`；
- `char` 与 `String`；
- 局部变量作用域；
- Testcase 与 Submit 隐藏测试的区别。

## 近期需要复习

- [ ] 10～15 分钟重写 Merge Strings 优化版本
- [ ] 用直接布尔表达式重写 Kids With Candies
- [ ] 尝试 Can Place Flowers 单循环边界版本
- [ ] 用只保留一个匹配指针的简化版本重写 Is Subsequence
- [ ] 三天内用 `left/right`、`!isVowel()` 重写 Reverse Vowels 简化版

当天新题优先；复刷根据精力和实际进度安排。

## 下一道候选任务

[283. Move Zeroes](https://leetcode.com/problems/move-zeroes/)

重点将是：

- 同方向快慢双指针；
- 原地修改数组；
- 保持非零元素相对顺序；
- 区分“扫描位置”和“写入位置”。

实际任务仍以当天询问“今天的任务是什么”时的安排为准。

## 学习原则

- 数据结构采用“题目驱动、即时补充”，不重新完整听一遍基础课；
- Easy 独立思考 20～25 分钟，Medium 35～45 分钟；
- 允许查 Java 语法和 API，不应一开始搜索完整答案；
- 一道题 Accepted 后只做一次必要 Code Review，不长时间打磨基础 Easy；
- A 题每周抽查，B 题 3 天内复刷，C / D 题 48 小时内重做；
- 每次反馈记录知识点、提问、语法错误、自己的代码、调试过程、复杂度和改进写法；
- 疲劳日优先保持学习连续性，不通过强行补量透支第二天状态。

## 数据结构路线

- [ ] 数组与字符串
- [ ] HashMap 与 HashSet
- [ ] 双指针与滑动窗口
- [ ] 栈与队列
- [ ] 二分查找
- [ ] 链表
- [ ] 二叉树
- [ ] 堆与优先队列
- [ ] 图
- [ ] 回溯
- [ ] 动态规划
- [ ] 区间、贪心、位运算与 Trie

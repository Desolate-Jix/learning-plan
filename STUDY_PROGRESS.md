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
  2026-07-17.md                   # Day 5 当天唯一笔记
  2026-07-18.md                   # Day 6 当天唯一笔记
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
| [2026-07-17](./daily/2026-07-17.md) | 快慢双指针、原地修改、稳定压缩数组 | Move Zeroes Accepted，75 / 75 |
| [2026-07-18](./daily/2026-07-18.md) | 第一道 Medium、面积公式、左右双指针与贪心 | Day 6 已安排，等待反馈 |

## 当前进度

- **LeetCode 75：** 6 / 75
- **已完成题目：**
  1. [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
  2. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)
  3. [Can Place Flowers](https://leetcode.com/problems/can-place-flowers/)
  4. [Is Subsequence](https://leetcode.com/problems/is-subsequence/)
  5. [Reverse Vowels of a String](https://leetcode.com/problems/reverse-vowels-of-a-string/)
  6. [Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- **掌握等级：** 前三题 B；Is Subsequence 为 A；Reverse Vowels 算法独立性 A-；Move Zeroes 为 B
- **当前阶段：** 双指针；已经接触同方向匹配、左右扫描和快慢写入，今天进入第一道双指针 Medium
- **本周目标：** 完成今天的 Medium 后达到本周 7 / 75 目标

## 今日任务｜2026-07-18

[Container With Most Water](https://leetcode.com/problems/container-with-most-water/)

今天重点：

- 面积公式：`(right - left) * min(height[left], height[right])`；
- 为什么水位由较短的一边决定；
- 为什么每轮移动较短的一边；
- 暴力枚举所有组合是 `O(n²)`；
- 双指针版本是 `O(n)`、额外空间 `O(1)`。

详细安排见：[Day 6 当天笔记](./daily/2026-07-18.md)

今天只做这一道 Medium，不追加第二道新题。

## 当前已掌握 / 初步接触

- 字符串下标、`length()`、`charAt()`、`substring()`；
- `StringBuilder`、`append()`、`toString()`；
- 变量初始化、作用域、`return`、`void`；
- `if`、`for`、`while` 的基本职责；
- 数组与 List 的区别；
- `List<Boolean>`、`ArrayList<>()`、`add/get/set/size`；
- 基本类型和包装类型；
- 数组边界与首尾特殊情况；
- Java 大括号决定代码块范围；
- 修改数组状态解决相邻约束问题；
- 同方向匹配双指针；
- 左右双指针；
- 快慢 / 扫描与写入双指针；
- 原地修改数组；
- 稳定压缩并保持元素相对顺序；
- `toCharArray()`、字符交换、`new String(char[])`；
- `indexOf()`；
- `char` 与 `String`；
- Testcase 与 Submit 隐藏测试的区别。

## 近期需要复习

- [ ] 10～15 分钟重写 Merge Strings 优化版本
- [ ] 用直接布尔表达式重写 Kids With Candies
- [ ] 尝试 Can Place Flowers 单循环边界版本
- [ ] 用只保留一个匹配指针的简化版本重写 Is Subsequence
- [ ] 用 `left/right`、`!isVowel()` 重写 Reverse Vowels 简化版
- [ ] 三天内用显式 `write / scan` 版本重写 Move Zeroes

当天新题优先；复刷根据精力和实际进度安排。

## 学习原则

- 数据结构采用“题目驱动、即时补充”，不重新完整听一遍基础课；
- Easy 独立思考 20～25 分钟，Medium 35～45 分钟；
- 允许查 Java 语法和 API，不应一开始搜索完整答案；
- 一道题 Accepted 后只做一次必要 Code Review，不长时间打磨基础题；
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

# 面试学习进度

> 每次学习反馈后更新本页。详细知识、语法错误和代码审查保存在每日复习文件中。

## 当前目标

- **截止日期：** 2026-09-22
- **每天学习时间：** 约 2 小时
- **刷题语言：** Java
- **主线：** LeetCode 75
- **完整路线图：** [2026-09-22 刷题路线图](./ROADMAP_TO_2026-09-22.md)
- **Day 1 详细笔记：** [每日知识与错题复习笔记](./DAILY_REVIEW.md)
- **Day 2 详细笔记：** [StringBuilder、ArrayList 与线性扫描](./DAY2_REVIEW_2026-07-14.md)

## 当前进度

- **LeetCode 75：** 2 / 75
- **已完成题目：**
  1. [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
  2. [Kids With the Greatest Number of Candies](https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/)
- **当前掌握等级：** 两题均为 B
- **当前阶段：** 数组与字符串主线；通过题目即时补充 Java 集合语法
- **本周目标：** 2026-07-19 前再完成 5 道 LeetCode 75 新题

## 下一道任务

[Can Place Flowers](https://leetcode.com/problems/can-place-flowers/)

本题重点：

- 相邻位置判断；
- 数组边界处理；
- 修改数组或使用条件判断记录已种数量；
- 继续练习 `for` 循环和布尔条件。

## 学习原则

- 数据结构采用“题目驱动、即时补充”，不重新完整听一遍基础课；
- Easy 独立思考 20～25 分钟，Medium 35～45 分钟；
- 允许查 Java 语法和 API，不应一开始搜索完整答案；
- 一道题 Accepted 后只做一次必要 Code Review，不长时间打磨基础 Easy；
- A 题每周抽查，B 题 3 天内复刷，C / D 题 48 小时内重做；
- 每次反馈都记录知识点、语法错误、自己的代码和改进写法。

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

## 每日记录

### 2026-07-13｜Day 1

- **题目：** Merge Strings Alternately
- **结果：** Accepted，108 / 108
- **完成方式：** B；算法方向由自己提出，Java 语法接受提示
- **主要收获：** `length()`、`charAt()`、下标边界、变量初始化、`return`、字符串拼接
- **主要问题：** `for` 语法、漏分号、`length` / `length()`、`charAt` 拼写、字符串反复 `+`

### 2026-07-14｜Day 2

#### 任务 A：Merge Strings Alternately 优化复刷

- **结果：** Accepted
- **完成方式：** B；整体结构独立写出，查过少量语法
- **主要收获：** `new StringBuilder()`、变量作用域、`substring(start, end)` 的 `[start, end)` 规则
- **出现的错误：**
  - `New` 应写为 `new`
  - `new StringBuilder` 漏写 `()`
  - 大括号不匹配导致 `reached end of file while parsing`
  - 循环内声明的 `i` 无法在循环外使用
  - `substring` 的结束位置不包含，不能使用 `length - 1`

#### 任务 B：Kids With the Greatest Number of Candies

- **结果：** Accepted
- **完成方式：** B；两遍扫描算法由自己提出，List 语法接受提示
- **算法：** 第一遍找最大值，第二遍判断加糖后是否达到最大值
- **主要收获：**
  - 数组和 List 的区别
  - `List<Boolean>`、`ArrayList<>()`
  - `add()`、`get()`、`set()`、`size()`
  - 泛型使用 `Boolean`，不能使用基本类型 `boolean`
  - 两个线性循环仍然是 `O(n)`
- **出现的错误：**
  - `boolean candy[]` 与方法要求的 `List<Boolean>` 不匹配
  - `return candy[]` 不是合法返回语法
  - 比较表达式漏掉 `>`
  - `list<boolean>`、`Arraylist` 大小写及泛型类型错误
  - 把 List 当数组写成 `candy[b]`
- **详细记录：** [Day 2 StringBuilder、ArrayList、代码与 Reviewer 点评](./DAY2_REVIEW_2026-07-14.md)
- **计划调整：** 数组已学过，不单独重学；继续按 9 月 22 日目标加速推进 LeetCode 75

## 题目记录

| 日期 | 题目 | 结果 | 掌握等级 | 后续 |
|---|---|---|---|---|
| 2026-07-13 | Merge Strings Alternately | Accepted | B | 三天后用 10～15 分钟抽查核心循环 |
| 2026-07-14 | Kids With the Greatest Number of Candies | Accepted | B | 三天内用简化布尔表达式重写 |

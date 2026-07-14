# 面试学习进度

> 这是一份持续维护的在线学习记录。每次我反馈学习结果后，ChatGPT 需要先读取最新版本，再更新本页，并据此安排下一次任务。

## 当前状态

- **每天可学习时间：** 约 2 小时
- **刷题语言：** Java
- **主要目标：** 为 Junior / Graduate 软件开发面试准备算法、数据结构、SQL 和项目表达
- **当前基础判断：** 学过一些 Java；数据结构第一次学习时没有真正理解，因此按“第一次学懂”处理，而不是简单复习
- **学习节奏：** 每天一个小概念 + 图示/手动模拟 + 对应 Java 用法 + 一道匹配的 Easy 题
- **执行原则：** 先理解再做题，不追求短期刷题数量；学习阶段允许查 Java API 和提示，看过题解后必须关闭资料重新写
- **详细复习文档：** [每日知识与错题复习笔记](./DAILY_REVIEW.md)——保存每天的知识点、提问、语法错误、自己的代码、代码审查与改进版本

## 当前学习位置

- **正在学习：** 字符串巩固 + 数组基础
- **当前任务 1：** 闭卷重写 [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/) 的 `StringBuilder + while + substring` 版本
- **当前任务 2：** 通过任务 1 后，完成 [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/)
- **当前状态：** Day 2 已安排，等待反馈
- **下一步重点：** 理解数组是“固定长度、带下标的一排格子”，掌握 `int[]`、`nums.length`、`nums[i]`、修改数组元素和按顺序累计

## 数据结构学习路线

- [ ] 数组与字符串
- [ ] HashMap 与 HashSet
- [ ] 栈
- [ ] 队列
- [ ] 链表
- [ ] 二叉树
- [ ] 堆与优先队列
- [ ] 图
- [ ] 递归与回溯
- [ ] 动态规划

完成一个主题的标准不是“看过”，而是能够：

1. 用自己的话说明它解决什么问题；
2. 手动画出数据怎样存放和变化；
3. 使用对应的 Java 基本操作；
4. 独立或在少量提示下完成一道基础题。

## 每次反馈后的记录规则

每次学习反馈后更新以下四项：

1. **实际完成了什么；**
2. **独立完成、提示后完成、看题解后重写，还是仍未理解；**
3. **具体卡点和已经理解的部分；**
4. **下一次只安排一个清晰的主任务。**

掌握等级：

- **A：** 完全独立完成，并能解释思路；
- **B：** 看提示后完成；
- **C：** 看题解后能关闭资料重写；
- **D：** 看完后仍不能解释或重写，需要重新学习概念。

## 每日记录

### 2026-07-11｜学习档案建立

- **完成内容：** 建立在线学习进度文档，确定 Java 为刷题主语言
- **重要反馈：** 数据结构第一次学习时就没有理解，后续必须从直觉、图示和实际操作重新学习

---

### 2026-07-13｜Day 1：数组与字符串入门

- **今日任务：** [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/)
- **核心目标：** 把字符串理解成“有下标的一排格子”，掌握 `length()`、`charAt()`、结果变量初始化、循环与 `return`
- **实际完成：** 自己设计“同时遍历 + 处理剩余字符”的方案，逐步修复编译错误，最终 108 / 108 测试通过；随后阅读并理解了 `StringBuilder + while + substring` 的更简洁写法
- **完成方式：** B（在语法提示帮助下完成，主要算法思路由自己提出）
- **已经理解：**
  - `String.length()` 与数组 `.length` 的区别
  - 合法下标范围是 `0` 到 `length() - 1`
  - 变量必须先初始化才能在右侧使用
  - 返回类型为 `String` 的方法必须 `return` 一个字符串
  - 一个字符串先结束后，需要继续追加另一个字符串的剩余部分
  - `StringBuilder` 更适合循环拼接，`substring(i, length)` 可以一次追加剩余部分
- **仍需巩固：**
  - `for`、`while` 和 `if` 的职责区别
  - 更简洁的循环边界写法：`i < word.length()`
  - 独立写出 `StringBuilder + while + substring` 版本
  - 不把 LeetCode 单次 runtime 百分位当作可靠算法快慢结论
- **详细笔记：** [Day 1 知识点、语法错误、代码审查与改进写法](./DAILY_REVIEW.md#day-12026-07-13java-字符串循环与第一道-leetcode)
- **Day 1 状态：** 已完成

---

### 2026-07-14｜Day 2：字符串巩固与数组入门

- **必做任务：** 不看参考代码，使用一个下标、`StringBuilder`、`while` 和 `substring` 重写 Merge Strings Alternately
- **进入新题的条件：** 重写版本 Accepted，并能说明 `while` 什么时候停止、`substring(i)` 为什么可以处理剩余字符
- **新知识：**
  - 数组是固定长度、按下标存放相同类型数据的一排格子
  - Java 声明示例：`int[] nums = {1, 2, 3};`
  - 数组长度：`nums.length`，没有括号
  - 读取元素：`nums[i]`
  - 修改元素：`nums[i] = 新值`
- **新题：** [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/)
- **两小时安排：**
  - 0–35 分钟：闭卷重写 Day 1 改进版本
  - 35–50 分钟：对照笔记检查并再次从空白修正
  - 50–70 分钟：手动画数组下标、读取和修改过程
  - 70–110 分钟：独立完成 Running Sum，允许查 Java 数组语法，不直接搜完整答案
  - 110–120 分钟：用中文解释数组每个位置如何从旧值变成累计值
- **兜底规则：** 如果前 50 分钟仍无法独立重写，不进入新题；剩余时间继续巩固字符串与循环，这仍算正常完成 Day 2
- **完成情况：** 等待反馈

## 题目记录

| 日期 | 题目 | 主题 | 结果 | 掌握等级 | 是否需要复刷 |
|---|---|---|---|---|---|
| 2026-07-13 | [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/) | 数组与字符串 | Accepted，108 / 108；已理解参考写法 | B | 是：Day 2 用 StringBuilder 独立重写 |
| 2026-07-14 | [Running Sum of 1d Array](https://leetcode.com/problems/running-sum-of-1d-array/) | 数组基础 | 等待开始 | 未评估 | 待定 |

## SQL 与项目面试

目前先建立 Java 和数据结构基础。等基础刷题节奏稳定后，再逐步加入：

- SQL 基础题；
- Java / Spring Boot 面试知识；
- Windows GUI Agent 项目讲解；
- 英文解题和行为面试表达。

# 面试学习进度

> 本页保存当前进度、固定规则和每日笔记索引。详细长期安排见 `WEEKDAY_4H_STUDY_PLAN.md`；每天的代码、错误和 Reviewer 点评只写入当天唯一的 `daily/YYYY-MM-DD.md`。

## 核心文件

- [LeetCode 75 白名单与完成状态](./LEETCODE_75_CHECKLIST.md)
- [工作日算法 + 周六基础学习计划](./WEEKDAY_4H_STUDY_PLAN.md)
- [截至 2026-09-22 的路线图](./ROADMAP_TO_2026-09-22.md)

## 2026-07-28 当前状态

- **当前正式进度：** 14 / 75
- **剩余：** 61 题
- **当前日期：** 2026-07-28（周二，新西兰时间）
- **目标截止：** 2026-09-22
- **理想完成第一遍：** 2026-09-08
- **缓冲完成线：** 2026-09-11
- **刷题语言：** Java
- 当前计入的 14 道题全部属于 LeetCode 75。

## 固定周计划

```text
周一：LeetCode × 2
周二：LeetCode × 2；项目技术表达 20～30 分钟可选
周三：LeetCode × 2
周四：LeetCode × 2；行为 / 英文表达 20～30 分钟可选
周五：LeetCode × 2
周六：计算机基础 + Python + C#，最多 3 小时
周日：完整休息
```

调整说明：

- 工作日不再强制学习数据库、Python 或 C#；
- 两道算法题完成后，精力不足可以直接结束；
- 数据库与其他语言统一放到周六；
- 周二、周四的项目表达可跳过，不形成欠账；
- 周日不补题、不补课；
- 求职扫描、简历和投递由本人另行安排。

## 工作日两道题规则

1. 默认安排“一道较难 + 一道较轻”；
2. 如果第一题接近两小时，第二题只做题意、手算、模式、骨架和卡点；
3. 第二题下一工作日优先继续，未 Accepted 不计入进度；
4. Easy 独立思考 20～25 分钟，Medium 35～45 分钟；
5. 超时后依次使用：小提示 → 思路提示 → 完整题解；
6. 每周计划容量 10 道，最低有效目标 9 道 Accepted；
7. 周末不补题，不增加到三题。

## 周六基础学习块

```text
数据库 / 计算机基础：60 分钟
Python 对照 Java：60 分钟
C# 对照 Java：45 分钟
整理笔记与口述：15 分钟
```

精力不足时优先保留数据库和 Python，C# 可以隔周学习；周日保持休息。

学习路线：

```text
计算机基础：数据库 → 并发 → 计算机网络 → 操作系统
语言：变量与类型 → 条件 → 循环与函数 → 集合 → 类与对象 → 异常与文件 → async / await → FastAPI
```

## 今日任务｜2026-07-28

### LeetCode A｜Medium

[1004. Max Consecutive Ones III](https://leetcode.com/problems/max-consecutive-ones-iii/)

- **主题：** 可变长度滑动窗口；
- **核心状态：** `left`、`right`、`zeroCount`；
- **合法条件：** 窗口中 `0` 的数量不超过 `k`；
- **收缩规则：** `zeroCount > k` 时移动左边界；
- **目标复杂度：** `O(n)` 时间、`O(1)` 额外空间；
- **当前状态：** 等待开始与反馈。

### LeetCode B｜Easy

[1207. Unique Number of Occurrences](https://leetcode.com/problems/unique-number-of-occurrences/)

- **主题：** `HashMap` 统计出现次数 + `HashSet` 检查次数重复；
- **Java：** `put()`、`getOrDefault()`、`values()`、`Set.add()` 的布尔返回值；
- **目标平均复杂度：** `O(n)` 时间、`O(n)` 空间；
- **当前状态：** 等待开始与反馈。

### 可选项目表达｜20～30 分钟

完成一个 30 秒 GUI Agent 项目概述：项目是什么、解决什么问题、Agent / Operation / Gate / Trace 的核心边界。状态差时可以跳过，不形成欠账。

两道题都 Accepted 后，正式进度将达到 **16 / 75**。详细步骤见：[2026-07-28 当天笔记](./daily/2026-07-28.md)。

## LeetCode 进度线

当前还剩 61 题。从 2026-07-28 到 2026-09-11 还有 34 个工作日，共 68 个题位，保留 7 个题位缓冲。

| 工作周 | 理想累计 | 最低累计 |
|---|---:|---:|
| 7月27日－7月31日 | 22 / 75 | 21 / 75 |
| 8月3日－8月7日 | 32 / 75 | 30 / 75 |
| 8月10日－8月14日 | 42 / 75 | 39 / 75 |
| 8月17日－8月21日 | 52 / 75 | 48 / 75 |
| 8月24日－8月28日 | 62 / 75 | 57 / 75 |
| 8月31日－9月4日 | 72 / 75 | 66 / 75 |
| 9月7日－9月11日 | 75 / 75 | 75 / 75 |

## 已完成的 14 道官方题

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
14. [Find the Difference of Two Arrays](https://leetcode.com/problems/find-the-difference-of-two-arrays/)

完整勾选状态以 [LEETCODE_75_CHECKLIST.md](./LEETCODE_75_CHECKLIST.md) 为准。

## 当前掌握情况

- Is Subsequence：A；
- Reverse Vowels：算法独立性 A-，代码简洁度 B；
- Container With Most Water：B+；
- Find the Highest Altitude：B+；
- Product of Array Except Self：B+；
- Maximum Average Subarray I：B+；
- Maximum Number of Vowels：B+；
- Find the Difference of Two Arrays：B+；
- 其余已完成题当前主要为 B；
- Find Pivot Index 已 Accepted，但仍需从 `O(n²)` 优化为 `O(n)`。

## 近期复习

- [ ] 用“进入下标 `i`、离开下标 `i-k`”闭卷重写 Maximum Number of Vowels；
- [ ] 简化 Find the Difference of Two Arrays，直接遍历两个去重后的 Set；
- [ ] 用 `windowSum / maxWindowSum` 闭卷重写 Maximum Average Subarray I；
- [ ] 用 `leftProduct / rightProduct` 重写 Product of Array Except Self；
- [ ] 闭卷写出 GCD of Strings 的拼接一致性 + 长度 GCD 版本；
- [ ] 用 `totalSum + leftSum` 把 Pivot Index 重写为 `O(n)`；
- [ ] 用显式 `write / scan` 重写 Move Zeroes；
- [ ] 用 `left/right/maxArea` 重写 Container With Most Water。

复刷不重复计入 75 题进度。

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
| [2026-07-22](./daily/2026-07-22.md) | 字符串公因子、数学 GCD | GCD of Strings Accepted |
| [2026-07-24](./daily/2026-07-24.md) | 前后缀乘积、状态复用 | Product of Array Except Self Accepted |
| [2026-07-25](./daily/2026-07-25.md) | 固定长度滑动窗口、整数除法 | Maximum Average Subarray I Accepted |
| [2026-07-27](./daily/2026-07-27.md) | 滑动窗口、HashSet、周计划调整 | 两道 LeetCode 均 Accepted；基础学习移到周六 |
| [2026-07-28](./daily/2026-07-28.md) | 可变滑动窗口、HashMap 计数 | 今日任务已安排 |

## 每次生成“今日任务”的检查流程

### 周一至周五

1. 检查新西兰当前日期；
2. 读取本页和 `LEETCODE_75_CHECKLIST.md`；
3. 先处理上一工作日顺延题；
4. 选择一难一轻两道白名单未完成题；
5. 周二、周四可附轻量项目表达任务；
6. 创建或更新当天唯一笔记；
7. Accepted 后同步白名单、总体进度和当天笔记。

### 周六

安排数据库 / 计算机基础、Python、C#，总时长不超过三小时。

### 周日

直接说明休息，不安排必做任务。

# 面试学习进度

> 本页保存当前进度、固定规则和每日笔记索引。详细长期安排见 `WEEKDAY_4H_STUDY_PLAN.md`；每天的代码、错误和 Reviewer 点评只写入当天唯一的 `daily/YYYY-MM-DD.md`。

## 核心文件

- [LeetCode 75 白名单与完成状态](./LEETCODE_75_CHECKLIST.md)
- [工作日算法 + 周六基础学习计划](./WEEKDAY_4H_STUDY_PLAN.md)
- [截至 2026-09-22 的路线图](./ROADMAP_TO_2026-09-22.md)

## 2026-07-29 当前状态

- **当前正式进度：** 14 / 75
- **剩余：** 61 题
- **当前日期：** 2026-07-29（周三，新西兰时间）
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

- 工作日不强制学习数据库、Python 或 C#；
- 两道算法题完成后，精力不足可以直接结束；
- 周二、周四的表达任务可跳过，不形成欠账；
- 周末不补工作日 LeetCode 欠题。

## 工作日两道题规则

1. 优先处理上一工作日未完成题；
2. 默认安排“一道较难 + 一道较轻”；
3. 第一题接近两小时，第二题只做题意、手算、模式、骨架和卡点；
4. 未 Accepted 不计入进度；
5. Easy 独立思考 20～25 分钟，Medium 35～45 分钟；
6. 超时后依次使用：小提示 → 思路提示 → 完整题解；
7. 周末不补题，不增加到三题。

## 今日任务｜2026-07-29

### 任务 A｜1004. Max Consecutive Ones III

[打开题目](https://leetcode.com/problems/max-consecutive-ones-iii/)

- **状态：** 昨日未完成，今日第一优先级；
- **目标：** 从空白编辑器重写两个 `O(n)` 版本；
- **版本 1：** 标准合法窗口，`zero > k` 时持续移动 `left`；
- **版本 2：** 自己的“最大长度只增不减”版本，超限时让 `left` 同步前进一格；
- 两个版本都 Submit Accepted 后，1004 才计入进度；
- 完成后正式进度为 **15 / 75**。

### 任务 B｜1207. Unique Number of Occurrences

[打开题目](https://leetcode.com/problems/unique-number-of-occurrences/)

- **状态：** 昨日未开始，继续顺延为第二任务；
- **主题：** `HashMap` 计数 + `HashSet` 检查次数重复；
- **Java：** `put()`、`getOrDefault()`、`values()`、`Set.add()` 的返回值；
- **目标平均复杂度：** `O(n)` 时间、`O(n)` 空间；
- 两题都 Accepted 后，正式进度为 **16 / 75**。

详细任务见：[2026-07-29 当天笔记](./daily/2026-07-29.md)。

## 今日执行顺序

```text
1. 1004 标准版闭卷重写并提交
2. 1004 自己的固定长度平移版闭卷重写并提交
3. 对比两个版本的不变量
4. 精力允许时完成 1207
```

如果 1004 两个版本已经接近两小时，1207 今天只做题意、手算和骨架，不为追题量牺牲理解。

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

## 近期复习

- [ ] 1004 标准合法窗口版闭卷重写；
- [ ] 1004 固定长度平移版闭卷重写并解释不变量；
- [ ] 用“进入下标 `i`、离开下标 `i-k`”闭卷重写 Maximum Number of Vowels；
- [ ] 简化 Find the Difference of Two Arrays，直接遍历两个去重后的 Set；
- [ ] 用 `windowSum / maxWindowSum` 闭卷重写 Maximum Average Subarray I；
- [ ] 用 `totalSum + leftSum` 把 Pivot Index 重写为 `O(n)`。

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
| [2026-07-28](./daily/2026-07-28.md) | 可变滑动窗口尝试与实现复盘 | 1004 进行中；1207 顺延 |
| [2026-07-29](./daily/2026-07-29.md) | 1004 两版重写、1207 | 今日任务已安排 |

## 每次生成“今日任务”的检查流程

### 周一至周五

1. 检查新西兰当前日期；
2. 读取本页和 `LEETCODE_75_CHECKLIST.md`；
3. 先处理上一工作日顺延题；
4. 选择一难一轻两道白名单未完成题；
5. 创建或更新当天唯一笔记；
6. Accepted 后同步白名单、总体进度和当天笔记。

### 周六

安排数据库 / 计算机基础、Python、C#，总时长不超过三小时。

### 周日

直接说明休息，不安排必做任务。
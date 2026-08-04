# 面试学习进度

> 本页保存当前进度、固定规则和每日笔记索引。详细长期安排见 `WEEKDAY_4H_STUDY_PLAN.md`；每天的代码、错误和 Reviewer 点评只写入当天唯一的 `daily/YYYY-MM-DD.md`。

## 核心文件

- [LeetCode 75 白名单与完成状态](./LEETCODE_75_CHECKLIST.md)
- [工作日算法 + 周六基础学习计划](./WEEKDAY_4H_STUDY_PLAN.md)
- [Java / Python / C# 基础语法对照](./JAVA_PYTHON_CSHARP_COMPARISON.md)
- [截至 2026-09-22 的路线图](./ROADMAP_TO_2026-09-22.md)

## 2026-08-04 当前状态

- **当前正式进度：** 20 / 75
- **剩余：** 55 题
- **当前日期：** 2026-08-04（周二，新西兰时间）
- **目标截止：** 2026-09-22
- **理想完成第一遍：** 2026-09-08
- **缓冲完成线：** 2026-09-11
- **刷题语言：** Java
- 当前计入的 20 道题全部属于 LeetCode 75。

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

## 今日完成情况｜2026-08-04

### 1679. Max Number of K-Sum Pairs｜已完成

[打开题目](https://leetcode.com/problems/max-number-of-k-sum-pairs/)

- **结果：** Accepted，51 / 51；
- **难度：** Medium；
- **提交记录：** 39 ms、70.47 MB；单次排名仅作参考；
- **主题：** 两数配对、HashMap 频率计数；
- **平均复杂度：** `O(n)` 时间、`O(n)` 空间；
- **掌握等级：** B；
- **第一次实现：** 使用 `ArrayList` 查找并删除补数，逻辑正确但为 `O(n²)`，在 42 / 51 测试处 TLE；
- **最终优化：** 使用 Map 保存尚未配对数字的剩余数量，遇到补数时数量减一；
- **本题 API：** `getOrDefault()`、`get()`、`put()`，以及 `ArrayList.remove(index)` 与 `remove(Object)` 的区别。

详细代码、TLE 分析和重复数字示例见：[2026-08-04 当天笔记](./daily/2026-08-04.md)。

### 374. Guess Number Higher or Lower｜未开始

[打开题目](https://leetcode.com/problems/guess-number-higher-or-lower/)

- **原因：** 完成 1679 后需要准备晚上外出开会；
- **安排：** 下一学习日优先处理；
- **今晚不补题，不追加第三题。**

## 已完成的 20 道官方题

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
15. [Max Consecutive Ones III](https://leetcode.com/problems/max-consecutive-ones-iii/)
16. [Unique Number of Occurrences](https://leetcode.com/problems/unique-number-of-occurrences/)
17. [Longest Subarray of 1's After Deleting One Element](https://leetcode.com/problems/longest-subarray-of-1s-after-deleting-one-element/)
18. [Increasing Triplet Subsequence](https://leetcode.com/problems/increasing-triplet-subsequence/)
19. [N-th Tribonacci Number](https://leetcode.com/problems/n-th-tribonacci-number/)
20. [Max Number of K-Sum Pairs](https://leetcode.com/problems/max-number-of-k-sum-pairs/)

完整勾选状态以 [LEETCODE_75_CHECKLIST.md](./LEETCODE_75_CHECKLIST.md) 为准。

## 近期复习

- [ ] 闭卷重写 1679 的 HashMap 版本，并解释重复数字如何通过 value 计数；
- [ ] 解释 `ArrayList.remove(0)` 为什么使原方案达到 `O(n²)`；
- [ ] 用三个滚动变量把 1137 重写为 `O(1)` 额外空间；
- [ ] 闭卷重写 334，并解释 `second` 不一定和当前 `first` 配对；
- [ ] 隔一天闭卷重写 1207，不看 `HashMap` API 提示；
- [ ] 闭卷重写 1493，避免把 `j - i` 写反；
- [ ] 1004 标准合法窗口版闭卷重写；
- [ ] 用“进入下标 `i`、离开下标 `i-k`”重写 Maximum Number of Vowels；
- [ ] 用 `totalSum + leftSum` 把 Pivot Index 重写为 `O(n)`；
- [ ] 对照复习 Java / Python / C# 的输入、类型转换和条件语法。

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
| [2026-07-29](./daily/2026-07-29.md) | 1004 Accepted、标准窗口理解 | 1004 Accepted；1207 顺延 |
| [2026-07-30](./daily/2026-07-30.md) | HashMap 计数、删除一个元素的滑动窗口 | 两道题均 Accepted，进度 17 / 75 |
| [2026-07-31](./daily/2026-07-31.md) | 贪心递增三元组、Tribonacci | 两道题均 Accepted，进度 19 / 75 |
| [2026-08-01](./daily/2026-08-01.md) | 数据库范式、Python 与 C# 基础、三语言对照 | 周六基础学习完成，LeetCode 保持 19 / 75 |
| [2026-08-03](./daily/2026-08-03.md) | 锻炼、社交与主动休息 | Skip，不形成欠账 |
| [2026-08-04](./daily/2026-08-04.md) | ArrayList 暴力解、TLE、HashMap 配对计数 | 1679 Accepted，进度 20 / 75；374 未开始 |

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
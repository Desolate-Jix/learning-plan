# 面试学习进度

> 本页保存总体进度、当前目标和每日笔记索引。每天的知识点、代码、错误与 Reviewer 点评只保存在当天唯一的日期文件中。

## 仓库核心文件

```text
STUDY_PROGRESS.md                 # 当前进度与每日索引
LEETCODE_75_CHECKLIST.md          # 官方 75 题白名单与完成状态
ROADMAP_TO_2026-09-22.md          # 截止 9 月 22 日的路线图
daily/YYYY-MM-DD.md               # 每个学习日唯一笔记
```

- [LeetCode 75 白名单与检查表](./LEETCODE_75_CHECKLIST.md)
- [完整路线图](./ROADMAP_TO_2026-09-22.md)

## 防止超出 LeetCode 75 的强制规则

1. 新题只从 `LEETCODE_75_CHECKLIST.md` 中尚未完成的题目选择；
2. 不在白名单中的题目不得计入 `x / 75`；
3. 完成 75 / 75 前，默认不安排额外 LeetCode 热身题；
4. 需要热身或补基础时，只复刷已经完成的白名单题；
5. 每次安排任务前核对：题号、英文标题、链接、完成状态；
6. 每次 Accepted 后同步更新：白名单、总体进度、当天笔记。

## 2026-07-22 当前审计

- **当前正式进度：10 / 75**
- **剩余：65 题**
- 当前计入的 10 道题全部属于 LeetCode 75；
- 没有题单外题目被错误计入进度；
- `Running Sum of 1d Array`、`Two Sum II - Input Array Is Sorted` 不属于当前 LeetCode 75，不再进入主计划；
- `Product of Array Except Self` 仍属于白名单未完成题，顺延到下一个学习日。

## 当前目标

- **当前日期：** 2026-07-22
- **截止日期：** 2026-09-22
- **第一遍完成目标：** 2026-09-13
- **每天学习时间：** 通常约 2 小时；疲劳日可缩短到 60～75 分钟
- **刷题语言：** Java
- **当前进度：** 10 / 75
- **剩余：** 65 题
- **建议节奏：** 每周约 8～9 道白名单新题

## 每日笔记索引

| 日期 | 内容 | 当天结果 |
|---|---|---|
| [2026-07-13](./daily/2026-07-13.md) | Java 字符串、循环、Merge Strings Alternately | 1 道新题 Accepted |
| [2026-07-14](./daily/2026-07-14.md) | StringBuilder 复刷、ArrayList、线性扫描、数组边界 | 2 道新题 Accepted + 1 次复刷 |
| [2026-07-15](./daily/2026-07-15.md) | 同方向双指针、字符串边界、隐藏测试调试 | Is Subsequence Accepted；最终修复独立完成 |
| [2026-07-16](./daily/2026-07-16.md) | 左右双指针、字符数组、`indexOf()`、交换元素 | Reverse Vowels Accepted，480 / 480 |
| [2026-07-17](./daily/2026-07-17.md) | 快慢双指针、原地修改、稳定压缩数组 | Move Zeroes Accepted，75 / 75 |
| [2026-07-18](./daily/2026-07-18.md) | 第一道 Medium、暴力优化、左右双指针与贪心 | Container With Most Water Accepted，65 / 65 |
| [2026-07-20](./daily/2026-07-20.md) | 前缀和、最高海拔、中心下标 | 两道 Easy 均 Accepted |
| [2026-07-22](./daily/2026-07-22.md) | 字符串公因子、字符串 API、候选验证与数学 GCD 优化 | GCD of Strings Accepted；Product 顺延 |

## 已完成的 10 道官方题

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

完整勾选状态以 [LEETCODE_75_CHECKLIST.md](./LEETCODE_75_CHECKLIST.md) 为准。

## Day 8 当前情况｜2026-07-22

### 任务 1｜已完成

[1071. Greatest Common Divisor of Strings](https://leetcode.com/problems/greatest-common-divisor-of-strings/)

- **结果：** Accepted，129 / 129
- **实际用时：** 提交页面记录约 2 小时 24 分钟
- **掌握等级：** B
- **自己完成的算法：** 找最长公共前缀；从长到短缩短候选；每轮回到两个原字符串检查能否被候选重复铺满
- **已学习的标准数学优化：**
  - 先用 `(str1 + str2).equals(str2 + str1)` 判断两个字符串是否来自同一种重复结构；
  - 再用欧几里得算法求 `gcd(str1.length(), str2.length())`；
  - 返回 `str1.substring(0, gcdLength)`。
- **主要收获：**
  - `charAt()` 返回 `char`，字符使用 `==`；
  - 字符串内容使用 `.equals()`；
  - `substring(0, length - 1)` 可以删除末尾字符；
  - 同时访问两个字符串时必须受较短字符串边界保护；
  - 空候选不能参与 `%` 运算；
  - 最大公因子要求从长到短找，不能先返回最小重复单位；
  - 拼接顺序一致可以判断两个字符串是否共享同一重复单位；
  - 最长公共字符串因子的长度等于两个字符串长度的最大公约数。
- **出现并修复的问题：**
  - `char cannot be dereferenced`；
  - `StringIndexOutOfBoundsException`；
  - `ArithmeticException: / by zero`；
  - 缺少方法右大括号；
  - String 使用 `== ""`；
  - 从短到长检查导致返回非最长答案。
- **复杂度：**
  - 自己的验证法：最坏约 `O(n²)`，额外空间约 `O(n)`；
  - 数学快捷法：`O(n + m)` 时间，Java 字符串拼接带来约 `O(n + m)` 额外空间。
- **详细记录：** [2026-07-22 当天笔记](./daily/2026-07-22.md)

### 任务 2｜顺延

[238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)

- **状态：** 未开始；不计入进度；
- **顺延原因：** 第一题已超过当天两小时预算；
- **下次重点：** 左侧乘积、右侧乘积、不能使用除法、从 `O(n²)` 优化到 `O(n)`。

## 当前掌握情况

- Merge Strings Alternately：B；
- Greatest Common Divisor of Strings：B；已理解验证法与数学 GCD 优化；
- Kids With Candies：B；
- Can Place Flowers：B；
- Is Subsequence：独立调试表现 A；
- Reverse Vowels：算法独立性 A-，代码简洁度 B；
- Move Zeroes：B；
- Container With Most Water：B+；
- Find the Highest Altitude：B+；
- Find Pivot Index：当前暴力版 B，待用前缀和降为 `O(n)`。

## 近期复习

- [ ] 三天内用 `while (!candidate.isEmpty())` 重写 GCD of Strings 的验证法；
- [ ] 三天内闭卷写出 GCD of Strings 的拼接一致性 + 长度最大公约数版本；
- [ ] 用 `totalSum + leftSum` 把 Pivot Index 重写为 `O(n)`；
- [ ] 用显式 `write / scan` 重写 Move Zeroes；
- [ ] 用 `left/right/maxArea` 重写 Container With Most Water；
- [ ] 用 `left/right` 与 `!isVowel()` 重写 Reverse Vowels。

复刷不重复计入 75 题进度。

## 每次生成今日任务的检查流程

1. 检查新西兰当前日期；
2. 读取本页当前进度；
3. 读取 `LEETCODE_75_CHECKLIST.md`；
4. 确认候选题未完成且属于白名单；
5. 核对题号、标题和链接；
6. 安排 1 道 Medium，或 1～2 道 Easy；特殊补进度日可安排 1 Easy + 1 Medium，但必须都在白名单；
7. 创建或更新当天唯一的 `daily/YYYY-MM-DD.md`；
8. 明确说明开始进度和完成后的进度。

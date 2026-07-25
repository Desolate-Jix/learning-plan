# 面试学习进度

> 本页只保存总体进度、当前任务和每日笔记索引。每天的知识点、代码、错误与 Reviewer 点评只写入当天唯一的 `daily/YYYY-MM-DD.md`。

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
4. 需要热身时，只复刷已经完成的白名单题；
5. 每次安排任务前核对题号、英文标题、链接和完成状态；
6. 每次 Accepted 后同步更新白名单、总体进度和当天笔记。

## 2026-07-25 当前状态

- **当前正式进度：** 12 / 75
- **剩余：** 63 题
- **当前日期：** 2026-07-25（新西兰时间）
- **截止日期：** 2026-09-22
- **第一遍完成目标：** 2026-09-13
- **每天学习时间：** 通常约 2 小时；疲劳日可缩短到 60～75 分钟
- **刷题语言：** Java
- **建议节奏：** 每周约 8～9 道白名单新题
- 当前计入的 12 道题全部属于 LeetCode 75；
- `Maximum Average Subarray I` 已 Accepted 并同步勾选。

## 每日笔记索引

| 日期 | 内容 | 当天结果 |
|---|---|---|
| [2026-07-13](./daily/2026-07-13.md) | Java 字符串、循环、Merge Strings Alternately | 1 道新题 Accepted |
| [2026-07-14](./daily/2026-07-14.md) | StringBuilder 复刷、ArrayList、线性扫描、数组边界 | 2 道新题 Accepted + 1 次复刷 |
| [2026-07-15](./daily/2026-07-15.md) | 同方向双指针、字符串边界、隐藏测试调试 | Is Subsequence Accepted |
| [2026-07-16](./daily/2026-07-16.md) | 左右双指针、字符数组、`indexOf()` | Reverse Vowels Accepted |
| [2026-07-17](./daily/2026-07-17.md) | 快慢双指针、原地修改、稳定压缩数组 | Move Zeroes Accepted |
| [2026-07-18](./daily/2026-07-18.md) | 暴力优化、左右双指针与贪心 | Container With Most Water Accepted |
| [2026-07-20](./daily/2026-07-20.md) | 前缀和、最高海拔、中心下标 | 两道 Easy 均 Accepted |
| [2026-07-22](./daily/2026-07-22.md) | 字符串公因子、字符串 API、数学 GCD 优化 | GCD of Strings Accepted |
| [2026-07-24](./daily/2026-07-24.md) | 前缀乘积、后缀乘积、状态复用 | Product of Array Except Self Accepted |
| [2026-07-25](./daily/2026-07-25.md) | 固定长度滑动窗口、窗口状态更新、整数除法 | Maximum Average Subarray I Accepted，128 / 128 |

## 已完成的 12 道官方题

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

完整勾选状态以 [LEETCODE_75_CHECKLIST.md](./LEETCODE_75_CHECKLIST.md) 为准。

## Day 10 完成情况｜2026-07-25

[643. Maximum Average Subarray I](https://leetcode.com/problems/maximum-average-subarray-i/)

- **结果：** Accepted，128 / 128；
- **提交记录：** 2 ms、69.59 MB；单次排名只作参考；
- **掌握等级：** B+；
- **核心公式：** `新窗口和 = 旧窗口和 - 离开元素 + 进入元素`；
- **自己的实现：**
  - 先计算第一个长度为 `k` 的窗口和；
  - 用 `t - nums[i] + nums[i + k]` 计算下一个窗口；
  - 比较新窗口后，把结果保存回 `t`，让下一轮继续复用当前状态；
  - 最后使用 `(double) maxsum / k` 避免整数除法；
- **自己发现的错误：** 最初忘记更新 `t`，会导致后续窗口一直错误地从第一个窗口推导；
- **复杂度：** `O(n)` 时间，`O(1)` 额外空间；
- **详细记录：** [2026-07-25 当天笔记](./daily/2026-07-25.md)。

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
- Find Pivot Index：当前暴力版 B，待用前缀和降为 `O(n)`；
- Product of Array Except Self：B+；已理解前缀乘积、后缀乘积与状态复用；
- Maximum Average Subarray I：B+；已理解固定长度窗口与状态更新。

## 近期复习

- [ ] 三天内用 `windowSum / maxWindowSum` 命名闭卷重写 Maximum Average Subarray I；
- [ ] 尝试 Maximum Average Subarray I 的常见下标写法：`i = k`，离开元素为 `nums[i - k]`；
- [ ] 三天内用更清楚的 `leftProduct / rightProduct` 命名重写 Product of Array Except Self；
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
6. 安排 1 道 Medium，或 1～2 道 Easy；
7. 创建或更新当天唯一的 `daily/YYYY-MM-DD.md`；
8. 明确说明开始进度和完成后的进度。

# 当前学习进度｜体系课程v2

更新：2026-10-09。主课程仍在 S09/PY02（C/进行中）：今日能在提示后写出复制订单列表、dict新增字段、append及return，但一度把按status判断误写成按id判断；嵌套tags共享变式独立通过，尚无完整无提示实现验收，不升B。PY01 +7新变式通过。GUI读过discover/select及窗口枚举Windows API；Agent小专题Tool Calling/Function Calling/MCP已讲；系统原理F01通过、F02明天学。

- **当前队列位置：S09（进行中）**。下次只需一个独立Python函数新变式及边界判断再评B，不重讲已懂的copy机制。GUI主线按实际操作原语 discover→select（窗口身份验证）→capture→click→type_text，暂不追持续变化的上层逻辑。
- **计算机系统原理（跨课程每日10分钟）**：2026-10-09 [SYSTEMS_FOUNDATIONS.md](SYSTEMS_FOUNDATIONS.md) F01“Program / Process / Thread”首次短验证通过；用户指定**今天到Thread结束，F02 CPU结构/Registers明天才正式学**，不能虚记F02完成。
- **LeetCode历史：24/75，最近已有记录2026-08-11，主语言Java。** 剩余51题；本次重构没有产生新Accepted。
- **当前熟练程度：待诊断**，不能因为有旧Accepted就默认B，也不能把历史题数清零。
- [每日队列](SCHEDULE.md) · [现行规则](LEARNING_RULES.md) · [课程目录](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/README.md) · [历史完整记录](archive/STUDY_PROGRESS_before_2026-09-26.md)

## 单元能力状态

|单元|等级|最近独立验收日期|证据|
|---|---|---|---|
|[DB01](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB01.md)|B|2026-09-30|[2026-09-30复测](daily/2026-09-30.md)：N:N关联表与SQL筛选/排序新变式通过|
|[DB02](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB02.md)|B|2026-10-01|[2026-10-01复测](daily/2026-10-01.md)：AND/OR/NULL 与 DISTINCT/粒度变式通过|
|[DB03](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB03.md)|B|2026-10-03|[2026-10-03复测](daily/2026-10-03.md)：WHERE/GROUP BY/HAVING/SUM/COUNT 综合逻辑闭卷通过；COUNT/NULL 边界题通过|
|[DB04](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB04.md)|B|2026-10-07|[2026-10-07验收](daily/2026-10-07.md)：学生选课零匹配统计逻辑独立完成；fan-out新场景独立推导6行/重复COUNT-SUM并说明pre-aggregation到student grain|
|[DB05](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB05.md)|待诊断|未记录|无|
|[DB06](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB06.md)|待诊断|未记录|无|
|[DB07](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB07.md)|待诊断|未记录|无|
|[DB08](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/DB08.md)|待诊断|未记录|无|
|[PY01](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/PY01.md)|B|2026-10-02|[2026-10-02复测](daily/2026-10-02.md)：两个汇总函数核心逻辑独立通过；dict.get/default 变式通过，语法错误显著减少|
|[PY02](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/PY02.md)|C|未记录|[2026-10-08第一日](daily/2026-10-08.md)：assignment/shallow/deep copy与mutable default机制理解；独立Python实现仍需语法提示|
|[PY03](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/PY03.md)|待诊断|未记录|无|
|[ALG01](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/ALG01.md)|B|2026-10-05|[2026-10-05复测](daily/2026-10-05.md)：Move Zeroes 闭卷逻辑、O(n)/O(1) 与 loop invariant 延迟复测通过|
|[ALG02](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/ALG02.md)|待诊断|未记录|无|
|[ALG03](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/ALG03.md)|待诊断|未记录|无|
|[ALG04](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/ALG04.md)|待诊断|未记录|无|
|[ALG05](https://github.com/Desolate-Jix/course-review/blob/main/curriculum/lessons/ALG05.md)|待诊断|未记录|无|

## 时段执行状态

状态允许：未开始、进行中、已完成、暂停待条件。一个单元可拆多个时段；前半时段做完不等于整节达到B。每次更新找最早未完成编号；若先修尚未通过则回到相应单元补学。

|编号|单元|执行状态|实际日期|证据|
|---|---|---|---|---|
|S01|DB01|已完成|2026-09-29–2026-09-30|[2026-09-30复测](daily/2026-09-30.md)：达到B；GUI-00完成|
|S02|DB02|已完成|2026-09-30–2026-10-01|2026-10-01短变式复测通过，DB02达到B|
|S03|PY01|已完成|2026-10-01–2026-10-02|延迟复测通过，达到B|
|S04|DB03|已完成|2026-10-02–2026-10-03|延迟闭卷综合验收通过，达到B|
|S05|ALG01|已完成|2026-10-03–2026-10-05|延迟复测通过，达到B|
|S06|R1|已完成|2026-10-05|6/8通过；薄弱点：OR/NULL 组合条件、Python return-inside-loop 跟踪|
|S07|DB04|已完成|2026-10-06|[2026-10-06](daily/2026-10-06.md)：INNER/LEFT、ON/WHERE、COUNT右表字段、无订单/无paid、fan-out/CROSS JOIN；第一日目标完成，不等于DB04达到B|
|S08|DB04|已完成|2026-10-07|[2026-10-07](daily/2026-10-07.md)：LEFT JOIN聚合新场景、grain/fan-out/pre-aggregation独立迁移通过；DB04达到B|
|S09|PY02|进行中|2026-10-08–2026-10-09|[2026-10-09](daily/2026-10-09.md)：能自主构建新列表、复制dict、append及return；业务条件按id而非status，已订正；nested tags变式通过；待无提示新函数验收决定是否达B|
|S10|ALG02|未开始|未记录|无|
|S11|DB05|未开始|未记录|无|
|S12|DB06|未开始|未记录|无|
|S13|R2|未开始|未记录|无|
|S14|ALG03|未开始|未记录|无|
|S15|DB07|未开始|未记录|无|
|S16|DB07|未开始|未记录|无|
|S17|PY03|未开始|未记录|无|
|S18|DB08|未开始|未记录|无|
|S19|DB08|未开始|未记录|无|
|S20|ALG04|未开始|未记录|无|
|S21|R3|未开始|未记录|无|
|S22|ALG05|未开始|未记录|无|
|S23|LAB|未开始|未记录|无|
|S24|LAB|未开始|未记录|无|
|S25|FINAL|未开始|未记录|无|
|S26|REVIEW|未开始|未记录|无|

## 历史与新增题计数

原始24道题及所有旧笔记保存在历史快照和[题单](LEETCODE_75_CHECKLIST.md)，本轮不改动其已完成勾选。933是计划中的白名单新题，当前仍未开始。

新题只有实际Accepted、解释思路与复杂度、保存当天证据后，才同时更新题单和本页题数。复刷、原创练习不增加题数。

## 更新顺序

先写当天证据，再更新时段与单元等级，最后更新[复习队列](REVIEW_QUEUE.md)与[错因记录](MISTAKES.md)。未报告完成时，不自动按日历推进。

## 面试表达记录

2026-09-30 DB01 延迟复测：N:N 场景能独立写出两侧FK与组合主键；SQL新场景能独立写出SELECT/FROM/WHERE/ORDER BY并正确处理升序。结果无需机械重复抄写即可形成足够证据，因此 DB01 评 B，S01 完成。英文60秒模板已整理，独立口述可放入后续短复习，不阻塞S02。

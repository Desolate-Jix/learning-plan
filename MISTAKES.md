# 错因与补学

当前为空；不把过去面试表现直接写成今天练习失败。错误记录要能指出下一次怎么练，避免只写“SQL不会”。

|实际日期|单元/题目|原判断或错误代码|错误原因|最小反例|补学动作|复测结果/证据|
|---|---|---|---|---|---|---|
|2026-10-02|DB03 / Result Granularity|最初把 GROUP BY 后的一行描述成“有用户住在这个城市/大于两条的部门”|业务含义方向对，但没有精确到“一行代表一个分组键对应的聚合结果”|改为：one row = one group / one grouped summary；例如一行=一个 department group|下次先说 grouping key，再说 HAVING 条件是否保留该组|待延迟复测|
|2026-10-02|DB03 / GROUP BY 查询结构|首次综合题写出 SELECT/WHERE/HAVING，但漏 `FROM orders` 和 `GROUP BY user_id`|已理解筛行与筛组，但写完整聚合查询时结构尚未自动化|后续已能独立写出 `FROM` + `WHERE` + `GROUP BY` + `HAVING` 的综合 SQL|下次闭卷写一题包含 SUM + COUNT 双 HAVING 条件的查询|待延迟复测|
|2026-10-01|PY01 / dict 与函数语法|写出 `total{row['user_id']}`、`int row['amount']`，以及一次 `status` 拼写错误/return 缩进错误|Java→Python 语法迁移不熟；混淆 dict 创建 `{}` 与按 key 访问 `[]`，以及 Python 函数调用括号|`total[uid] = total.get(uid,0) + int(row['amount'])`|下次独立重写两个汇总函数，要求无语法提示且覆盖空输入|待复测|
|2026-10-01|PY01 / return 与条件|把第一条 pending 的 amount=200 误判为会先累计再 return|忽略了 `if status == 'paid'` 为 False 时不会执行累计；循环内 return 会在第一轮结束函数|第一条 pending、第二条 paid 时错误 return 会直接返回0|下次用两条最小数据闭卷手推循环、if、return 顺序|待复测|
|2026-09-30|DB02 / FROM 与 WHERE|把状态值 `paid` 写成 `FROM paid`|混淆“从哪张表读取”与“筛选哪些行”|正确结构为 `FROM orders WHERE status = 'paid'`|下次新场景先口述 SELECT→FROM→WHERE→ORDER BY 的职责，再独立写 SQL|2026-10-01 新场景逻辑复测通过；另有字符串漏引号的小语法疏漏|
|2026-09-29|DB01 / SQL筛选排序|\`WHERE user_id = 1,\` 且预测结果只列 id|SQL子句之间误加逗号；验证时没有逐列对照 SELECT 输出|\`SELECT id,user_id,amount,status FROM orders WHERE user_id=1 ORDER BY id;\` 应返回完整4列|下次换数据闭卷写 SELECT/FROM/WHERE/ORDER BY，并逐列预测完整结果|2026-09-30 Products 新场景独立通过核心查询与升序；不要求机械抄写结果|
|2026-09-29|DB01 / N:N建模|关联表只写 author_id、article_id，首次未说明两列FK和防重复约束|能识别 Junction Table，但边界约束未独立补全|同一 author_id + article_id 重复两次应被阻止|下次新场景独立写两侧FK + Composite PK/UNIQUE，并解释为什么|2026-09-30 新 Student–Club 场景独立通过|

可用错误类别：概念/结果粒度/NULL/边界/数据结构选择/复杂度/语言API/共享对象/验证不足/表达。

修复标准：解释原因、通过原反例、再通过一个新变式。看完答案立即重写标“有提示”，不算延迟独立通过。

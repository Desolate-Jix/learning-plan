# 错因与补学

当前为空；不把过去面试表现直接写成今天练习失败。错误记录要能指出下一次怎么练，避免只写“SQL不会”。

|实际日期|单元/题目|原判断或错误代码|错误原因|最小反例|补学动作|复测结果/证据|
|---|---|---|---|---|---|---|
|2026-09-29|DB01 / SQL筛选排序|\`WHERE user_id = 1,\` 且预测结果只列 id|SQL子句之间误加逗号；验证时没有逐列对照 SELECT 输出|\`SELECT id,user_id,amount,status FROM orders WHERE user_id=1 ORDER BY id;\` 应返回完整4列|下次换数据闭卷写 SELECT/FROM/WHERE/ORDER BY，并逐列预测完整结果|待复测|
|2026-09-29|DB01 / N:N建模|关联表只写 author_id、article_id，首次未说明两列FK和防重复约束|能识别 Junction Table，但边界约束未独立补全|同一 author_id + article_id 重复两次应被阻止|下次新场景独立写两侧FK + Composite PK/UNIQUE，并解释为什么|待复测|

可用错误类别：概念/结果粒度/NULL/边界/数据结构选择/复杂度/语言API/共享对象/验证不足/表达。

修复标准：解释原因、通过原反例、再通过一个新变式。看完答案立即重写标“有提示”，不算延迟独立通过。

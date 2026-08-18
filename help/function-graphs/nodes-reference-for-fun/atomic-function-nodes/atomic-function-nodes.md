---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: 了解Substance函数图中用于构建自定义函数的最小节点单位 — 原子函数节点。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 原子函数节点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 17%

---


# 原子函数节点

与[Substance图中的原子节点](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)类似，Substance函数图中的原子节点是该类型图中的最小节点单位。

它们可按用途分为几类：

| 类别 | 节点 | 输入类型 | 输出类型 | 描述 |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [常量](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | 浮点 | - | 浮点 | 定义常量浮动值，例如0.1 |
|                                                                                                                                        | 浮点 2 | - | 浮点 2 | 定义一个包含2个浮动值的常量矢量，例如(0.1， 0.2) |
|                                                                                                                                        | 浮点 3 | - | 浮点 3 | 定义一个包含3个浮动值的常量矢量，例如(0.1、0.2、0.3) |
|                                                                                                                                        | 浮点 4 | - | 浮点 4 | 定义4个浮动值的常量矢量，例如(0.1、0.2、0.3、0.4) |
|                                                                                                                                        | 整数 | - | 整数 | 定义常量整数值，例如1 |
|                                                                                                                                        | 整数 2 | - | 整数 2 | 定义2个整数值的常量矢量，例如(1， 2) |
|                                                                                                                                        | 整数 3 | - | 整数 3 | 定义3个整数值的常量矢量，例如(1， 2， 3) |
|                                                                                                                                        | 整数 4 | - | 整数 4 | 定义4个整数值的常量矢量，例如(1， 2， 3， 4) |
|                                                                                                                                        | 布尔型 | - | 布尔型 | 定义常量布尔值，例如True或False |
|                                                                                                                                        | 字符串 | - | 字符串 | 定义常量字符串值，例如“Substance” |
| [矢量](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | 矢量浮点 2 | Float1 | 浮点 2 | 在具有2个坐标的矢量中投射2个浮动值 |
|                                                                                                                                        | 矢量浮点 3 | Float1 / Float2 | 浮点 3 | 在具有3个坐标的矢量中投射2个浮动值 |
|                                                                                                                                        | 矢量浮点 4 | 浮点1 / 2 / 3 | 浮点 4 | 在具有4个坐标的矢量中投射2个浮动值 |
|                                                                                                                                        | Swizzle 浮点 1 | 矢量浮点 | Float1 | 从矢量中提取浮动坐标 |
|                                                                                                                                        | Swizzle 浮点 2 | 矢量浮点 | 浮点 2 | 从矢量提取2个浮动坐标 |
|                                                                                                                                        | Swizzle 浮点 3 | 矢量浮点 | 浮点 3 | 从矢量提取3个浮动坐标 |
|                                                                                                                                        | Swizzle 浮点 4 | 矢量浮点 | 浮点 4 | 从矢量提取4个浮动坐标 |
|                                                                                                                                        | 矢量整数 2 | 整数 2 | 矢量整数 2 | 在具有2个坐标的矢量中投射2个整数值 |
|                                                                                                                                        | 矢量整数 3 | 整数 3 | 整数 3 | 在具有3个坐标的矢量中投射2个整数值 |
|                                                                                                                                        | 矢量整数 4 | 整数 4 | 整数 4 | 在具有4个坐标的矢量中投射2个整数值 |
|                                                                                                                                        | Swizzle 整数 1 | 矢量整数 | 整数1 | 从矢量中提取整数坐标 |
|                                                                                                                                        | Swizzle 整数 2 | 矢量整数 | 整数 2 | 从矢量提取2个整数坐标 |
|                                                                                                                                        | Swizzle 整数 3 | 矢量整数 | 整数 3 | 从矢量提取3个整数坐标 |
|                                                                                                                                        | Swizzle 整数 4 | 矢量整数 | 整数 4 | 从矢量提取4个整数坐标 |
| [变量](../../../function-graphs/variables/variables.md) | 设置 | 任何 | 输入类型 | 设置变量 |
|                                                                                                                                        | 获取整数1 | - | 整数1 | 获取函数或图形整数值输入 |
|                                                                                                                                        | 获取整数 2 | - | 整数 2 | 获取函数或图形Integer2值输入 |
|                                                                                                                                        | 获取整数 3 | - | 整数 3 | 获取函数或图形Integer3值输入 |
|                                                                                                                                        | 获取整数 4 | - | 整数 4 | 获取函数或图形Integer4值输入 |
|                                                                                                                                        | 获取Float1 | - | Float1 | 获取函数或图形浮动值输入 |
|                                                                                                                                        | 获取浮点 2 | - | 浮点 2 | 获取函数或图形Float2值输入 |
|                                                                                                                                        | 获取浮点 3 | - | 浮点 3 | 获取函数或图形Float3值输入 |
|                                                                                                                                        | 获取浮点 4 | - | 浮点 4 | 获取函数或图形Float4值输入 |
|                                                                                                                                        | 获取布尔 | - | 布尔型 | 获取函数或图形布尔值输入 |
| 采样器 | 取样灰色 | 矢量浮点 2 | 浮点 4 | 返回输入图像在给定UV坐标(float2)下的灰度值 |
|                                                                                                                                        | 取样颜色 | 矢量浮点 2 | 浮点 4 | 以给定的UV坐标(float2)返回输入图像的颜色值 |
| 强制转换 | 到浮点 | 整数1 | Float1 | 将整数转换为浮点数 |
|                                                                                                                                        | 到浮点 2 | 整数 2 | 浮点 2 | 将整数2转换为Float2 |
|                                                                                                                                        | 到浮点 3 | 整数 3 | 浮点 3 | 将Integer3转换为Float3 |
|                                                                                                                                        | 到浮点 4 | 整数 4 | 浮点 4 | 将Integer4转换为Float4 |
|                                                                                                                                        | 到整数 | Float1 | 整数1 | 将浮点转换为整数 |
|                                                                                                                                        | 到整数 2 | 浮点 2 | 整数 2 | 将浮点2转换为Integer2 |
|                                                                                                                                        | 到整数 3 | 浮点 3 | 整数 3 | 将浮点3转换为Integer3 |
|                                                                                                                                        | 到整数 4 | 浮点 4 | 整数 4 | 将浮点4转换为Integer4 |
| [运算符](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | 加 | 矢量浮点/整数 | a和b类型 | 将相同类型的2个值相加： a + b |
|                                                                                                                                        | 减 | 矢量浮点/整数 | a和b类型 | 相减2个相同类型的值：a - b |
|                                                                                                                                        | 乘 | 矢量浮点/整数 | a和b类型 | 将相同类型的2个值相乘：a \* b |
|                                                                                                                                        | 标量乘法 | 矢量浮点 | 类型 | 将某个值乘以一个浮动值：一个\*标量 |
|                                                                                                                                        | 除 | Float1 / Integer1 | a和b类型 | 将相同类型的2个值相除：a / b |
|                                                                                                                                        | 求反 | Float1 / Integer1 | 类型 | 返回负值： -a |
|                                                                                                                                        | 取模 | Float1 / Integer1 | 类型 | 返回模数值：mod（a，除数） |
|                                                                                                                                        | 点积 | 矢量浮点 | a和b类型 | 返回相同类型的2个值的点积： dot(a， b) |
| [逻辑](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | 与 | 布尔型 | 布尔型 | 如果2个布尔值条目为true，则返回true。 如果其中一个条目为false，则返回false。 |
|                                                                                                                                        | 或 | 布尔型 | 布尔型 | 如果布尔条目中有1个为true，则返回true。 如果它们都为false，则返回false。 |
|                                                                                                                                        | 不为 | 布尔型 | 布尔型 | 返回条目的否定布尔值： ！a |
| [比较](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | 等于 | Float1 / Integer1 | 布尔型 | 如果a = b，则返回true |
|                                                                                                                                        | 不等于 | Float1 / Integer1 | 布尔型 | 如果!=b |
|                                                                                                                                        | 大于 | Float1 / Integer1 | 布尔型 | 如果a > b，则返回true |
|                                                                                                                                        | 大于等于 | Float1 / Integer1 | 布尔型 | 如果a >= b，则返回true |
|                                                                                                                                        | 较低 | Float1 / Integer1 | 布尔型 | 如果&lt; b，则返回true |
|                                                                                                                                        | 小于或等于 | Float1 / Integer1 | 布尔型 | 如果&lt;= b |
| 函数 | 绝对值 | Float1 / Integer1 | Float1 | 返回a： abs(a)的绝对值 |
|                                                                                                                                        | 向下取整 | Float1 / Integer1 | Float1 | 返回小于或等于a：floor(a)的最高值 |
|                                                                                                                                        | 上限 | Float1 / Integer1 | Float1 | 返回大于或等于a：ceil(a)的最小值 |
|                                                                                                                                        | 余弦 | Float1 / Integer1 | Float1 | 返回a： cos(a)的余弦值 |
|                                                                                                                                        | 正弦 | Float1 / Integer1 | Float1 | 返回a： sin(a)的正弦值 |
|                                                                                                                                        | 正切 | Float1 / Integer1 | Float1 | 返回a： tan(a)的切值 |
|                                                                                                                                        | 反正切 2 | 矢量浮点 2 | Float1 | 返回vector2条目的arctan2值： arctan2(xa， ya) |
|                                                                                                                                        | 直角坐标 | Float1 | 浮点 2 | 将2个极坐标转换为笛卡尔坐标：carth(rho， theta) |
|                                                                                                                                        | 平方根 | Float1 / Integer1 | Float1 | 返回平方根值 |
|                                                                                                                                        | 对数 | Float1 / Integer1 | Float1 | 返回： log(a)的对数值 |
|                                                                                                                                        | 指数 | Float1 / Integer1 | Float1 | 返回a：exp(a)的指数值 |
|                                                                                                                                        | Pow 2 | Float1 / Integer1 | Float1 | 返回2的幂值 |
|                                                                                                                                        | 线性插值 | Float1 / Integer1 | Float1 | 返回两个值之间的线性插值，具体取决于浮动值： (1-x)a + x \* b |
|                                                                                                                                        | 最小 | Float1 / Integer1 | a和b类型 | 返回a和b之间的最小值 |
|                                                                                                                                        | 最大 | Float1 / Integer1 | a和b类型 | 返回介于a和b之间的最大值 |
| 随机 |                       | Float1 | Float1 | 生成介于0和 |
| [控件](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | 序列 | 任何 | 输入类型 | 允许选择在2个值之间首先计算哪个值。 |
|                                                                                                                                        | If...Else | 布尔值/a和b | a和b类型 | 如果If中的条件为true，则返回true。 如果为false，则返回false。 |

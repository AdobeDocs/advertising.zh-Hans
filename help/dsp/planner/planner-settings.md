---
title: 已连接电视接入计划的设置
description: 查看有关已连接电视接入计划的设置说明。
feature: DSP Planner
source-git-commit: 72ee396019d5a444bd326fe659ce68eb3490a439
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 已连接电视接入计划的设置

*Beta版功能*

| 参数 | 描述 | 必需？ |
| --- | --- | --- |
| 名称 | 用于标识计划的名称。 | 是 |
| 广告商 | 正在为其创建计划的帐户中的特定广告商。 | 是 |
| 媒体类型 | 要包含在计划中的媒体类型。<br><br>当前，仅限 [!UICONTROL Connected TV] 可用。 | 是 |
| 日期范围 | 计划的开始日期和结束日期。<br><br>开始日期不能早于当前日期。 日期范围不能大于90天。 | 是 |
| 目标类型 | 目标的类型(如 [!UICONTROL Budget])，以便考虑该计划。<br><br>当前，仅限 [!UICONTROL Budget] 可用。 | 是 |
| 目标值 | 预测的目标值。 要获得更准确的预测结果，请使用大于5000 USD的值。 | 是 |
| 最高出价 | 为1000次展示支付的最大金额。 如果 [!UICONTROL Connected TV] 选择媒体类型，请输入至少10美元的值。 | 是 |
| 频率限制 | 某个独特家庭应获得广告的次数。<br><br>当您实施计划并且必须创建多个投放位置时，请在包级别（而非投放位置级别）应用频率上限设置，以确保正确投放。 | 是 |
| 地理定位 | 作为目标包含或排除的位置。 | 是 |
| 库存定位 | 作为目标包含或排除的清单源。 至少选择一个信息源或源。 | 是 |
| 受众定位 | 作为目标包含或排除的受众。 | 否 |
| 广告持续时间 | 要考虑用于计划的广告持续时间。 | 否 |

>[!MORELIKETHIS]
>
>* [关于DSP Planner工具](planner-about.md)
>* [创建连接电视接入计划](planner-create.md)
>* [复制连接的电视接入计划](planner-duplicate.md)
>* [编辑连接的电视接入计划](planner-edit.md)
>* [导出连接的电视覆盖范围计划](planner-export.md)
>* [重新生成“连接电视覆盖计划”的预测](planner-forecast.md)
>* [存档连接的电视接入计划](planner-archive.md)

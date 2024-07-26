---
title: 已连接电视接入计划的设置
description: 查看有关已连接电视接入计划的设置说明。
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 84cf49c9e366938479e9fea2ede55925f1cb3e51
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 已连接电视接入计划的设置

| 参数 | 描述 | 必需？ |
| --- | --- | --- |
| [!UICONTROL Name] | 用于标识计划的名称。 | 是 |
| [!UICONTROL Advertiser] | 正在为其创建计划的帐户中的特定广告商。 | 是 |
| [!UICONTROL Media Type] | 要包含在计划中的媒体类型。<br><br>当前，只有[!UICONTROL Connected TV]可用。 | 是 |
| [!UICONTROL Date Range] | 计划的开始日期和结束日期。<br><br>开始日期不能早于当前日期。 日期范围不能大于90天。 | 是 |
| [!UICONTROL Goal Type] | 要考虑用于计划的目标类型（如[!UICONTROL Budget]）。<br><br>当前，只有[!UICONTROL Budget]可用。 | 是 |
| [!UICONTROL Goal Value] | 预测的目标值。 要获得更准确的预测结果，请使用大于5000 USD的值。 | 是 |
| [!UICONTROL Max Bid] | 为1000次展示支付的最大金额。 如果选择[!UICONTROL Connected TV]媒体类型，请输入至少10美元的值。 | 是 |
| [!UICONTROL Frequency Cap] | 某个独特家庭应获得广告的次数。<br><br>当您实施计划并且必须创建多个投放位置时，请在包级别而非投放位置级别应用频率上限设置，以确保正确投放。 | 是 |
| [!UICONTROL Geo-Targeting] | 作为目标包含或排除的位置。 选项包括：<ul><li>国家/地区、城市、州：单击&#x200B;**[!UICONTROL Country/State/City]**&#x200B;选项卡；选择区域是&#x200B;*国家/地区*、*州*&#x200B;还是&#x200B;*城市*；可以选择展开任何位置以查看其子组件，然后单击位置旁边的&#x200B;**[!UICONTROL Include]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**。</li><li>美国的指定市场区域(DMA)：单击&#x200B;**[!UICONTROL DMA]**&#x200B;选项卡；可以选择展开任何状态以查看其DMA，然后单击位置旁边的&#x200B;**[!UICONTROL Include]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**。</li><li>邮政编码：您可以：<ul><li>单击“**[!UICONTROL Search postal code]**”选项卡，选择国家/地区，输入完整的城市名称或城市名称中包含的字母，然后按&#x200B;**[Enter]**&#x200B;键，单击正确的城市名称以查看城市的所有邮政编码，单击正确的邮政编码，然后单击&#x200B;**[!UICONTROL Include]**&#x200B;或&#x200B;**[!UICONTROL Exclude]**。</li><li>单击&#x200B;**[!UICONTROL Paste postal code]**&#x200B;选项卡，选择国家/地区，输入或粘贴逗号分隔的值，然后单击&#x200B;**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。</li></ul></li></ul> | 是 |
| [!UICONTROL Inventory Targeting] | 作为目标包含或排除的清单源。 至少选择一个信息源或源。 | 是 |
| [!UICONTROL Site/App Targeting] | 要作为目标包含或排除的网站和应用程序。 每行输入一个网址，然后单击&#x200B;**[!UICONTROL Include All]**&#x200B;或&#x200B;**[!UICONTROL Exclude All]**。 | 否 |
| [!UICONTROL Audience Targeting] | 作为目标包含或排除的受众。 | 否 |
| [!UICONTROL Ad duration] | 要考虑用于计划的广告持续时间。 | 否 |

>[!MORELIKETHIS]
>
>* [关于DSP Planner工具](planner-about.md)
>* [创建连接的电视访问计划](planner-create.md)
>* [复制连接的电视访问计划](planner-duplicate.md)
>* [编辑连接的电视访问计划](planner-edit.md)
>* [导出连接的电视访问计划](planner-export.md)
>* [重新生成连接电视到达计划的预测](planner-forecast.md)
>* [存档连接的电视访问计划](planner-archive.md)

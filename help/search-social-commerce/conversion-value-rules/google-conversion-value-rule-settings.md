---
title: '[!DNL Google Ads]转换值规则设置'
description: 引用 [!DNL Google Ads] 转换值规则的设置。
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# [!DNL Google Ads]转换值规则设置

<!-- Go through all -->

| 部分 | 参数 | 描述 |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | 广告网络。 |
| | [!UICONTROL Account] | 广告网络帐户。 |
| | [!UICONTROL Campaign] | 广告营销活动。 |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[条件类型\] | （现有规则只读）触发值调整必须满足的条件类型：<ul><li>**设备：**&#x200B;定位所有或特定的设备类型。</li><li>**位置：**&#x200B;定位所有国家和地区，或定位并排除特定位置。</li><li>**受众：**&#x200B;定向所有或特定受众</li></ul>**注意：**&#x200B;帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。 |
| | 条件类型>设备 | （仅限设备条件）要定位的设备类型：<ul><li>**所有设备** — 定向所有设备类型。</li><li>**选择设备** — 指定一个或多个要定位的设备类型： **桌面**、**移动设备**&#x200B;和&#x200B;**平板电脑**。</li></ul>在一个条件内，使用布尔运算符OR连接多个目标，以便满足任何选项以启动值调整。 示例：如果\[Device is Mobile OR Tablet\]，则添加1.5。 |
| | 完成情况类型>位置 | （仅限位置条件）位置目标和排除项：<ul><li>**所有国家和地区** — 针对所有国家和地区，或针对并排除特定地点。</li><li>**输入位置** — 定位和排除特定位置。</li></ul><ul><li>要展开某个位置或子位置，请单击名称后面的> 。</li><li>要添加目标，请选择目标一次，以显示绿色复选标记。</li><li>要排除某个目标，请再次选择该目标以显示红色的&#x200B;**[!UICONTROL X]**。</li><li>要删除目标或排除项，请执行下列操作之一：<ul><li>单击![列中该项旁边的](/help/search-social-commerce/assets/delete.png "删除")删除[!UICONTROL Selections]。</li><li>选择目标，直到没有复选标记或[!UICONTROL X]显示。</li></ul></li></ul>在一个条件中，多个目标或排除项使用布尔运算符OR进行连接，以便满足任何选项来启动值调整。 示例：如果\[Location is Alignalia OR Tunities\]，则添加1.5。 |
| | 条件类型>受众 | （仅限受众条件）受众目标：<ul><li>**所有受众区段** — 用于定位所有[!DNL Google Ads]受众区段。</li><li>**输入受众区段** — 定向特定的[!DNL Google Ads]受众区段。</li></ul><ul><li>要将某个类别或子类别展开到其区段中，请单击名称后面的> 。</li><li>要添加目标，请选择该目标。</li><li>要删除目标，请取消选择该目标或单击“选择”列中该项旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。</li></ul>在一个条件中，多个目标或排除项使用布尔运算符OR进行连接，以便满足任何选项来启动值调整。 示例：如果\[受众是廉价旅行者或家庭度假者\]，则添加1.5。<br><br>**注意：**&#x200B;保存受众目标后，您可以添加其他受众，但无法在[!DNL Google Ads]编辑器之外删除这些受众。 如果需要删除受众目标，请直接登录[!DNL Google Ads]并使用[!DNL Google Ads]编辑器。 |
| 条件>次要条件 | | （可选，对于现有规则为只读）触发值调整必须满足的条件类型。 包括次要条件时，次要条件将使用布尔运算符ALL连接到主要条件，因此必须同时满足这两个条件才能启动值调整。 示例：如果\[Location is Alignalia OR Tunity\]和\[Device is Mobile OR Tablet\]，则添加1.5。<br><br>有关说明，请参见Primary Condition条目。<br><br>**注意：**&#x200B;帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。 |
| 值调整 | 值 | 指定调整类型，然后输入一个正值：<ul><li>**添加** — 将指定的值添加到传递的转换值。 该值必须大于零(0)。</li><li>**乘** — 将传递的转换值乘以指定的值。 该值必须介于0.5和10之间。</li></ul> |

>[!MORELIKETHIS]
>
>* [关于 [!DNL Google Ads] 转换值规则](about-google-conversion-value-rules.md)
>* [创建 [!DNL Google Ads] 转化值规则](create-google-conversion-value-rule.md)
>* [编辑a [!DNL Google Ads] 转换值规则](edit-google-conversion-value-rule.md)
>* [更改 [!DNL Google Ads] 转换值规则](change-the-status-of-google-conversion-value-rule.md)的状态


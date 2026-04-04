---
title: 创建 [!DNL Google Ads] 转化值规则
description: 了解如何创建 [!DNL Google Ads] 转化值规则。
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# 创建[!DNL Google Ads]转化值规则

您可以在[!DNL Google Ads]帐户中创建帐户级别和营销活动级别的转化值规则，在个人帐户级别或更低级别跟踪这些帐户的转化。 您不能为在主帐户层跟踪的具有跨帐户转换的帐户创建规则。

每个规则最多包括两个条件，以及当满足条件时要应用的转换值调整。 帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。

您可以为每个营销活动创建多个营销活动级别的规则。 但是，当帐户级别规则已存在时，[!DNL Google Ads]尚不提供在[!DNL Google Ads]编辑器之外创建新帐户级别规则的功能。 要创建其他帐户级别的规则，请直接登录到[!DNL Google Ads]并使用[!DNL Google Ads]编辑器。

**注意：**&#x200B;营销活动级别的转化值规则将覆盖帐户级别的规则，并且只能将一个规则应用于转化。 有关详细信息，请参阅[当转换满足多个规则的条件时，如何 [!DNL Google Ads] 确定将哪个规则应用于转换](https://support.google.com/google-ads/answer/10520348)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**。

   默认情况下，选择&#x200B;**[!UICONTROL Campaign]**&#x200B;选项卡以显示所有营销活动级别的规则。

1. （可选）要创建帐户级别的规则，请单击&#x200B;**[!UICONTROL Account]**&#x200B;选项卡。

1. 在工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。<!-- Upload newer icon -->

1. 选择广告网络和帐户。 对于营销活动级别的规则，还应选择营销活动。 然后单击&#x200B;**[!UICONTROL Next]**。

1. 配置[转换规则设置](google-conversion-value-rule-settings.md)。

   必须配置主要条件和值调整。 您可以选择配置辅助条件。

   在一个条件中，多个目标或排除项使用布尔运算符OR进行连接，以便满足任何选项来启动值调整。 包括次要条件时，次要条件将使用布尔运算符ALL连接到主要条件，因此必须同时满足这两个条件才能启动值调整。 示例：如果\[Location is Alignalia OR Tunity\]和\[Device is Mobile OR Tablet\]，则添加1.5。

   **注意：**&#x200B;帐户中的所有规则必须使用相同类型的主条件和（可选）辅助条件。 例如，如果规则1包含主要条件“Audience”和次要条件“Location”，则帐户中的所有其他规则必须具有主要条件“Audience”。 当其他规则包含次要条件时，它必须是“位置”。

1. 单击&#x200B;**[!UICONTROL Review and Save]**&#x200B;以查看设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [关于 [!DNL Google Ads] 转换值规则](about-google-conversion-value-rules.md)
>* [编辑a [!DNL Google Ads] 转换值规则](edit-google-conversion-value-rule.md)
>* [更改 [!DNL Google Ads] 转换值规则](change-the-status-of-google-conversion-value-rule.md)的状态
>* [[!DNL Google Ads] 转换值规则设置](google-conversion-value-rule-settings.md)


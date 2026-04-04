---
title: 关于 [!DNL Google Ads] 转换值规则
description: 了解如何在Search、Social和Commerce中查看和管理 [!DNL Google Ads] 转化值规则。
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# 关于[!DNL Google Ads]转换值规则

Search、Social和Commerce会自动从您的[帐户同步](https://support.google.com/google-ads/answer/10518330)转化值规则[!DNL Google Ads]。 转化值规则允许您根据用户信息（包括设备类型、位置和受众区段）调整转化事件的值。 通过Google智能竞价，您可以在搜索、显示、购物和性能最大化营销活动中使用基于价值的竞价规则。 对于具有尽可能提高转化次数和目标ROAS竞价策略的营销活动，[!DNL Google Ads]算法将开始偏好具有较高值的转化。

营销活动级别的转化值规则将覆盖帐户级别的规则。 当转化满足多个转化值规则时，将仅应用其中一个规则。 通常应用最具体的规则，但请参阅[[!DNL Google Ads] 有关不同规则条件类型](https://support.google.com/google-ads/answer/10520348)的优先级的文档。

## [!UICONTROL Conversion Value Rules]视图和功能

在[!DNL Google Ads]界面中创建的所有规则将在24小时内同步，并可在[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]视图中找到。 某些帐户可以管理其转化值规则：

* 对于在个人帐户或营销活动级别跟踪转化的帐户，您可以创建、编辑和更改帐户级别和营销活动级别规则的状态。

  这些帐户可以链接到[!DNL Google Ads]经理帐户，但它们不能使用跨帐户转化跟踪（针对该跟踪，将跨经理帐户中的所有帐户跟踪转化）。

* 在使用跨帐户转化跟踪的帐户中，帐户级别和营销活动级别的规则继承自经理帐户，并且是只读的。

## 包含搜索、社交和Commerce项目组合的转化值规则

当广告商帐户配置为将Search、Social和Commerce目标上传到[!DNL Google Ads]，并且您在具有目标的项目组合中包含使用转化值规则的营销活动时，[!DNL Google Ads]会将转化值规则应用于目标中指定的原始转化值。 因此，搜索、社交和Commerce中的转化数据与[!DNL Google Ads]中的转化数据不同。

例如，假设目标使用单个转化量度“潜在客户”，并将来自移动设备的转化权重为10，将来自非移动设备的转化权重为10。 Search、Social和Commerce将任一设备类型的事件计为一(1)次转化，并将转化值计为10。 但是，假设该组合中的某个营销活动使用转化值规则“如果设备是移动设备，则乘以2。” 在跟踪该营销活动的移动潜在客户事件时，[!DNL Google Ads]还会将转化计数计为一(1)，但转化值会计为(10 x 2) = 20。

要查看有关规则的更多信息，包括应用规则之前的原始转化值，请参阅[&#x200B; [!DNL Google Ads]中的](https://support.google.com/google-ads/answer/10519848)转化值规则报告。

>[!MORELIKETHIS]
>
>* [创建 [!DNL Google Ads] 转化值规则](create-google-conversion-value-rule.md)
>* [编辑a [!DNL Google Ads] 转换值规则](edit-google-conversion-value-rule.md)
>* [更改 [!DNL Google Ads] 转换值规则](change-the-status-of-google-conversion-value-rule.md)的状态
>* [[!DNL Google Ads] 转换值规则设置](google-conversion-value-rule-settings.md)


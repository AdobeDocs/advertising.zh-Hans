---
title: 自定义目标的最佳实践
description: 了解为针对最低CPA或最高ROAS优化的包定义自定义目标的最佳实践。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# 自定义目标的最佳实践

自定义目标定义广告商实现其业务目标所需的成功事件。 每个使用优化目标“[!UICONTROL Highest Return on Ad Spend (ROAS)"]”或“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的包都必须包含一个自定义目标，以帮助实现整体优化目标。 您可以创建自定义目标作为&#x200B;*[自定义目标](/help/dsp/admin/custom-objectives-manage.md)*。

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

每个自定义目标（目标）包含要跟踪和优化的一个或多个转化量度以及这些量度的相对权重。 您可以[为包](/help/dsp/campaign-management/packages/package-settings.md)分配自定义目标，以便使用[!DNL Adobe AI]进行报告和算法优化。

要创建和管理自定义目标，请参阅&quot;[管理自定义目标](/help/dsp/admin/custom-objectives-manage.md)&quot;。

## 具有单个量度的自定义目标

以下示例显示如何配置针对单个转化量度的目标。

### 优化目标为“[!UICONTROL Highest Return on Ad Spend (ROAS)]”的促销活动示例

如果您的促销活动目标是收入([!UICONTROL Highest Return on Ad Spend (ROAS)])，并且所有设备类型的收入对您同样重要，则请包含权重为1 (1)的“[!UICONTROL Revenue]”量度。 选择量度类型&#x200B;*[!UICONTROL Goal]*。

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 对于任何设备上展示广告跟踪的每个$1收入，一(1)的权重等于一(1)的值。 例如，权重为1 (1)的$250转化报告为$250的转化。 如果将转化量度的权重分配为0.5，则$250转化在Adobe Advertising中报告为$125（$250转化* 0.5 [!UICONTROL weight] = $125）。

### 优化目标为“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的促销活动示例

如果您的促销活动目标是每次客户获取的最低成本(CPA)，并且它只需要一个成功事件（例如“应用程序提交”），则请包含该量度并将量度类型指定为&#x200B;*[!UICONTROL Goal]*。 最佳实践是将权重设置为一(1)。

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 对于为在任何设备上显示广告跟踪的每个转化，一个(1)的权重等于一个(1)的值。 例如，如果跟踪了10个申请提交转换，则报告了10个申请提交转换。 但是，如果为转化量度分配的权重为0.5，则在Adobe Advertising中，10次转化将报告为五(5)（10次转化* 0.5 [!UICONTROL weight] = 5）。

## 具有多个量度的自定义目标

在以下两种情况下，您将在自定义目标中使用多个量度：

* 您的营销活动目标有多个成功事件。 例如，您可能在为多个网站操作（PDF下载、联系我们，以及电子邮件注册）打广告，所有这些操作都有助于您的CPA目标。 如果目标包括三个单独的量度，每个量度的权重为1，则[!DNL Adobe AI]支持的算法会将每个量度和用户设备类型视为同等重要性。 如果不同的指标具有不同的成本或重要性，则相应地调整其相对权重。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* 自定义目标中的单个转化量度没有达到优化性能所需的最少每天10次转化。 由于每天的程序包支出最少或自然转化次数有限，因此可能会发生转化次数减少。 将其他支持量度添加到自定义目标可以帮助您实现每天10次转化阈值。 10个支持事件可以帮助程序包达到10/天阈值，即使每个事件的权重都低于一(1)也是如此。 但您可能不需要添加这么多事件。

  在向自定义目标添加支持量度时，请根据支持量度对主要成功事件的相对重要性为其加权，并牢记数据点的数量。 这允许由[!DNL Adobe AI]支持的算法平衡多个量度并根据目标进行优化。

  以下示例目标包含三个指标，每个指标的权重不同：应用程序提交= 1，应用程序开始= 0.1，广告商登陆页面= 0.01。 这意味着，每个应用程序提交转化对贵企业的价值与平均10次应用程序开始转化和100次广告商登陆页面转化相同。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

相反，如果您将登陆页面访问量平均加权到提交的应用程序，那么登陆页面访问量的自然增加可能会压倒您的目标，并使优化朝着登陆页面访问的方向倾斜。

>[!MORELIKETHIS]
>
>* [管理自定义目标](/help/dsp/admin/custom-objectives-manage.md)
>* [优化目标及使用方法](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)

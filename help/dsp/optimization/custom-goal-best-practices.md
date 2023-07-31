---
title: 构建自定义目标的最佳实践
description: 了解构建自定义目标以定义成功事件的最佳实践。
feature: DSP Optimization, DSP Best Practices
exl-id: 8b1247cd-083d-4c8c-8588-9e8c03c4cc67
source-git-commit: 2c2f65f45fb7515068cee36493f514ce2e456e75
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 构建自定义目标的最佳实践

## 具有单个属性的自定义目标

以下示例显示如何配置针对单个转化量度的目标。

### 使用&quot;[!UICONTROL Highest ROAS - Custom Goal]»优化目标

如果您的促销活动目标是收入([!UICONTROL Highest ROAS - Custom Goal])，则您的自定义目标（目标）将包括&quot;[!UICONTROL Revenue]权重为一(1)的&quot;指标。

![具有单个转化量度的ROAS自定义目标示例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 对于跟踪的每个$1收入，1的值等于1。
>
> 例如，权重为1的$250转化报告为$250。 如果转化量度的权重为0.5，则$250的转化将报告为$125的Adobe Advertising（$250的转化* 0.5） [!UICONTROL Property Weight] = $125)。

### 使用&quot;[!UICONTROL Lowest CPA - Custom Goal]»优化目标

如果您的促销活动目标是每次客户获取的最低成本(CPA)，并且它只需要一个成功事件，那么您将包括一个量度（在以下示例中为“应用程序提交”）。 最佳实践是将权重设置为一(1)。

![具有单个转化量度的CPA自定义目标示例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 对于跟踪的每次转化，一个ID值等于一个ID。
>
> 例如，如果跟踪了10个申请提交转换，则报告了10个申请提交转换。  如果为转化量度分配的权重为0.5，则将10次转化报告为Adobe Advertising中的五(5)次（10次转化*0.5次） [!UICONTROL Property Weight] = 5)。

## 具有多个属性的自定义目标

在以下两种情况下，您可以在自定义目标中使用多个属性：

* 您的营销活动目标有多个成功事件。 例如，您可能在为多个现场操作投放广告，并且所有操作都归因于您的CPA目标。 以下示例目标包含三个单独的属性(PDF下载、联系我们，以及电子邮件注册)，每个属性的权重为1，用于告知 [!DNL Adobe Sensei] 每个属性的重要性都相同的算法。 如果包含具有不同成本或重要性的属性，则可以相应地调整其相对权重。

  ![具有多个属性的自定义目标示例](/help/dsp/assets/custom-goal-multiple-properties.png)

* 自定义目标中的单个转化量度没有达到优化性能所需的最少每天10次转化。 发生这种情况可能是因为每日程序包支出最少或自然转化次数有限。 向自定义目标添加其他支持属性可以帮助您实现每天10次转化阈值。 10个支持事件可以帮助程序包达到10/天阈值，即使每个事件的权重都低于一(1)也是如此。 但您可能不需要添加这么多事件。

  在向自定义目标添加支持属性时，请根据支持属性在主要成功事件中的相对重要性为其加权，并牢记数据点的数量。 这允许Adobe Sensei算法平衡多个属性并根据目标进行优化。

  以下示例目标包括三个属性，每个属性具有不同的权重：申请提交= 1、申请开始= 0.1、广告商登陆页面= 0.01。这意味着，每个应用程序提交转化对贵企业的价值与平均10次应用程序开始转化和100次广告商登陆页面转化相同。

  ![具有多个属性的自定义目标示例](/help/dsp/assets/custom-goal-multiple-properties2.png)

  相反，如果您将登陆页面访问量平均计入提交的应用程序，则登陆页面访问量的自然增加可能会压倒您的目标并扭曲到登陆页面访问量。<!--reword-->

>[!MORELIKETHIS]
>
>* [关于自定义目标](custom-goal-about.md)
>* [创建自定义目标](custom-goal-create.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化活动](optimization-how-dsp-optimizes-campaigns.md)

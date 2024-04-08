---
title: 自定义目标
description: 了解自定义目标，以定义针对最低CPA或最高ROAS优化的包中的成功事件。
feature: DSP Optimization
source-git-commit: f05d0f909cda6248260eaafd2fd24a8eca7f47e5
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# 自定义目标

自定义目标定义广告商实现其业务目标所需的成功事件。 每个使用优化目标的包»[!UICONTROL Highest Return on Ad Spend (ROAS)"] 或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]”必须包括有助于实现整体优化目标的自定义目标。 您可以创建自定义目标作为 *目标* 在 [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

每个自定义目标由一个或多个转化量度以及这些量度的相对权重组成。 可用的转化量度包括使用Adobe Advertising转化像素并通过Adobe Analytics跟踪的所有量度。

例如，假设三个转化指标与某个促销活动中的特定包相关：价值20美元的“PDF下载”、价值30美元的“电子邮件注册”和价值40美元的“订单确认”。 如果您要根据客户操作的一次性货币值来赋予权重，则量度的相对权重为1、1.5和2。

一旦您 [创建自定义目标](#custom-goal-create)，您可以 [将其分配给资源包](/help/dsp/campaign-management/packages/package-settings.md) 以使用Adobe Sensei优化报表和算法。

## 创建自定义目标 {#custom-goal-create}

要创建自定义目标，必须将DSP帐户链接到 [!DNL Search, Social, & Commerce] 中具有相同Adobe Experience Cloud组织ID的帐户 [!DNL Search, Social, & Commerce] 客户端设置。 如果您的DSP帐户未关联到 [!DNL Search, Social, & Commerce] 然后，联系您的Adobe客户团队。

1. 登录 [!DNL Advertising Search, Social, & Commerce] at（北美用户） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他用户） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. 确保您要在目标中包含的量度受到跟踪，在产品中可用，并包含显示名称：

   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. 找到量度，并确保 **[!UICONTROL Show in UI and Reports]** 为指标启用。

      >[!NOTE]
      >
      >* [!DNL Analytics] 自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 示例： `custom_event_16_examplersid`

   1. 如果量度在 **[!UICONTROL Display Name]** 列，然后在单元格中单击，输入显示名称，然后单击 **[!UICONTROL Apply].**

1. 创建自定义目标作为 *目标*：

   1. 在主菜单中，单击 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. 在工具栏中，单击 ![创建](/help/dsp/assets/create-search-ui.png "创建").

   1. 输入目标设置，包括非移动设备和移动设备的关联指标及其相对数字权重，然后保存目标。

      必须至少有一个量度具有量度类型 *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] 自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`. 示例： `custom_event_16_examplersid`
      >* [!DNL Analytics] 维度和区段不可用于Adobe Advertising优化。

在使用优化目标的包的DSP包设置中[!UICONTROL Highest Return on Ad Spend (ROAS)"] 或&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]，”目标名称现在包含在中 [!UICONTROL Custom Goals] 列表。 当选择目标作为资源包的自定义目标时， [!UICONTROL Conversion Metric] 列表包含目标的所有目标量度。

>[!TIP]
>
>为获得最佳性能，自定义目标（目标）中的组合量度必须每天至少总计10次转化。 如果不包含，最佳实践是为目标添加其他支持转化量度，如产品页面或应用程序启动次数。 请参阅 [构建自定义目标的最佳实践](custom-goal-best-practices.md) 以了解准则。

## 构建自定义目标的最佳实践 [#custom-goal-best-practices]

### 具有单个量度的自定义目标

以下示例显示如何配置针对单个转化量度的目标。

#### 使用&quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]»优化目标

如果您的促销活动目标是收入([!UICONTROL Highest Return on Ad Spend (ROAS)])，并且所有设备类型的收入对您同样重要，因此请包含&quot;[!UICONTROL Revenue]“量度，具有一(1)的非移动权重（用于来自非移动设备的转化）和一(1)的移动权重（用于来自移动设备的转化）。 选择量度类型 *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 移动权重或移动权重为1(1)就等于跟踪的每个$1收入值为1(1)。
>
> 例如，非移动权重为1 (1)的$250转化报告为$250的转化。 如果将转化量度分配给0.5的非移动权重，则来自非移动设备的转化$250的Adobe Advertising将报告为$125（$250转化* 0.5） [!UICONTROL Non-mobile Weight] = $125)。

#### 使用&quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]»优化目标

如果您的促销活动目标是每次客户获取的最低成本(CPA)，并且它只需要一个成功事件（例如“应用程序提交”），则请包括一个量度并指定量度类型 *[!UICONTROL Goal]*. 最佳做法是将非移动权重和移动权重都设置为一(1)。

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 一个(1)的移动权重或非移动权重等于被跟踪的每个转换的一(1)的值。 例如，如果跟踪了10个申请提交转换，则报告了10个申请提交转换。 但是，如果为转化量度分配了0.5的非移动权重，则10个非移动转化在Adobe Advertising中将被报告为五(5)（10个转化*0.5） [!UICONTROL Non-mobile Weight] = 5)。

### 具有多个量度的自定义目标

在以下两种情况下，您将在自定义目标中使用多个量度：

* 您的营销活动目标有多个成功事件。 例如，您可能正在广告多个网站上的操作(PDF下载、联系我们，以及电子邮件注册)，并且所有操作都有助于实现您的CPA目标。 如果目标包括三个单独的量度，每个量度具有一(1)的非移动和移动权重，则 [!DNL Adobe Sensei] 算法会将每个量度和用户设备类型视为同等重要性。 如果不同的量度和设备类型具有不同的成本或重要性，则应相应地调整其相对权重。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* 自定义目标中的单个转化量度没有达到优化性能所需的最少每天10次转化。 发生这种情况可能是因为每日程序包支出最少或自然转化次数有限。 将其他支持量度添加到自定义目标可以帮助您实现每天10次转化阈值。 10个支持事件可以帮助程序包达到10/天阈值，即使每个事件的权重都低于一(1)也是如此。 但您可能不需要添加这么多事件。

  在向自定义目标添加支持量度时，请根据支持量度对主要成功事件的相对重要性为其加权，并牢记数据点的数量。 这允许Adobe Sensei算法平衡多个量度并根据目标进行优化。

  以下示例目标包括三个指标，每个指标具有不同的非移动权重：应用程序提交= 1，应用程序开始= 0.1，广告商登陆页面= 0.01。这意味着来自非移动设备的每个应用程序提交转化对您的业务具有相同的价值，即平均有10次来自非移动设备的应用程序启动转化和100次来自非移动设备的广告商登陆页面转化。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

相反，如果您将登陆页面访问量平均计入提交的应用程序，那么登陆页面访问量的自然增加可能会压倒您的目标并扭曲到登陆页面访问量。<!--reword-->

>[!MORELIKETHIS]
>
>* [优化目标及其使用方式](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化活动](optimization-how-dsp-optimizes-campaigns.md)

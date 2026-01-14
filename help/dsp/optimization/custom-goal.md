---
title: 自定义目标
description: 了解自定义目标，以定义针对最低CPA或最高ROAS优化的包中的成功事件。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 0%

---

# 自定义目标

自定义目标定义广告商实现其业务目标所需的成功事件。 每个使用优化目标“[!UICONTROL Highest Return on Ad Spend (ROAS)"]”或“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的包都必须包含一个自定义目标，以帮助实现整体优化目标。 您可以在&#x200B;*中创建自定义目标作为*&#x200B;目标[!DNL Advertising Search, Social, & Commerce]。 DSP每个目标的名称必须以“ADSP_”为前缀。

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

每个自定义目标（目标）由一个或多个转化指标及其相对权重组成。 可用的转化量度包括使用Adobe Advertising转化像素并通过Adobe Analytics跟踪的所有量度。 DSP自定义目标仅考虑非移动权重，但它们将用于所有广告类型。

例如，假设三个转化指标与某个营销活动中的特定包相关：价值20美元的“PDF下载”、价值30美元的“电子邮件注册”和价值40美元的“订单确认”。 如果您要根据客户操作的一次性货币值来赋予权重，则量度的相对权重为1、1.5和2。

在[创建自定义目标](#custom-goal-create)后，您可以[将其分配给包](/help/dsp/campaign-management/packages/package-settings.md)，以便使用[!DNL Adobe AI]进行报告和算法优化。

权重推荐是为DSP在目标中归因的量度自动生成的，只需单击一下即可应用所有权重推荐。 对以“ADSP_”为前缀的目标所做的所有权重更改均在两天内以算法方式应用于DSP。 有关权重建议的更多信息，请参阅有关“目标”的“优化指南”一章，该章节可从搜索、社交和Commerce中获取。

## 创建自定义目标 {#custom-goal-create}

要创建自定义目标，必须从[!DNL Search, Social, & Commerce]客户端设置中将DSP帐户链接到具有相同Adobe Experience Cloud组织ID的[!DNL Search, Social, & Commerce]帐户。 如果您的DSP帐户未关联到[!DNL Search, Social, & Commerce]帐户，请联系您的Adobe帐户团队。

1. [登录到Advertising Search、Social和Commerce](/help/search-social-commerce/getting-started/sign-in.md){target="_blank"}。

1. 确保您要在目标中包含的量度受到跟踪，在产品中可用，并包含显示名称：

   1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]** > **[!UICONTROL Conversions]**。

      转化视图将在新的浏览器或浏览器选项卡中打开。

   1. 找到该量度，并确保为该量度启用&#x200B;**[!UICONTROL Show in UI and Reports]**。

      >[!NOTE]
      >
      >* [!DNL Analytics]自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 示例： `custom_event_16_examplersid`

   1. 如果该量度在&#x200B;**[!UICONTROL Display Name]**&#x200B;列中没有任何值，请单击单元格，输入显示名称，然后单击&#x200B;**[!UICONTROL Apply]。**

1. [创建自定义目标作为&#x200B;*目标*](/help/search-social-commerce/new-ui/goals/objectives/objective-create.md){target="_blank"}。 请考虑以下事项：

   * 对于用于Advertising DSP包的目标，目标名称必须以“ADSP_”为前缀，如“ADSP_Registrations”。 前缀不区分大小写。

   * 仅包括归因于DSP的指标。 归因于“搜索”、“社交”和“Commerce”或任何其他广告网络的任何量度将被忽略。

   * 至少一个量度必须具有量度类型&#x200B;*[!UICONTROL Goal]*。

   * DSP对所有广告使用非移动权重。 指定的任何移动权重都将被忽略。

   >[!NOTE]
   >
   >* [!DNL Analytics]自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 示例： `custom_event_16_examplersid`
   >* [!DNL Analytics]维度和区段不可用于Adobe Advertising优化。

   >[!TIP]
   >
   >为获得最佳性能，自定义目标（目标）中的组合量度必须每天至少总计10次转化。 如果不包含，最佳实践是为目标添加其他支持转化量度，如产品页面或应用程序启动次数。 有关准则，请参阅[构建自定义目标的最佳实践](#custom-goal-best-practices)。

在使用优化目标“[!UICONTROL Highest Return on Ad Spend (ROAS)"]”或“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的包的DSP包设置中，目标名称现在包含在[!UICONTROL Custom Goals]列表中。 当您选择目标作为包的自定义目标时，[!UICONTROL Conversion Metric]列表包括该目标的所有目标量度。

## 构建自定义目标的最佳实践 {#custom-goal-best-practices}

### 具有单个量度的自定义目标

以下示例显示如何配置针对单个转化量度的目标。

#### 优化目标为“[!UICONTROL Highest Return on Ad Spend (ROAS)]”的促销活动示例

如果您的促销活动目标是收入([!UICONTROL Highest Return on Ad Spend (ROAS)])，并且所有设备类型的收入对您而言同样重要，则请包含非移动权重为1 (1)的“[!UICONTROL Revenue]”量度；将忽略移动权重。 选择量度类型&#x200B;*[!UICONTROL Goal]*。

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 对于任何设备上用于展示广告的跟踪收入$1，一(1)的非移动权重等于一(1)的值。 例如，非移动权重为1 (1)的$250转化报告为$250的转化。 如果为转化量度分配了0.5的非移动权重，则$250转化在Adobe Advertising中报告为$125（$250转化* 0.5 [!UICONTROL Non-mobile Weight] = $125）。

#### 优化目标为“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的促销活动示例

如果您的促销活动目标是每次客户获取的最低成本(CPA)，并且它只需要一个成功事件（例如“应用程序提交”），则请包含该量度并将量度类型指定为&#x200B;*[!UICONTROL Goal]*。 最佳实践是将非移动权重设置为一(1)；忽略移动权重。

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 对于为在任何设备上显示广告跟踪的每个转化，一个(1)的非移动权重等于一个(1)的值。 例如，如果跟踪了10个申请提交转换，则报告了10个申请提交转换。 但是，如果为转化量度分配了0.5的非移动权重，则10次转化在Adobe Advertising中报告为五(5)（10次转化* 0.5 [!UICONTROL Non-mobile Weight] = 5）。

### 具有多个量度的自定义目标

在以下两种情况下，您将在自定义目标中使用多个量度：

* 您的营销活动目标有多个成功事件。 例如，您可能在为多个网站操作(PDF下载、联系我们，以及电子邮件注册)打广告，所有这些操作都有助于您的CPA目标。 如果目标包括三个单独的量度，每个量度的非移动权重为1，则[!DNL Adobe AI]支持的算法会将每个量度和用户设备类型视为同等重要性。 如果不同量度的成本或重要性不同，请相应地调整其相对权重。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* 自定义目标中的单个转化量度没有达到优化性能所需的最少每天10次转化。 发生这种情况可能是因为每日程序包支出最少或自然转化次数有限。 将其他支持量度添加到自定义目标可以帮助您实现每天10次转化阈值。 10个支持事件可以帮助程序包达到10/天阈值，即使每个事件的权重都低于一(1)也是如此。 但您可能不需要添加这么多事件。

  在向自定义目标添加支持量度时，请根据支持量度对主要成功事件的相对重要性为其加权，并牢记数据点的数量。 这允许由[!DNL Adobe AI]支持的算法平衡多个量度并根据目标进行优化。

  以下示例目标包括三个指标，每个指标具有不同的非移动权重：应用程序提交= 1，应用程序开始= 0.1，广告商登陆页面= 0.01。这意味着，每个应用程序提交转化对贵企业的价值与平均10次应用程序开始转化和100次广告商登陆页面转化相同。

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

相反，如果您将登陆页面访问次数平均计入提交的应用程序，那么登陆页面访问次数的自然增加可能会压倒您的目标，并扭曲到登陆页面访问次数。<!--reword-->

>[!MORELIKETHIS]
>
>* [优化目标及其使用方式](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化您的营销活动](optimization-how-dsp-optimizes-campaigns.md)

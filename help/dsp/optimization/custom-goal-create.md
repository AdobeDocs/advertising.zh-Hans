---
title: 创建自定义目标
description: 创建自定义目标
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# 创建自定义目标

您可以创建自定义目标作为 *目标* 范围 [!DNL Advertising Search, Social, & Commerce].

要创建自定义目标，必须将DSP帐户链接到 [!DNL Search, Social, & Commerce] 中具有相同Adobe Experience Cloud组织ID的帐户 [!DNL Search, Social, & Commerce] 客户端设置。 如果您的DSP帐户未关联到 [!DNL Search, Social, & Commerce] 联系您的Adobe客户团队。

>[!TIP]
>
>请参阅 [创建自定义目标的最佳实践](custom-goal-best-practices.md) 以获取有关如何配置自定义目标的提示。

1. 登录 [!DNL Advertising Search, Social, & Commerce] at（北美用户） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他用户） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 确保您要在目标中包含的量度受到跟踪，在产品中可用，并包含显示名称：
   1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. 找到量度，并确保 **[!UICONTROL Show in UI and Reports]** 为指标启用。
   1. 如果量度在 **[!UICONTROL Display Name]** 列，在单元格中单击，输入显示名称，然后单击 **[!UICONTROL Apply].**
1. 创建自定义目标作为 *目标*：
   1. 在主菜单中，单击 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. 在工具栏中，单击 **[!UICONTROL Create objective].**
   1. 输入目标设置：
      1. 在 **[!UICONTROL Change Objective Name]** 字段，输入目标名称。

         目标名称将显示在 [!UICONTROL Custom Goals] DSP列表。

      1. 将资产与以下目标关联：

         >[!NOTE]
         >
         > 默认情况下，为广告商跟踪的所有转化量度都会列在 [!UICONTROL Available Properties] 列表。

         * 要导入包含转化量度及其权重的CSV文件，请单击 **[!UICONTROL Import]** 并找到要导入的文件。

           广告商的导入转化量度必须已存在；名称不区分大小写。

           导入的转化量度将替换指定的任何现有属性。

         * 要手动指定具有默认权重(1)的第一个转化量度，请从为广告商跟踪的所有转化量度的列表中进行选择。

         * 要手动添加另一个具有默认权重(1)的转化量度，请单击 **[!UICONTROL +]** .

           >[!TIP]
           >
           > 要在列表中搜索指标，请在指标名称中的任何位置输入一个字符串。

         * 要手动添加多个转化量度，请单击 **[!UICONTROL Add Multiple Properties].** 对于要添加的每个转化指标，单击以下位置中的指标名称： [!UICONTROL Available Properties] 列并将其拖动到 [!UICONTROL Added Properties] 列。 添加完量度后，单击 **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* 要在列表中搜索指标，请在输入字段的指标名称中的任何位置输入一个字符串。
           >* 要过滤列表以排除报告中排除的指标，请选择选项 **[!UICONTROL Hide properties excluded from reports].**

         * （当目标包含多个转化指标时）要更改指标相对于目标中其他指标的权重，请在 **[!UICONTROL Weight]** 字段。

      1. 在设置底部，单击 **[!UICONTROL Save]**.

创建目标后，如果优化目标是&#39;&#39;，则可以将其作为自定义目标分配给DSP包[!UICONTROL Highest ROAS - Custom Goal]”或“[!UICONTROL Lowest CPA - Custom Goal]“

>[!TIP]
>
>为获得最佳性能，自定义目标（目标）中的组合量度必须每天至少总计10次转化。 如果不包含，最佳实践是为目标添加其他支持转化量度，如产品页面或应用程序启动次数。 请参阅 [构建自定义目标的最佳实践](custom-goal-best-practices.md) 以了解准则。

>[!MORELIKETHIS]
>
>* [关于自定义目标](custom-goal-about.md)
>* [构建自定义目标的最佳实践](custom-goal-best-practices.md)
>* [优化目标及其使用方式](optimization-goals.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何优化活动](optimization-how-dsp-optimizes-campaigns.md)

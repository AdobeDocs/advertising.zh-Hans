---
title: 创建可重复使用的受众
description: 了解如何创建可重用受众，该受众由受众区段和其他保存的受众组成。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# 创建可重复使用的受众

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以保存和管理可重用受众，这些受众是受众区段组，甚至是其他保存的受众，您可以将其用作多个投放位置的定位或排除项。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。

1. 输入唯一的&#x200B;**[!UICONTROL Audience Name]**。

1. （可选）取消选择&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的选项。

   当您共享受众时，该受众将可用作帐户中所有广告商的目标或排除项。 但是，受众中的各个区段仅适用于共享这些区段的用户。 例如，如果您将包含Adobe Analytics区段的受众与未映射到同一[!DNL Analytics]帐户的广告商共享，则该受众不会预览该广告商的区段。 在受众中只会预览对该广告商可用的区段。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. 构建受众：

   >[!NOTE]
   >
   >构建受众时，右侧面板中更新了[受众规模的详细信息](audience-about.md)

   * 要使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]选项卡](audience-settings.md)上可用的区段手动创建区段逻辑，请执行以下操作。

      * 要添加第一个区段，请在左侧面板中查找该区段，然后选中区段名称旁边的复选框。

      * 要将区段添加到现有区段组，请执行以下操作：

         1. 单击右侧面板中的区段组。

         1. （可选）根据需要将组逻辑更改为&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

            *[!UICONTROL Exclude All]*&#x200B;不可用于第一个区段组。 对于仅包含排除项的受众，请将此受众构建为&#x200B;*[!UICONTROL Include Any]*，然后在投放位置中，从“排除的受众”菜单中选择该受众。

         1. 在左侧面板中找到新区段，然后选中区段名称旁边的复选框。

            区段组会自动更新为新区段。

      * 要添加新区段组，请执行以下操作：

         1. 单击右侧面板中的&#x200B;**[!UICONTROL + New Group]**。

         1. （可选）根据需要将上一个组与新组之间的逻辑更改为&#x200B;*[!UICONTROL And]*&#x200B;或&#x200B;*[!UICONTROL Or]*。

         1. 在左侧面板中找到新组的区段，并选中区段名称旁边的复选框。

         1. （可选）根据需要将组逻辑更改为&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

   * 要使用现有受众的区段逻辑，请执行以下操作：

      1. 通过以下任一方式从现有受众复制区段逻辑：

         * 在“所有受众”视图中，将光标悬停在受众行上，然后单击&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在现有受众的设置中，单击区段逻辑面板顶部的&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在文本编辑器中，使用字母数字区段ID和[布尔语法](audience-segment-logic-syntax.md)手动创建区段逻辑，并将其复制到剪贴板。

      1. 单击&#x200B;**[!UICONTROL paste in an audience rule to begin building]**，将现有区段逻辑粘贴到输入字段中，然后单击&#x200B;**[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果受众已包含任何区段逻辑，则在新的区段逻辑中粘贴将覆盖现有逻辑。

1. 单击&#x200B;**[!UICONTROL Create]**。

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [可用的第三方数据提供程序](third-party-data-providers.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建并实施[!UICONTROL CCPA Opt-Out-of-Sale]区段](ccpa-opt-out-segment-create.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)

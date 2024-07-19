---
title: 编辑可重用受众
description: 了解如何编辑可重复使用的受众。
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 编辑可重用受众

当您编辑在任何投放位置或其他可重用受众中使用的受众时，更改将立即应用于这些投放位置和受众。<!-- verify -->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**。

1. 将光标悬停在受众行上并单击&#x200B;**[!UICONTROL Edit]**。

1. 通过下列任一方式编辑受众设置：

   >[!NOTE]
   >
   >如果您编辑受众区段逻辑，则右侧面板中会更新详细的[受众规模数据](audience-about.md)。

   * （可选）要编辑&#x200B;**[!UICONTROL Audience Name]**，请单击受众名称旁边的![编辑](/help/dsp/assets/edit.png)，输入唯一的受众名称，然后单击&#x200B;**[!UICONTROL Apply]**。

   * （可选）要使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]选项卡](audience-settings.md)上可用的区段手动编辑区段逻辑，请执行以下操作。

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

1. 单击&#x200B;**[!UICONTROL Save]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Continue]**。

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [复制可重复使用的受众](reusable-audience-duplicate.md)
>* [查看有关可重用受众的详细信息](reusable-audience-view-details.md)
>* [共享可重复使用的受众](reusable-audience-share.md)
>* [导出可重复使用的受众](reusable-audience-export.md)
>* [将可重用受众的区段密钥复制到剪贴板](reusable-audience-clipboard.md)
>* [删除可重复使用的受众](reusable-audience-delete.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [可用的第三方数据提供程序](third-party-data-providers.md)

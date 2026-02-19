---
title: 将动态创意添加到创意库
description: 了解如何将动态创意添加到创意库。
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
source-git-commit: 2a89d5f3997345c051728d41af865dc0e75541f5
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# 将动态创意添加到创意库

将动态创意添加到您的[创意库](creative-library-manage.md)中以与动态[广告体验](/help/creative/experiences/experience-about.md)一起使用。 您可以从单个广告模板创建单个静态HTML5广告或动态HTML5广告。 对于动态HTML5广告，使用从馈送文件创建的指定目录中的资源。

>[!PREREQUISITES]
>
>在将动态创意添加到创意库之前，您必须完成其他步骤 — 包括创建广告模板、上传资源以及(动态HTML5广告)创建信息源模板和目录。 请参阅[动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)。

<!-- This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## 使用动态HTML5广告模板添加动态创意

1. 执行以下任一操作：

   * 从创意库：

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

      1. 单击库名称。

      1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**。

   * 从广告模板：

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

      1. 将光标悬停在广告模板行上并单击&#x200B;**[!UICONTROL Create Dynamic Ad]**。

1. 指定[动态广告设置](/help/creative/creative-libraries/creative-settings-dynamic.md)：

   1. 指定基本广告详细信息，包括创意类型。

   1. 选择要用于创意人员的广告模板。

      将HTML5广告模板用于显示广告，将视频广告模板用于视频广告。

   1. 选择要从中生成广告的目录。

   1. 选择用于创建广告的目录行的标准。

   1. 将指定广告模板中的每个属性（动态广告字段）映射到指定馈送文件（目录标签）中的列，或输入静态值。

   1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;预览要生成的创意。 您可以在预览中执行以下任一操作：

      * 要按目录、筛选值<!-- explain more-->和广告大小筛选创意，请使用预览区域上方的筛选器。

      * 在预览区域下方的搜索字段中按产品的唯一ID搜索产品。

      * 要更改显示的列，请单击预览区域下方的![列筛选器](/help/creative/assets/custom-columns.png "列筛选器")。

      * 要预览特定创意，请选中行的复选框。

      * 更改内容：

         * （仅显示广告）要编辑表中单元格的值，请单击单元格内部并编辑该值。 单击单元格外部或按&#x200B;**[!DNL Enter]**&#x200B;键保存更改。

         * 要将单个产品标记为默认<!--Explain what this means. -->，请将光标悬停在该行上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Set as Default]**。

         * （当广告包含多个选件时）要将多个产品标记为默认值，请选择行（最多包含选件数），然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Set as Default]**。

      * 要从目录中删除产品，请将光标悬停在该行上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete Row]**。

      * （当广告包含多个选件时）要从目录中删除多个产品，请选择行（最多包含选件数），然后单击批量操作工具栏中的&#x200B;**[!UICONTROL Delete Row]**。

1. 保存创意：

   * 要保存广告并将其添加到库中的[创意包](/help/creative/creative-libraries/bundle-manage.md)，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Save and Attach to Bundle]**。

      1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;保存广告。

      1. 选择包，然后单击&#x200B;**[!UICONTROL Attach Creative to Bundles]**。

   * 若要保存广告并退出设置，请单击&#x200B;**[!UICONTROL Save]**，然后再次单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [动态创意设置](creative-settings-dynamic.md)
>* [在创意库中编辑动态创意](creative-edit-dynamic.md)
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)

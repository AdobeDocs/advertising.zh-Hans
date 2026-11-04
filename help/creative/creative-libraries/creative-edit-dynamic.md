---
title: 编辑和质量检查动态创意
description: 了解如何在创意库中编辑动态创意设置和质量检查目录内容。
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# 编辑和质量检查动态创意

编辑创意设置以更改创意的配置，例如其名称、目录和属性映射。 使用QA代理审查生成的广告并更正目录值。

## 编辑创意设置 {#edit-creative-settings}

### 通过新的UI {#from-the-new-ui}

1. 打开创意设置：

   * 从创意库：

     1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

     1. 通过以下任一方式打开库：

        * 单击库名称。

        * 在库名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Open]**。

     1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击创意名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Edit]**。

   * 从[!UICONTROL Creative Studio]：

     1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]>[!UICONTROL Creative Studio]**。

     1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

        此时将打开一个全屏编辑器，左侧显示广告预览，右侧显示设置面板。

1. 使用&#x200B;**[!UICONTROL Details]**&#x200B;和&#x200B;**[!UICONTROL Attribute Mapping]**&#x200B;选项卡编辑创意设置：

   **[!UICONTROL Details]**&#x200B;选项卡：

   * **[!UICONTROL Advertiser]**、**[!UICONTROL Ad Library]**&#x200B;和&#x200B;**[!UICONTROL Ad template]**&#x200B;是只读的。
   * **[!UICONTROL Dynamic creative name]：**&#x200B;创意内容的显示名称。
   * **[!UICONTROL Number of cards]：**&#x200B;每个广告组合中包含的目录选件数(1-50)。
   * （可选）在&#x200B;**[!UICONTROL Catalogs]**&#x200B;下，更新目录选择：
     * 使用&#x200B;**[!UICONTROL Catalog template]**&#x200B;筛选可用目录。 若要选择下载模板文件，请单击&#x200B;**[!UICONTROL Download feed template]**。
     * 搜索并从列表中选择目录，或通过将新目录文件拖到上传区域或单击&#x200B;**[!UICONTROL Browse Files]**&#x200B;来上传新目录文件（支持的格式：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP、MP4；最大25 MB；一次一个文件）。 上传的目录在芯片列表中标记为&#x200B;**（已上传）**。

     所有目录必须属于同一目录模板系列。

   **[!UICONTROL Attribute Mapping]**&#x200B;选项卡：

   * 在&#x200B;**[!UICONTROL Targeting]**&#x200B;下，至少选择一个数据源： **[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**&#x200B;或&#x200B;**[!UICONTROL Audience Segment]**。
   * 在&#x200B;**[!UICONTROL Attribute Mapping]**&#x200B;下，更新每个模板层名称到相应目录列标签的映射。

1. 单击&#x200B;**[!UICONTROL Update Creative]**。

### 从旧版UI {#from-the-legacy-ui}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击&#x200B;**[!UICONTROL Switch to classic UI]**。

1. 单击库名称。

1. 将光标悬停在创意行上并单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[动态广告设置](creative-settings-dynamic.md)。

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

   * 要保存广告并将其添加到库中的[创意包](bundle-manage.md)，请执行以下操作：

     1. 单击&#x200B;**[!UICONTROL Save and Attach to Bundle]**。

     1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;保存广告。

     1. 选择包，然后单击&#x200B;**[!UICONTROL Attach Creative to Bundles]**。

   * 若要保存广告并退出设置，请单击&#x200B;**[!UICONTROL Save]**，然后再次单击&#x200B;**[!UICONTROL Save]**。

## 质量检查动态创意（仅限新UI） {#qa-dynamic-creative}

使用新UI中的QA代理，根据动态创意的模板分析目录行，预览生成的广告，并确定潜在的内容问题。 您可以使用&#x200B;**[!UICONTROL AI Assistant]**&#x200B;筛选和分组广告，查看目录警报，并在发布更改之前手动更正目录值。

>[!NOTE]
>
>您可以对来自[!UICONTROL Creative Libraries]或[!UICONTROL Creative Studio]的动态创意进行质量检查。 有关其他入口点，请参阅“[Quality-check a dynamic creative from Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative)”。

QA代理仅适用于基于动态模板的动态显示创意，而不适用于标准创意或动态视频创意。

### 打开QA代理 {#open-qa-agent}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 通过以下任一方式打开库：

   * 单击库名称。
   * 在库名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Open]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击动态创意名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL QA Agent]**。

   将打开&#x200B;**[!UICONTROL Dynamic Creative QA]**&#x200B;屏幕，其中显示预览画布和&#x200B;**[!UICONTROL AI Assistant]**&#x200B;聊天面板。

1. 如果创意内容使用多个目录，请从标题中的&#x200B;**[!UICONTROL Catalog]**&#x200B;中选择要查看的目录。

   助理分析所选目录。 当创意仅使用一个目录时，将禁用目录选择器。

### 使用AI分析和过滤广告 {#analyze-ads}

1. 在&#x200B;**[!UICONTROL AI Assistant]**&#x200B;面板中，在&#x200B;**[!UICONTROL Ask anything]**&#x200B;中键入请求并按&#x200B;**[!UICONTROL Enter]**，或单击建议的提示之一：

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   助理在聊天面板中进行响应，并在画布上显示匹配的目录行作为广告预览。 在提交请求之前，画布会提示您请求助理分析目录。

1. 通过后续请求继续完善审查。 该助理可以帮助您：

   * 按受众区段、语言、地理位置或邮政编码过滤广告。
   * 使用指定的阈值检查字符长度。
   * 检查馈送错误、缺少内容和可疑内容。
   * 查看翻译状态。
   * 比较A/B测试变体。
   * 将广告分组以供审阅，例如按产品或问题分组。

   验证助理的响应并在保存更改之前检查预览。

### 查看预览和警报 {#review-previews}

* 使用画布工具栏可以：

  * 调整缩放。
  * 在&#x200B;**[!UICONTROL Thumbnail view]**&#x200B;和&#x200B;**[!UICONTROL Actual size]**&#x200B;之间切换。
  * 单击&#x200B;**[!UICONTROL Replay animations]**&#x200B;重播预览。
  * 选择每页的行数，选择页码，或使用&#x200B;**[!UICONTROL Previous page]**&#x200B;和&#x200B;**[!UICONTROL Next page]**。

* 当助理对结果分组时，单击链接可查看组中的所有创意。 使用&#x200B;**[!UICONTROL Back to groups]**&#x200B;返回分组结果，或使用&#x200B;**[!UICONTROL Catalog Rows]**&#x200B;离开分组视图。

* 当预览显示&#x200B;**[!UICONTROL Issues detected]**&#x200B;时，将光标悬停在指示器上可查看问题详细信息。

* 当目录警报可用时，单击&#x200B;**[!UICONTROL View Alerts]**。 **[!UICONTROL Alerts]**&#x200B;对话框列出了每个问题的目录、行号、列和错误消息。 单击&#x200B;**[!UICONTROL Close]**&#x200B;以返回画布。

### 更正目录值 {#correct-catalog-values}

无需离开QA屏幕，即可从广告预览中手动编辑目录值。

1. 在要更正的预览上，单击&#x200B;**[!UICONTROL Edit]**。

1. 在“编辑”对话框中，选择要在&#x200B;**[!UICONTROL Catalog columns to edit]**&#x200B;下更改的列。 若要查找列，请使用&#x200B;**[!UICONTROL Search columns]**。

1. 在&#x200B;**[!UICONTROL Columns content]**&#x200B;下，更新所选字段值。

1. 单击&#x200B;**[!UICONTROL Update]**。

   预览会刷新以反映更新的值。 在保存动态创意之前，不会发布目录更改。

>[!IMPORTANT]
>
>这些编辑可更新目录数据，而不仅仅是广告预览。 在发布值之前对其进行审核。

### 保存更改或退出 {#save-or-exit}

* 要保存现有的动态创意并发布任何目录编辑，请执行以下操作：

  1. 单击标题中的&#x200B;**[!UICONTROL Save Dynamic Creative]**。

  1. 在&#x200B;**[!UICONTROL Update Dynamic Creative]**&#x200B;确认对话框中，单击&#x200B;**[!UICONTROL Update]**。

     返回到创意库。

* 要离开而不发布挂起的目录编辑，请单击页眉中的&#x200B;**[!UICONTROL Cancel]**。

>[!MORELIKETHIS]
>
>* [动态创意设置](creative-settings-dynamic.md)
>* [将动态创意添加到创意库](creative-add-dynamic.md)
>* [查看创意内容的更改日志](/help/creative/creative-libraries/creative-view-change-log.md)
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)

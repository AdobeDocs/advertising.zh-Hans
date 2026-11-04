---
title: 在Creative Studio中管理动态创意人员
description: 了解如何在Adobe Advertising Creative Studio中构建、质量检查、编辑、复制和删除目录驱动型动态创意。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b9a68528b3c622aae44a46bca9b3bb747019bc95
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# 在[!UICONTROL Creative Studio]中管理动态创意

[!UICONTROL Creative Studio]中的&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡按库列出了您的动态创意。 在此处，您可以构建新的目录驱动型动态创意、使用AI检查创意的质量、编辑现有创意的详细信息和属性映射、查看更改日志、复制创意以及删除创意。

## 构建动态创意 {#build-dynamic-creative}

使用此工作流可创建目录驱动的动态创意。 四步引导式向导将指导您选择模板、连接目录以及将目录字段映射到模板元素。 设置后，[!UICONTROL AI Assistant]可帮助您预览和质量检查从目录数据生成的每个广告组合。

动态创意与标准广告的一个关键区别在于：AI代理无法修改目录源内容。 它可以过滤、分析和标记问题 — 但要更改广告内容，您必须手动更新目录值，无论是在QA屏幕中还是在源目录中。

### 先决条件

* 您的模板库中必须至少存在一个用户创建的显示广告模板（不是系统模板）。
* 您的帐户中提供了产品或内容目录（馈送）。

### 步骤1：打开[!UICONTROL Build Dynamic Creative]向导 {#open-wizard}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Build dynamic creatives from catalog data]**&#x200B;快速操作信息卡中的&#x200B;**[!UICONTROL Build]**。

   此时将打开四步&#x200B;**[!UICONTROL Build Dynamic Creative]**&#x200B;对话框。

### 第2步：选择模板 {#select-template}

>[!NOTE]
>
>模板库仅列出您创建的显示广告模板。 系统模板和视频广告模板不能作为动态创意的起点。

1. 在模板库中，单击模板以将其选定。

   在选择模板之前，**[!UICONTROL Next]**&#x200B;按钮处于禁用状态。

1. 单击&#x200B;**[!UICONTROL Use this template]**。

### 第3步：选择目录 {#select-catalog}

1. 配置创意设置：

   * **[!UICONTROL Ad Library]：**&#x200B;选择要保存创意的创意库。
   * **[!UICONTROL Dynamic creative name]：**&#x200B;输入动态创意的名称。
   * **[!UICONTROL Number of cards]：**&#x200B;输入要包含在每个广告组合中的目录选件数量(1-50)。
   * **[!UICONTROL Assign dynamic creative to a bundle]：**（可选）启用时，保存的创意将附加到捆绑包。 从库中选择捆绑包。

1. 选择一个或多个目录：

   1. （可选）使用&#x200B;**[!UICONTROL Catalog template]**&#x200B;将目录列表筛选到特定的模板系列。 若要选择下载模板文件以进行审阅，请单击&#x200B;**[!UICONTROL Download feed template]**。

   1. 搜索并从列表中选择目录。 所有选定的目录必须属于同一个目录模板系列；如果尝试混合系列，则会出现警告。

   1. （可选）要上传新的目录文件，请将该文件拖放到上传区域或单击&#x200B;**[!UICONTROL Browse Files]**。 支持的格式：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP和MP4。 最大文件大小：25 MB。 您可以一次上传一个文件。 上传的目录显示在标记为&#x200B;**（已上传）**&#x200B;的芯片列表中。

1. 单击&#x200B;**[!UICONTROL Continue]**。

### 步骤4：将目录字段映射到模板元素 {#attribute-mapping}

将每个目录字段映射到模板中的相应元素。 例如，将目录的产品名称字段映射到模板的标题元素，将产品图像字段映射到背景图像元素。

1. 在&#x200B;**[!UICONTROL Targeting]**&#x200B;下，选择至少一个数据源以个性化创意： **[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**&#x200B;或&#x200B;**[!UICONTROL Audience Segment]**。

1. 对于每个模板元素，从下拉列表中选择匹配的目录字段。

1. 单击&#x200B;**[!UICONTROL Continue]**。

### 步骤5：使用人工智能预览和QA {#qa}

1. 选择是&#x200B;*[!UICONTROL Save Dynamic Creative & Skip QA]*&#x200B;还是&#x200B;*[!UICONTROL Continue to QA]*。

   如果继续QA，则会打开&#x200B;**[!UICONTROL Dynamic Creative QA]**&#x200B;屏幕，其中显示预览画布和&#x200B;**[!UICONTROL AI Assistant]**&#x200B;聊天面板。

1. 如果继续QA，请按照“[质量检查动态创意](#qa-dynamic-creative)”中的过程来[分析和过滤广告](#analyze-ads)、[查看预览和警报](#review-previews)，并可选[更正目录值](#correct-catalog-values)。 完成后，[保存动态创意](#save-or-exit)。

## 编辑动态创意 {#edit-dynamic-creative}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

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

## 对动态创意内容进行质量检查 {#qa-dynamic-creative}

使用QA助手可针对动态创意内容的模板分析目录行，预览生成的广告，并确定潜在的内容问题。 您可以使用&#x200B;**[!UICONTROL AI Assistant]**&#x200B;筛选和分组广告，查看目录警报，并在发布更改之前手动更正目录值。

>[!NOTE]
>
>您可以对来自[!UICONTROL Creative Studio]或[!UICONTROL Creative Libraries]的动态创意进行质量检查。 虽然菜单标签不同，但两个入口点都打开了功能相同的同一&#x200B;**[!UICONTROL Dynamic Creative QA]**&#x200B;屏幕。 分析取决于所选的创意、目录和请求。 有关其他入口点，请参阅&quot;[质量检查Creative Libraries中的动态创意](/help/creative/creative-libraries/creative-edit-dynamic.md#qa-dynamic-creative)&quot;。

QA助手适用于动态显示创意，而非标准创意或动态视频创意。

### 打开QA助手 {#open-qa-agent}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，在[!UICONTROL Generate or Build Creatives]部分下的创意库中找到该动态创意。

1. 将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**。

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

* 要保存动态创意并发布任何目录编辑，请执行以下操作：

  1. 单击标题中的&#x200B;**[!UICONTROL Save Dynamic Creative]**。

  1. 确认保存：

     * 对于新创意，在&#x200B;**[!UICONTROL Create Dynamic Creative]**&#x200B;确认对话框中，单击&#x200B;**[!UICONTROL Create]**。
     * 对于现有的创意，在&#x200B;**[!UICONTROL Update Dynamic Creative]**&#x200B;确认对话框中，单击&#x200B;**[!UICONTROL Update]**。

     返回[!UICONTROL Creative Studio]。

* 要离开而不发布挂起的目录编辑，请单击页眉中的&#x200B;**[!UICONTROL Cancel]**。

## 查看动态创意的更改日志 {#view-change-log}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Change Log]**。

## 复制动态创意 {#duplicate-dynamic-creative}

复制动态创意内容以将具有相同设置的新创意内容添加到库。 您稍后可以重命名新的创意并根据需要编辑设置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

   新创意名为`<original name> (copy)`。

## 删除动态创意 {#delete-dynamic-creative}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [关于Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理模板](creative-studio-manage-templates.md)

---
title: 在Creative Studio中管理动态创意人员
description: 了解如何在Adobe Advertising Creative Studio中构建、编辑、复制和删除目录驱动型动态创意。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# 在[!UICONTROL Creative Studio]中管理动态创意

*Beta功能*

[!UICONTROL Creative Studio]中的&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡按库列出了您的动态创意。 在此页面中，您可以构建新的目录驱动型动态创意，编辑现有创意的详细信息和属性映射，查看更改日志、复制创意以及删除创意。

## 构建动态创意 {#build-dynamic-creative}

使用此工作流可创建目录驱动的动态创意。 四步引导式向导将指导您选择模板、连接目录以及将目录字段映射到模板元素。 设置后，[!UICONTROL AI Assistant]可帮助您预览和质量检查从目录数据生成的每个广告组合。

动态创意与标准广告的一个关键区别在于：AI代理无法修改目录源内容。 它可以过滤、分析和标记问题，但要更改广告内容，您必须更新源目录。

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

   如果继续QA，画布将显示从目录生成的所有广告组合，显示为行，模板中呈现的每个目录条目均带有预览。

1. 如果继续QA：

   1. 执行以下任一操作：

      * 使用&#x200B;**[!UICONTROL Zoom in]**&#x200B;和&#x200B;**[!UICONTROL Zoom out]**&#x200B;控件调整画布视图。

      * 使用分页控件(**X-Y / Z**)逐页浏览目录行。

      * 要编辑广告组合，请执行以下操作：

         1. 将光标悬停在目录行上并单击&#x200B;**[!UICONTROL Edit]**。

         1. 在&#x200B;**[!UICONTROL Edit Row]**&#x200B;对话框中，更新字段值。

         1. 单击&#x200B;**[!UICONTROL Save]**。

        画布将刷新，以反映更新的值。

      * 使用&#x200B;**[!UICONTROL AI Assistant]**&#x200B;聊天面板来分析和筛选目录组合。 在&#x200B;**[!UICONTROL Ask anything]**&#x200B;字段中键入您的请求，或单击建议的提示之一：

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        AI代理可以：

         * 筛选画布以显示与特定受众区段、地理位置、语言、类别或其他目录字段匹配的广告。
         * 检查质量问题，如字符限制溢出、内容溢出或出血、图像链接断开和免责声明可见性。
         * 比较A/B测试分析的广告组合
         * 将广告整理到不同的组中，以便进行并排审查。

        AI代理无法修改目录源内容。 要更改广告内容，请更新源目录。

   1. 在标题中保存&#x200B;**[!UICONTROL Save Dynamic Creative]**。

   1. 在确认消息中，单击&#x200B;**[!UICONTROL Create]**。

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

## 为动态创意重新打开QA助手 {#qa-dynamic-creative}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**。

   将打开QA屏幕。 有关可用的画布控件和AI助手功能，请参阅“[步骤5：使用AI](#qa)预览和QA”。

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

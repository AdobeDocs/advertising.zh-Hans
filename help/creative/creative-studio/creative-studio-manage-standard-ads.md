---
title: 在Creative Studio中管理标准广告
description: 了解如何在Creative Studio创意内容库中创建、编辑、复制、下载和删除标准显示广告。
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# 在[!UICONTROL Creative Studio]中管理标准广告

*Beta功能*

[!UICONTROL Creative Studio]中的&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡是从模板生成的标准显示广告库。 在此处，您可以使用[!UICONTROL Ad Variations Generator]创建广告、编辑保存的广告、从现有广告生成新变体、查看更改日志、复制、下载和删除。

## 创建标准广告 {#create-standard-ads}

使用[!UICONTROL Ad Variations Generator]从模板生成显示广告内容。 AI助手可生成和优化标题、CTA、图像、颜色等，并可在单个会话中创建新的大小变量。

>[!NOTE]
>
>标准广告生成当前仅支持显示广告模板。 视频广告模板不能作为起点，不能从&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡或&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡开始。

### 先决条件

模板库中必须至少存在一个显示广告模板。

### 生成标准广告

1. 通过以下任一方式打开[!UICONTROL Ad Variations Generator]：

   * **从[!UICONTROL Creatives]选项卡：**

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

      1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Generate standard ads from templates]**&#x200B;快速操作信息卡中的&#x200B;**[!UICONTROL Generate]**。

      1. 在模板选择对话框中，单击模板以将其选中，然后单击&#x200B;**[!UICONTROL Use this template]**。

   * （仅显示广告）**从[!UICONTROL Templates]选项卡：**

      1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

      1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

      1. 将光标悬停在模板卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**。

   将打开[!UICONTROL Ad Variations Generator]。 画布显示具有模板可用广告格式的&#x200B;**[!UICONTROL Template Sizes]**&#x200B;部分和将显示所生成内容的&#x200B;**[!UICONTROL Ad Concepts]**&#x200B;部分。

1. （可选）要将品牌配置文件应用到广告，请在画布工具栏中选择&#x200B;**[!UICONTROL Brand Profile]**。

   AI助手在生成内容时使用您品牌的徽标、调色板、语音准则、图像标准和渠道准则。

1. 使用[!UICONTROL AI Assistant]生成广告变体：

   1. 在&#x200B;**[!UICONTROL Ask AI to generate ad variations…]**&#x200B;字段中，键入请求并按&#x200B;**[!UICONTROL Enter]**，或单击功能提示之一：

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      AI在画布上生成结果并将结果组织为&#x200B;*概念*，每个概念表示不同的内容变体。 **[!UICONTROL Ad Concepts]**&#x200B;部分中的概念计数器跟踪存在的概念数(例如，**(2/10)**)。 每个会话最多允许10个概念。

   1. 通过发送跟进消息继续优化。 示例：

      * “让所有文案变得更好玩，更少企业化。”
      * “将徽标更改为白色版本。”
      * “将CTA设置为在所有概念上‘立即购买’。”
      * “将此广告的大小调整为所有6个IAB标准显示大小。”
      * “给我3个不同的标题概念，每个概念都有匹配的背景图像。”

      >[!NOTE]
      >
      >AI助手可以生成和修改文本（标题、副标题、CTA、正文）、交换背景图像、应用品牌颜色、切换徽标版本以及创建新大小模板。 它无法更改模板结构：元素位置、布局、间距、填充、字体系列、字体大小或边框。 在启动会话之前，在模板编辑器中执行结构性更改。 请参阅[编辑模板](creative-studio-manage-templates.md#edit-template)。

   1. （可选）要在请求中包含可视化引用，请单击聊天输入区域中的&#x200B;**[!UICONTROL +]**&#x200B;按钮。 在&#x200B;**[!UICONTROL Select from Asset Library]**&#x200B;对话框中：

      * 要在资源库中使用资源，请单击该资源，然后单击&#x200B;**[!UICONTROL Add to chat]**。 提交消息以包含作为上下文的资产。

      * 要上传一个或多个资产，请单击&#x200B;**[!UICONTROL Upload Assets]**&#x200B;并选择设备或网络上的文件。

1. （可选）使用画布工具栏查看生成的广告：

   * **[!UICONTROL Brand]：**&#x200B;选择或更改应用于会话的品牌配置文件。
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]：**&#x200B;调整画布缩放级别。
   * **[!UICONTROL Fit to screen]：**&#x200B;重置视图以显示所有大小。
   * **[!UICONTROL Replay animations]：**&#x200B;重播模板动画。

   当AI创建新大小时，**[!UICONTROL Adjust]**、**[!UICONTROL Keep]**&#x200B;和删除控件将显示在新大小卡上。 单击&#x200B;**[!UICONTROL Keep]**&#x200B;接受现有大小，单击&#x200B;**[!UICONTROL Adjust]**&#x200B;在显示编辑器中打开模板（可在其中进行结构更改），然后单击&#x200B;**[!UICONTROL Update Ad Format]**&#x200B;进行保存，或单击“删除”图标删除新大小。

1. （可选）管理概念和变体：

   * 若要管理概念，请将光标悬停在概念标签上（例如，**[!UICONTROL Concept 3]**），然后单击&#x200B;**[!UICONTROL ...]**，然后选择选项：

      * **[!UICONTROL Add to chat]：**&#x200B;在下一个提示中引用该概念。
      * **[!UICONTROL Delete]：**&#x200B;删除概念。

   * 要管理单个变体，请将光标悬停在变体卡片上并单击&#x200B;**[!UICONTROL ...]**，然后选择选项：

      * **[!UICONTROL Add to Chat]：**&#x200B;在下一个提示中引用变量。 您还可以直接单击变体卡正文以切换提及方式。
      * **[!UICONTROL Edit Data]：**&#x200B;打开一个对话框，您可以在其中更新变体&#x200B;**[!UICONTROL Name]**&#x200B;以及模板中定义的每个点击标记的点进URL。 单击&#x200B;**[!UICONTROL Save]**&#x200B;以应用。
      * **[!UICONTROL Delete]：**&#x200B;删除变体。

1. 如果您对生成的概念感到满意，请单击标题中的&#x200B;**[!UICONTROL Save Standard Ads]**。

   在至少存在一个概念之前，该按钮处于禁用状态。

1. 在&#x200B;**[!UICONTROL Save Standard Ads]**&#x200B;对话框中，指定以下设置，然后单击&#x200B;**[!UICONTROL Save Standard Ads]**。

   **[!UICONTROL Advertiser]：**（必需）要保存创意的广告商。

   **[!UICONTROL Creative Library]：**（必需）要将创意内容保存到的创意库。 库选取器将在您选择广告商后启用。

   **[!UICONTROL Attach to Bundles]：**（可选）启用后，保存的创意将附加到一个或多个包。 对于每个广告变体，请选择一个捆绑包，或输入一个新的捆绑包名称。

   **\[每个广告的设置\]：**&#x200B;对于每个广告变体，您可以查看并可以选择更改&#x200B;**[!UICONTROL Name]、**、**[!UICONTROL Language]、**&#x200B;和&#x200B;**[!UICONTROL click URL]。**

## 编辑标准广告 {#edit-standard-ad}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**。

   此时将打开一个全屏编辑器，左侧显示实时广告预览，右侧显示设置面板。

1. 使用&#x200B;**[!UICONTROL Details]**&#x200B;和&#x200B;**[!UICONTROL Attributes]**&#x200B;选项卡编辑广告设置：

   **[!UICONTROL Details]**&#x200B;选项卡：

   * **[!UICONTROL Creative Name]：**（必需）创意内容的显示名称。
   * **[!UICONTROL Language]：**（必需）广告内容的语言。
   * **[!UICONTROL Creative Size]：**（只读）广告维度。
   * **点击标记：**&#x200B;如果模板定义了点击标记，则每个点击标记都将显示为标记为标记名称的必填字段。 输入每个标记的点进目标URL。
   * 用于组织创意的&#x200B;**[!UICONTROL Label]：**（可选）标签。 选择现有标签，或输入新标签并单击&#x200B;**[!UICONTROL Add tag].**

   **[!UICONTROL Attributes]**&#x200B;选项卡：

   实时预览会在您编辑时实时更新。 加载预览时，**[!UICONTROL Attributes]**&#x200B;选项卡不可用。

   * **文本属性：**&#x200B;输入模板中定义的每个可编辑文本图层的文本值。
   * **图像属性：**&#x200B;显示当前图像的缩略图。 单击&#x200B;**[!UICONTROL Replace Image]**&#x200B;以上传替换内容（PNG、JPEG、GIF、WebP或SVG）。

1. 单击&#x200B;**[!UICONTROL Update Creative]**。

## 为标准广告生成广告变体 {#generate-ad-variations}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**。

   将打开[!UICONTROL Ad Variations Generator]并预加载所选的广告。

1. 使用AI聊天界面生成和细化其他变体。 有关完整的工作流，请参阅&quot;[创建标准广告](#create-standard-ads)&quot;。

## 复制标准广告 {#duplicate-standard-ad}

复制标准广告以向库中添加具有相同设置的新创意。 您稍后可以重命名新的创意并根据需要编辑设置。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**。

   新创意名为`<original name> (copy)`。

## 查看标准广告的更改日志 {#view-change-log}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Change Log]**。

   此时将打开一个对话框，其中显示了广告的更改表。

## 下载标准广告 {#download-standard-ad}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   创意内容将按照浏览器的正常过程进行下载。

## 删除标准广告 {#delete-standard-ad}

>[!NOTE]
>
>无法撤消此操作。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，将光标悬停在创意卡片上并单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [关于Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理动态创意](creative-studio-manage-dynamic-ads.md)
>* [在Creative Studio中管理模板](creative-studio-manage-templates.md)
>* [在Advertising Creative中管理品牌配置文件](/help/creative/brands/brand-manage.md)


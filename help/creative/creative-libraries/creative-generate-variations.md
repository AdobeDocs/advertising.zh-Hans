---
title: 生成灵活的HTML5创意内容变体
description: 了解如何从创意库中生成并保存灵活HTML5创意的AI辅助变体。
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# 生成灵活的HTML5创意内容变体

使用[!UICONTROL Ad Variations Generator]创建现有灵活HTML5创意内容的新变体。 AI助手可生成和优化标题、CTA、图像、颜色等，并可在单个会话中创建新的大小变量。 将生成的变体另存为创意库中的新标准广告。

>[!NOTE]
>
>您还可以从[!UICONTROL Creative Studio]生成广告变体。 两个入口点打开相同的[!UICONTROL Ad Variations Generator]。 请参阅“[在Creative Studio中为标准广告生成广告变体](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)”以获取其他入口点。

## 可用性 {#availability}

**[!UICONTROL Generate Variations]**&#x200B;操作适用于新[!UICONTROL Creative Libraries] UI中的灵活HTML5创意，包括基于系统模板的创意。 它不适用于其他创意类型，包括动态创意内容。

当创意内容没有生成器所需的内部父广告模板引用时，将禁用操作。 此引用不是您可以编辑的设置；在创意的&#x200B;**[!UICONTROL Template]**&#x200B;选项卡上上传或替换文件不会明确设置它。

## 打开广告变体生成器 {#open-generator}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 通过以下任一方式打开库：

   * 单击库名称。
   * 在库名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Open]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击灵活的HTML5创意名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Generate Variations]**。

   将打开[!UICONTROL Ad Variations Generator]并显示选定创意的内容。 画布显示具有模板可用广告格式的&#x200B;**[!UICONTROL Template Sizes]**&#x200B;部分和将显示所生成内容的&#x200B;**[!UICONTROL Ad Concepts]**&#x200B;部分。

## 生成和优化变体 {#generate-variations}

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
      >AI助手可以生成和修改文本（标题、副标题、CTA、正文）、交换背景图像、应用品牌颜色、切换徽标版本以及创建新大小模板。 它无法更改模板结构：元素位置、布局、间距、填充、字体系列、字体大小或边框。 在启动会话之前，在模板编辑器中执行结构性更改。 请参阅[编辑模板](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template)。

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

## 保存变体 {#save-variations}

1. 如果您对生成的概念感到满意，请单击标题中的&#x200B;**[!UICONTROL Save Standard Ads]**。

   在至少存在一个概念之前，该按钮处于禁用状态。

1. 在&#x200B;**[!UICONTROL Save Standard Ads]**&#x200B;对话框中，查看以下设置，然后单击&#x200B;**[!UICONTROL Save Standard Ads]**。

   **[!UICONTROL Advertiser]：**&#x200B;与源创意库关联的广告商。 您无法更改此值。

   **[!UICONTROL Creative Library]：**&#x200B;保存新广告的源创意库。 您无法更改此值。

   **[!UICONTROL Attach to Bundles]：**（可选）启用后，保存的创意将附加到一个或多个包。 对于每个广告变体，请选择一个捆绑包，或输入一个新的捆绑包名称。

   **\[每个广告的设置\]：**&#x200B;对于每个广告变体，您可以查看并可以选择更改每个点击标记的&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Language]**&#x200B;和点进URL。

   返回到创意库。

>[!MORELIKETHIS]
>
>* [编辑标准创意](creative-edit-standard.md)
>* [在Creative Studio中管理标准广告](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [在Advertising Creative中管理品牌配置文件](/help/creative/brands/brand-manage.md)
>* [!UICONTROL Creative Studio]&#x200B;[&#128279;](/help/creative/creative-studio/creative-studio-content-credentials.md)中的C2PA元数据

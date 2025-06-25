---
title: 管理库存馈送的广告模板
description: 了解如何管理广告模板，通过这些模板可处理库存数据，以管理帐户结构和投放动态广告。
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# 管理库存馈送的广告模板

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

在上传数据之前或之后，您可以创建特定于搜索引擎的广告模板，以便通过这些模板处理数据。 您可以为文本广告和扩展/扩展的文本广告、[!DNL Google Ads]和[!DNL Microsoft Advertising]响应式搜索广告以及[!DNL Google Ads]和[!DNL Microsoft Advertising]购物广告创建模板。

您可以将每个模板与一个信息源文件、[!DNL Google Merchant Center]帐户或[!DNL Microsoft Merchant Center]帐户关联，还可以将多个模板与同一信息源文件或帐户关联。 广告模板可以包含变量，这些变量会被上传文件或帐户中的实际数据列替换。 在大多数情况下，变量还可以包括您在Search、Social和Commerce中设置的[修饰符组](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)，以便为数据文件中的每个适用行创建多个广告、关键字、促销活动或广告组。 利用模板选项，可为广告创建新帐户结构（促销活动、广告组、关键词），或将广告映射到现有帐户结构。

除了从头开始创建新模板之外，您还可以通过克隆现有模板和编辑现有模板来创建新模板。

创建模板并将其与数据馈送文件或商户中心帐户关联后，您可以通过模板传播文件中的数据以创建促销活动数据和帐户结构，可以选择创建批量处理工作表文件以供审阅或立即发布到广告网络。

可以激活、暂停或删除任何模板。 馈送数据只能通过活动模板自动传播。 但是，您可以通过暂停的模板手动传播数据。

## 创建、克隆或编辑信息源模板

为文本和扩展/扩展的文本广告、响应式搜索广告、[!DNL Google Ads]购物广告和[!DNL Microsoft Advertising]购物广告创建单独的模板。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 执行以下操作之一：

   * 要从头开始创建模板，请单击数据表上方工具栏中的&#x200B;**[!UICONTROL Create/Clone]**，然后选择适用的广告网络。

   * 要克隆现有模板：

      1. 选中要复制的模板旁边的复选框。

      1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Create/Clone]**，然后选择适用的广告网络。

   * （要编辑现有模板）在模板名称旁边，单击![查看/编辑设置](/help/search-social-commerce/assets/settings.png "查看/编辑设置")。

1. 指定[文本广告模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md)、[[!DNL Google Ads] 购物广告模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)或[[!DNL Microsoft Advertising] 购物广告模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md)的设置：

   1. 在模板设置窗口的顶部，指定模板名称和适用的帐户。

      克隆现有模板时，请重命名新模板，以便从新模板创建的广告不与从源模板创建的广告相关联。

   1. （可选）在左列中，指定其数据将通过模板传播的产品信息源文件或商家中心帐户：

      * （对于产品信息源文件）要选择以前上载的文件，请单击![向下箭头](/help/search-social-commerce/assets/arrow-down-dropdown.png "向下箭头")，然后从可用信息源文件列表中选择一个文件。 要上载新文件，请输入完整路径和文件名，或单击&#x200B;**[!UICONTROL Browse]**&#x200B;在设备或网络上查找该文件，然后单击&#x200B;**[!UICONTROL Upload]**。

      * （对于已同步的商家中心帐户）选择帐户名称。

      将显示选定文件或帐户的列。

   1. 在&#x200B;**[!UICONTROL Account Structure]**&#x200B;选项卡上，指定帐户结构设置。

   1. （仅限文本广告）单击&#x200B;**[!UICONTROL Keywords]**&#x200B;选项卡，然后指定关键词设置。

   1. （仅限文本和响应式搜索广告）单击&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡，然后执行以下任一操作：

      >[!NOTE]
      >
      >* 每个标准文本广告模板最多可以包含四个广告变体模板，每个扩展/扩展文本广告模板最多可以包含五个广告变体模板，每个响应式搜索广告模板最多可以包含三个广告变体模板。
      >* 每个广告组最多可以包含三个启用的响应式搜索广告。
      >* 您无法编辑现有的标准文字广告变体，并且现有模板不再生成标准文字广告。
      >* 如果更改广告变体模板，则通过模板传播数据时，可能会删除现有广告并创建新广告，[具体取决于广告类型和广告网络](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md)。

      * 要添加广告变体，请执行以下操作：

         1. 单击&#x200B;**[!UICONTROL Add Ad Variation]**&#x200B;可创建文本广告，**[!UICONTROL Add ETA Variation]**&#x200B;可创建扩展/扩展的文本广告，或单击&#x200B;**[!UICONTROL Add RSA Variation]**&#x200B;可创建响应式文本广告。

            指定广告类型后，您只能使用该模板创建该广告类型。

         1. 指定广告设置。

            对于响应式搜索广告，您可以包含3-15个标题和2-4个描述。

         1. （可选）要使用原始广告副本字段中的文本预填所有备用广告副本字段，请选中&#x200B;**[!UICONTROL Prefill]**&#x200B;旁边的复选框。

         1. （可选）要将另一组广告副本添加到广告，如果原始广告副本中的任何行在传播期间任何动态参数被数据替换后超出最大长度，则可以使用该广告副本，请单击&#x200B;**[!UICONTROL Add Alternate]**，然后添加替代值。

            >[!NOTE]
            >
            >* 如果选择了[!UICONTROL Prefill]选项，则备用字段会预填充原始字段，您可以根据需要编辑它们。
            >* 只有超出最大长度的广告文案字段会被替换成替换值。 例如，如果只有原始标题或标题太长，则生成的广告变体使用替代标题或标题以及原始描述。 因此，请确保将备用广告副本与原始广告副本结合使用时有意义。
            >* 如果原始广告副本满足搜索引擎的长度要求，则会丢弃替代广告副本。
            >* 您最多可以为每个广告副本字段指定四个替代项。

         * 要编辑广告变体，请执行以下操作：

            1. 编辑广告设置。

               对于响应式搜索广告，您可以包含3-15个标题和2-4个描述。

            1. （可选）要使用原始广告副本字段中的文本预填所有备用广告副本字段，请选中&#x200B;**[!UICONTROL Prefill]**&#x200B;旁边的复选框。

            1. （可选）要将另一组广告副本添加到广告，如果原始广告副本中的任何行在传播期间任何动态参数被数据替换后超出最大长度，则可以使用该广告副本，请单击&#x200B;**[!UICONTROL Add Alternate]**，然后添加替代值。

               >[!NOTE]
               >
               >* 如果选择了[!UICONTROL Prefill]选项，则备用字段会预填充原始字段，您可以根据需要编辑它们。
               >* 只有超出最大长度的广告文案字段会被替换成替换值。 例如，如果只有原始标题或标题太长，则生成的广告变体使用替代标题或标题以及原始描述。 因此，请确保将备用广告副本与原始广告副本结合使用时有意义。
               >* 如果原始广告副本满足搜索引擎的长度要求，则会丢弃替代广告副本。
               >* 您最多可以为每个广告副本字段指定四个替代项。

         * 要删除广告变体，请单击广告变体旁边的&#x200B;**[!UICONTROL Remove ETA Variation]**（适用于展开/扩展的文本广告）或&#x200B;**[!UICONTROL Remove RSA Variation]**（适用于响应式搜索广告）（如果适用）。

   1. （仅限购物模板）单击&#x200B;**[!UICONTROL Product Groups]**&#x200B;选项卡，然后指定有关要定位的产品组的信息。

   1. （可选）单击&#x200B;**[!UICONTROL Feed Filters]**&#x200B;选项卡，然后指定要传播的信息源文件中的哪些行。

   1. （可选）单击&#x200B;**[!UICONTROL Label Classifications tab]**，然后指定要分配给所创建的不同营销活动组件的标签分类值：

      1. 单击&#x200B;**[!DNL \[Component\] Label Classifications]**&#x200B;旁边的复选框。

      1. 对于要分配给组件的每个标签分类，执行以下操作：

         1. 单击&#x200B;**[!UICONTROL Add Label Classification]**。

         1. 选择标签分类，然后选择现有值或输入新值。

1. 保存模板：

   * 要仅保存模板，请单击&#x200B;**[!UICONTROL Save]**，然后再次单击&#x200B;**[!UICONTROL Save]**。

   * 要保存模板并通过它传播指定的数据文件，请单击&#x200B;**[!UICONTROL Save]**，然后单击&#x200B;**[!UICONTROL Save & Propagate]**。

## 更改信息源模板的状态

您可以激活任何暂停的数据馈送模板，或暂停任何活动的数据馈送模板。

>[!NOTE]
>
>您可以通过暂停的模板手动传播数据，但数据不会自动通过该模板传播。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 选中要更改其状态的每个模板旁边的复选框。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Change Status]**，然后单击&#x200B;**[!UICONTROL Activate]**&#x200B;或&#x200B;**[!UICONTROL Pause]**。

## 删除馈送模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 选中要删除的每个模板旁边的复选框。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Yes]**。

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动进行广告管理](../inventory-feeds-about.md)
>* [文本广告和响应式搜索广告模板设置](template-text-rsa.md)
>* [[!DNL Google Ads] 购物广告模板设置](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] 购物广告模板设置](template-microsoft-shopping.md)
>* [通过模板传播馈送数据](../feed-data-propagate.md)

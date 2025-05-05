---
title: 关于使用库存信息源自动化广告管理
description: 了解高级促销活动管理，它允许您根据产品或服务库存的相关数据自动管理帐户结构和投放动态广告。
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# 关于使用库存信息源自动化广告管理

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

高级促销活动管理的[!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]视图允许您自动创建和更新广告网络帐户结构，并根据有关产品或服务库存的数据投放动态广告。 您可以每天或根据需要经常上载包含产品数据的新文件，或者直接链接到[!DNL Google]或[!DNL Microsoft]商家中心帐户。 使用该功能可以：

* 从有序的数据源构建新的营销活动。

* 在处理新数据时动态更新文本和响应式搜索广告、[!DNL Google Ads]购物广告或[!DNL Microsoft Advertising]购物广告，使用可更改数据元素（如价格或数量）的动态变量。 每次更改数据时，都会删除现有广告并创建新广告。

* 当库存低于特定级别时、根据指定的结束日期时，或者在馈送数据中忽略现有组件时，自动暂停或移除广告组、关键词和广告。

要设置广告，请创建包含变量（占位符）的库存馈送模板，然后使用已同步的上传文件或[Google或Microsoft商家中心帐户中的实际数据列替换变量](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。 变量还可以包括您在文件中设置的修饰符组或文件中的单个行，以便为数据文件中的每个适用行创建多个广告、关键字、促销活动或广告组。 例如，如果您在广告标题中使用修饰符组变量，并且该修饰符组包含两个修饰符（“便宜”和“折扣”），则系统会为每个产品创建两个单独的广告 — 每个修饰符各一个。 对于[!DNL Google Ads]和[!DNL Microsoft Advertising]动态搜索广告，您还可以包含广告自定义程序的值。

| 模板的[!UICONTROL Ad Variation]部分 | 搜索、社交和Commerce中的修饰符 | 信息源内容 | 生成的广告 |
|----|----|----|----|
| 标题：购买高端\{<i>产品类别</i>\} &lt;<i>廉价列表</i>>。<br><br>描述1： \{<i>产品名称</i>\}的库存量很大。<br><br>描述2：折扣率为\{<i>折扣百分比</i>\}%。 | 修饰符组“Co廉价List”的值： <br><br>“折扣价”<br><br>“ | 产品类别、产品名称、折扣百分比<br>电子、iPod、10<br><br>服装、衬衫、15<br><br><b>注意：</b>您可以使用逗号或制表符分隔值。 | <u>低价购买高端电子产品。</u><br>大量平板电脑库存。 可享受10%的折扣。<br><br><u>以折扣价购买高端电子产品。</u><br>大量平板电脑库存。 可享受10%的折扣。<br><br><u>廉价购买高档服装。</u><br>大量衬衫库存。 可享受15%的折扣。<br><br><u>购买高端服装时打折。</u><br>大量衬衫库存。 可享受15%的折扣。 |

生成广告后，您可以选择查看这些广告，然后将它们发布到广告网络。

>[!NOTE]
>要使用电子表格文件批量创建或编辑促销活动数据，请参阅“关于使用批量工作表管理促销活动数据[&#128279;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)”。

## 使用库存信息源管理营销活动数据的工作流

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

最初，请至少测试一个信息源文件或帐户，然后您可以完全自动化该过程，或在每个步骤继续控制该过程：

1. （可选）请联系您的Adobe客户团队以设置用于存放数据文件的FTP目录。

   如果您使用FTP目录，则信息源服务每两小时检查一次新文件。

   否则，您可以在[!UICONTROL Advanced (ACM)]视图中手动上传文件。

1. 设置[参数以处理馈送数据](feed-settings-manage.md#feed-data-settings)。

   如果您使用FTP，最初不要自动将数据发布到广告网络。 验证第一个文件的输出并对结果感到满意后，可以更改设置。

1. 将数据文件上载到FTP目录，[在[!UICONTROL Advanced (ACM) view]中手动上载数据文件](feed-files-manage.md)，或者[启用对Google或Microsoft商家中心帐户的访问](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。

要手动上传文件，您可以等到创建使用数据文件的模板为止。

1. （可选）创建[修饰符](modifiers-manage.md)的组以用作馈送数据模板中各个数据字段中的变量。

1. [创建一个或多个模板](ad-templates/ad-template-manage.md)，这些模板使用数据列为特定广告网络帐户创建促销活动、广告组、关键字和/或广告副本。

1. [通过模板](feed-data-propagate.md)传播馈送数据，该模板用文件或帐户中的数据替换模板中的列名。 根据模板选项，Search、Social和Commerce可以使用默认设置为广告创建新帐户结构（促销活动、广告组、关键词），或将广告映射到现有帐户结构。

1. （可选） [在[!UICONTROL Advanced (ACM)]视图中预览输出](propagated-data-view.md)，并可以选择在[!UICONTROL Propagations]选项卡上查看数据更改的摘要。

1. [将数据](propagated-data-post.md)发布到相关的广告网络帐户。

1. （如果使用FTP或商户中心帐户上传数据，可选）验证第一个馈送文件的输出后，请[编辑参数](feed-settings-manage.md#feed-data-settings)以通过关联的模板自动传播后续数据，并将其发布到相关广告网络。

1. （当您有新数据文件时）根据需要，上传新文件，通过模板传播数据，然后将数据发布到相关广告网络。 您可以选择一步传播和发布数据。

>[!MORELIKETHIS]
>
>* [清单信息源何时创建或删除帐户组件？](when-are-components-created-deleted.md)

---
title: 关于使用库存信息源自动化广告管理
description: 了解高级促销活动管理，它允许您根据有关产品或服务库存的数据自动管理帐户结构和投放动态广告。
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# 关于使用库存信息源自动化广告管理

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

此 [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] 高级促销活动管理视图允许您自动创建和更新广告网络帐户结构，并根据有关产品或服务库存的数据投放动态广告。 您可以每天或根据需要尽可能频繁地上传包含产品数据的新文件，或直接链接到 [!DNL Google] 或 [!DNL Microsoft®] 商户中心帐户。 使用该功能可以：

* 从有序的数据源构建新的营销活动。

* 动态更新文本和响应式搜索广告， [!DNL Google Ads] 购物广告，或 [!DNL Microsoft® Advertising] 每当处理新数据时，使用可更改数据元素（如价格或数量）的动态变量进行购物广告。 每次更改数据时，都会删除现有广告并创建新广告。

* 当库存低于特定级别时、根据指定的结束日期时，或者在馈送数据中忽略现有组件时，自动暂停或移除广告组、关键词和广告。

要设置广告，请创建包含变量（占位符）的库存馈送模板，然后使用上传文件或中的实际数据列替换变量 [已同步的Google或Microsoft®商家中心帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 这些变量还可以包括您在文件中设置的修饰符组或文件中的单个行，以便为数据文件中的每个适用行创建多个广告、关键字、促销活动或广告组。 例如，如果您在广告标题中使用修饰符组变量，并且该修饰符组包含两个修饰符（“表示廉价”和“打折”），则系统会为每个产品创建两个单独的广告 — 每个修饰符各一个。 对象 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 动态搜索广告，您还可以包含广告自定义器的值。

| [!UICONTROL Ad Variation] 模板部分 | 搜索、社交和商务中的修饰符 | 信息源内容 | 生成的广告 |
|----|----|----|----|
| 标题：购买高端\{<i>产品类别</i>\} &lt;<i>廉价清单</i>>.<br><br>描述1：大量\{<i>产品名称</i>\}。<br><br>描述2：位于\{<i>折扣百分比</i>\}%折扣。 | 修饰符组“CoapList”的值：<br><br>“廉价”<br><br>“打折” | 产品类别、产品名称、折扣百分比<br>电子，iPods，10<br><br>服装，衬衫，15<br><br><b>注意：</b> 可以使用逗号或制表符来分隔值。 | <u>廉价购买高端电子产品。</u><br>平板电脑库存巨大。 可享受10%的折扣。<br><br><u>以折扣价购买高端电子产品。</u><br>平板电脑库存巨大。 可享受10%的折扣。<br><br><u>廉价购买高档服装。</u><br>衬衫存量很大。 可享受15%的折扣。<br><br><u>以折扣价购买高端服装。</u><br>衬衫存量很大。 可享受15%的折扣。 |

生成广告后，您可以选择查看广告，然后将其发布到广告网络。

>[!NOTE]
>要使用电子表格文件批量创建或编辑促销活动数据，请参阅[关于使用批量处理工作表管理营销活动数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).”

## 使用清单信息源管理营销活动数据的工作流

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

最初，请至少测试一个信息源文件或帐户，然后您可以完全自动化该过程，或继续在每一步对其进行控制：

1. （可选）请联系您的Adobe客户团队以设置用于存放数据文件的FTP目录。

   如果您使用FTP目录，则信息源服务每两小时检查一次新文件。

   否则，您可以手动上传文件 [!UICONTROL Advanced (ACM)] 视图。

1. 设置 [用于处理馈送数据的参数](feed-settings-manage.md#feed-data-settings).

   如果您使用的是FTP，开始时请勿自动将数据发布到广告网络。 验证第一个文件的输出并对结果满意后，可以更改设置。

1. 将数据文件上传到FTP目录， [手动上传数据文件](feed-files-manage.md) 在 [!UICONTROL Advanced (ACM) view]，或 [启用对Google或Microsoft®商家中心帐户的访问权限](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

要手动上传文件，您可以等到创建使用数据文件的模板时再上传。

1. （可选）创建组 [修饰符](modifiers-manage.md) 在馈送数据模板的各种数据字段中用作变量。

1. [创建一个或多个模板](ad-templates/ad-template-manage.md) 使用数据列为特定广告网络帐户创建促销活动、广告组、关键字和/或广告副本。

1. [通过模板传播馈送数据](feed-data-propagate.md)，用文件或帐户中的数据替换模板中的列名称。 根据模板选项，搜索、Social和Commerce可以使用默认设置为广告创建新帐户结构（促销活动、广告组、关键词），或将广告映射到现有帐户结构。

1. （可选） [预览输出](propagated-data-view.md) 在 [!UICONTROL Advanced (ACM)] 查看数据，并（可选）查看上数据更改的摘要 [!UICONTROL Propagations] 选项卡。

1. [发布数据](propagated-data-post.md) 至相关广告网络帐户。

1. （如果使用FTP或商户中心帐户上传数据；可选）验证第一个馈送文件的输出后， [编辑参数](feed-settings-manage.md#feed-data-settings) 以通过关联的模板自动传播后续数据，并将其发布到相关广告网络。

1. （当您有新数据文件时）如有必要，请上传新文件，通过模板传播数据，然后将数据发布到相关广告网络。 您可以选择在一个步骤中传播和发布数据。

>[!MORELIKETHIS]
>
>* [清单信息源何时创建或删除帐户组件？](when-are-components-created-deleted.md)

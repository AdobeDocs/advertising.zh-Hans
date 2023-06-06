---
title: 关于使用库存信息源自动化广告管理
description: 了解高级促销活动管理，它允许您根据有关产品或服务库存的数据自动管理帐户结构和投放动态广告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
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

>[!MORELIKETHIS]
>
>* [使用清单信息源管理营销活动数据的工作流](inventory-feeds-workflow.md)
>* [清单信息源何时创建或删除帐户组件？](when-are-components-created-deleted.md)


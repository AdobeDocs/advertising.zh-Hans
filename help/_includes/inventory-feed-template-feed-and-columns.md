---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---
# 文本广告模板 — 信息源与列

**[!UICONTROL Feed & Columns]：** A [信息源文件](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md) 或与模板关联的商家帐户，以及所选文件或帐户的列（标题）：

* *[!UICONTROL Feed File]：* 上传文件或从可用信息源文件列表中选择文件。

* *[!UICONTROL Google Merchant Center]：* 选择 [已同步 [!DNL Google Merchant Center] 帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 搜索、Social和Commerce仅创建产品组； [!DNL Google Ads] 自动为产品组生成购物广告。 不支持自定义列。

* *[!UICONTROL Microsoft Merchant Center]：* ([!DNL Microsoft Advertising] 仅限购物模板)选择 [已同步 [!DNL Microsoft Merchant Center] 帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 搜索、Social和Commerce仅创建产品组； [!DNL Microsoft Advertising] 自动为产品组生成产品广告。 不支持自定义列。

在准备好使用该模板创建广告之前，将模板与信息源文件或商家帐户关联是可选的。

在模板字段中插入馈送列时，插入的值表示为 `[field_name]`，其中“field_name”是指定的字段名称，表示该值是一个变量。

>[!NOTE]
>
>* 如果更改信息源文件或现有模板的帐户，则当新文件包含不同的标头时，可能需要调整模板参数。
>* 如果删除或禁用与模板关联的信息源文件或帐户，则也会删除关联，您必须先选择新的信息源文件，然后才能使用模板创建更多广告。 如果新的信息源文件或帐户不包含与原始文件相同的标头，则您可能需要相应地调整模板参数。


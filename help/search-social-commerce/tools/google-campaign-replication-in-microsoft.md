---
title: 复制 [!DNL Google Ads] 中的营销活动 [!DNL Microsoft® Advertising]
description: 了解如何在中导出已同步的营销活动 [!DNL Google Ads] 帐户直接转入已同步 [!DNL Microsoft® Advertising] 帐户。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# 复制 [!DNL Google Ads] 中的营销活动 [!DNL Microsoft® Advertising]

您可以将同步的营销活动导出到 [!DNL Google Ads] 帐户直接转入已同步 [!DNL Microsoft® Advertising] 将帐户作为增强型CPC (eCPC)促销活动。 现有竞价和营销活动预算可缩放。 现有的搜索、社交和商务跟踪未导入。

您可以复制以下类型的营销活动及其营销活动结构：

* [!DNL Google Ads] 搜索营销活动并将其显示在中 [!DNL Microsoft® Advertising] 搜索和显示营销活动。

* [!DNL Google Display Network] 将营销活动（包括广告图像）转换为 [!DNL Microsoft® Advertising] Microsoft®受众网络上的受众营销活动。

   如果要复制基于购物馈送的显示营销活动，请首先复制您的 [!DNL Google Merchant Center] 产品选件至 [!DNL Microsoft® Merchant Center]. 复制活动时，选择 [!DNL Microsoft® Merchant Center] 将商店存储在导入选项中，以将商店链接到基于信息源的受众营销活动。

* [!DNL Google Ads] 将效果最佳的营销活动（包括本地库存广告）引入 [!DNL Microsoft® Advertising] 智能购物营销活动。

您可以选择更新一次营销活动；每周或每月更新一次；或根据 [!DNL Microsoft® Advertising]的推荐计划。 您可以选择在每次运行导入作业或发生错误或更改时配置通知。 将营销活动导入后 [!DNL Microsoft® Advertising]中，您可以检查导入作业的状态、查看任何错误日志、手动运行导入作业，以及编辑、暂停、启用或删除导入计划。

并非所有营销活动信息都已复制，您可能需要向中添加一些信息 [!DNL Microsoft® Advertising] 营销活动。 有关导入数据的更多信息，请参阅 [!DNL Microsoft® Advertising] 有关“”的帮助[导入自何处 [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).” 由于搜索、社交和商务跟踪未导入，因此您还应该在 [帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)， [营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)， [广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，或 [广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 设置。

## 复制 [!DNL Google Ads] 营销活动

>[!NOTE]
>
>如果要复制基于购物馈送的显示营销活动，请首先 [复制您的 [!DNL Google Merchant Center] 中的产品选件 [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). 复制活动时，选择 [!DNL Microsoft® Merchant Center] 将商店存储到导入选项，以将商店链接到基于信息源的受众营销活动。

参见 [导入自 [!DNL Google Ads] 营销活动](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. 从获取导入凭据ID [!DNL Microsoft® Advertising] 以代表您的 [!DNL Google Ads] 凭据。

   自动生成 [!DNL Microsoft® Advertising] 导入凭据不可用，原因是 [!DNL Microsoft® Advertising] API限制。 联系Adobe技术支持或您的Adobe客户团队，他们将生成凭据并提供ID。

   您必须具有ID才能配置导入作业。

1. 在“搜索、社交和商务”主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 单击 **[!UICONTROL +Import]**.

1. 指定 [导入设置](#campaign-import-settings)：

   1. 在 **[!UICONTROL Select accounts]** 部分，选择源帐户和目标帐户以及凭据ID [!DNL Microsoft® Advertising] 需要。

   1. 在 **[!UICONTROL Select campaigns & ad groups]** 部分，指定要导入的营销活动和广告组。

   1. 在 **[!UICONTROL Customize your import]** 部分，指定要导入的项目类型。

   1. 在 **[!UICONTROL Set schedule]** 部分，指定运行导入作业的时间。

1. 单击 **[!UICONTROL Post]**.

1. （可选）将搜索、社交和商务跟踪添加到 [帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)， [营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)， [广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，或 [广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 设置。

## 编辑营销活动导入作业的详细信息

参见 [导入自 [!DNL Google Ads] 营销活动](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 选中导入作业旁边的复选框，然后单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑").

1. 编辑 [导入设置](#campaign-import-settings).

   1. 在 **[!UICONTROL Select accounts]** 部分，选择源帐户和目标帐户以及凭据ID [!DNL Microsoft® Advertising] 需要。

   1. 在 **[!UICONTROL Select campaigns & ad groups]** 部分，指定要导入的营销活动和广告组。

   1. 在 **[!UICONTROL Customize your import]** 部分，指定要导入的项目类型。

   1. 在 **[!UICONTROL Set schedule]** 部分，指定运行导入作业的时间。

1. 单击 **[!UICONTROL Post]**.

## 查看您的营销活动导入作业

您可以列出所有导入作业，包括源作业 [!DNL Google Ads] 帐户，目标 [!DNL Microsoft® Advertising] 帐户、导入时间或计划，以及创建作业的用户。 如果多次运行导入作业（包括在定期计划的导入期间），则每次发生次数都会作为单独的作业列出。

* 执行以下任一操作：

   * 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

      默认情况下，视图打开 [!UICONTROL List of Import Jobs] 选项卡。

   * 从 [[!UICONTROL Import Logs] 选项卡](#campaign-import-log)，单击 **[!UICONTROL List of Import Jobs]** 选项卡。

## 运行营销活动导入作业

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 选中导入作业旁边的复选框。

1. 单击 ![立即运行](/help/search-social-commerce/assets/run.png "立即运行").

## 查看营销活动导入作业的日志 {#campaign-import-log}

您可以列出所有已完成或失败的导入作业，包括开始时间、源 [!DNL Google Ads] 帐户，目标 [!DNL Microsoft® Advertising] 帐户、创建作业的用户、成功和失败操作的数量，以及接收每个作业通知的任何电子邮件地址。 您可以查看有关对目标所做的更改的详细信息 [!DNL Microsoft® Advertising] 每个作业发生的帐户，包括添加、同步、删除的项目数，以及在帐户中为每个实体级别（如营销活动或关键词）产生错误的帐户。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 单击 **[!UICONTROL Import Logs]** 选项卡。

1. （可选）要查看任何导入作业的详细信息，请单击 [!UICONTROL Summary] 列。

## Campaign导入作业设置 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]：** 已同步 [!DNL Google Ads] 从中导出营销活动数据的帐户。

**[!UICONTROL Credential ID]：** ID能够 [!DNL Microsoft® Advertising] 使用表示 [!DNL Google Ads] 凭据。

自动生成 [!DNL Microsoft® Advertising] 导入凭据不可用，原因是 [!DNL Microsoft® Advertising] 限制。 联系Adobe技术支持或您的Adobe客户团队，他们将生成凭据并提供ID。

**[!UICONTROL Target Microsoft® Ads account]：** 已同步 [!DNL Microsoft® Advertising] 营销活动数据导入到的帐户。

### [!UICONTROL Select campaigns & ad groups]

**\[要导入的数据\]：** 指定要导入的数据：

* *[!UICONTROL Import all new and existing campaigns]：* 导入已存在的所有营销活动和不存在于中的所有营销活动的数据 [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]：* 选择特定的营销活动和广告组。

   * 要将营销活动展开至其子广告组，请单击 **[!UICONTROL >]** 在营销活动名称之后。

   * 要选择营销活动或广告组，请选择相应的项目，以便显示复选标记。

   * 要删除营销活动或广告组，请执行以下操作：

      * 在 [!UICONTROL Campaigns] 或 [!UICONTROL Adgroups] 列中，取消选择营销活动或广告组，以便复选标记消失。

      * 在 [!UICONTROL Selected] 列，单击 ![删除](/help/search-social-commerce/assets/delete.png "删除").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]：** 允许您指定要导入的内容、竞价和预算以及其他选项。

**[!UICONTROL What to import]：** 定义要导入的项目。 默认情况下会选择导入物料类别的选项，并会选择所有物料类型。 要仅包含特定项目类型，请单击 **[!UICONTROL Show advanced options]** 并更改要包括的项目类型。

**[!UICONTROL Bids and budgets]：** 定义要导入、更新和自定义的竞价和预算设置。

**[!UICONTROL Other options]：** 定义如何处理导入的登陆页面URL、跟踪模板以及其他营销活动、广告和定位选项。

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]：** 导入作业的名称。

**[!UICONTROL When]：** 何时导入指定的营销活动： *自动* (以允许 [!DNL Microsoft® Advertising] 设置计划以最佳地优化活动)， *[!UICONTROL Now]* （在发布作业设置时运行作业）， *[!UICONTROL Once]* 在指定的时间， *[!UICONTROL Daily]* 在指定的时间， *[!UICONTROL Weekly]* 在指定时间，或者 *[!UICONTROL Monthly]* 在指定时间。

**[!UICONTROL Receive email notifications]：** 是否以及何时向收件人字段中的电子邮件地址发送有关导入作业的电子邮件通知。

**[!UICONTROL Send reports to]：** 用于接收有关导入作业通知的电子邮件地址。 用逗号(`,`)。

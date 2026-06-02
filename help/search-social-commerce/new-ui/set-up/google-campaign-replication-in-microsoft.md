---
title: （新UI）在Microsoft Advertising中复制Google Ads营销活动
description: 了解如何将Google Ads帐户中同步的促销活动直接导出到同步的Microsoft Advertising帐户。
feature: Search Campaign Management
exl-id: d4f8e452-7b3d-4a1f-9c3e-6b8d2e5a4917
source-git-commit: 3f769f18ce006278b12a62f8d837d60affffda65
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# （新UI）在[!DNL Microsoft Advertising]中复制[!DNL Google Ads]营销活动

*Beta功能*

您可以将[!DNL Google Ads]帐户中同步的营销活动直接导出到已同步的[!DNL Microsoft Advertising]帐户，作为增强型CPC (eCPC)营销活动。 现有竞价和营销活动预算可缩放。 现有的搜索、社交和Commerce跟踪不会导入。

您可以复制以下类型的营销活动及其营销活动结构：

* [!DNL Google Ads]在[!DNL Microsoft Advertising]个搜索和显示营销活动中搜索和显示营销活动。

* 在Microsoft Audience Network上，将[!DNL Google Display Network]个营销活动（包括广告图像）引入[!DNL Microsoft Advertising]个受众营销活动中。

  如果要复制基于购物馈送的显示营销活动，请先将[!DNL Google Merchant Center]产品选件复制到[!DNL Microsoft Merchant Center]。 复制营销活动时，在导入选项中选择[!DNL Microsoft Merchant Center]存储，以将存储链接到基于信息源的受众营销活动。

* 将[!DNL Google Ads]个效果最佳的营销活动（包括本地库存广告）合并为[!DNL Microsoft Advertising]个效果最佳的营销活动。

您可以选择更新营销活动一次；每天、每周或每月；或根据[!DNL Microsoft Advertising]的建议计划更新。 您可以选择在每次导入作业运行或发生错误或更改时配置通知。 将营销活动导入[!DNL Microsoft Advertising]后，您可以检查导入作业的状态、查看任何错误日志、手动运行导入作业，以及编辑、暂停、启用或删除导入计划。

并非所有营销活动信息都已复制，您可能需要向[!DNL Microsoft Advertising]营销活动添加一些信息。 有关导入哪些数据的详细信息，请参阅[!DNL Microsoft Advertising]有关“[从 [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}导入哪些数据”的帮助。 由于未导入搜索、社交和Commerce跟踪，因此您还应该在[帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)或[广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)设置中添加跟踪。

## 复制[!DNL Google Ads]营销活动

>[!NOTE]
>
>如果要复制基于购物馈送的显示促销活动，请先[在 [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}中复制 [!DNL Google Merchant Center] 产品选件。 复制营销活动时，在导入选项中选择[!DNL Microsoft Merchant Center]存储，以将存储链接到基于信息源的受众营销活动。

查看从 [!DNL Google Ads] 营销活动](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}导入的[内容。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 单击&#x200B;**[!UICONTROL Import Campaigns]**。

1. 指定[导入设置](#campaign-import-settings)：

   1. 在&#x200B;**[!UICONTROL Select accounts]**&#x200B;步骤中：

      1. 在&#x200B;**[!UICONTROL Import Name]**&#x200B;字段中输入导入作业的名称。

      1. 选择源[!DNL Google Ads]帐户和目标[!DNL Microsoft Advertising]帐户。

      1. 输入您的&#x200B;**[!UICONTROL Credential ID]**。 如果您没有凭据ID，请联系您的Adobe客户团队 — 由于[!DNL Microsoft Advertising]限制，自动生成不可用。

      1. 单击&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Select campaigns & ad groups]**&#x200B;步骤中，指定要导入的营销活动和广告组，然后单击&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Customize your import]**&#x200B;步骤中，根据需要指定要导入的项目类型、竞价和预算设置以及其他选项，然后单击&#x200B;**[!UICONTROL Next]**。

   1. 在&#x200B;**[!UICONTROL Set schedule]**&#x200B;步骤中，指定何时运行导入作业以及如何接收通知。

1. 在摘要中查看您的选择，然后单击&#x200B;**[!UICONTROL Start Import]**。

1. （可选）在[帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)或[广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)设置中添加搜索、社交和Commerce跟踪。

## 编辑活动导入作业的计划设置

查看从 [!DNL Google Ads] 营销活动](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}导入的[内容。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 单击&#x200B;**[!UICONTROL Jobs]**&#x200B;选项卡。

1. 单击导入作业的名称，然后单击&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;**[!UICONTROL Set schedule]**&#x200B;步骤中，指定[计划设置](#campaign-import-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 查看您的营销活动导入作业

您可以列出所有导入作业，包括源[!DNL Google Ads]帐户、目标[!DNL Microsoft Advertising]帐户、导入时间或计划以及创建作业的用户。 如果多次运行导入作业（包括在定期计划的导入期间），则每次出现都将作为单独的作业列出。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

   默认情况下，该视图将打开到&#x200B;**[!UICONTROL Jobs]**&#x200B;选项卡。

## 运行活动导入作业

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 单击&#x200B;**[!UICONTROL Jobs]**&#x200B;选项卡。

1. 选中导入作业旁边的复选框，然后单击&#x200B;**[!UICONTROL Run Now]**。

## 查看活动导入作业的日志 {#campaign-import-log}

您可以列出所有已完成或失败的导入作业，包括开始时间、源[!DNL Google Ads]帐户、目标[!DNL Microsoft Advertising]帐户、创建作业的用户、成功和失败的操作数以及收到每个作业通知的任何电子邮件地址。 您可以查看有关每个作业发生的目标[!DNL Microsoft Advertising]帐户更改的更多详细信息，包括添加、同步、删除的项目数，以及帐户中每个实体级别（如营销活动或关键字）发生错误的项目数。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**。

1. 单击&#x200B;**[!UICONTROL Logs]**&#x200B;选项卡。

1. （可选）要查看任何导入作业的详细信息，请单击[!UICONTROL Summary]列中的值。

## Campaign导入作业设置 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Import Name]：**&#x200B;用于标识导入作业的名称。

**[!UICONTROL Source Google Ads account]：**&#x200B;从中导出营销活动数据的同步[!DNL Google Ads]帐户。

**[!UICONTROL Target Microsoft Ads account]：**&#x200B;活动数据导入到的同步[!DNL Microsoft Advertising]帐户。

**[!UICONTROL Credential ID]：** [!DNL Microsoft Advertising]用于表示您的[!DNL Google Ads]凭据的ID。 由于[!DNL Microsoft Advertising]限制，无法自动生成导入的[!DNL Microsoft Advertising]凭据。 请联系您的Adobe客户团队，他们将会生成凭据并向您提供ID。

### [!UICONTROL Select campaigns & ad groups]

**\[要导入的数据\]：**&#x200B;要导入的数据：

* *[!UICONTROL Import all new and existing campaigns]：*&#x200B;导入[!DNL Microsoft Advertising]中已存在和不存在的所有营销活动的数据。

* *[!UICONTROL Import specific campaigns and adgroups]：*&#x200B;选择特定的营销活动和广告组。

   * 要将营销活动展开到其子广告组，请单击营销活动名称后面的&#x200B;**[!UICONTROL >]**。

   * 要选择营销活动或广告组，请选择相应的项目，以便显示复选标记。

   * 要删除营销活动或广告组，请取消选择该项目或单击[!UICONTROL Selected]列中的删除图标。

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]：**&#x200B;允许您指定要导入的内容、竞价和预算以及其他选项。

**[!UICONTROL What to import]：**&#x200B;定义要导入的项目。 默认情况下，会选择导入物料类别的选项，并会选择所有物料类型。 要仅包含特定项类型，请单击&#x200B;**[!UICONTROL Show advanced options]**&#x200B;并将项类型更改为包含。 您还可以选择将UET标记ID与任何之前未导入[!DNL Microsoft Advertising]的再营销列表或受众关联。

**[!UICONTROL Bids and budgets]：**&#x200B;定义要导入、更新和自定义的竞价和预算设置，包括按指定百分比增加或减少[!DNL Microsoft Advertising]的竞价和预算的选项。

**[!UICONTROL Other options]：**&#x200B;定义如何处理导入的登陆页面URL、跟踪模板以及其他促销活动、广告和定位选项，包括用于查找和替换文本以及插入后缀的选项。

### [!UICONTROL Set schedule]

**[!UICONTROL When]：**&#x200B;何时导入指定的营销活动： *自动*（让[!DNL Microsoft Advertising]设置一个计划以最好地优化您的营销活动）、*[!UICONTROL Now]*（在发布作业设置时运行作业）、*[!UICONTROL Once]*（在指定时间）、*[!UICONTROL Daily]*（在指定时间）、*[!UICONTROL Weekly]*（在指定时间）或&#x200B;*[!UICONTROL Monthly]*（在指定时间）。

**[!UICONTROL Receive email notifications]：**&#x200B;是否以及何时将有关导入作业的电子邮件通知发送到[!UICONTROL Send reports to]字段中的地址： *[!UICONTROL No emails]*、*[!UICONTROL Only if there are changes or errors]*（默认值）、*[!UICONTROL Only if there are errors]*&#x200B;或&#x200B;*[!UICONTROL Every time this import runs]*。

**[!UICONTROL Send reports to]：**&#x200B;接收导入作业相关通知的电子邮件地址。 用逗号(`,`)分隔多个地址。

>[!MORELIKETHIS]
>
>* [管理广告网络帐户](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)

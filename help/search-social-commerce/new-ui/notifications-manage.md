---
title: （新UI）管理通知
description: 了解如何查看、配置和管理搜索、社交和Commerce通知，包括推送通知和通知中心Web应用程序。
feature: Search Notifications
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# （新UI）管理通知

*Beta功能*

您可以将通知设置配置为订阅或取消订阅不同类型的警报。 您可以通过以下任意方式查看通知：

* 来自[!UICONTROL Notifications]面板，该面板位于右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")处。 从面板中，您可以筛选列表、编辑通知设置或打开[!UICONTROL Notification Center]。

* 来自[!UICONTROL Notification Center]，将在Search、Social和Commerce之外的单独窗口中打开。 要从[!UICONTROL Notifications]面板中打开[!UICONTROL Notification Center]，请单击&#x200B;**[!UICONTROL View All]**。

* 来自[!UICONTROL Notification Center] Web应用程序，该应用程序在Search、Social和Commerce之外的单独窗口中打开[!UICONTROL Notification Center]。

  应用程序加载速度比常规浏览器版本更快，并且会自动更新。 您可以安装应用程序，并使用浏览器的应用程序管理器来管理应用程序。

* 从推送通知到浏览器。

  启用推送通知后，将根据浏览器的通知约定显示推送通知。

您可以查看通知、将通知标记为已读或未读以及删除通知。

## 通知类型

* **[!UICONTROL Notices]**：版本、停机时间和其他变更管理通知。

* **[!UICONTROL Recommendations]**：已识别提高性能、实施最佳实践等机会。

* **[!UICONTROL Warnings]**：需要注意但对优化或管理无关紧要的问题。

* **[!UICONTROL Issues]**：需要立即注意的严重问题。 包括帐户授权错误通知。

## 通知类别

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**： [批量工作表操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)已完成或失败的通知。<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**： Search、Social和Commerce缺少[广告网络管理器帐户](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)的凭据的通知，这些凭据是正确设置关键功能所必需的。<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**：关于在后台执行的作业已完成或失败的通知。 作业类型包括[批量工作表作业](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available-->、批量编辑数据表中的作业或使用工具栏、实体分配作业或用户界面中的其他操作（如与广告网络同步、粘贴行或重命名实体）。 实体分配包括向任何实体分配或取消分配[标签分类值](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)、向项目组合分配营销活动以及[向实体分配或取消分配竞价约束](/help/search-social-commerce/new-ui/goals/constraints-manage.md)。

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：通知已通过[手动帐户数据上传](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md)上传帐户数据文件或帐户数据上传失败。<!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**：通知已通过[将帐户数据上传到 [!DNL Amazon] [!DNL S3]存储段](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md)上载帐户数据文件或帐户数据上传失败。<!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**：通知Search、Social和Commerce无法访问[广告网络帐户](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)，因为凭据无效或授权令牌无效或过期。

      * **[!UICONTROL Account Missing]**： Search、Social和Commerce缺少[广告网络帐户](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)的凭据的通知。

      * **[!UICONTROL Manager Account Auth Error]**：通知Search、Social和Commerce无法与[广告网络管理器帐户](/help/search-social-commerce/admin/manager-accounts.md)同步，因为凭据无效，或授权令牌无效或过期。<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**： [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md)已完成或失败的通知。

   * **[!UICONTROL Custom Alerts]**：为警报模板触发了[警报实例](/help/search-social-commerce/new-ui/alerts-manage.md)的通知。

   * **[!UICONTROL Spreadsheet Feeds]**： [电子表格馈送](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md)完成或失败的通知。

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**：有关特定视图的数据视图报告（例如[!UICONTROL Camapigns]视图中数据表的内容）已完成或失败的通知。

      * **[!UICONTROL Reports]**： [自定义或计划报告](/help/search-social-commerce/new-ui/reports/management/report-manage.md)完成或失败的通知。

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**：禁用当天优化时的通知。

      * **[!UICONTROL Simulation Report]**：有关[模拟作业](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md)的通知。

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**：广告商级别有关成功和失败自动分配营销活动转化目标的通知。

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**：项目组合级别有关成功和失败自动分配营销活动转化目标的通知。

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**：有关[项目组合通过批量处理工作表批量编辑作业的通知](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md)。

         * **[!UICONTROL Portfolio Settings]**：有关[项目组合设置](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md)更改的通知。

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## 可用操作

* [查看您的通知](#notification-view)

* [编辑您的通知设置](#notification-edit)

* [将通知标记为已读或未读](#notification-mark-read-unread)

* [删除通知](#notification-delete)

* [启用和禁用推送通知](#notification-push-enable-disable)

* [安装并卸载[!UICONTROL Notification Center] Web应用程序](#notification-app-install-uninstall)

## 查看您的通知 {#notification-view}

当您[订阅了有关帐户身份验证错误、触发的自定义警报以及生成的[!UICONTROL Advertising Insights]的通知](#notification-edit)时，您可以在[!UICONTROL Notifications]面板或[!UICONTROL Notification Center]中查看您的通知。

### 在[!UICONTROL Notifications]面板中查看通知

1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. （可选）执行以下任一操作：

   * 要查看任何通知的详细信息，请单击通知名称。

     在某些通知中，[!UICONTROL Action Recommended]部分可能包含一个链接，该链接会打开受影响或负责的实体的筛选视图。

   * 要将通知标记为&#x200B;*已读*&#x200B;或&#x200B;*未读*，请将光标悬停在警报名称上，然后单击![标记为已读或未读](/help/search-social-commerce/assets/notifications-read-unread.png "标记为已读或未读")。

     标记为&#x200B;*读取*&#x200B;的通知采用浅色文本，但在您删除它们之前仍可用。

     ![已读和未读通知](/help/search-social-commerce/assets/notifications-read-vs-unread.png "已读和未读通知")

   * 若要更改通知类型的订阅首选项，请单击通知旁边的![设置](/help/search-social-commerce/assets/settings-nc.png "设置")，更改设置，然后单击&#x200B;**[!UICONTROL Save]**。

   * 要删除通知，请单击通知旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。

   * 要打开[!UICONTROL Notification Center]，请单击&#x200B;**[!UICONTROL View All]**。

### 在[!UICONTROL Notification Center]中查看通知

1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 单击&#x200B;**[!UICONTROL View All]**。

1. （可选）要按类型筛选通知，请单击&#x200B;*[!UICONTROL Notices]、[!UICONTROL Recommendations]、[!UICONTROL Warnings]或[!UICONTROL Issues]*。

1. （可选）执行以下任一操作：

   * 要查看任何通知的详细信息，请单击通知名称。

     在某些通知中，[!UICONTROL Action Recommended]部分可能包含一个链接，该链接会打开受影响或负责的实体的筛选视图。

   * 要将通知标记为&#x200B;*已读*&#x200B;或&#x200B;*未读*，请将光标悬停在警报名称上，然后单击![标记为已读或未读](/help/search-social-commerce/assets/notifications-read-unread.png "标记为已读或未读")。

     标记为&#x200B;*读取*&#x200B;的通知采用浅色文本，但在您删除它们之前仍可用。

   * 若要更改通知类型的订阅首选项，请单击通知旁边的![设置](/help/search-social-commerce/assets/settings-nc.png "设置")，更改设置，然后单击&#x200B;**[!UICONTROL Save]**。

   * 要删除通知，请单击通知旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。

## 编辑您的通知设置 {#notification-edit}

您可以选择订阅或取消订阅有关帐户身份验证错误、触发的所有自定义警报以及完成您生成的[!UICONTROL Advertising Insights]的电子邮件和Web通知。

1. 通过以下任一方式打开通知设置：

   * 在任意页面的右上角，单击![通知](/help/search-social-commerce/assets/notifications.png "通知")以打开[!UICONTROL Notifications]面板。 单击右上角的![设置](/help/search-social-commerce/assets/settings-nc.png "设置")。

   * 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")，单击&#x200B;**[!UICONTROL View All]**&#x200B;打开[!UICONTROL Notification Center]，然后在左侧菜单中单击![设置](/help/search-social-commerce/assets/settings-nc.png "设置")。

1. 更改上面列出的任何通知类别的设置：

   * 要订阅或取消订阅通知，请移动[!UICONTROL Subscribe]列中的滑块：

      * 要取消订阅所有通知类型，请将滑块向左移动（已禁用）。

      * 要订阅一个或多个通知类型，请将滑块向右移动（已启用）。

   * （启用[!UICONTROL Subscribe]时）要订阅电子邮件通知，请选中&#x200B;**[!UICONTROL Email]**&#x200B;列中的复选框。

   * （禁用[!UICONTROL Subscribe]时）要在Search、Social和Commerce中订阅Web通知，并在浏览器中启用推送通知时，选中&#x200B;**[!UICONTROL Web]**&#x200B;列中的复选框。

     Web通知仅在您[启用推送通知](#notification-push-enable-disable)到浏览器时发送。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 将通知标记为已读或未读 {#notification-mark-read-unread}

将通知标记为&#x200B;*已读*&#x200B;或&#x200B;*未读*&#x200B;将更改每页顶部[!UICONTROL Notifications]链接中指示的未读通知数（如具有未读通知计数器的![通知图标](/help/search-social-commerce/assets/notifications-unread.png "具有未读通知计数器的通知图标")）。

标记为&#x200B;*读取*&#x200B;的通知采用浅色文本，但在您删除它们之前仍可用。

![已读和未读通知](/help/search-social-commerce/assets/notifications-read-vs-unread.png "已读和未读通知")

1. [打开通知面板或通知中心](#notification-view)。

1. 将光标悬停在警报名称上，然后单击![标记为已读或未读](/help/search-social-commerce/assets/notifications-read-unread.png "标记为已读或未读")。

## 删除通知 {#notification-delete}

### 删除[!UICONTROL Notifications]面板中的通知

1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 单击通知旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。

### 删除[!UICONTROL Notification Center]中的通知

1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 单击&#x200B;**[!UICONTROL View All]**。

1. （可选）要按类型筛选通知，请单击&#x200B;*[!UICONTROL Notices]*、*[!UICONTROL Recommendations]*、*[!UICONTROL Warnings]*&#x200B;或&#x200B;*[!UICONTROL Issues]*。

1. 单击通知旁边的![删除](/help/search-social-commerce/assets/delete.png "删除")。

## 启用和禁用推送通知 {#notification-push-enable-disable}

您可以在Search、Social和Commerce中启用通知，通知会根据浏览器的通知约定显示在这里。 在使用[!DNL Microsoft Windows]的设备上，通知显示在屏幕（系统托盘）的右下方。 在[!DNL Apple Mac]设备上，通知显示在右侧菜单中。

推送通知在以下浏览器中可用：

* [!DNL Google Chrome] 40及更高版本

* [!DNL Microsoft Edge] 17及更高版本

* [!DNL Mozilla Firefox] 44及更高版本

您可以根据浏览器的标准过程禁用推送通知。

### 启用推送通知

1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 单击&#x200B;**[!UICONTROL View All]**。

1. 单击右下角的![启用推送通知](/help/search-social-commerce/assets/notifications-push.png "启用推送通知")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Enable]**。

1. 将浏览器配置为允许来自[!UICONTROL Notification Center] （位于`https://alert-center-ui-na.efrontier.com`）的通知。

   默认通知设置因浏览器而异，您可以a)自动显示允许来自[!UICONTROL Notification Center]的通知的选项，或者b)需要手动管理通知设置。 例如，在[!DNL Microsoft Edge]中，您可以允许浏览器工具栏中的[!UICONTROL Notification Center]通知。 请参阅浏览器帮助中的说明。

   ![在Microsoft Edge中管理通知设置的位置](/help/search-social-commerce/assets/notifications-blocked-dialog.png "在Microsoft Edge中管理通知设置的位置")

1. 在您的[通知设置](#notification-edit)中，为要推送的警报类型启用[!UICONTROL Web]通知。

### 禁用推送通知

在浏览器的通知管理器中从`https://alert-center-ui-na.efrontier.com`删除通知。 例如，在[!DNL Google Chrome]中，您可以从位于`chrome://settings/content/notifications`的指定站点删除或阻止通知。

请参阅浏览器帮助中的说明。

## 安装并卸载[!UICONTROL Notification Center] Web应用程序 {#notification-app-install-uninstall}

通过安装[!UICONTROL Notification Center] Web应用程序，您可以在浏览器之外接收和管理通知。 该应用程序与Search、Social和Commerce中的[!UICONTROL Notification Center]看起来相同，并且具有相同的功能。 应用程序适用于[!DNL Google Chrome] 40及更高版本或[!DNL Microsoft Edge] 17及更高版本。

安装[!UICONTROL Notification Center]应用程序后，将在浏览器的应用程序管理器中自动启用该应用程序，并将其作为单独的窗口加载，其布局将根据窗口大小动态排列。 您可以从浏览器的应用程序管理器中打开和关闭应用程序，或将其固定到操作系统的任务栏或坞站。 应用程序会自动更新。

![Microsoft Windows任务栏中的通知中心图标](/help/search-social-commerce/assets/windows-taskbar.png "Microsoft Windows任务栏中的通知中心图标")

您可以从浏览器的应用程序管理器中禁用或卸载应用程序。 有关管理Web应用程序的其他信息，请参阅浏览器的帮助。

### 为[!DNL Google Chrome]安装[!UICONTROL Notification Center] Web应用程序

1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

1. 单击&#x200B;**[!UICONTROL View All]**。

1. 单击右下角的![安装通知中心Web应用](/help/search-social-commerce/assets/notifications-install-app.png "安装通知中心Web应用")。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Add]**。

1. 在安装应用程序中？ 消息，请单击&#x200B;**[!UICONTROL Install]**。

### 为[!DNL Microsoft Edge]安装[!UICONTROL Notification Center] Web应用程序

* 从Search、Social和Commerce中：

   1. 单击任何页面右上角的![通知](/help/search-social-commerce/assets/notifications.png "通知")。

   1. 单击&#x200B;**[!UICONTROL View All]**。

   1. 单击右下角的![安装通知中心Web应用](/help/search-social-commerce/assets/notifications-install-app.png "安装通知中心Web应用")。

   1. 在确认消息中，单击&#x200B;**[!UICONTROL Add]**。

   1. 在[!UICONTROL Install Notification Center]应用消息中，单击&#x200B;**[!UICONTROL Install]**。

* 从[!DNL Edge]主菜单：

   1. 在浏览器工具栏中，单击&#x200B;**...** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**。

   1. 在[!UICONTROL Install Notification Center]应用消息中，单击&#x200B;**[!UICONTROL Install]**。

### 卸载[!DNL Google Chrome]的[!UICONTROL Notification Center] Web应用程序

* 在[!DNL Chrome]中，转到`chrome://apps`，右键单击&#x200B;**[!UICONTROL notification-center]**，然后单击&#x200B;**[!UICONTROL Remove from Chrome]**。

### 卸载[!DNL Microsoft Edge]的[!UICONTROL Notification Center] Web应用程序

1. 在[!DNL Edge]浏览器工具栏中，单击&#x200B;**...** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**。 或者，转到`edge://apps`。

1. 右键单击&#x200B;**[!UICONTROL Notification Center]**&#x200B;并单击&#x200B;**[!UICONTROL Uninstall]**。

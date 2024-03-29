---
title: 关于通知
description: 了解通知，包括不同的类型和类别。
exl-id: a21dae13-b948-48e0-922a-d865f86e72f8
feature: Search Notifications
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 关于通知

*Beta版功能*

您可以将通知设置配置为订阅或取消订阅不同类型的警报。 您可以通过以下任意方式查看通知：

* 从 [!UICONTROL Notifications] 面板，可从以下位置的主菜单访问： ![通知](/help/search-social-commerce/assets/notifications-panel.png "通知").

* 从 [!UICONTROL Insights & Reports] > [!UICONTROL Notification Center Beta].

* 从 [!UICONTROL Notification Center] Web应用程序，打开 [!UICONTROL Notification Center] 在“搜索”、“社交”和“商务”之外的单独窗口中。

  应用程序加载速度比常规浏览器版本更快，并且会自动更新。 您可以安装应用程序，并使用浏览器的应用程序管理器来管理应用程序。

* 从推送通知到浏览器。

  启用推送通知后，将根据浏览器的通知约定显示推送通知。

您可以查看通知、将通知标记为已读或未读以及删除通知。

## 通知类型

* **[!UICONTROL Notices]**：版本、停机时间和其他变更管理通知。

* **[!UICONTROL Recommendations]**：识别出的提高性能、实施最佳实践等机会。

* **[!UICONTROL Warnings]**：需要注意但对优化或管理无关紧要的问题。

* **[!UICONTROL Issues]**：需要立即关注的严重问题。 包括帐户授权错误通知。

## 通知类别

* [!UICONTROL Campaign Management]

   * **[!UICONTROL UI Actions]**：关于在后台执行的作业已完成或失败的通知。 作业类型包括 [批量处理工作表作业](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，批量编辑数据表中的作业，或者使用工具栏、实体分配作业或用户界面中的其他操作（例如与广告网络同步、粘贴行或重命名实体）。 实体分配包括分配或取消分配 [标签分类值](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md) 将促销活动分配给项目组合，并将约束条件分配给或取消分配给项目组合。<!--Link "constraint" to constraint-about.md if that file is ever public -->

   * **[!UICONTROL Bulksheets]**：通知 [批量工作表操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 已完成或失败。

   * **[!UICONTROL Manager Account Missing]**：通知Search、Social and Commerce缺少 [ad network manager帐户](/help/search-social-commerce/admin/manager-accounts.md)，这些组件用于正确设置关键函数。

  <!--
  * [!UICONTROL Setup Errors]
  
    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: : Notifications that the [!UICONTROL Landing Page Suffix] value is incorrect, missing, or contains an incorrect [AMO ID template](/help/integrations/analytics/ids.md#amo-id-formats); or it's overridden at a lower level by an incorrect value.
    
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are for the correct setup of critical functions.
  -->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Manager Account Auth Error]**：通知Search、Social和Commerce无法与 [ad network manager帐户](/help/search-social-commerce/admin/manager-accounts.md) 由于凭据无效或授权令牌无效或过期。

      * **[!UICONTROL Account Auth Error]**：通知Search、Social和Commerce无法访问 [广告网络帐户](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) 由于凭据无效或授权令牌无效或过期。

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**：用于封闭测试版

      * **[!UICONTROL File Upload to Cloud Storage]**：用于封闭测试版

<!--
* [!UICONTROL Optimization]
-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Custom Alerts]**：通知 [警报实例](/help/search-social-commerce/alerts/alert-about.md) 为警报模板触发。

   * **[!UICONTROL Spreadsheet Feeds]**：通知 [电子表格馈送](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md) 已完成或失败。

   * **[!UICONTROL Reports]**：通知 [自定义或计划报告](/help/search-social-commerce/reports/report-about.md) 已完成或失败。

   * **[!UICONTROL Advertising Insights]**：通知 [一个 [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) 已完成或失败。

<!--
* [!UICONTROL System]
-->

>[!MORELIKETHIS]
>
>* [查看您的通知](notification-view.md)
>* [将通知标记为已读或未读](notification-mark-read-unread.md)
>* [删除通知](notification-delete.md)
>* [编辑您的通知设置](notification-edit.md)
>* [启用和禁用来自的推送通知 [!UICONTROL Notification Center]](notifications-push-enable-disable.md)
>* [安装并卸载 [!UICONTROL Notification Center] Web应用程序](notification-app-install-uninstall.md)

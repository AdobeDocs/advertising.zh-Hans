---
title: 重新验证a [!DNL Google Analytics] 数据源
description: 了解如何在更改相关密码或证书过期时重新验证 [!DNL Google Analytics] 数据源。
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# 重新验证[!DNL Google Analytics]数据源

*仅限Agency管理员、Agency客户经理、Adobe客户经理和管理员*

如果更改用于数据源的电子邮件帐户的密码，或者帐户的[!DNL OAuth]证书过期，则与该电子邮件帐户的所有打开连接都将关闭，您必须重新进行身份验证才能继续同步数据。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**。

1. 选中要重新验证的数据源旁边的复选框。

1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 编辑[数据源设置](data-source-settings.md)：

   1. 在[!UICONTROL Connect to Google Analytics]部分中，执行以下操作。

      1. （如有必要）输入新的电子邮件地址，用于访问此数据源的数据。 电子邮件地址必须注册到[!DNL Google]帐户，并且具有[!DNL Google Analytics]帐户的“读取和分析”权限。 请参阅[有关在 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587)中分配用户权限的说明。

         >[!TIP]
         >
         >要确保Search、Social和Commerce中仅提供特定[!DNL Google Analytics]属性和视图，请使用只能访问这些属性和视图的电子邮件地址登录。

   1. 选中此复选框可授权搜索、社交和Commerce访问帐户的量度。

   1. 单击&#x200B;**[!UICONTROL Re-Authenticate]**。

1. 单击&#x200B;**[!UICONTROL Post]**。

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置a [!DNL Google Analytics] 数据源的先决条件](data-source-prerequisites.md)
>* [将a [!DNL Google Analytics] 视图配置为数据源](data-source-configure.md)
>* [编辑a [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停同步数据源](data-source-pause.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 指标](data-source-ga-metrics.md)

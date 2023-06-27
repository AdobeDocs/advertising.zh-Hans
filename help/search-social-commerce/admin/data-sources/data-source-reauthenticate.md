---
title: 重新验证 [!DNL Google Analytics] 数据源
description: 了解如何重新验证 [!DNL Google Analytics] 数据源。
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# 重新验证 [!DNL Google Analytics] 数据源

*仅限机构管理员、机构客户经理、Adobe客户经理和管理员*

如果您更改用于数据源的电子邮件帐户的密码，或者 [!DNL OAuth] 帐户的证书过期，则与电子邮件帐户的所有打开连接都将关闭，您必须重新进行身份验证才能继续同步数据。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. 选中要重新验证的数据源旁边的复选框。

1. 在数据表上方的工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑").

1. 编辑 [数据源设置](data-source-settings.md)：

   1. 在 [!UICONTROL Connect to Google Analytics] 部分，请执行以下操作。

      1. （如有必要）输入用于访问此数据源的数据的新电子邮件地址。 电子邮件地址必须注册到 [!DNL Google] 帐户并具有的“读取和分析”权限 [!DNL Google Analytics] 帐户。 请参阅 [在中分配用户权限的说明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >确保仅特定于 [!DNL Google Analytics] 可在Search、Social和Commerce中访问属性和视图，使用只能访问这些属性和视图的电子邮件地址登录。

   1. 选中此复选框可授权Search、Social和Commerce访问帐户的指标。

   1. 单击 **[!UICONTROL Re-Authenticate]**.

1. 单击 **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置的前提条件 [!DNL Google Analytics] 数据源](data-source-prerequisites.md)
>* [配置 [!DNL Google Analytics] 作为数据源查看](data-source-configure.md)
>* [编辑 [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停数据源同步](data-source-pause.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)

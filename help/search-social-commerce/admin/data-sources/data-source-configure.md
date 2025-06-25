---
title: 将 [!DNL Google Analytics] 视图配置为数据源
description: 了解如何从 [!DNL Google Analytics] 视图配置数据源。
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 将[!DNL Google Analytics]视图配置为数据源

*仅限Agency管理员、Agency客户经理、Adobe客户经理和管理员*

您可以为每个[!DNL Google Analytics]帐户、属性和视图组合创建一个数据源。

要集成多个属性的量度或集成单个属性的多个视图的量度，请为每个属性设置单独的数据源。

1. [执行集成 [!DNL Google Analytics] 帐户](data-source-prerequisites.md)的所有先决条件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 在[!UICONTROL Deployment Prerequisites]对话框中，选中该复选框以确认在[!DNL Google Analytics]帐户中实施了所需的自定义维度“ef_id”，然后单击&#x200B;**[!UICONTROL Continue]**。

   贵组织中的其他角色可能已执行某些先决条件。 如果您对先决条件有任何疑问，请联系Adobe客户团队。

1. 输入[数据源设置](data-source-settings.md)：

   1. 在&#x200B;**[!UICONTROL Connect to [!DNL Google Analytics]]**&#x200B;部分中，执行以下操作。

      1. 输入[!DNL Google Analytics]帐户的数值ID。

      1. 输入用于访问此数据源数据的电子邮件地址。 电子邮件地址必须注册到[!DNL Google]帐户，并且具有[!DNL Google Analytics]帐户的“读取和分析”权限。 请参阅[有关在 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587)中分配用户权限的说明。

         >[!TIP]
         >
         >要确保Adobe Advertising中只有特定的[!DNL Google Analytics]属性和视图可用，请使用只能访问这些属性和视图的电子邮件地址登录。

         >[!NOTE]
         >
         >如果您稍后更改此电子邮件帐户的密码，则会关闭与该电子邮件帐户的所有打开连接。 若要继续同步数据，请返回此页面并[重新进行身份验证](data-source-reauthenticate.md)。

      1. 选中此复选框可授权Adobe Advertising访问帐户的指标。

      1. 单击&#x200B;**[!UICONTROL Authenticate]**。

   1. 在[!UICONTROL Account Details]部分中，指定要导入的量度的属性和视图。 此外，指定使用“ef_id”查询字符串参数的值填充的自定义维度。

   1. 在[!UICONTROL Import Metrics]部分中，指定要包含在信息源中的量度。

      您不能删除自动包含的[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]或[!UICONTROL Session Duration]。 您最多可以添加16个其他有效量度或量度，而无需数据。

      >[!WARNING]
      >
      >[!DNL Google Analytics]在单个数据馈送中最多允许10个量度。 Search、Social和Commerce最多可支持两个包含20个量度的馈送，但使用第二个馈送会将您的API调用翻倍到[!DNL Google Analytics]。 如果您有许多量度，请仅选择要在优化目标中使用的量度。 查看有关 [!DNL Google Analytics][&#128279;](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)的API请求的配额和调用限制的详细信息。

   1. 在[!UICONTROL Metric Tag]部分中，输入要附加到数据源的每个量度的标记名称。

1. 单击右上角的&#x200B;**[!UICONTROL Post]**。

   该数据源名为“AccountName > PropertyName > ViewName”，且会自动激活。 要暂停数据源，请参阅“[暂停来自数据Source的馈送](data-source-pause.md)”。

   完成每日数据同步（从广告商所在时区的05:00开始）后的第二天，这些量度将可用。 量度可用后，即可在[[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)中看到它们。 每个新的转化量度都名为“`ga:backEndMetricName_propertyID_viewID`”，其中“backEndMetricName”是API使用的量度名称。 每个新转化量度的显示名称是“`friendlyMetricName_ga:MetricTag`”，其中“friendlyMetricName”是出现在[!DNL Google Analytics]中的量度名称，“MetricTag”是在数据源设置中定义的[!UICONTROL Metric Tag]。

   您可以将这些量度直接添加到营销活动管理和项目组合管理视图、报表和优化目标。

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置a [!DNL Google Analytics] 数据源的先决条件](data-source-prerequisites.md)
>* [编辑a [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停同步数据源](data-source-pause.md)
>* [重新验证a [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 指标](data-source-ga-metrics.md)

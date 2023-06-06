---
title: 配置 [!DNL Google Analytics] 作为数据源查看
description: 了解如何从配置数据源 [!DNL Google Analytics] 视图。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 配置 [!DNL Google Analytics] 作为数据源查看

*仅限机构管理员、机构客户经理、Adobe客户经理和管理员*

您可以为每个报表包创建一个数据源 [!DNL Google Analytics] 帐户、属性和视图组合。

要集成多个属性的量度或单个属性的多个视图的量度，请为每个属性设置单独的数据源。

1. [执行集成的所有先决条件 [!DNL Google Analytics] 帐户](data-source-prerequisites.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 在 [!UICONTROL Deployment Prerequisites] 对话框中，选中该复选框以确认在中实施了所需的自定义维度“ef_id” [!DNL Google Analytics] 帐户，然后单击 **[!UICONTROL Continue]**.

   贵组织中的其他角色可能已执行某些先决条件。 如果您对先决条件有任何疑问，请联系Adobe客户团队。

1. 输入 [数据源设置](data-source-settings.md)：

   1. 在 **[!UICONTROL Connect to [!DNL Google Analytics]]** 部分，请执行以下操作。

      1. 输入数值ID [!DNL Google Analytics] 帐户。

      1. 输入用于访问此数据源的数据的电子邮件地址。 电子邮件地址必须注册到 [!DNL Google] 帐户并具有的“读取和分析”权限 [!DNL Google Analytics] 帐户。 请参阅 [在中分配用户权限的说明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >确保仅特定于 [!DNL Google Analytics] 属性和视图在Adobe广告中可用，请使用只能访问这些属性和视图的电子邮件地址登录。

         >[!NOTE]
         >
         >如果您稍后更改此电子邮件帐户的密码，则将关闭与该电子邮件帐户的所有已打开连接。 要恢复同步数据，请返回此页面并 [重新身份验证](data-source-reauthenticate.md).

      1. 选中此复选框可授权Adobe广告访问帐户的指标。

      1. 单击 **[!UICONTROL Authenticate]**.
   1. 在 [!UICONTROL Account Details] 部分，指定要导入的量度的属性和视图。 此外，指定使用“ef_id”查询字符串参数的值填充的自定义尺寸。

   1. 在 [!UICONTROL Import Metrics] 部分，指定要包含在信息源中的量度。

      无法删除 [!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]，或 [!UICONTROL Session Duration]，自动包含。 您最多可以添加16个其他有效指标或指标，而无需数据。

      >[!WARNING]
      >
      >[!DNL Google Analytics] 在单个数据馈送中最多允许10个量度。 搜索、Social和Commerce最多可支持两个馈送，总共20个量度，但使用第二个馈送会将您的API调用翻倍 [!DNL Google Analytics]. 如果您有许多量度，请仅选择要在优化目标中使用的量度。 查看更多关于 [API请求的配额和调用限制为 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. 在 [!UICONTROL Metric Tag] 部分，输入要附加到数据源的每个量度的标记的名称。


1. 在右上角，单击 **[!UICONTROL Post]**.

   该数据源名为“AccountName > PropertyName > ViewName”，且会自动激活。 要暂停数据源，请参阅“[暂停数据源馈送](data-source-pause.md).”

   完成每日数据同步（从广告商所在时区的05:00开始）后的第二天，这些量度将可用。 量度可用后，便可在以下位置查看： [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). 每个新的事务属性都命名为&#39;&#39;`ga:backEndMetricName_propertyID_viewID`，”其中，“backEndMetricName”是API使用的量度名称。 每个新事务属性的显示名称为“`friendlyMetricName_ga:MetricTag`，其中“friendlyMetricName”是中显示的指标名称 [!DNL Google Analytics] 而“MetricTag”是 [!UICONTROL Metric Tag] 在数据源设置中定义。

   您可以将这些量度直接添加到营销活动管理和项目组合管理视图、报表和优化目标。

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置的前提条件 [!DNL Google Analytics] 数据源](data-source-prerequisites.md)
>* [编辑 [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停数据源同步](data-source-pause.md)
>* [重新验证 [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)


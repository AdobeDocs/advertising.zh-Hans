---
title: 配置 [!DNL Google Analytics] 作为数据源查看
description: 了解如何从配置数据源 [!DNL Google Analytics] 视图。
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# 配置 [!DNL Google Analytics] 作为数据源查看

*仅限代理管理员、代理客户经理、Adobe客户经理和管理员*

您可以为每个报表包创建一个数据源 [!DNL Google Analytics] 帐户、属性和视图组合。

要集成多个属性的量度或集成单个属性的多个视图的量度，请为每个属性设置单独的数据源。

1. [执行所有集成的前提条件 [!DNL Google Analytics] 帐户](data-source-prerequisites.md).

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 在 [!UICONTROL Deployment Prerequisites] 对话框中，选中该复选框以确认在中实施了所需的自定义维度“ef_id” [!DNL Google Analytics] 帐户，然后单击 **[!UICONTROL Continue]**.

   贵组织中的其他角色可能已执行某些先决条件。 如果您对先决条件有任何疑问，请联系Adobe客户团队。

1. 输入 [数据源设置](data-source-settings.md)：

   1. 在 **[!UICONTROL Connect to [!DNL Google Analytics]]** 部分，执行以下操作。

      1. 输入数值ID [!DNL Google Analytics] 帐户。

      1. 输入用于访问此数据源数据的电子邮件地址。 电子邮件地址必须注册到 [!DNL Google] 帐户并具有的“读取和分析”权限 [!DNL Google Analytics] 帐户。 请参阅 [在中分配用户权限的说明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >为了确保 [!DNL Google Analytics] 属性和视图在Adobe Advertising中可用，请使用只能访问这些属性和视图的电子邮件地址登录。

         >[!NOTE]
         >
         >如果您稍后更改此电子邮件帐户的密码，则会关闭与该电子邮件帐户的所有打开连接。 要恢复同步数据，请返回此页并 [重新进行身份验证](data-source-reauthenticate.md).

      1. 选中此复选框可授权Adobe Advertising访问帐户的指标。

      1. 单击 **[!UICONTROL Authenticate]**.

   1. 在 [!UICONTROL Account Details] 部分，指定要导入的度量的属性和视图。 此外，指定使用“ef_id”查询字符串参数的值填充的自定义维度。

   1. 在 [!UICONTROL Import Metrics] 部分，指定要包含在信息源中的量度。

      无法删除 [!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]，或 [!UICONTROL Session Duration]，自动包含这些字段。 您最多可以添加16个其他有效量度或量度，而无需数据。

      >[!WARNING]
      >
      >[!DNL Google Analytics] 在单个数据馈送中最多允许10个量度。 搜索、Social和Commerce最多可支持两个包含总共20个量度的馈送，但使用第二个馈送会将您的API调用翻倍 [!DNL Google Analytics]. 如果您有许多量度，请仅选择要在优化目标中使用的量度。 查看更多关于 [将API请求的配额和调用限制分配给 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. 在 [!UICONTROL Metric Tag] 部分，输入要附加到数据源的每个量度的标记的名称。

1. 在右上角，单击 **[!UICONTROL Post]**.

   该数据源名为“AccountName > PropertyName > ViewName”，且会自动激活。 要暂停数据源，请参阅“[暂停数据源馈送](data-source-pause.md)“

   完成每日数据同步（从广告商所在时区的05:00开始）后的第二天，这些量度将可用。 量度可用后，即可在以下位置查看： [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). 每个新的事务属性都命名为&#39;&#39;`ga:backEndMetricName_propertyID_viewID`，”其中，“backEndMetricName”是API使用的量度名称。 每个新事务属性的显示名称为&#39;&#39;`friendlyMetricName_ga:MetricTag`，“friendlyMetricName”是中显示的量度名称 [!DNL Google Analytics] 而“MetricTag”是 [!UICONTROL Metric Tag] 在数据源设置中定义。

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

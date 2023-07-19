---
title: 关于自定义报表
description: 了解手动或使用预配置的报表模板创建自定义报表的选项。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: ab892528a2fbc0ed5994938ead23cd8e33e8b45f
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# 关于自定义报表

通过自定义报表，您可以使用促销活动维度（例如广告商、版面、网站或地域）以及对您最重要的量度来自定义报表数据的内容和交付。 您可以：

* 在粒度级别完全配置营销活动效果报表。
* 从预配置的报表模板中进行选择，并可以选择进一步自定义它们。

您可以生成报告一次，也可以安排在指定时区的每日、每周或每月的03:00生成报告。 生成报告后，报告将发送给每个指定的电子邮件收件人或链接 [报告目标](/help/dsp/reports/report-destinations/report-destination-about.md) 下列类型之一：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL（测试版）

>[!NOTE]
>
>您还可以查看促销活动所有级别（促销活动、资源包、投放位置或广告）的按需数据 [在相关的营销活动管理视图中](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## 可用报表类型

* **[!UICONTROL Custom]：** 此报表是一个空白模板，您可以使用大多数维度和量度创建自己的自定义报表。 [!UICONTROL Conversion]， [!UICONTROL Device]， [!UICONTROL Geo]、和 [!UICONTROL Site] 报告是此模板的变体，具有针对其各自用例预先选定的列和维度。

* 预配置的报表模板

   * **[!UICONTROL Billing]：** 使用此报表可了解关键计费指标，如按营销活动划分的媒体计费的支出指标。

     >[!NOTE]
     >
     >此报表包括关于计费区段的数据。 如果向用户或设备提供了属于多个区段的展示，则只会将一个可计费区段计入该展示。

   * **[!UICONTROL Conversion]：** 使用此报告可以基于通过Adobe Advertising转化跟踪捕获的转化量度，了解促销活动的执行情况。 此报表包含多点接触归因。

   * **[!UICONTROL Device]：** 使用此预填充模板可按设备相关的维度查看关键量度。

   * **[!UICONTROL Frequency (by Impression)]：** 使用此报表可了解向独特查看者显示的展示次数分布（例如，有多少位独特查看者查看了一次展示、两次展示、三次展示等等）。 数据按投放位置或营销活动提供。

     >[!NOTE]
     >
     >* 数据在2019年3月1日后可用。
     >* 基于数据采样来估计频率。
     >* 对于某些库存，发布者不会传递设备标识符，这会阻止频率跟踪。 此报表仅包含设备标识符可用的展示次数。

   * **[!UICONTROL Frequency (by App/Site)]：** 使用此报表可了解通过应用程序或站点到达的独特用户数。 您还可以查看仅通过特定应用程序或网站（“不同的独特用户”）访问过多少个独特用户。

     >[!NOTE]
     >
     >* 数据在2018年11月15日后可用。
     >* 对于某些私有库存，发布者不会传递设备标识符，这会阻止频率跟踪。

   * **[!UICONTROL Geo]**：使用此预填充模板可查看按地理维度划分的关键量度。

   * **[!UICONTROL Margin]：** 使用此报表可以查看关键量度，如利润率、利润和按促销活动或投放位置列出的其他支出量度。

   * **[!UICONTROL Segment]：** 使用此预填充模板可查看按区段划分的关键量度。

     >[!NOTE]
     >
     >* 此报表旨在显示不同目标区段的表现。 它使用区段成员资格数据。 当向属于两个或多个目标区段的用户或设备提供展示时，此报表将为每个区段包含一行。 因此，此报表中的总计可能与实际交付内容不匹配。
     >* 区段的转化量度和自定义目标数据在2019年8月2日后可用。 区段的所有其他数据在2018年6月1日后可用。

   * **[!UICONTROL Site]：** 默认情况下，包括标准量度、媒体净支出总额以及按网站划分的可计费净支出总额。

   * **[!UICONTROL Household Reach & Frequency]：** 使用此报表可根据IP地址而不是设备/Cookie级别，在家庭级别查看跨广告格式的单个维度的展示次数、覆盖范围和频率。 利用这些见解优化您的媒体组合、提高性能并发现增量访问的机会。 参见“[有关家庭报表的常见问题解答](/help/dsp/reports/faq-household-report.md)”以了解更多信息。

   * **[!UICONTROL Household Conversions]：** 使用此报表可查看基于IP地址的家庭级别而非设备/Cookie级别的显示到达转化。 使用见解来衡量和优化营销活动绩效。 参见“[有关家庭报表的常见问题解答](/help/dsp/reports/faq-household-report.md)”以了解更多信息。

## 跨帐户报告 {#cross-account-reporting}

任何拥有多个DSP帐户的组织，都可以根据需要选择在自定义报表中启用跨帐户数据。 例如，您可以授予帐户A访问帐户B数据的权限，并授予帐户B访问帐户C（但不访问帐户A）数据的权限。 要启用和配置此功能，请联系您的Adobe客户团队。

为您的组织启用该功能后，您可以 [过滤器](report-settings.md) 按帐户列出的以下任意报表类型：  [!UICONTROL Custom]， [!UICONTROL Site]， [!UICONTROL Segment]， [!UICONTROL Geo]， [!UICONTROL Device]， [!UICONTROL Frequency (by Impression)]、和 [!UICONTROL Conversion].

您的帐户设置位于 [!UICONTROL Settings] > [!UICONTROL Account] 指示a)其数据可供您的帐户使用的其他帐户，以及b)可以访问您的帐户数据的其他帐户。

>[!MORELIKETHIS]
>
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [关于的常见问题解答 [!UICONTROL Household] 报告](/help/dsp/reports/faq-household-report.md)
>* [关于平台内报告](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用报表列](/help/dsp/reports/report-columns.md)
>* [关于 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

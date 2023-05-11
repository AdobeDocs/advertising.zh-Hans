---
title: 关于自定义报表
description: 了解手动创建自定义报表或使用预配置报表模板的选项。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 858b00ec28158ada1edfc70a2efc3540fa46a376
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# 关于自定义报表

自定义报表允许您使用促销活动维度（如广告商、版面、网站或地点）和对您最重要的量度，自定义报表数据的内容和交付。 您可以：

* 在粒度级别完全配置营销活动效果报表。
* 从预配置的报表模板中进行选择，或者进一步自定义这些模板。

您可以生成一次报表，或安排在指定时区的03:00每天、每周或每月生成报表。 生成报表后，报表会提交给每个指定的电子邮件收件人或链接的 [报告目标](/help/dsp/reports/report-destinations/report-destination-about.md) 类型：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL（测试版）

>[!NOTE]
>
>您还可以查看营销活动所有级别的按需数据（营销活动、包、版面或广告） [在相关的促销活动管理视图中](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## 可用报表类型

* **[!UICONTROL Custom]:** 此报表是一个空白模板，您可以使用该模板创建您自己的自定义报表，并使用大多数维度和量度。 [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo]和 [!UICONTROL Site] 报表是此模板的变体，其中包含预先选择的列和用于其各自用例的维度。

* 预配置的报表模板

   * **[!UICONTROL Billing]:** 使用此报表可了解关键计费量度，如按促销活动划分的媒体计费支出量度。

      >[!NOTE]
      >
      >此报表包含有关账单区段的数据。 如果向用户或设备提供属于多个区段的展示，则仅有一个可计费区段会计入展示。

   * **[!UICONTROL Conversion]:** 使用此报表可了解您的促销活动如何根据使用Adobe广告转化跟踪捕获的转化量度执行。 此报表包含多接触点归因。

   * **[!UICONTROL Device]:** 使用此预填充模板可按设备相关维度查看关键量度。

   * **[!UICONTROL Frequency (by Impression)]:** 使用此报表可了解展示给独特查看者的展示次数分布（例如，有多少独特查看者查看了一次展示、两次展示、三次展示等）。 数据可按版面或营销活动使用。

      >[!NOTE]
      >
      >* 2019年3月1日之后可使用数据。
      >* 根据数据采样来估计频率。
      >* 对于某些内容库，发布者不会传递设备标识符，这会阻止频度跟踪。 此报表仅包含设备标识符可用的展示次数。


   * **[!UICONTROL Frequency (by App/Site)]:** 使用此报表可了解通过应用程序或网站访问了多少个独特用户。 您还可以查看仅通过特定应用程序或网站（“不同的独特用户”）访问了多少个独特用户。

      >[!NOTE]
      >
      >* 2018年11月15日之后可使用数据。
      >* 对于某些专用内容库，发布者不会传递设备标识符，这会阻止频度跟踪。


   * **[!UICONTROL Geo]**:使用此预填充模板可按地理维度查看关键量度。

   * **[!UICONTROL Margin]:** 使用此报表可按促销活动或版面查看关键量度，如利润、利润和其他支出量度。

   * **[!UICONTROL Segment]:** 使用此预填充模板可按区段查看关键量度。

      >[!NOTE]
      >
      >* 此报表旨在显示不同目标区段的执行情况。 它使用区段成员资格数据。 当向属于两个或更多目标区段的人员或设备提供展示时，此报表会为每个区段包含一行。 因此，此报表中的总数可能与实际提交不匹配。
      >* 区段的转化量度和自定义目标数据在2019年8月2日之后可用。 区段的所有其他数据均可在2018年6月1日之后开始使用。


   * **[!UICONTROL Site]:** 默认情况下，包括标准量度、媒体净支出总额和按网站划分的可计费净支出总额。

   * **[!UICONTROL Household]:** 使用此报表可在基于IP地址的家庭级别（而不是设备/Cookie级别）查看不同广告格式的单个维度的展示次数、访问次数和频度。 利用这些洞察优化您的媒体组合、提高性能，并发现增加访问的机会。 请参阅“[有关家庭报表的常见问题解答](/help/dsp/reports/faq-household-report.md)“ ”以了解详细信息。

## 跨帐户报告 {#cross-account-reporting}

具有多个DSP帐户的任何组织都可以根据组织的需要，选择在自定义报表中启用跨帐户数据。 例如，您可以授予帐户A访问帐户B数据的权限，并授予帐户B访问帐户C（但不授予帐户A）数据的权限。 要启用和配置此功能，请联系您的Adobe帐户团队。

为贵组织启用该功能后，您可以 [过滤器](report-settings.md) 按帐户划分的以下任何报表类型：  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]和 [!UICONTROL Conversion].

您的帐户设置位于 [!UICONTROL Settings] > [!UICONTROL Account] 指示a)其数据可用于您的帐户的其他帐户，以及b)可访问您帐户数据的其他帐户。

>[!MORELIKETHIS]
>
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [关于 [!UICONTROL Household] 报表](/help/dsp/reports/faq-household-report.md)
>* [关于平台内报表](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用报表列](/help/dsp/reports/report-columns.md)
>* [关于 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)


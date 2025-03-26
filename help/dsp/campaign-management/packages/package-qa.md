---
title: 使用批量处理工作表查看和编辑包设置
description: 了解如何使用电子表格批量查看和编辑关键包设置。
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# 使用批量处理工作表查看和编辑包设置

您可以以XLSX （[!DNL Microsoft Excel]电子表格）格式下载一个或多个包的设置以供审阅。 *批量处理工作表*&#x200B;文件包含带有航班信息的单独选项卡。

要一次更新多个设置，您可以执行以下任一操作：

* 进行更改以选择字段，保存文件，然后将编辑后的批量工作表文件上传回DSP。

* 要对营销活动中的其他包、投放位置或广告进行更改，请下载营销活动的批量处理工作表。 将更新的设置输入或粘贴到文件中，然后上传文件以进行更改。 有关说明，请参阅“[使用批量处理工作表查看和编辑Campaign组件设置](/help/dsp/campaign-management/campaign-components-review-edit.md)”。

可编辑字段包含大多数通常可编辑的设置。

>[!TIP]
>
>若要快速编辑一个或多个包的多个字段，请参阅“[编辑包](/help/dsp/campaign-management/packages/package-edit.md)”。

## 营销活动中所有包的下载设置

当您下载促销活动中所有包的设置时，批量工作表会为包设置和航班信息包含单独的选项卡。 您可以选择包含与包关联的投放位置和广告的设置；还包含用于投放位置和广告设置的附加选项卡。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * 在营销活动旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

   * 单击营销活动名称。 单击右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

1. 在[!UICONTROL Bulksheet Download]对话框中，取消选择要从下载文件中排除其设置的所有Campaign组件，然后单击&#x200B;**[!UICONTROL Download]**。

默认情况下，将选择与包关联的所有投放位置和广告的设置。

通知消息指示文件何时可供下载。

1. 要下载文件，请执行以下任一操作：

   * 在通知消息中，单击&#x200B;**[!UICONTROL Download].**

   * 单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。 单击作业旁边的&#x200B;**[!UICONTROL Download]**。

     文件已保存到浏览器的“下载”文件夹中。<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     要编辑任何设置，请直接编辑文件，然后上传更改。 所有可编辑的列都以蓝色突出显示。

## 特定包的下载设置

当您下载特定包的设置时，批量工作表文件包含用于包设置和航班信息的单独选项卡，并且该文件可编辑。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Packages]**。

1. 选中要下载其设置的包的复选框。

1. 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**。

   通知消息指示批量处理工作表文件何时可供下载。

1. 要下载批量处理工作表，请执行以下任一操作：

   * 在通知消息中，单击&#x200B;**[!UICONTROL Download].**

   * 单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。 单击作业旁边的&#x200B;**[!UICONTROL Download]**。

     该文件将保存到浏览器的“下载”文件夹中。 有关包含的列的列表，请参阅[已下载/上传批量处理工作表中的位置列](#qa-sheet-columns)。

     要编辑任何设置，请直接编辑文件，然后上传更改。 所有可编辑的列都以蓝色突出显示。 要对字段使用正确的格式，请从相关的包设置或放置设置中选择并复制值。 对于某些目标设置，例如分时段、自定义目标和转化量度，在设置中提供了一个复制选项。

## 上载具有包设置的批量工作表 {#upload-bulksheet-package}

您可以在批量工作表文件中上传包的设置，包括与包关联的投放位置和广告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 执行以下任一操作：

   * 在父营销活动旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

   * 单击营销活动名称。 单击右上角的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

     此选项可从[!UICONTROL Packages]、[!UICONTROL Placements]或[!UICONTROL Ads]选项卡获得。

   * 在子菜单中，单击&#x200B;**[!UICONTROL Packages]**，然后选中任何包的复选框。 在批量操作工具栏中，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**。

1. 在[!UICONTROL Upload Bulksheet]对话框中：

   1. 将文件拖放到框中，或者单击框内部以从设备或网络中选择文件。

   1. 单击&#x200B;**[!UICONTROL Upload]**。

1. （可选）要验证是否已处理更新，请单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。

当任何设置更新失败时，您可以下载带有颜色编码的批量工作表错误文件，以显示已保存哪些设置（行）以及哪些设置（行）失败，以及每个失败的原因。 然后，您可以在同一文件中解决问题，并再次上传它以处理更正后的信息。

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [使用批量处理工作表查看和编辑Campaign组件设置](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [编辑包](/help/dsp/campaign-management/packages/package-edit.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)

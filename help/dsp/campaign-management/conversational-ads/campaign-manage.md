---
title: 管理[!DNL ChatGPT Ads]个对话式广告营销活动
description: 了解如何创建和管理[!DNL ChatGPT Ads]营销活动、广告组和聊天卡广告，这是一项Beta版功能，可在AI助理对话中放置广告。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%
---
# 管理[!DNL ChatGPT Ads]对话式广告营销活动、广告组和广告

*Beta功能*

在[对话式广告帐户](account-manage.md)中管理[!DNL ChatGPT Ads]促销活动、广告组和聊天卡广告。

当月末您的其他发票使用[!DNL ChatGPT Ads]时，您将记帐。 有关计费问题，请联系您的Adobe客户团队。

## [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns]视图 {#campaign-views-about}

[!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns]视图包含三个选项卡： [!UICONTROL Campaigns]、[!UICONTROL Ad Groups]和[!UICONTROL Ads]。 每个选项卡都列出了选定帐户的促销活动、广告组或广告，以及选定日期范围的效果数据。 营销活动、广告组和广告级别的效果数据包括[!UICONTROL Impressions]、[!UICONTROL Clicks]、[!UICONTROL Spend]、[!UICONTROL CTR]、[!UICONTROL Avg CPC]和[!UICONTROL Avg CPM]。

>[!NOTE]
>
>* 配置为在报表视图中查看税值的组织在[!DNL ChatGPT Ads]中将看不到它们。 人工计算税值。

### 可用操作

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [创建](#campaign-create)或[编辑](#campaign-edit)营销活动

* [创建](#ad-group-create)或[编辑](#ad-group-edit)现有营销活动的广告组

* [创建](#ad-create)或[编辑](#ad-edit)现有广告组的广告

* [激活或暂停营销活动、广告组或广告](#pause-activate)

* [存档营销活动、广告组或广告](#archive)

* [从促销活动向下展开至广告组和广告](#drill-down)

* [刷新营销活动、广告组或广告列表](#refresh)

## 营销活动

### 创建[!DNL ChatGPT Ads]对话式广告营销活动 {#campaign-create}

在创建营销活动时，您可以选择创建其第一个广告组和广告。 每个步骤都会在您单击&#x200B;**[!UICONTROL Next]**&#x200B;后立即创建该实体，因此您无法返回上一步 — 如果您随后需要更改某些内容，请在向导关闭后对其进行编辑。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**&#x200B;选项卡。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 单击右上角的&#x200B;**[!UICONTROL Create]>[!UICONTROL Campaign]**。

1. 指定[营销活动设置](#campaign-settings)。

1. 单击&#x200B;**[!UICONTROL Next]**&#x200B;以保存营销活动设置。

1. 执行以下任一操作：

   * 如果不想为营销活动创建广告组，请单击&#x200B;**[!UICONTROL Close]**。

     >[!TIP]
     >
     >若要稍后创建广告组或广告，请参阅“[创建广告组](#ad-group-create)”或“[创建广告](#ad-create)”。

   * （可选）创建广告组：

     1. 指定[广告组设置](#ad-group-settings)。

     1. 单击&#x200B;**[!UICONTROL Next]**&#x200B;保存广告组设置。

     1. （可选）如果您不想为促销活动创建广告，请单击&#x200B;**[!UICONTROL Close]**。

   * （创建广告组后可选）创建广告：

     1. 指定[广告设置](#ad-settings)。

     1. 单击&#x200B;**[!UICONTROL Create ad]**。

### 编辑[!DNL ChatGPT Ads]对话式广告促销活动设置 {#campaign-edit}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左侧的子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. （如有必要）在数据表上方，单击&#x200B;**[!UICONTROL Campaigns]**&#x200B;选项卡。

1. 将光标悬停在行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

1. 编辑任何[促销活动设置](#campaign-settings)、[广告组设置](#ad-group-settings)和[广告设置](#ad-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

### [!DNL ChatGPT Ads]对话式广告营销活动设置 {#campaign-settings}

**[!UICONTROL Campaign name]：**&#x200B;营销活动的唯一名称。 名称必须至少包含三个字符。

**[!UICONTROL Campaign type]：** （只读） *Standard*&#x200B;是唯一可用的类型。

**[!UICONTROL Objective]：**&#x200B;促销活动要聚焦的量度： *达到*&#x200B;或&#x200B;*点击*。 目标确定促销活动广告组的竞价类型。

**[!UICONTROL Locations]：**（可选）要定位的一个或多个特定位置。 要定位所有位置，请将此设置留空。 要指定特定位置，请至少输入出现在名称中的任何位置的两个字母，然后单击搜索结果中的名称。

**[!UICONTROL Budget type]：** *每日预算*&#x200B;或&#x200B;*生命周期预算*。

**[!UICONTROL Budget]：**&#x200B;指定预算类型的预算。 该值必须大于零(0)。

**[!UICONTROL Start date]：**&#x200B;营销活动开始的日期，以帐户的时区表示。

**[!UICONTROL Set an end date]：**（可选）允许您指定营销活动的结束日期。 选择此选项时，请指定&#x200B;**[!UICONTROL End date]**。

## 广告组

### 为现有营销活动创建[!DNL ChatGPT Ads]广告组 {#ad-group-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**&#x200B;选项卡。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 单击右上角的&#x200B;**[!UICONTROL Create]>[!UICONTROL Ad Group]**。

1. 指定[广告组设置](#ad-group-settings)，包括父营销活动。

1. 单击&#x200B;**[!UICONTROL Create ad group]**。

## 编辑[!DNL ChatGPT Ads]广告组 {#ad-group-edit}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左侧的子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Ad Groups]**&#x200B;选项卡。

1. 将光标悬停在行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

1. 编辑[广告组](#ad-group-settings)设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

### [!DNL ChatGPT Ads]广告组设置 {#ad-group-settings}

**[!UICONTROL Parent campaign]：** （仅现有营销活动的广告组）广告组所属的营销活动。

**[!UICONTROL Ad group name]：**&#x200B;广告组的唯一名称。 名称必须至少包含三个字符。

**[!UICONTROL Maximum CPC bid]**&#x200B;或&#x200B;**[!UICONTROL Maximum CPM bid]：**&#x200B;每次点击或1,000次展示所支付的最大金额。 该值必须大于零(0)。 促销活动的目标确定竞价字段：*点击次数*&#x200B;促销活动显示&#x200B;**[!UICONTROL Maximum CPC bid]**，*覆盖范围*&#x200B;促销活动显示&#x200B;**[!UICONTROL Maximum CPM bid]**。

>[!TIP]
>
>出价越高，拍卖会就越多。

**[!UICONTROL Context hints]：** （可选）与您的产品或服务相关的对话、主题或关键字的说明。 这些提示可指导匹配，但不是完全匹配的定位规则。

## 广告

### 为现有广告组创建[!DNL ChatGPT Ads]聊天卡广告 {#ad-create}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**&#x200B;选项卡。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 单击右上角的&#x200B;**[!UICONTROL Create]>[!UICONTROL Ad]**。

1. 指定[广告设置](#ad-settings)，包括父营销活动和广告组。

1. 单击&#x200B;**[!UICONTROL Create ad]**。

## 编辑[!DNL ChatGPT Ads]聊天卡广告 {#ad-edit}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左侧的子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡。

1. 将光标悬停在行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

1. 编辑[ad](#ad-settings)设置。

1. 单击&#x200B;**[!UICONTROL Save]**。

### [!DNL ChatGPT Ads]聊天卡广告设置 {#ad-settings}

**[!UICONTROL Parent campaign]**&#x200B;和&#x200B;**[!UICONTROL Parent ad group]：** （仅现有广告组中的广告）广告所属的营销活动和广告组。

**[!UICONTROL Ad name]：**&#x200B;广告的唯一名称。 名称必须至少包含三个字符。

**[!UICONTROL Ad URL (Link)]：**&#x200B;登陆页面URL，以`http://`或`https://`开头。

**[!UICONTROL Title (headline)]：**&#x200B;广告标题。 标题必须为3至50个字符。 **注意：**&#x200B;在某些版面类型中，标题可能会被截断。

**[!UICONTROL Description]：**&#x200B;广告的正文文本。 描述必须介于3到100个字符之间。

**[!UICONTROL Ad image]：**&#x200B;要包含在广告中的JPG或PNG图像。 要上传图像，请单击（新广告） **[!UICONTROL Upload image (PNG/JPG)]**&#x200B;或&#x200B;**[!UICONTROL Change image]**，然后在您的设备或网络上查找并选择文件。

**[!UICONTROL Preview]：**&#x200B;基于广告设置的广告预览。

## 激活或暂停[!DNL ChatGPT Ads]营销活动、广告组或广告 {#pause-activate}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左侧的子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 在&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡上，查找行。

1. 在&#x200B;**[!UICONTROL Active]**&#x200B;列中，执行以下操作之一：

   * 要激活暂停的项目，请打开切换开关（位于右侧）。

   * 要暂停活动项目，请关闭切换开关（左侧）。

## 存档[!DNL ChatGPT Ads]营销活动、广告组或广告 {#archive}

存档将从[!UICONTROL Conversational Ads]视图中永久删除营销活动、广告组或广告。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在左侧的子菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 在右上角，选择一个广告商和一个[!DNL ChatGPT Ads]帐户。

1. 在&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡上，将光标悬停在行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Archive]**。

## 从[!DNL ChatGPT Ads]营销活动深入到广告组和广告 {#drill-down}

* 单击促销活动行以在&#x200B;**[!UICONTROL Ad Groups]**&#x200B;选项卡上仅查看其广告组，或单击广告组行以在&#x200B;**[!UICONTROL Ads]**&#x200B;选项卡上仅查看其广告。

要删除筛选器并查看视图中的所有行，请单击数据表上方筛选器中的&#x200B;**X**。

## 刷新营销活动、广告组或广告列表 {#refresh}

当其他用户可能已进行更改或添加时，重新显示促销活动、广告组或广告的列表。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**&#x200B;或&#x200B;**[!UICONTROL Ads]**&#x200B;视图中，单击数据表上方的&#x200B;**[!UICONTROL Refresh]**。

>[!MORELIKETHIS]
>
>* [管理对话式广告帐户](account-manage.md)

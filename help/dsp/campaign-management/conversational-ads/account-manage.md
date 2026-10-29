---
title: 管理[!DNL ChatGPT Ads]对话广告帐户
description: 了解如何为[!DNL ChatGPT Ads]聊天卡广告创建和管理帐户，这是一项Beta版功能，可在AI助理对话中放置广告。
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
source-wordcount: '898'
ht-degree: 0%
---
# 管理[!DNL ChatGPT Ads]对话广告帐户

*Beta功能*

通过Adobe DSP与[!DNL OpenAI Ads]的集成，您可以运行[!DNL ChatGPT Ads]聊天卡广告，这些广告显示在[!DNL ChatGPT]对话中。 对于此功能，DSP会创建一个对话式广告帐户，并代表贵组织购买媒体。 您将无法从ads.openai.com访问广告帐户。 使用此功能测试AI媒体，而不与[!DNL ChatGPT Ads]建立直接关系。

您将独立于结构不同的常规DSP促销活动管理[!DNL ChatGPT Ads]对话广告帐户，包括其促销活动、广告组和广告。 您还将与您的DSP促销活动分开[查看 [!DNL ChatGPT Ads] 促销活动、广告组和广告](campaign-manage.md#campaign-views-about)的效果数据。

## 资格

以下内容确定此功能是否适用：

* **现有[!DNL Search, Social, & Commerce]客户：**&#x200B;如果您的广告商已使用[!DNL Search, Social, & Commerce]，则[在Search、Social和Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)中而不是在DSP中创建和管理其 [!DNL ChatGPT Ads] 促销活动。

* **受限行业：**&#x200B;受限类别（例如，金融或医疗保健）中的广告商无法创建对话式广告帐户或营销活动。

如果所选广告商不合格，则[!UICONTROL Accounts]和[!UICONTROL Campaigns]选项卡将指明原因。 您仍然可以使用广告商选择器切换到其他广告商。

要使用该功能，请联系您的Adobe客户团队以开始载入流程。

## 计费

当月末使用其他发票时，使用您DSP帐户的计费货币和计费时区向您计费[!DNL ChatGPT Ads]（无论 [!DNL ChatGPT Ads] 帐户[&#128279;](#account-settings)使用的货币和时区如何）。 有关计费问题，请联系您的Adobe客户团队。

## [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts]视图 {#accounts-view}

[!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts]选项卡列出了选定广告商的[!DNL OpenAI]帐户。 每个帐户的信息包括：

**[!UICONTROL Status]：**&#x200B;帐户当前是否提供广告： *活动*&#x200B;或&#x200B;*已暂停*。 您无法更改帐户的状态；如果要暂停或重新激活帐户，请联系您的Adobe客户团队。

**[!UICONTROL Review status]：** [!DNL OpenAI]审阅状态：*正在审阅*、*已批准*&#x200B;或&#x200B;*已不批准*。 将光标悬停在状态上（如果可用）。

**[!UICONTROL Active campaigns]：**&#x200B;帐户中当前活动的营销活动数。

**[!UICONTROL Cost]：**&#x200B;帐户的总支出。

### 可用操作

* [查看帐户限制](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [创建帐户](#account-create)

* [编辑帐户](#account-edit)

* [刷新帐户列表](#account-refresh)

* [返回到DSP主菜单](#return-to-menu)

## 管理帐户

### 查看帐户限制 {#account-limits}

帐户限制可将帐户的总支出限制在特定日期范围内。 您可以查看帐户的限制，但只有您的Adobe帐户团队才能创建、编辑或删除限制。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Accounts]**&#x200B;视图中，将光标悬停在帐户行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL View account limit]**。

[!UICONTROL Account limits]页列出了帐户的每个限制：

**[!UICONTROL Name]：**&#x200B;限制的名称。

**[!UICONTROL Amount]：**&#x200B;限制期间的总支出上限。

**[!UICONTROL Period]：**&#x200B;限制适用的日期范围。

**[!UICONTROL Status]：** *活动*、*即将推出*&#x200B;或&#x200B;*已完成*。

**[!UICONTROL Spent]：**&#x200B;限制期内到目前为止的花费金额。

>[!NOTE]
>
>您无法编辑或删除已完成的限制，并且同一帐户的限制期间不能重叠。

### 创建[!DNL ChatGPT Ads]对话式广告帐户 {#account-create}

要为广告商创建两个[!DNL ChatGPT Ads]以上的帐户，请联系您的Adobe客户团队。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 执行以下操作之一：

   * （仅限您的第一个帐户）在欢迎屏幕上，单击&#x200B;**[!UICONTROL Create an Account]**。

   * 在&#x200B;**[!UICONTROL Accounts]**&#x200B;视图中，选择一个广告商，然后单击&#x200B;**[!UICONTROL Create Account]**。

1. 指定[帐户设置](#account-settings)。

1. 选中&#x200B;**[!UICONTROL I agree to the Terms and Conditions]**&#x200B;复选框。

1. 单击&#x200B;**[!UICONTROL Create account]**。

新帐户是在暂停状态下创建的，而[!DNL OpenAI]正在审核它们。 在帐户获得批准后，DSP会激活该帐户。

### 编辑[!DNL ChatGPT Ads]对话式广告帐户 {#account-edit}

在创建帐户后，您可以编辑该帐户的合法企业名称和网站。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Accounts]**&#x200B;视图中，将光标悬停在帐户行上并单击&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit account]**。

1. 编辑&#x200B;**[!UICONTROL Legal Business Name]**&#x200B;和/或&#x200B;**[!UICONTROL Advertiser Website]**。 有关这些字段的详细信息，请参阅“[帐户设置](#account-settings)”。

1. 单击&#x200B;**[!UICONTROL Save changes]**。

>[!IMPORTANT]
>
>保存更改将重新启动[!DNL OpenAI]的帐户审核。 在重新批准帐户之前，该帐户将不再提供广告。

### 刷新帐户列表 {#account-refresh}

当其他用户可能已进行更改或添加时，重新显示帐户列表。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Conversational Ads Beta]**。

1. 在&#x200B;**[!UICONTROL Accounts]**&#x200B;视图中，单击帐户列表上方的&#x200B;**[!UICONTROL Refresh]**。

### 返回到DSP主菜单 {#return-to-menu}

* 在主菜单上方，单击&#x200B;**[!UICONTROL Back to DSP]**。

### [!DNL ChatGPT Ads]对话广告帐户设置 {#account-settings}

**[!UICONTROL Legal Business Name]：**&#x200B;组织的注册业务名称。

**[!UICONTROL Advertiser Website]：**&#x200B;广告商网站的URL，以`http://`或`https://`开头。

**[!UICONTROL Country]：**&#x200B;组织合法注册的国家/地区（不是您运行广告的国家/地区）。 它必须与该组织DSP合同所使用的国家/地区相同。 保存帐户后，无法更改此值。

**[!UICONTROL Currency]：** （只读）您的Adobe帐户团队为[!DNL ChatGPT Ads]帐户设置的货币。 这可能与DSP帐户的货币不同，后者在DSP中的其他位置可见。 **注意：**&#x200B;无论此值如何，所有使用帐单都将采用用于DSP帐户的&#x200B;*记帐货币*。

**[!UICONTROL Timezone]：** （只读）您的Adobe帐户团队为[!DNL ChatGPT Ads]帐户设置的时区。 这可能与DSP帐户使用的时区不同，该时区在DSP中的其他位置可见。 **注意：**&#x200B;无论此值如何，所有使用帐单都将表示用于DSP帐户的&#x200B;*计费时区*。

**[!UICONTROL Favicon]：**&#x200B;用作帐户网站favicon的图像文件。<!-- How is this used within this context? --> 浏览器会在不同位置显示图标，例如地址栏、选项卡或书签。 文件必须是JPG、PNG或WEBP格式，并且至少为256x256像素。

要上传图标，请单击&#x200B;**[!UICONTROL Upload favicon]**，然后在您的设备或网络上查找并选择文件。

**[!UICONTROL I agree to the Terms and Conditions]：**&#x200B;一个复选框，表示您同意所有法律条款。 选中此复选框可创建帐户或更新帐户设置。

>[!MORELIKETHIS]
>
>* [管理对话式广告营销活动](campaign-manage.md)

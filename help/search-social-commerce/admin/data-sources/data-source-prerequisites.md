---
title: 配置的前提条件 [!DNL Google Analytics] 数据源
description: 了解在配置之前必须完成的步骤 [!DNL Google Analytics] 数据源。
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 配置的前提条件 [!DNL Google Analytics] 数据源

在您可以设置 [!DNL Google Analytics] 数据源，您必须将Search、Social和Commerce查询字符串参数“ef_id”设置为从中传递数据的主键 [!DNL Google Analytics] 搜索、社交和商务。 为每个设置主键 [!DNL Google Analytics] 要同步其数据的帐户和属性组合。 组织中的其他人可能需要完成这些任务；请参阅以下内容以了解更多信息。

如果您的广告或关键词的登陆页面URL尚未包含搜索、社交和商务重定向，请首先添加它们。

## 先决条件1：在登陆页面URL中为所有适用的广告帐户实施搜索、社交和商务令牌（“ef_id”查询字符串参数）

在每个付费搜索中，单击相关营销策划的 `ef_id` 必须生成并作为查询字符串附加到登陆页面URL，例如 `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`，其中 `&ef_id=abcde:123456789:s` 是附加符号， `ef_id` 键，和 `ef_id` 值。 要包含ef_id，相关广告网络帐户和营销活动必须具有 [!UICONTROL Tracking Type] ”[!UICONTROL EF Redirect]”和 [!UICONTROL Redirect Type] ”[!UICONTROL Token].”

对于现有帐户和营销活动，可能已经实施了ef_id。

如果不包含ef_id，请向您的Adobe帐户团队寻求帮助。

完成所有先决条件后， `ef_id` 用作从中传递数据的主键 [!DNL Google Analytics] 搜索、社交和商务。

## 先决条件2：在自定义维度中为每个相关捕获搜索、社交和商务令牌（“ef_id”查询字符串参数） [!DNL Google Analytics] 属性

对每个重复以下任务 [!DNL Google Analytics] 要为其同步数据的帐户和属性组合。 参见 [[!DNL Google Analytics] 有关创建和实施自定义维度的文档](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) 以获取这些任务的帮助。

1. In [!DNL Google Analytics]，创建一个名为“”的自定义维度`ef_id`“。 将维度的范围设置为 [!DNL User]，并将维度设置为活动。

   >[!NOTE]
   >
   >此先决条件要求具有相关属性的编辑权限。

1. 更新您的 [!DNL Google Analytics] 用于捕获ef_id查询字符串参数的值（当该参数存在于登陆页面URL中时）并将其存储在ef_id自定义维度中的跟踪代码。

   >[!NOTE]
   >
   >ef_id应仅在登陆页面URL中。

   例如，如果登陆页面URL为 `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`，则中的ef_id维度的值 [!DNL Google Analytics] 是 `abcde:123456789:s`.

   >[!NOTE]
   >
   >此先决条件应由符合条件的开发人员完成。

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置 [!DNL Google Analytics] 作为数据源查看](data-source-configure.md)
>* [编辑 [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停数据源同步](data-source-pause.md)
>* [重新验证 [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)

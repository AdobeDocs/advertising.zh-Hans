---
title: 配置 [!DNL Google Analytics] 数据源的先决条件
description: 了解在配置 [!DNL Google Analytics] 数据源之前必须完成的步骤。
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 配置[!DNL Google Analytics]数据源的先决条件

在设置[!DNL Google Analytics]数据源之前，必须将Search、Social和Commerce查询字符串参数“ef_id”设置为主键，以将数据从[!DNL Google Analytics]传递到Search、Social和Commerce。 为要同步数据的每个[!DNL Google Analytics]帐户和属性组合设置主键。 您组织中的其他人可能需要完成这些任务；请参阅以下内容以了解更多信息。

如果您的广告或关键词的登陆页面URL尚不包括Search、Social和Commerce重定向，请首先添加它们。

## 前提条件1：在所有适用的广告帐户的登陆页面URL中实施搜索、社交和Commerce令牌（“ef_id”查询字符串参数）

在相关营销活动的每次付费搜索单击中，必须生成唯一的`ef_id`并将其作为查询字符串附加到登陆页面URL中，例如`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`，其中`&ef_id=abcde:123456789:s`是附加符号、`ef_id`键和`ef_id`值。 要包含ef_id，相关广告网络帐户和营销活动必须具有[!UICONTROL Tracking Type]“[!UICONTROL EF Redirect]”和[!UICONTROL Redirect Type]“[!UICONTROL Token]”。

对于现有帐户和营销活动，可能已实施ef_id。

如果不包含ef_id，请向您的Adobe帐户团队寻求帮助。

完成所有先决条件后，`ef_id`将用作主键，以将数据从[!DNL Google Analytics]传递到Search、Social和Commerce。

## 先决条件2：在每个相关[!DNL Google Analytics]属性的自定义维度中捕获搜索、社交和Commerce令牌（“ef_id”查询字符串参数）

对要同步数据的每个[!DNL Google Analytics]帐户和属性组合重复以下任务。 有关这些任务的帮助，请参阅有关创建和实施自定义维度的[[!DNL Google Analytics] 文档](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article)。

1. 在[!DNL Google Analytics]中，创建名为“`ef_id`”的自定义维度。 将维度的范围设置为[!DNL User]，并将维度设置为活动。

   >[!NOTE]
   >
   >此先决条件需要相关属性的编辑权限。

1. 更新您的[!DNL Google Analytics]跟踪代码，以捕获登陆页面URL中存在的ef_id查询字符串参数的值，并将其存储在ef_id自定义维度中。

   >[!NOTE]
   >
   >ef_id应仅位于登陆页面URL中。

   例如，如果登陆页面URL为`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`，则[!DNL Google Analytics]中ef_id维度的值为`abcde:123456789:s`。

   >[!NOTE]
   >
   >此先决条件应由符合条件的开发人员完成。

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [将a [!DNL Google Analytics] 视图配置为数据源](data-source-configure.md)
>* [编辑a [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停同步数据源](data-source-pause.md)
>* [重新验证a [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 指标](data-source-ga-metrics.md)

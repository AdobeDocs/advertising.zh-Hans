---
title: 有关营销活动的常见问题解答
description: 查看有关营销活动管理和营销活动数据视图的问题的答案。
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 88b415fff52d623a5daeb00355bfe00054d5402b
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# 有关营销活动管理的常见问题解答

## 一般信息

+++我是否可以将营销活动和组件从一个帐户移动到另一个帐户？

请勿将具有唯一ID的营销活动或营销活动组件移动或复制到具有不同帐户ID的帐户。 这样做会导致数据错误。
+++

+++何时从广告网络更新点击数据？

从搜索引擎提取前一天点击数据的过程在广告商时区的06:00开始。

此外，在广告商所在时区的08[!DNL Google Ads]和16:00拉取了搜索网络上当天的:00个营销活动级绩效指标。
+++

+++哪些操作会导致关键词和广告丢失其历史记录？

>[!NOTE]
>
>（具有产品组合的广告商）在Search、Social和Commerce收集数据以为其创建模型时，期望新关键词和匹配类型组合的性能不稳定。

**在[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns]视图、批量处理工作表发布过程中以及广告网络自己的编辑器中执行的操作：**

在下列情况下，将删除现有关键字或广告并创建另一个关键字或广告：

* （[!DNL Baidu]、[!DNL Google Ads]和[!DNL Yandex]）编辑关键字名称。

* （[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yandex]）您更改关键字的匹配类型。

* 可在广告组之间移动关键字。

* （[!DNL Google Ads]个动态搜索广告、[!DNL Microsoft Advertising]个扩展文本广告以及其他支持的广告网络上的所有广告类型）编辑广告文案（标题/标题或描述）或广告图像。

* 您可以在广告组之间移动广告。

**产品库存馈送过帐过程中的事件：**

在以下情况下，将删除现有广告或关键字，并创建另一个广告或关键字：

* 馈送文件包含在广告变体中使用的列的新值。

* 自上次传播以来，广告的模板设置发生了更改。

* 新的馈送文件包含用于广告或关键字的行，其中a)位于上一个文件中，但b)自那时起已被忽略，并根据馈送数据设置暂停或删除。

根据[馈送数据设置](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)，在以下情况下可能会删除现有广告或关键字：

* 新的馈送文件不包含现有广告或关键字的行。

* 已发布的信息源文件的组件计划结束日期出现。

* 物料的库存水平降至信息源数据设置中指定的最低值以下。
+++

+++（[!DNL Google Ads]个营销活动）对我的[!DNL Google]跟踪的转化的显示名称所做的更改已恢复。

如果您在“搜索”、“社交”和“Commerce”中更改转化量度的显示名称，则所做的更改将被[!DNL Google Ads]中配置的名称覆盖。 在[!DNL Google Ads]中进行任何名称更改。
+++

+++(Google广告营销活动)是否可以为项目组合中的营销活动使用共享预算？

为了获得最佳结果，如果营销活动在配置为“[!DNL Google Ads]”的优化项目组合中，请勿将[!DNL Google Ads]营销活动添加到[!UICONTROL Auto adjust campaign budget limits]共享预算。 如果这样做，[!DNL Google Ads]将覆盖Search、Social和Commerce优化的活动预算，这可能导致竞价效率低下。
+++

+++（[!DNL Google Ads]个营销活动）我是否可以将移动用户和非移动用户发送到不同的登陆页面？

您可以使用[!DNL Google Ads] [!DNL ValueTrack]参数`{ifmobile}`和`{ifnotmobile}`，通过适用于您网站的两种方式之一来确定登陆页面的域名：

* 使用`{ifmobile:m}{ifnotmobile:www}`将移动设备指定为主机服务器。

  例如，`http://{ifmobile:m}{ifnotmobile:www}.example.com`将移动用户转到m.example.com ，将非移动用户转到www.example.com。

* 使用`{ifmobile:mobi}{ifnotmobile:com}`将移动设备指定为顶级域。

  例如，`http://www.example.{ifmobile:mobi}{ifnotmobile:com}`将移动用户转至www.example.mobi，将非移动用户转至www.example.com。

在这两种情况下，包含Search、Social和Commerce跟踪的基本URL都包含未编码的`{}`标记以及附加到基础URL的任何其他参数。

>[!NOTE]
>
>请勿使用完整URL作为ifnotmobile和ifmobile参数的值；请仅使用URL的变量部分（例如“m”与“www”或“mobi”与“com”）。

+++

+++（搜索网络上的[!DNL Google Ads]个营销活动）今天显示了哪些数据？

在广告商所在时区的08[!DNL Google Ads]和16:00拉取了搜索网络上当天的:00营销活动级别的绩效指标。

在[!UICONTROL Campaigns] > [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns]视图和[!UICONTROL Campaigns] > [!UICONTROL Optimization]视图的[!UICONTROL Portfolios]选项卡中，当您报告[!UICONTROL Today]或包含当天的自定义日期范围时，数据包含最近同步的数据。

>[!NOTE]
>
>点击、展示和转化数据会延迟三个小时，直到下一次数据提取才会完成。

+++

+++跟踪模板和登陆页面后缀之间有何区别？

仅对支持并行跟踪的广告网络使用登陆页面后缀。 在Search、Social和Commerce中，跟踪模板和登陆页面后缀都应包含来自广告网络的点击标识符，但跟踪模板应包含其他跟踪参数。

有关用户单击广告时如何加载跟踪模板和登陆页面后缀的详细信息，请参阅有关[并行跟踪支持](#parallel-tracking)的下一个常见问题解答。

+++

+++（[!DNL Google Ads]和[!DNL Microsoft Advertising]） Search、Social和Commerce是否支持[!DNL Google Ads]或[!DNL Microsoft Advertising]中广告的并行跟踪？{#parallel-tracking}

并行跟踪可将客户直接从您的广告发送到最终URL，其中可能包括来自最终URL后缀或“登陆页面后缀”的附加参数。 跟踪模板URL（包含用于点击测量的其他参数）将在后台单独加载；因此，登陆页面加载速度更快。

搜索、社交和Commerce支持使用广告网络的点击标识符（`msclkid`为[!DNL Microsoft Advertising]，`gclid`为[!DNL Google Ads]）并行跟踪搜索和购物营销活动。 使用[帐户级别](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings)或[促销活动级别](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix]（在广告网络中称为“[!DNL final URL suffix]”），将其附加到登陆页面URL以跟踪来自支持并行跟踪的浏览器的子广告点击量。 查看[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)必需后缀格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)必需后缀格式。

当用户在不支持并行跟踪的浏览器上查看您的广告时，广告网络而是使用顺序跟踪：客户首先被发送到您的跟踪模板URL，这会将客户重定向到中间跟踪服务器，然后再将他们重定向到最终URL（可能会在登陆页面后缀中包含其他参数）。 广告网络帐户的所有跟踪模板都应包含您在[!UICONTROL Landing Page Suffix]中使用的相同点击标识符参数。 查看[的 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)跟踪模板格式和[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)跟踪模板格式。
+++

+++为什么我的广告的跟踪URL包含&quot;`&EV_HASH={<hash>}`&quot;？

对于具有搜索、社交和Commerce像素重定向以及关键词和创意级别跟踪的帐户，当您使用[产品库存信息源](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)上传广告时，Search、Social和Commerce会将该哈希参数和值添加到广告的跟踪模板或目标URL，以识别它是使用库存信息源功能创建的。
+++

## 清单信息源

+++（产品库存信息源）我是否应该暂停或删除过时的广告，或者是否为库存水平低于指定最低值的产品广告？

这取决于广告商的业务要求。

当您暂停广告时，如果您重新提交相同的广告或库存水平高于最低值，则会重新激活广告。 这允许您保留广告的历史记录。

当您删除并重新提交广告时，将会创建新广告，并且需要为新广告累积历史数据。 但是，如果您不希望重新提交已删除的广告，则拥有历史数据并不重要。
+++

+++（产品库存信息源）如果我删除一个广告模板，然后创建一个新的相同模板，则下一个信息源文件中是否缺少项目（在将信息源文件设置配置为这样做时）？

如果下一个馈送文件缺少行项目，并且您之前未通过上一个馈送文件从新模板发布这些行项目，则缺少的行项目不会识别为“缺失”，因此不会创建它们。 要避免出现这种情况，请在传播新文件并发布新文件中的数据之前，通过新模板传播上一个信息源文件并发布数据。
+++

+++（产品库存信息源）我能否在不影响广告质量分数的情况下更新产品价格？

对于[!DNL Google Ads]营销活动，是： [!DNL Google Ads] `{Param 1}`和`{Param 2}`变量允许您在广告变量中动态插入数值，而不删除和重新创建广告，因此不会影响质量分数。

要为价格数据使用`{Param 1}`或`{Param 2}`变量，请将数据文件中的价格列映射到相应馈送模板中的该变量，然后将该变量包含在广告变量模板中。

例如，如果该列名为“Price”，则打开创建广告的信息源模板，单击&#x200B;**[!UICONTROL Param 1]**&#x200B;旁边的输入字段，然后单击&#x200B;**[!UICONTROL Price]**&#x200B;列表中的[!UICONTROL Feeds/Available Columns]列，该列将插入`[Price]`作为[!UICONTROL Param 1]的值。 然后，在馈送模板底部的广告变体模板中插入`{param1:default text}`，其中，“默认文本”是当馈送文件中的参数列对于广告行为空时要使用的文本。

在提交数据时，[!UICONTROL Param1]和[!UICONTROL Param2]列的数据字段最多可包含25个字符，包括数字数据、货币符号和货币代码以及以下非数字字符： `, . % + - /`
+++

+++从库存馈送生成的营销活动具有许多孤立交易记录。

如果[馈送数据设置](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)配置为在各种情况下删除广告，则点击广告后发生的任何延迟转化都可能会导致[孤立事务](/help/search-social-commerce/glossary.md#o-p)。 最佳实践是暂停广告而不是删除广告。 如果广告在很长时间后仍未收到任何收入，则您可以通过批量处理工作表或广告管理视图将其删除。
+++

## 与帐户和营销活动相关的性能问题

+++我的某些营销活动的支出或多或少于营销活动预算。

* 在配置了&quot;[!UICONTROL Auto adjust campaign budget limits]&quot;选项的优化产品组合中，这是正常的。 启用此选项后，每个营销活动的预算最多可支出&#x200B;*N*&#x200B;次，其中&#x200B;*N*&#x200B;是“[!UICONTROL Multiple]”设置的值。 此选项允许优化功能根据需要调整单个活动的支出，同时指导整个项目组合达到其目标。
* 如果[!DNL Google Ads]营销活动使用共享预算，则[!DNL Google Ads]会根据需要调整单个营销活动的支出，以支出整个共享预算。
+++

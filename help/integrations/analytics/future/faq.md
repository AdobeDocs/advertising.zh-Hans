---
title: 常见问题解答
description: xxx
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 常见问题解答xxx

## 标题

https://adobeadcloud.zendesk.com/agent/tickets/14214默认情况下，Adobe Analytics会在每个报表中报告所有捕获的事件。 &quot;[!UICONTROL Unspecified]”事件表示未连接到Adobe Advertising的表单完成事件。 例如，在广告平台报表中，电子邮件促销活动驱动的自然转化或转化将属于“未指定”。

您可以使用过滤器通过删除“包括未指定（无）”选项的复选标记从报表中删除未指定的事件。 <!-- Not sure if this is in DSP or in Analytics Workspace -->

## 标题

https://adobeadcloud.zendesk.com/agent/tickets/24323将Analytics事件标记放置在与Ad Cloud像素相同的位置，以确保XXX匹配。

## 标题

https://adobeadcloud.zendesk.com/agent/tickets/24323

问：在内部安全审核期间，当我们将Ad Cloud集成到现有的Adobe Analytics安装中时，某些功能被标记为已启用的安全隐患。

有问题的集成位于AdCloud和Adobe Audience Manager之间。 此功能提高了AdCloud与Adobe Audience Manager之间访客ID的匹配率。 为此，它会向pagead.l.doubleclick.net、star-mini.c10r.facebook.com和pug88000nf.pubmatic.com发送网络请求，以确定这些服务是否具有可以利用的访客的现有ID。 这些网络请求已标记为安全风险，正在所有网站访客中发生。

我们的审核人员要求我们禁用此功能。 如果我们阻止这些网络请求，会发生什么情况？

答：我们检查了产品，他们提到相关像素旨在提高Ad Cloud、特定库存/SSP合作伙伴(与DSP相关)和AAM之间的Cookie匹配率。  如果删除它们，客户可能会看到AAC/AAM与各自像素对应的库存合作伙伴之间的匹配率在一定程度上降低，但他们不会预期匹配率会很高。

对于Ad Cloud Search，我们确实看到为Mathworks设置了广告商的Experience Cloud组织ID，但我们的产品团队没有看到Mathworks设置来激活Ad Cloud中的受众。 您是否使用AdobeAudience Manager将受众发送至Ad Cloud Search？ 如果没有，删除这些项不会影响当前工作流。 如果您不希望触发这些像素，AAM客户关怀团队可以协助您移除这些像素。


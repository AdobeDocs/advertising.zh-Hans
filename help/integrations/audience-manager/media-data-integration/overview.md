---
title: 将DSP媒体曝光数据发送到Adobe Audience Manager的概述
description: 了解如何使用Audience Manager事件像素从Advertising DSP营销活动中捕获展示级别和点击级别的数据
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 将DSP媒体曝光数据发送到Adobe Audience Manager的概述

*仅使用Advertising DSP的广告商*

*仅集成Adobe Advertising-Adobe Audience Manager的广告商*

具有Adobe Audience Manager的Advertising DSP客户可以使用Audience Manager事件像素从DSP营销活动中捕获展示级别数据和点击级别数据。 事件像素将数据作为可操作信号发送到Audience Manager。 这些信号支持各种DSP用例，例如更高级的分段、频率管理、营销分析和报表见解。

DSP不会向您收取向Audience Manager发送这些信号的费用。 但是，根据Audience Manager合同，您会根据服务器调用支付标准的Audience Manager引入成本。 Audience Manager可删除通过两种不同方式跟踪的重复事件，以便每个事件只计费一次。

>[!NOTE]
>
> Audience Manager还支持从广告服务器日志文件捕获数据，这样提供的灵活性较低。 本文档未介绍该流程。

## 主要优势

* DSP campaign数据会实时流入Audience Manager，您可以使用该数据构建用于定义区段的基于规则的特征。

* 区段可在用户特征和区段鉴别后立即定位，从而支持实时定位工作。

* 您可以将促销活动数据用于各种用例，例如跨创意内容设置频率上限、重新定位曾接触过先前促销活动的用户，以及分析下游网站行为和入口点。

* 聚合数据提供了促销活动性能的统一视图，有助于识别自定义转化路径，并且可用于改进通过Audience Manager [!DNL Audience Optimization Reports]或通过与Adobe Analytics[[!DNL Audience Analytics] 的](/help/integrations/audience-manager/audience-analytics.md)集成导致转化的事件序列。

## 如何跟踪数据

Audience Manager展示和点击事件像素基于Cookie。 像素不会捕获在没有Cookie的环境中发生的事件，例如移动应用程序和连接的电视(CTV)。<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### 展示跟踪像素

当您向广告附加1xl像素透明事件跟踪像素时，Audience Manager会跟踪广告的展示数据。 每次将广告提供给用户并由Web浏览器加载时，都会加载事件像素。 像素从特定于Audience Manager的旧域[`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)的客户端子域加载，并包含键值对形式的参数。 该事件调用会收集展示和转化数据，并将其发送到Audience Manager数据收集服务器。

### 点击跟踪像素

Audience Manager跟踪点击次数的方式与跟踪展示次数类似，不同之处在于，它不会在每次投放广告时加载透明事件像素。 相反，会在广告的点进URL中跟踪点击数据。 广告指向[`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)的特定于客户端的子域，该子域是Audience Manager的旧域，可供Audience Manager数据收集服务器处理。 然后，服务器将用户重定向到预期的登陆页面。 URL包含作为键值对的参数。

>[!NOTE]
>
>如果您的组织使用[!DNL Analytics]跟踪，则您可能不需要Audience Manager点击跟踪。 Adobe Analytics可捕获点击信号，并可通过[服务器端转发](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)将其发送到Audience Manager。

>[!MORELIKETHIS]
>
>* [从Advertising DSP营销活动中收集点击和展示数据](collect.md)
>* [用例](use-cases.md)

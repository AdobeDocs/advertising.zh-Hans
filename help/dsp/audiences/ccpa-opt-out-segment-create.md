---
title: 创建和实施CCPA选择退出销售区段
description: 了解如何创建并实施区段，以跟踪消费者选择退出销售请求中的用户ID。
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# 创建和实施CCPA选择退出销售区段

您可以创建一个区段，以根据《加州消费者隐私法案》(CCPA)跟踪您网站上消费者选择退出销售请求的用户ID。 用户无限期地停留在CCPA选择退出销售区段中。

实施区段像素标记后，Adobe Advertising即开始代表广告商收集ID池。

>[!NOTE]
>
>* 有关如何使用Adobe Experience Platform Privacy Service API向Adobe Advertising传达CCPA选择退出销售请求的信息，请参阅 [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* 要跟踪访问网页的用户（这些用户访问网页的目的与跟踪CCPA选择退出销售事件无关）以及接触到台式机、移动设备和CTV设备广告的用户，请创建 [自定义区段](/help/dsp/audiences/custom-segment-create.md).

1. 创建区段：

   1. 在主菜单中，单击 **受众>区段**.

   1. 在数据表的上方，单击 **[!UICONTROL Create]**.

   1. 输入唯一值 **[!UICONTROL Segment Name]**.

      建议的区段名称：“&lt;”*您的广告商名称*> - CCPA选择退出销售”（如“Acme - CCPA选择退出销售”）

   1. 对于 [!UICONTROL Segment Type]，选择 **[!UICONTROL CCPA Opt-out of sale]**.

   1. 单击 **[!UICONTROL Save]**.

1. 复制并实施像素标记以跟踪区段：

   1. 返回到 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 在区段行中，将光标悬停在新区段上并单击 **[!UICONTROL Get pixel]**.

   1. 复制图像像素(以 `<img src="https://rtd-tm.everesttech.net"`)以收集网页中桌面和移动设备访客的用户ID。

   1. 将标记提供给广告商或网站联系人，以使用公司用于跟踪CCPA选择退出销售请求的机制进行部署（例如使用同意管理平台）。

      广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

      在实施像素后，Adobe Advertising即开始代表广告商收集ID池。

      尽管实施选择和逻辑取决于广告商，但广告商如何触发像素的示例如下：

      1. 消费者登陆广告商的主页。
      1. 消费者找到并点击广告商的“CCPA选择退出销售”按钮。
      1. 向消费者呈现广告商与之合作的服务提供商的列表。
      1. 消费者勾选方框，选择不向Adobe Advertising出售数据。

         此操作会触发像素触发并收集指定&#39;&#39;内消费者的Cookie ID[!UICONTROL CCPA Opt-out of sale]”区段。

>[!MORELIKETHIS]
>
>* [Adobe Advertising对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表](ccpa-opt-out-about.md)
>* [检索消费者选择退出销售报表](ccpa-opt-out-segment-report-retrieve.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [关于受众管理](audience-about.md)

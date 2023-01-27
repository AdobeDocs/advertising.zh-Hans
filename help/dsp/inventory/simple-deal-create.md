---
title: 创建 [!UICONTROL Simple Ad Serving] 交易
description: 了解如何为 [!UICONTROL Simple Ad Serving] 交易。
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 创建 [!UICONTROL Simple Ad Serving] 交易

1. 在主菜单中，单击 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. 在数据表上方，单击 **[!UICONTROL Create]**，然后选择 **[!UICONTROL Simple Ad Serving]**.

1. 输入 [交易设置](simple-deal-settings.md):

   1. 在 [!UICONTROL Select Ad Source] 部分，指定有关发布者、广告商和营销活动以及广告类型的信息，然后单击 **[!UICONTROL Next]**.

   1. 在 [!UICONTROL Select Ad(s)] 部分，指定要用作DSP代理的广告：

      1. 执行以下任一操作：

         * 对于现有广告，请选择要使用的广告。

         * 对于新广告，请创建代理 [第三方广告](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP不提供您指定的广告。 发布者提供广告。

      1. 单击 **[!UICONTROL Next]**.
   1. 在馈送详细信息中，编辑馈送详细信息，然后单击 **[!UICONTROL Next]**.

      DSP会自动生成名为“SAS放置 — &lt;*交易名称*>，”。 在版面中，交易会在 [!UICONTROL Inventory Targets] 中。 所有其他定位选项均不适用。



1. 将事件跟踪像素发送到发布者，以通过以下任一方式实施：

   * （可选）从 [!UICONTROL Activate Tag with Publisher] 屏幕中，将交易标记发送到发布者。

      完成上述步骤后，DSP会生成一封电子邮件，您可以将其发送给发布者。 该消息包括交易详细信息、用于检索交易标记的链接以及该链接的授权代码。

      1. 查看交易详细信息，然后执行以下任一操作：

         * 要将信息粘贴到设备上电子邮件应用程序的电子邮件中，请单击 **[!UICONTROL Email & Done]** 并选择电子邮件应用程序。 的 [!UICONTROL CC:] 字段中预填充了 [!DNL Adobe] 支持地址。 然后，您可以将消息发送给发布者的相应联系人。

         * 要将信息复制到剪贴板，请单击 **[!UICONTROL Copy Email].** 然后，您可以手动将内容粘贴到电子邮件中，并将其发送给发布者的相应联系人。 您必须在 `publisher-support-global@adobe.com`. 复制完消息后，单击 **[!UICONTROL Email & Done]**.
      1. （如有必要）跟进发布者，查看标记是否包含相应的宏，以便标记可与发布者的广告服务器配合使用。
   * （可选）将事件跟踪像素手动发送给发布者：

      1. 在 [!UICONTROL Deals] 查看，单击 ![“选项”菜单](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         事件像素包括 [!UICONTROL Clickthrough] 像素和 [!UICONTROL Impression] 像素。 视频和音频广告还包括按四分位数(从 [!UICONTROL 25% Complete] to [!UICONTROL 100% Complete])。

      1. 复制事件跟踪像素并将其提供给您的发布者。



>[!MORELIKETHIS]
>
>* [关于 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] 设置](simple-deal-settings.md)
>* [查看交易的详细报表](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->

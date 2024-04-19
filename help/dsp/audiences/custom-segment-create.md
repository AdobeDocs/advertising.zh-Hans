---
title: 创建和实施自定义区段
description: 了解如何创建和实施自定义区段以跟踪向广告公开的用户或访问您网页的用户。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 9fc4c123fb682bbc2aee0ae72931c63d31f020be
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# 创建和实施自定义区段

您可以通过创建和实施自定义DSP区段来收集您自己的第一方受众数据。 您可以使用区段跟踪a)从桌面和移动设备向广告展示的用户以及b)访问特定网页的用户。 之后，您可以使用其他广告重新定位区段中的用户，或阻止区段中的用户接收其他广告。

>[!NOTE]
>
>要根据加州消费者隐私法案(CCPA)在网站上跟踪消费者选择退出销售请求的用户ID，请创建 [CCPA选择退出销售区段](ccpa-opt-out-segment-create.md).

## 跟踪ID5 ID的区段的先决条件

*Beta版功能*

* 在生成区段以跟踪与ID5 ID关联的用户之前，您必须使用签署协议 [!DNL ID5] 并获取您组织的合作伙伴ID。 有关说明，请联系您的Adobe客户团队。

* 要在Adobe Analytics中进行测量，您必须：

   1. 全部完成 [实施的先决条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 和 [跟踪URL中的AMO ID和EF ID](/help/integrations/analytics/ids.md).

   1. 将以下参数添加到您网页中的之前或内部 [需要JavaScript代码才能使用 [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)  — 初始化最后一个事件服务之前的任意位置。

      `window.id5PartnerId=Your_ID5_PartnerID;`

      示例：

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

## 创建和实施自定义区段

1. 创建区段：

   1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 在数据表的上方，单击 **[!UICONTROL Create]**.

   1. 输入唯一值 **[!UICONTROL Segment Name]**.

   1. 对于 **[!UICONTROL Segment Type]**，选择 *[!UICONTROL Custom]*.

   1. 输入 **[!UICONTROL Lookback Window]**，即用户的Cookie在区段中保留的天数。

      默认窗口为45天。 输入一个介于1 (1)到365之间的值。

   1. 单击 **[!UICONTROL Advanced]** 要展开高级设置，然后选择区段标记将跟踪的用户标识符类型：

      * *[!UICONTROL Cookies]：* （默认）区段标记将跟踪Cookie。

      * [!UICONTROL Universal IDs (Beta)]：

         * *[!UICONTROL ID5]：* 将跟踪区段标记 [!DNL ID5] ID。 对于传送到通用ID的展示，不产生任何费用。

        **[!UICONTROL Terms of Service]：** 使用通用ID的服务协议条款。 您或DSP帐户中的其他用户必须接受一次这些条款，然后才能将通用ID用于新ID类型。 对于签订托管服务合同的客户，您的Adobe客户团队将代表贵组织获得您的同意并接受相关条款。 要阅读术语，请单击 **>**. 要接受条款，请滚动到条款的底部并单击 **[!UICONTROL Accept]**.

   1. 单击 **[!UICONTROL Save]**.

1. 根据需要复制并实施标记以跟踪区段：

   1. 返回到 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. 将光标悬停在区段行上并单击 **[!UICONTROL Get Pixel]**.

      * 要跟踪网页的桌面和移动设备访客，请执行以下操作：

         1. 复制标记为“ ”的页面查看跟踪标记[!UICONTROL Desktop or mobile websites]“

         1. 将标记提供给广告商或网站联系人以进行部署。

            广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

      * 要在桌面或移动设备上跟踪向广告单元公开的用户，请执行以下操作：

         1. 复制标记为的展示跟踪标记&quot;[!UICONTROL Desktop or mobile ads]“

   1. (用于跟踪的区段的标记 [!DNL ID5] 网页的桌面和移动设备访客的ID)在复制的标记中，替换 `ID5_PARTNER_ID` 合作伙伴ID为 [!DNL ID5] 已分配给您的组织。

   例如，如果您的ID5合作伙伴ID为 `abcde` 生成的区段标记为

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   然后替换 `ID5_PARTNER_ID` 替换为 `abcde` ，获取以下信息：

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   您的组织在与签署协议时收到了合作伙伴ID [!DNL ID5]. 如果您不知道自己的合作伙伴ID，请与您的Adobe客户团队联系。

   标记无需执行此步骤即可进行跟踪 [!DNL ID5] 在桌面或移动设备上向广告单元公开的用户的ID。

1. 将标记添加到 [!UICONTROL Pixel] 选项卡，或者转到 [!UICONTROL Event Pixels] 的部分 [[!UICONTROL Tracking] 每个相关投放位置的设置](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

实施跟踪标记后，您可以在受众目标或排除项中将该区段用于任何投放位置。

>[!TIP]
>
>在跟踪用户时跟踪区段大小。

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [编辑区段信息](segment-edit.md)
>* [删除区段](segment-delete.md)
>* [查看区段的跟踪像素](segment-view-pixels.md)
>* [共享或停止共享区段](segment-share.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [可用的第三方数据提供商](third-party-data-providers.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)

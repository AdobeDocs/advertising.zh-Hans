---
title: 管理重定位像素
description: 了解如何创建和实施重新定位像素以用作广告体验的目标。
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: ed3bf0200d3d3b31ef80c790c4e702914459c521
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# 管理重定位像素

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

您可以创建一个重定位像素，以识别使用用户Cookie或通用ID访问广告商登陆页面或转化页面的访客。 像素可跟踪访客在页面上执行的最新事件，并捕获页面正在跟踪这些访客的特定属性。 创建像素后，生成像素标记以插入到相关网页中以开始跟踪访客。<!-- Note to self: surfer id=cookie or universal ID -->

然后，您可以在广告体验中将像素用作任何创意内容的目标，以便仅向具有指定属性的用户显示广告，这些用户之前访问了与该像素关联的网页。 例如，如果网页跟踪这些属性值，则您可以定位那些查看大小为10的红鞋的访客。<!-- better example? Make sure they match attribute examples below -->体验级别目标与DSP的定位选项一起应用；层次结构定位行为可能因DSP而异。

重新定位用户档案会存储180天。

示例像素：

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative]仅支持Advertising DSP的通用ID。
>* 您还可以将来自Adobe Audience Manager和Adobe Analytics的第一方受众用作您的体验的[创意目标](/help/creative/experiences/experience-settings-targeting.md)。
>* 在Advertising DSP投放位置中使用体验作为广告时，您可以将投放位置定向到DSP中所有可供您使用的受众。 您还可以[创建自定义受众区段标记](/help/dsp/audiences/custom-segment-create.md)以跟踪特定登陆页面的所有访客，然后将这些区段用作投放的创意目标。 Advertising DSP对投放级别定位应用广告级别定位，而不是（代替）投放级别定位。
>* 选择退出跟踪以进行广告定位的网站访客不会根据受众区段或重新定位用户档案接收带有个性化创意内容的广告。

## 创建重定位像素

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 在数据表上方单击&#x200B;**[!UICONTROL Creative]**，然后选择> **[!UICONTROL Retargeting Pixel]**。

1. 指定[重定位像素设置](#retargeting-pixel-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. [生成像素标记](#retargeting-pixel-generate)以提供给广告商或网站联系人。

   重新定位像素标记必须是页面上的最后一个操作。<!-- verify here and below -->

   广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

## 编辑重定位像素

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 将光标悬停在像素名称上并单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[重定位像素设置](#retargeting-pixel-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. [生成要提供给广告商或网站联系人的像素标记](#retargeting-pixel-generate)，以便他们能够替换原始标记。

   重定向像素标记必须是登陆页面上的最后一个操作。

   广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

## 为重定位像素生成标记 {#retargeting-pixel-generate}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 将光标悬停在像素名称上并单击&#x200B;**[!UICONTROL Generate Tag]**。

1. 单击&#x200B;**[!UICONTROL Copy to Clipboard]**&#x200B;以将标记复制到计算机的剪贴板，您可以将文本粘贴到文件中进行保存。

1. 在像素标记中，通过将“`<img src>`”替换为值，为`<script src>`和`Insert <attribute>`部分中的每个属性指定一个值。 如果标记捕获通用ID，请指定ID5合作伙伴ID。

   如果手动添加其他属性，请包括URL编码。

   例如，如果您包含属性“category”、“color”和“size”并捕获ID5通用ID，则像素标记将包含以下参数： `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--`和`&id5pid=--Insert ID5_PARTNER_ID--`。 若要定位大小为10的红凉鞋用户，请将图像标记和脚本标记中的参数更改为`&ut1=sandals&ut2=red&ut3=10`，并在脚本标记中输入ID5合作伙伴ID，如`&id5pid=0123456789`。

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. 将已完成的像素标记以及要插入该标记的相关登陆页面的列表提供给广告商或网站联系人。

   重定向像素标记必须是登陆页面上的最后一个操作。

   广告商的IT部门或其他组可能需要计划标记部署或通知标记部署。

## 删除重定位像素

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**。

1. 将光标悬停在像素名称上并单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## 重新定位像素设置 {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]：**&#x200B;像素的名称。 **注意：**&#x200B;像素标记包含像素ID (`pxId=<ID>`)，而不是像素名称。

**[!UICONTROL Advertiser]：** （现有像素为只读）跟踪像素的广告商。

**[!UICONTROL Attribute 1]：**&#x200B;要包含在像素标记中的属性，如“SKU”、“类别”、“大小”或页面或页面上显示的产品的其他属性。 在将像素标签插入相关网页之前，请在像素标签中指定该属性的值。

当您将广告体验定位到展示给像素的用户时，定位设置会指定显示创意时必须显示的属性值。

**[!UICONTROL Attribute 2]**、**[!UICONTROL Attribute 3]**、**[!UICONTROL Attribute 4]**、**[!UICONTROL Attribute 5]：**（可选）要包含在像素标记中的其他属性。 在将像素标记插入相关网页之前，请为像素标记中的每个其他属性指定一个值。

当您将广告体验定位到展示给像素的用户时，定位设置会指定显示创意时必须显示的属性值。

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]：** （仅限新像素；可选）要跟踪的像素标记的通用ID类型：

* *[!UICONTROL ID5]：*&#x200B;像素标记跟踪[!DNL ID5] ID。 对于传送到通用ID的展示，不产生任何费用。

* *[!UICONTROL Ramp ID]：*&#x200B;像素标记跟踪[!DNL Ramp IDs]。 对于传送到通用ID的展示，不产生任何费用。

要使用此功能，您或DSP帐户中的其他用户必须接受服务协议条款中关于使用通用ID一次，然后才能将通用ID用于新ID类型。 对于签订托管服务合同的客户，您的Adobe客户团队将代表贵组织获得您的同意并接受条款。 若要阅读术语，请单击&#x200B;**[!UICONTROL Terms of Service]**。 要接受条款，请滚动到条款的底部并单击&#x200B;**[!UICONTROL Accept]**。

>[!MORELIKETHIS]
>
>* [目标广告体验设置](/help/creative/experiences/experience-settings-targeting.md)
>* [关于广告体验](/help/creative/experiences/experience-about.md)

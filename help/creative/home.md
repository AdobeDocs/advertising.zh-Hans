---
title: Advertising Creative 2.0的新增功能
description: 了解Adobe Advertising Creative 2.0中的最新更新和新增功能。
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
exl-id: 0d25f665-b5f9-4d27-851a-2a456fe2cbf8
source-git-commit: 9f537200eb66b5e7e0b6f98d6f4eb0ba3d316b09
workflow-type: tm+mt
source-wordcount: '788'
ht-degree: 0%

---

# [!DNL Creative] 2.0中有哪些不同之处？

*已关闭的测试版*

<!-- The following features are new or recently changed. -->

| 日期 | 功能 | 描述 | 了解更多信息 |
| ---- | ------- | ----------- | -------------------- |
| 2025年7月10日 | 视频创意 | 现在支持第一方视频创作人员以及特定于视频的捆绑包和体验：<ul><li>您现在可以上传第一方视频创意，并将其添加到视频特定的包。 在包设置中，“[!UICONTROL Bundle Type]”选项现在包括[!UICONTROL Standard Display]、[!UICONTROL Dynamic Display]和[!UICONTROL Standard Video]。</li><li>您可以创建特定于视频的广告体验，并包含视频包。 广告体验设置现在包括“[!UICONTROL Ad Type]”设置，其中包含[!UICONTROL Standard Display]、[!UICONTROL Dynamic Display]和[!UICONTROL Video]选项。 您可以根据点进率、完成率或自定义目标优化视频广告。</li><li>视频广告体验标记的标记由视频持续时间和比特率定义，而不是由广告大小定义。</li><li>视频广告会自动转码为Adobe Advertising DSP编码，以便您进行预览。 您可以选择将特定于DSP的转码应用于[!UICONTROL Tag Manager]中的任何广告体验标记。</li></ul> | 请参阅“[关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)”、“[管理创意包](/help/creative/creative-libraries/bundle-manage.md)”、“[目标体验设置](/help/creative/experiences/experience-settings-targeting.md)”、“[非目标体验设置](/help/creative/experiences/experience-settings-no-targeting.md)”和“[自定义视频广告体验标记的转码选项](/help/creative/experiences/experience-tag-video-transcoding.md)”。 |
| 2025年5月21日 | [!UICONTROL Creative Libraries] | 您现在可以将图像从Adobe Experience Manager资源库添加到[!UICONTROL Creative Libraries]，以便在广告体验中使用这些图像。 | 请参阅&quot;[配置对Adobe Experience Manager图像资源的访问权限](/help/creative/creative-libraries/aem-assets-configure.md)&quot;和&quot;[将标准创意添加到创意库](/help/creative/creative-libraries/creative-add-standard.md)&quot;。 |
| 2025年2月10日 | [!UICONTROL Creative Libraries] | 之前，您有一个创意库。 现在，您可以为每个广告商创建多个库。 | 请参阅“[关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)”。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | [!UICONTROL Creatives]视图包含[!UICONTROL Standard Ads]和[!UICONTROL Dynamic Ads]的选项卡。<ul><li>**[!UICONTROL Standard Ads]选项卡**&#x200B;允许您上传和管理图像、HTML5、灵活的HTML5和第三方创意。</li><li>**[!UICONTROL Dynamic Ads]**&#x200B;选项卡允许您管理使用定义的广告模板从上传的信息源文件创建的动态生成的广告；以前，动态广告是在[!DNL Adobe Advertising Dynamic Creative Optimization (DCO)]内生成的。<br><br>目前，您可以预览、复制和删除动态广告。 您还可以将动态广告附加到针对性广告体验的创意捆绑包中，或附加到非针对性体验的广告标记中。 只有管理员用户可以动态生成广告。</li></ul> | 请参阅“[关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)”。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | 将多个创意分组到一个&#x200B;*捆绑*&#x200B;中，以便轻松将它们添加到体验中。 您可以创建标准广告包，并将标准创意附加到该广告包。 同样，您可以创建动态广告包，并将动态创意附加到这些广告包。 | 请参阅&quot;[管理Creative包](/help/creative/creative-libraries/bundle-manage.md)&quot;。 |
| | [!UICONTROL Experiences] | 在新的广告体验设置中，您现在指定体验是否使用决策树定位，并且保存体验后无法更改设置。 具有决策树定位的体验和未具有决策树定位的体验的工作流不同。 | 请参阅“[创建具有定位的体验](/help/creative/experiences/experience-create-targeting.md)”和“[创建无定位的体验](/help/creative/experiences/experience-create-no-targeting.md)”。 |
| | [!UICONTROL Experiences] | 现在，您只能通过单个创意库中的创意捆绑包来创建有针对性的体验，而不能通过单独的创意来创建。 您仍然可以将单个库中的单个创意内容附加到非定向体验，而无需使用决策树定位。<br><br>由于结构变化，您的旧体验将在今年晚些时候弃用。 | 自助服务客户：在新用户界面中重建您的体验。 请参阅“[创建具有定位](/help/creative/experiences/experience-create-targeting.md)的体验”。<br><br>托管服务客户：您的Adobe帐户团队将在新用户界面中重新构建您的体验。 |
| | [!UICONTROL Experiences] | 使用Advertising DSP的广告商可以选择将标记作为广告直接上传到Advertising DSP促销活动。 | 请参阅&quot;[为实时体验导出和实施广告体验标记](/help/creative/experiences/experience-tag-export.md)&quot; |
| | DCO体验 | 旧版DCO体验将在今年晚些时候弃用。 您的Adobe客户团队将在[!DNL Creative]中重新构建DCO体验作为动态广告，但具有其他定位的DCO体验将重新构建为[!DNL Creative]体验。 | — |
| | 广告标记 | 广告服务器端点将更改为Advertising DSP广告服务器。<br><br>新广告标记包括用于传递通用ID的其他参数（除Cookie ID之外）。 | 自助客户：在[!DNL Creative]中提供体验后，替换现有营销活动中的广告标记。 请参阅&quot;[为实时体验](/help/creative/experiences/experience-tag-export.md)导出和实施广告体验标记。&quot;<br><br>托管服务客户：您的Adobe客户团队将替换现有营销活动中的广告标记。 |
| | 正在重新定位像素 | 重定位像素端点将更改为Adobe Advertising UDB服务。<br><br>除了Cookie ID之外，新像素还包含用于传递通用ID的其他参数。 | 自助服务客户：创建新的重定向像素并将其添加到您的网页。 请参阅“[管理重定位像素](/help/creative/pixels/retargeting-pixel-manage.md)”。<br><br>托管服务客户：如果适用，您的Adobe客户团队将创建并共享新的重定位像素；将新像素添加到您的网页。 |
| | 转换像素 | 旧版DCO像素将在今年晚些时候弃用，需要[!DNL Adobe]转换像素。 | 自助服务客户：具有[!DNL Analytics for Advertising]的客户必须将DCO转换像素替换为[!DNL Analytics for Advertising] [!DNL Last Event Service]像素和Adobe Analytics像素。 其他所有人都必须将DCO转换像素替换为Adobe Advertising转换像素。<br><br>托管服务客户：您的Adobe客户团队将创建并共享所有适用的Adobe Advertising转换像素；将您的DCO转换像素替换为Adobe Advertising转换像素。 |

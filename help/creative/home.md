---
title: Advertising Creative2.0的新增功能
description: 了解Adobe Advertising Creative2.0中的最新更新和新增功能。
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
source-git-commit: 561846c1a909620df198498aca8db8868bbf5fbe
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# [!DNL Creative] 2.0中有哪些不同之处？

*已关闭的测试版*

<!-- The following features are new or recently changed. -->

| 日期 | 功能 | 描述 | 了解更多信息 |
| ---- | ------- | ----------- | -------------------- |
| 2025年2月10日 | [!UICONTROL Creative Libraries] | 之前，您有一个创意库。 现在，您可以为每个广告商创建多个库。 | 请参阅“[关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)”。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | [!UICONTROL Creatives]视图包含[!UICONTROL Standard Ads]和[!UICONTROL Dynamic Ads]的选项卡。<ul><lu>**[!UICONTROL Standard Ads]选项卡**&#x200B;允许您上传和管理图像、HTML5、灵活HTML5和第三方创意。</li><li>**[!UICONTROL Dynamic Ads]**&#x200B;选项卡允许您管理使用定义的广告模板从上载的源文件创建的动态生成的广告；动态广告生成以前在[!DNL Adobe Advertising Dynamic Creative Optimization (DCO)]内完成。<br><br>目前，您可以预览、复制和删除动态广告，并将动态广告附加到针对性广告体验的创意捆绑包或附加到非针对性体验的广告标记。 只有管理员用户可以创建动态生成的广告。</li></ul> | 请参阅“[关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)”。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | 将多个创意分组到一个&#x200B;*捆绑*&#x200B;中，以便轻松将它们添加到体验中。 您可以创建标准广告包，并将标准创意附加到该广告包。 同样，您可以创建动态广告包，并将动态创意附加到这些广告包。 | 请参阅&quot;[管理创意包](/help/creative/creative-libraries/bundle-manage.md)&quot;。 |
| | [!UICONTROL Experiences] | 在广告体验设置中，您现在指定体验是否使用决策树定位。 具有决策树定位的体验和不具有此定位的体验的工作流是不同的。 | 请参阅“具有决策树定位的体验的工作流”和“没有决策树定位的体验的工作流”。 |
| | [!UICONTROL Experiences] | 现在，您只能通过单个创意库中的创意捆绑包来创建有针对性的体验，而不能通过单独的创意来创建。 您仍然可以将单个库中的单个创意内容附加到非定向体验，而无需使用决策树定位。<br><br>由于结构变化，您的旧体验将在今年晚些时候弃用。 | 自助服务客户：在新用户界面中重建您的体验。 请参阅“[创建具有定位](/help/creative/experiences/experience-create-targeting.md)的体验”。<br><br>托管服务客户：您的Adobe帐户团队将在新用户界面中重新构建您的体验。 |
| | [!UICONTROL Experiences] | 使用Advertising DSP的广告商可以选择将标记作为广告直接上传到Advertising DSP促销活动。 | 请参阅&quot;[为实时体验导出和实施广告体验标记](/help/creative/experiences/experience-tag-export.md)&quot; |
| | DCO体验 | 旧版DCO体验将在今年晚些时候弃用。 您的Adobe客户团队将在[!DNL Creative]中重新构建DCO体验作为动态广告，但具有其他定位的DCO体验将重新构建为[!DNL Creative]体验。 | — |
| | 广告标记 | 广告服务器端点将更改为Advertising DSP广告服务器。<br><br>广告标记将包含用于传递通用ID的其他参数（除Cookie ID之外）。 | 自助客户：在[!DNL Creative]中提供体验后，替换现有营销活动中的广告标记。 请参阅&quot;[为实时体验](/help/creative/experiences/experience-tag-export.md)导出和实施广告体验标记。&quot;<br><br>托管服务客户：您的Adobe客户团队将替换现有营销活动中的广告标记。 |
| | 正在重新定位像素 | 重定位像素端点将更改为Adobe AdvertisingUDB服务。<br><br>除了Cookie ID之外，新像素还将包含用于传递通用ID的其他参数。 | 自助服务客户：创建新的重定向像素并将其添加到您的网页。 请参阅“[管理重定位像素](/help/creative/pixels/retargeting-pixel-manage.md)”。<br><br>托管服务客户：您的Adobe帐户团队将创建并共享新的重定位像素（如果适用）；将新像素添加到您的网页。 |
| | 转换像素 | 旧版DCO像素将在今年晚些时候弃用，需要[!DNL Adobe]转换像素。 | 自助服务客户：具有[!DNL Analytics for Advertising]的客户必须将DCO转换像素替换为[!DNL Analytics for Advertising] [!DNL Last Event Service]像素和Adobe Analytics像素。 其他所有人都必须将DCO转换像素替换为Adobe Advertising转换像素。<br><br>托管服务客户：您的Adobe客户团队将创建并共享所有适用的Adobe Advertising转换像素；将您的DCO转换像素替换为Adobe Advertising转换像素。 |

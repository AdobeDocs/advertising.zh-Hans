---
title: 从馈送生成的数据的状态
description: 了解从清单数据馈送生成的数据的状态。
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 从馈送生成的数据的状态

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

每个组件都可以具有以下状态之一：

* *[!UICONTROL New]：*&#x200B;该组件在广告网络上不存在，并且未发布到广告网络，如有必要，您仍然可以通过单击组件名称来编辑其设置。 准备好发布数据时，请单击&#x200B;**[!UICONTROL Post to SE]**&#x200B;并指定要提交的数据。

* *[!UICONTROL Posted]：* （仅限营销活动和广告组）营销活动或广告组已部分发布到广告网络，但由于错误，某些组件未发布。 每个关键词和广告的验证状态会显示哪些信息需要更正。 您可以根据需要通过单击组件名称来编辑组件设置。

* *[!UICONTROL Active]：*&#x200B;该组件已在广告网络上处于活动状态，您无法在此处编辑其设置。 活动组件可能包含[!UICONTROL New]的子组件，如果数据有效，则可以发布这些子组件。

* *[!UICONTROL Paused]：*&#x200B;该组件已在广告网络上暂停，您无法在此处编辑其设置。 暂停的组件可能包括[!UICONTROL New]的子组件，如果数据有效，则可以发布这些子组件。

* *[!UICONTROL Deleted]：*&#x200B;该组件已在广告网络上删除，您无法在此处编辑其设置。 已删除的组件可能包含[!UICONTROL New]的子组件，如果数据有效，则可以发布这些子组件。

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)

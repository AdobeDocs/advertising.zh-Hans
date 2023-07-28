---
title: 从馈送生成的数据的状态
description: 了解从清单数据馈送生成的数据的状态。
exl-id: 8e5e7649-a16b-4634-896a-7c216185b367
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 从馈送生成的数据的状态

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

每个组件都可以具有以下状态之一：

* *[!UICONTROL New]：* 该组件在广告网络上不存在，并且未发布到广告网络，如有必要，您仍然可以通过单击组件名称来编辑其设置。 准备好发布数据后，单击 **[!UICONTROL Post to SE]** 并指定要提交的数据。

* *[!UICONTROL Posted]：* （仅限营销活动和广告组）营销活动或广告组已部分发布到广告网络，但由于错误，某些组件未发布。 每个关键词和广告的验证状态会显示哪些信息需要更正。 您可以根据需要通过单击组件名称来编辑组件设置。

* *[!UICONTROL Active]：* 该组件已在广告网络上处于活动状态，您无法在此处编辑其设置。 活动组件可能包括以下子组件 [!UICONTROL New]，在数据有效时可发布。

* *[!UICONTROL Paused]：* 该组件已在广告网络上暂停，您无法在此处编辑其设置。 暂停的组件可能包括 [!UICONTROL New]，在数据有效时可发布。

* *[!UICONTROL Deleted]：* 该组件已在广告网络上删除，您无法在此处编辑其设置。 已删除的组件可能包括 [!UICONTROL New]，在数据有效时可发布。

>[!MORELIKETHIS]
>
>* [关于清单信息源](inventory-feeds-about.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [从馈送生成的将营销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)

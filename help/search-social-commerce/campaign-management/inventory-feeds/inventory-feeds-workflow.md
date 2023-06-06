---
title: 关于使用库存信息源自动化广告管理
description: 了解根据产品或服务库存相关数据自动管理帐户结构和投放动态广告的工作流。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 使用清单信息源管理营销活动数据的工作流

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

最初，请至少测试一个信息源文件或帐户，然后您可以完全自动化该过程，或继续在每一步对其进行控制：

1. （可选）请联系您的Adobe客户团队以设置用于存放数据文件的FTP目录。

   如果您使用FTP目录，则信息源服务每两小时检查一次新文件。

   否则，您可以手动上传文件 [!UICONTROL Advanced (ACM)] 视图。

1. 设置 [用于处理馈送数据的参数](feed-settings-manage.md#feed-data-settings).

   如果您使用的是FTP，开始时请勿自动将数据发布到广告网络。 验证第一个文件的输出并对结果满意后，可以更改设置。

1. 将数据文件上传到FTP目录， [手动上传数据文件](feed-files-manage.md) 在 [!UICONTROL Advanced (ACM) view]，或 [启用对Google或Microsoft®商家中心帐户的访问权限](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

要手动上传文件，您可以等到创建使用数据文件的模板时再上传。

1. （可选）创建组 [修饰符](modifiers-manage.md) 在馈送数据模板的各种数据字段中用作变量。

1. [创建一个或多个模板](ad-templates/ad-template-manage.md) 使用数据列为特定广告网络帐户创建促销活动、广告组、关键字和/或广告副本。

1. [通过模板传播馈送数据](feed-data-propagate.md)，用文件或帐户中的数据替换模板中的列名称。 根据模板选项，搜索、Social和Commerce可以使用默认设置为广告创建新帐户结构（促销活动、广告组、关键词），或将广告映射到现有帐户结构。

1. （可选） [预览输出](propagated-data-view.md) 在 [!UICONTROL Advanced (ACM)] 查看数据，并（可选）查看上数据更改的摘要 [!UICONTROL Propagations] 选项卡。

1. [发布数据](propagated-data-post.md) 至相关广告网络帐户。

1. （如果使用FTP或商户中心帐户上传数据；可选）验证第一个馈送文件的输出后， [编辑参数](feed-settings-manage.md#feed-data-settings) 以通过关联的模板自动传播后续数据，并将其发布到相关广告网络。

1. （当您有新数据文件时）如有必要，请上传新文件，通过模板传播数据，然后将数据发布到相关广告网络。 您可以选择在一个步骤中传播和发布数据。

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动化广告管理](inventory-feeds-about.md)
>* [清单信息源何时创建或删除帐户组件？](when-are-components-created-deleted.md)


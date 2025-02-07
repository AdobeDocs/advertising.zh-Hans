---
title: 术语表
description: 请参阅关键术语的定义。
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# 术语表 {#glossary}

*已关闭的测试版*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**点进：**&#x200B;导致转化的广告点击。

**数据传递目标：**&#x200B;数据传递目标允许根据DSP、发布者或合作伙伴实时提供的数据选择广告元素。 这可能包括第三方数据。

<!-- verify this -->在广告体验中，每个数据传递目标最多可包含五个键值对；您可以在该级别的第一个目标节点中指定键和至少一个值，并且相同的键可用于同级目标节点。 每个键值对都将作为宏附加到此体验的广告标记中。 在广告展示时，DSP、发布者或合作伙伴负责将值替换为该展示专属的数据。 此信息将传递回[!DNL Creative]，以便根据体验中定义的规则显示相应的广告体验。

例如，要将一个或多个可能的创意定位到女性且位于区段1234中的查看者，您需要为目标节点配置数据传递目标`gender=female`和`segment=1234`。 为展示提供服务的DSP会使用性别和区段信息填充标记，并且符合指定要求的访客将显示为关联的创意内容之一。

**参与直达：**&#x200B;导致转化的广告参与（例如观看视频或展开广告）。

<!-- or flexible html5 creative variation? -->
**弹性HTML5创意的变体：**&#x200B;在[!UICONTROL Creative Libraries]中派生出弹性HTML5创意资源，在将创意分配给体验并更改体验中的任何默认属性时生成该派生项。

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**显示到达：**&#x200B;广告展示次数或展示次数字符串，用户无需单击广告即可进行转化。

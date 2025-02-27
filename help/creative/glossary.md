---
title: 术语表
description: 请参阅关键术语的定义。
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
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

**接洽：**&#x200B;导致转化的广告接洽（例如，滚动轮播广告或展开广告）。 此类事件与单击广告以访问登陆页面或登陆页面上的事件是分开的。

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**显示到达：**&#x200B;广告展示次数或展示次数字符串，用户无需单击广告即可进行转化。

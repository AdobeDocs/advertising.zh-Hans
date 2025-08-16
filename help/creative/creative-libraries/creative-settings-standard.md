---
title: Creative设置
description: 了解xxxx。
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '2100'
ht-degree: 0%

---

# Creative设置

这些设置因创意类型而异。

当您同时编辑多个创意时：

* 您可以同时或单独编辑每个创意内容的设置。 默认情况下，您选择的所有创意都处于选中状态，并且您指定的任何设置都适用于所有选定的创意。 要编辑特定创意的设置，请在编辑字段之前取消选择每个不适用的创意内容；如有必要，请对其他创意内容重复此操作。

* 某些设置将应用于所有选定的创意。

## 灵活的HTML5创意设置 {#creative-settings-flexible-html5}

### “详细信息”选项卡

**Creative名称：**&#x200B;创意的名称。 默认情况下使用模板名称或上传的文件名，但您可以更改名称。 对于多个创意，您可以编辑单个创意名称。 **提示：**&#x200B;在创意名称中包含广告大小，然后使用在体验中包含创意时可以轻松找到的名称。

**语言：**&#x200B;与创意内容关联的每个广告的默认语言。 上传或编辑多个创意时，相同的值将应用于每个选定的创意。

**Creative大小：**（现有创意为只读）创意的尺寸。 如果创意内容中包含的任何图像大于指定的大小，则会相应地调整其大小。

**[!UICONTROL Click Tags]：**&#x200B;允许从包含的横幅广告进行点击跟踪重定向的变量。 变量名称和相应的登陆页面URL会从上传的创意单元中填充，但您可以更改默认URL。 对于多个创意，您可以编辑单个点击标记。

<!-- I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**标签：**（可选）要应用于所有选定创意的任何标签。 您可以在[!DNL Creative]内的各种视图中按标签筛选创意，并在[!UICONTROL Creative Label]中包含[!UICONTROL Custom Creative Report]维度。

* 要选择现有标签，请单击![向下](/help/creative/assets/chevron-down.png "向下")，然后选中要应用的每个标签旁边的复选框。

* 要搜索现有标签，请在标签名称中开始输入文本字符串。

* 若要创建新的标签以应用于创意，请打开列表，单击&#x200B;**+添加标签**，在[!UICONTROL Label]字段中输入新的标签名称，然后单击&#x200B;**创建**。

* 要移除标签，请取消选中标签名称旁边的复选框。

### “属性”选项卡

**\[所有适用于创意的默认内容属性\]：**&#x200B;默认属性名称和值由灵活的创意单元填充，但您可以选择更改这些值。

>[!NOTE]
>
>将创意包含在体验中时，您还可以将任何创意属性的默认值替换为自定义值。 编辑体验中的属性会创建父创意内容的变体。

有关预定义模板中可用属性的信息，请参阅“[可用的灵活创意模板](#flexible-creative-templates-available)”。

### “模板”选项卡

*仅限现有创意*

面向创意人员的灵活HTML5模板文件。

您可以选择使用新模板替换现有模板，新模板具有与原始模板不同的布局，但属性名称集相同。 新模板必须为ZIP格式，最大为2 MB。 当创意位于捆绑包中时，使用该捆绑包的所有体验随后都会使用新模板中的布局。

当您更新具有子变体的父创意内容模板时，变体会随模板布局的任何更改而更新，但变体的属性值不会更改。

要替换现有的广告模板，请执行以下操作：

1. 单击&#x200B;**更新模板**。

1. 单击&#x200B;**继续**。

1. 通过以下任一方式指定ZIP文件：

   * 将文件拖放到设备或网络上的框中。

   * 单击&#x200B;**[!UICONTROL select a file]**&#x200B;在您的设备或网络上查找该文件。

   查看[灵活的广告规范](#flexible-ad-spec)。

1. 根据需要编辑新的[灵活HTML广告设置](#flexible-ad-settings)。

1. 单击&#x200B;**[!UICONTROL Edit]**

## HTML5创意设置 {#creative-settings-html5}

## “详细信息”选项卡

对于新创意，以下设置不在指定选项卡上。

**Creative名称：**&#x200B;创意的名称。 对于新创意，默认使用文件名，但您可以更改名称。 对于多个创意，您可以编辑单个创意名称。 **提示：**&#x200B;在创意名称中包含广告大小，然后使用在体验中包含创意时可以轻松找到的名称。

**语言：**&#x200B;与创意内容关联的每个广告的默认语言。 上传或编辑多个创意时，相同的值将应用于每个选定的创意。

**Creative大小：**（现有创意为只读）创意的尺寸。 如果创意内容中包含的任何图像大于指定的大小，则会相应地调整其大小。

**[!UICONTROL Click Tags]：** (仅限静态HTML5创意)允许从包含的横幅广告进行点击跟踪重定向的变量。 变量名称和相应的登陆页面URL会从上传的创意单元中填充，但您可以更改默认URL。 对于多个创意，您可以编辑单个点击标记。

>[!NOTE]
>
>将创意包含在体验中时，您可以将任何点击标记的默认值替换为自定义登陆页面URL，以生成基本创意的派生。

**登陆页面URL：**(仅带有一个登陆页面的简单HTML5创意)您与创意人员关联的每个广告的默认登陆页面URL。 它必须是以http://或https://开头的有效URL。 它可能包含第三方跟踪参数或[[!DNL Creative] 宏](/help/creative/creative-macros.md)供您自行使用。

在捆绑包中包含创意并将捆绑包分配给体验时，您可以选择更改登陆页面URL，并为捆绑包中的每个创意添加展示和点击跟踪URL以及JavaScript 。<!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**标签：**（可选）要应用于所有选定创意的任何标签。 您可以在[!DNL Creative]内的各种视图中按标签筛选创意。

* 要选择现有标签，请单击![向下](/help/creative/assets/chevron-down.png "向下")，然后选中要应用的每个标签旁边的复选框。

* 要搜索现有标签，请在标签名称中开始输入文本字符串。

* 若要创建新的标签以应用于创意，请打开列表，单击&#x200B;**+添加标签**，在[!UICONTROL Label]字段中输入新的标签名称，然后单击&#x200B;**创建**。

* 要移除标签，请取消选中标签名称旁边的复选框。

### “模板”选项卡

*仅限现有的静态HTML5创意*

创意的HTML5模板文件。

您可以选择使用新模板替换现有模板，新模板具有与原始模板不同的布局，但属性名称集相同。 新模板必须为ZIP格式，最大为2 MB。 当创意位于捆绑包中时，使用该捆绑包的所有体验随后都会使用新模板中的布局。

当您更新具有子变体的父创意内容模板时，变体会随模板布局的任何更改而更新，但变体的属性值不会更改。

要替换现有的广告模板，请执行以下操作：

1. 单击&#x200B;**更新模板**。

1. 单击&#x200B;**继续**。

1. 通过以下任一方式指定ZIP文件：

   * 将文件拖放到设备或网络上的框中。

   * 单击&#x200B;**[!UICONTROL select a file]**&#x200B;在您的设备或网络上查找该文件。

   请参阅[HTML广告规范](html5-creative-specification.md)。

1. 根据需要编辑新的[HTML5广告设置](#creative-settings-html5)。

1. 单击&#x200B;**[!UICONTROL Edit]**

## 图像创意设置 {#creative-settings-image}

**Creative名称：**&#x200B;创意的名称。 对于新创意，默认使用文件名，但您可以更改名称。 对于多个图像，您可以编辑单个创意名称。 **提示：**&#x200B;使用在体验中包含创意内容时可以轻松找到的名称。

**语言：**&#x200B;与创意内容关联的每个广告的默认语言。 相同的值将应用于所有选定的图像。 将创意包含到体验中时，您可以选择自定义体验的语言偏好设置。

**Creative大小：**（只读）上传图像的尺寸。

**登陆页面URL：**&#x200B;与创意内容关联的每个广告的默认登陆页面URL。 登陆页面URL必须是以http://或https://开头的有效URL。 它可能包含第三方跟踪参数或[[!DNL Creative] 宏](/help/creative/creative-macros.md)供您自行使用。 相同的值将应用于所有选定的图像。

如果您在捆绑包中包含某个创意，然后将该捆绑包分配给某个体验，则可以选择更改登陆页面URL，并为捆绑包中的每个创意添加展示和点击跟踪URL以及JavaScript 。<!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**标签：**（可选）要应用于所有选定创意的任何标签。 您可以在[!DNL Creative]内的各种视图中按标签筛选创意。

* 要选择现有标签，请单击![向下](/help/creative/assets/chevron-down.png "向下")，然后选中要应用的每个标签旁边的复选框。

* 要搜索现有标签，请在标签名称中开始输入文本字符串。

* 若要创建新的标签以应用于创意，请打开列表，单击&#x200B;**+添加标签**，在[!UICONTROL Label]字段中输入新的标签名称，然后单击&#x200B;**创建**。

* 要移除标签，请取消选中标签名称旁边的复选框。

## 第三方创意设置 {#creative-settings-third-party}

**JavaScriptCode：**&#x200B;指向第三方广告服务器上的创意的JavaScript标记(以及可选的不支持JavaScript的浏览器的替代标记)。 脚本可能因广告服务器而异。 编辑多个创意时，相同的值将应用于每个选定的创意。

所有[可用的宏](/help/creative/creative-macros.md)及其替代数据都列在输入字段的下方。 若要在标记中插入一个宏，请将光标悬停在宏描述上，单击![复制到剪贴板](/help/creative/assets/copy-to-clipboard.png "复制到剪贴板")，然后将图像粘贴到标记中所需的位置。

当您将此创意包含在DSP中作为广告实施的体验中时，DSP会使用此标记中的信息来显示广告并跟踪其展示次数和点击次数。 然后，DSP将标记推送到广告交换。 显示和单击广告后，广告服务器、DSP和[!DNL Creative]将跟踪这些事件。

**[!UICONTROL Advertiser]：** （只读）可用库的广告商。

**Creative名称：**&#x200B;创意的名称。 **提示：**&#x200B;使用在体验中包含创意内容时可以轻松找到的名称。

**Creative大小：**（现有广告为只读）创意的尺寸。 对于新创意，请从标准广告大小列表中进行选择。

**语言：**&#x200B;与创意内容关联的每个广告的默认语言。

**登陆页面URL：**&#x200B;用于验证与创意内容关联的每个广告的登陆页面URL。 第三方广告服务器确定每个广告的实际登陆页面。

**标签：**（可选）要应用于所有选定创意的任何标签。 您可以在[!DNL Creative]内的各种视图中按标签筛选创意。

* 要选择现有标签，请单击![向下](/help/creative/assets/chevron-down.png "向下")，然后选中要应用的每个标签旁边的复选框。

* 要搜索现有标签，请在标签名称中开始输入文本字符串。

* 若要创建新的标签以应用于创意，请打开列表，单击&#x200B;**+添加标签**，在[!UICONTROL Label]字段中输入新的标签名称，然后单击&#x200B;**创建**。

* 要移除标签，请取消选中标签名称旁边的复选框。

## 视频创作设置 {#creative-settings-video}

**Creative资源名称：**&#x200B;创意的名称。 对于新创意，默认使用文件名，但您可以更改名称。 对于多个图像，您可以编辑单个创意名称。 **提示：**&#x200B;使用在体验中包含创意内容时可以轻松找到的名称。

**持续时间：**（只读）自动填充的视频持续时间。

**语言：**&#x200B;与创意内容关联的每个广告的默认语言。 相同的值将应用于所有选定的图像。 将创意包含到体验中时，您可以选择自定义体验的语言偏好设置。

**登陆页面URL：**&#x200B;与创意内容关联的每个广告的默认登陆页面URL。 登陆页面URL必须是以http://或https://开头的有效URL。 它可能包含第三方跟踪参数或[[!DNL Creative] 宏](/help/creative/creative-macros.md)供您自行使用。 相同的值将应用于所有选定的图像。

如果您在捆绑包中包含某个创意，然后将该捆绑包分配给某个体验，则可以选择更改登陆页面URL，并为捆绑包中的每个创意添加展示和点击跟踪URL以及JavaScript 。<!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**标签：**（可选）要应用于所有选定创意的任何标签。 您可以在[!DNL Creative]内的各种视图中按标签筛选创意。

* 要选择现有标签，请单击![向下](/help/creative/assets/chevron-down.png "向下")，然后选中要应用的每个标签旁边的复选框。

* 要搜索现有标签，请在标签名称中开始输入文本字符串。

* 若要创建新的标签以应用于创意，请打开列表，单击&#x200B;**+添加标签**，在[!UICONTROL Label]字段中输入新的标签名称，然后单击&#x200B;**创建**。

* 要移除标签，请取消选中标签名称旁边的复选框。

>[!MORELIKETHIS]
>
>* [将标准创意添加到创意库](/help/creative/creative-libraries/creative-add-standard.md)
>* [编辑标准创意](/help/creative/creative-libraries/creative-edit-standard.md)
>* [可用于跟踪URL的宏](/help/creative/creative-macros.md)

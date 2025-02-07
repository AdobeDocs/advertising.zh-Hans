---
title: 目标体验设置
description: 请参阅针对性广告体验的所有设置的描述。
feature: Creative Experiences
source-git-commit: fbf663b38282f48facab57efaf5533892642a252
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---

# 目标广告体验设置

*已关闭的测试版*

## [!UICONTROL Experience basics]节

**[!UICONTROL Advertiser]：** （现有体验为只读）将对体验中包含的创意和目标组合进行竞价的广告商。 保存体验后，便无法更改广告商。

**[!UICONTROL Experience Name]：**&#x200B;体验的唯一名称。 **提示：**&#x200B;在Advertising DSP或其他DSP中将体验用作广告时，请使用容易找到的名称。

**[!UICONTROL Creative Library]：** （现有体验为只读）用于该体验的单个创意库。 保存体验后，便无法更改库。

## [!UICONTROL Default creatives]节

**\[指定的默认创意\]：**&#x200B;当浏览器无法显示分配给体验的创意(例如，浏览器未启用JavaScript或广告服务器由于延迟而无法个性化广告)时要使用的默认图像创意。 每个广告大小包含一个图像创意，体验适用于该图像创意。 您的选择决定了可用于体验的创意大小。<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. This feels a little wonky in that there isn't a distinct/obvious "Creative Sizes" setting to reference. -->

对于具有决策树定位的体验，您可以使用决策树中包含相同大小的创意的创意捆绑包覆盖默认创意内容。<!-- verify -->

* 要添加具有不同维度的默认创意，请单击&#x200B;**[!UICONTROL + Add Sizes]**，从右侧窗格中选中要添加的每个创意旁边的复选框，然后单击&#x200B;**[!UICONTROL Add Creatives]**。

* 要删除默认创意，请将光标悬停在创意缩略图上，然后单击![删除](/help/creative/assets/delete.png "删除")。

* 要删除所有默认创意，请单击![删除](/help/creative/assets/delete.png "删除") **[!UICONTROL Delete all]**。

* 若要显示或隐藏右侧的创意窗格，请单击右窗格右上角的![显示/隐藏](/help/creative/assets/hide-show-creatives.png "显示/隐藏")。

## [!UICONTROL Targeting]节

**[!UICONTROL Targeting]：** （现有体验为只读）启用使用决策树和自动标记创建的创意定位。 保存体验后，便无法更改此设置。

**[!UICONTROL Dynamic ads]：** （现有体验为只读）指示体验包含动态广告。 **注意：**&#x200B;体验可以包含所有标准广告或所有动态广告。 保存体验后，便无法更改此设置。

**[!UICONTROL Language Targeting]：** （仅具有标准广告的体验；可选；现有体验为只读）检查用户的浏览器语言设置，并在可以使用指定语言的创意内容时，使用该语言显示创意内容。 当浏览器指定语言的创意不可用时，将改用[!UICONTROL Preferred language]设置。

保存体验后，便无法更改此设置。

**[!UICONTROL Preferred language]：** （仅具有标准广告的体验；现有体验为只读）从体验创建的所有广告的语言，启用[!UICONTROL Language Targeting]时除外。 保存体验后，便无法更改此设置。

## [!UICONTROL Advanced]节

**数据传递：**（现有体验为只读；可选）根据DSP、发布者或合作伙伴在展示时实时传递的特定键值对定位用户。 您最多可以指定五个数据传递键（参数）。 在决策树中设置定位时，您可以包含一个级别的数据传递目标节点，并指定每个节点的目标值。 如果您在创建体验时没有在此字段中指定键，则仍可以在决策树中指定键。<!-- May move this to just within the decision tree.  -->

每个键都会作为广告体验中的宏附加
标记，您可以生成该标记以在DSP中作为广告实施。

**Radius：** （仅限具有动态广告的体验；可选）要定位的用户半径。 选择从0英里到200英里的半径。<!-- Affect within the decision tree? -->

**RT像素：** （现有体验为只读；可选）将像素重定位到潜在目标的[!UICONTROL Creative]。 在决策树中设置定位时，可以包含一级RT像素目标节点，并为每个节点指定要定位的像素，以及像素属性必须存在的所需值，以便在分配的创意捆绑包中显示创意。 如果在创建体验时没有在此字段中指定像素，则仍可以在决策树中指定像素。<!-- May move this to just within the decision tree. -->

**标签：** <!-- should be "Labels" -->（可选）要应用于体验的任何[!DNL Creative]特定的标签。 您可以在体验<!-- sic -->视图中按标签筛选体验。

* 要选择现有标签，请单击![向下](/help/creative/assets/chevron-down.png "向下")，然后选中要应用的每个标签旁边的复选框。

* 要搜索现有标签，请在标签名称中开始输入文本字符串。

* 若要创建要应用的新标签，请打开列表，单击“**+添加标签”**，在[!UICONTROL Label]字段中输入新标签名称，然后单击“**创建”**。

* 要移除标签，请取消选中标签名称旁边的复选框。

**展示跟踪URL：**（可选）要附加到从体验创建的任何广告的登陆页面URL的第三方展示跟踪URL。 您最多可以包含五个URL。 要添加其他URL，请单击![图标](/help/creative/assets/create.png) **[!UICONTROL Add More]并输入该URL。

输入URL后，页面下方会列出所有可用的宏及其替代数据。 要在URL中插入一个宏，请将光标悬停在宏描述上，单击![复制到剪贴板](/help/creative/assets/copy-to-clipboard.png "复制到剪贴板")，然后将宏粘贴到URL字段中所需的位置。

>[!NOTE]
>
>* [!DNL Creative]会自动将其自己的展示跟踪标记作为登陆页面URL的前缀。
>* 您可以[为体验](experience-tracking-urls-targeting.md)中的任何创意覆盖此URL。
>* 您还可以在[!UICONTROL Client JS]字段中输入第三方JavaScript展示跟踪代码

**点击跟踪URL：**（可选）（可选）要附加到登陆页面URL的第三方点击跟踪URL。 您最多可以包含五个URL。 要添加其他URL，请单击![图标](/help/creative/assets/create.png) **[!UICONTROL Add More]并输入该URL。

输入URL后，页面下方会列出所有可用的宏及其替代数据。 要在URL中插入一个宏，请将光标悬停在宏描述上，单击![复制到剪贴板](/help/creative/assets/copy-to-clipboard.png "复制到剪贴板")，然后将宏粘贴到URL字段中所需的位置。

>[!NOTE]
>
>* [!DNL Creative]会自动将其自己的展示跟踪标记作为登陆页面URL的前缀。
>* 您可以[为体验](experience-tracking-urls-targeting.md)中的任何创意覆盖此URL。

**客户端JS：**（可选）以下任意一项：

* （当广告商使用OBA合规供应商处理广告时）JavaScript代码指向广告叠加，允许用户选择退出在线行为定位(OBA)。

* 要附加到登陆页面的任何第三方JavaScript展示跟踪代码。 **注意：**&#x200B;您还可以在[!UICONTROL Impression Tracking URL]字段中输入第三方展示跟踪URL。

>[!MORELIKETHIS]
>
>* [使用决策树定位创建体验](experience-create-targeting.md)
>* [使用决策树定位编辑体验](experience-edit-targeting.md)

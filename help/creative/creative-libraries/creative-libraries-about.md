---
title: 关于您的创意库
description: 了解如何管理广告体验的创意。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 677596e41944de7782c520496f6751f03bf5d9a2
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# 关于您的创意库

*封闭测试版功能*

您的创意库允许您管理将在广告体验中使用的创意。 您可以创建多个库，每个库都包含一组创意和&#x200B;*创意包*，这些创意包是您可以作为一个单元添加到体验中的创意组。

您的库可以包括：

* **个人创意：**&#x200B;您可以直接在广告体验中包含没有定义用户目标的个人创意。 您还可以使用创意内容创建包，这些包可以包含在定向的[广告体验](/help/creative/experiences/experience-about.md)中。

   * **标准创意：**&#x200B;您可以上传和管理[各种格式的创意](#creative-creative-formats)。 对于每个创意，您可以指定与创意关联的每个广告的默认语言、用户单击包含创意的广告时打开的默认登陆页面，以及在[!DNL Creative]内的各种视图内用作过滤器的可选标签。

   * **动态创意：** (仅限现有Adobe Advertising DCO客户)管理员用户可以通过将广告模板中的动态变量映射到信息源文件中的值来创建动态生成的创意。 所有用户都可以预览、复制和删除现有的动态广告。

* **创意捆绑：**&#x200B;将创意分组到捆绑中，以在具有已定义用户目标的多个体验中使用。 您可以创建包含标准广告的&#x200B;*标准包*&#x200B;和包含动态生成的广告的&#x200B;*动态包*。

## 支持的Creative格式 {#creative-creative-formats}

### 标准创意内容的格式

您可以在[支持的创意大小](creative-sizes.md)中添加和管理以下创意类型。

>[!IMPORTANT]
>
>即使您打算将HTML5、弹性HTML5或第三方创意用于广告体验，您也必须为您使用的每个创意大小添加图像创意。
>
>每个体验都需要为分配给该体验的每个创意大小提供一个默认图像创意。 当浏览器未启用JavaScript或广告服务器由于延迟而无法个性化广告时，可以使用默认图像创意。

#### 灵活的HTML5

灵活的HTML5创意人员是HTML5创意人员，其所有图像和其他属性均作为标准HTML标记，您可以直接在[!DNL Creative]中、创意库或单个体验（这会创建原始创意内容的变体）中编辑这些内容。 在DSP中，灵活的HTML5创意适用于单个特定广告大小（以像素为单位）。 您可以选择更改在灵活的HTML5创作实例中指定的属性的默认值。 稍后，您可以为特定体验中的属性指定自定义值，这会创建父级创意内容的变体。

<!-- Removed:

Flexible HTML5 creatives are HTML5 creatives with all of their images and other attributes as standard HTML tags, which you can edit directly within [!DNL Creative], either within a creative library or within an individual experience (which creates a variation of the original creative). Flexible HTML5 creatives use the Interactive Advertising Bureau (IAB) Technology Laboratory's standard for an [ad portfolio](https://flexibleads.iabtechlab.com/), for which ad format sizes are flexible (rather than fixed) and are based on the ad’s aspect ratio and size range, and for which ads maintain their resolution across devices and publisher sites. You can optionally change the default values of the attributes specified in a flexible HTML5 creative. Later, you can specify custom values for the attributes within a specific experience, which creates a variation of the parent creative.

-->

您可以将灵活的HTML5创意内容上传为ZIP文件，也可以使用您帐户可用的模板之一作为起点。 请参阅灵活的HTML5创意的[规范](html5-creative-specification.md)。

<!-- Will flattening the view be possible later?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

#### HTML5创意人员

您可以上传指定了所有属性和图像的简单或静态HTML5创意作为ZIP文件。 您无法编辑任何属性或添加图像；请上传新的ZIP文件以添加新创意。 有关简单和静态的HTML5创意，请参阅[规范](html5-creative-specification.md)。

#### 图像创意

您可以采用GIF、JPEG、JPG或PNG格式包含图像创意。 您可以上传Adobe Experience Manager帐户中的图像，或者设备或网络中的图像。

每个广告体验都需要为分配给体验的每个创意大小提供一个默认图像创意。

#### 第三方创意人员

输入第三方广告服务器上托管的创意的JavaScript跟踪标记。 脚本因广告服务器而异；以下是示例：

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### 动态广告的格式

管理员用户可以通过将广告模板中的动态变量映射到信息源文件中的值，动态生成静态HTML5和动态HTML5格式的创意。 动态创意人员可能包括来自您的旧版Adobe Advertising Dynamic Creative Optimization (DCO)体验的创意人员。

## [!UICONTROL Creative Libraries]次查看

有关自定义每个视图的详细信息，请参阅[自定义数据视图](/help/creative/introduction/customize-data-views.md)。

### [!UICONTROL Creative Libraries]主视图

[!UICONTROL Creative Libraries]主视图显示所有创意库。 每个库的数据包括已为其分配库捆绑包的体验数量、捆绑包数量、创意内容数量、创意大小数量、默认语言目标数量、创建日期以及对库的任何元素的最后修改日期。 表格模式还包括用于广告商的列。

#### 可用操作

* 创建新库

* 对于每个创意库：

   * 编辑库名称

   * 打开库以查看分配给库的创意和捆绑包

   * 删除库

### [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]视图

#### [!UICONTROL Standard Ads]

[!UICONTROL Standard Ads]选项卡显示您已创建的所有标准创意。 每个创意的数据包括创意大小、创意类型和创建日期。 表模式还包括默认语言和默认登陆页面的列。

##### 可用操作

* [将标准创意添加到库](creative-add-standard.md)

* [编辑标准创意](creative-edit-standard.md)

* [预览标准创意](creative-preview.md)

* [将标准创意添加到标准捆绑中，并从标准捆绑中删除标准创意](creative-attach-detach-bundles.md)

* [复制标准创意](creative-duplicate.md)

* [下载标准创意](creative-download.md)

* [删除标准创意](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

[!UICONTROL Dynamic Ads]选项卡显示为您的创意目录动态创建的所有动态创意，但您[从[!UICONTROL Dynamic Ads]选项卡中手动删除](creative-delete.md)的任何动态创意除外。 如果您[手动复制](creative-duplicate.md)自上次处理目录后出现的任何动态创意，则该目录的创意列表也包含重复的创意。

每个创意的数据包括创意类型、创意大小、创意所属的目录数量和创建日期。 表模式还包括用于生成创意的模板的列和选件计数。

>[!NOTE]
>
>每次处理目录时，都会刷新该目录的现有动态创意数据。

##### 可用操作

创建和编辑动态创意的能力目前仅适用于Adobe客户团队。 但是，所有用户都可以：

* [预览动态创意](creative-preview.md)

* [将动态创意添加到动态捆绑包中，并从动态捆绑包中删除动态创意](creative-attach-detach-bundles.md)

* [复制动态创意](creative-duplicate.md)

* [删除动态创意](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]视图

[!UICONTROL Bundles]视图显示所有标准和动态捆绑包容器。 您可以查看每个捆绑包中包含的创意人员的创意名称、创意大小和语言。

#### 可用操作

* 将标准和动态捆绑包添加到库

* 列出并预览捆绑包中的创意

* 编辑包名称

* 将标准创意添加到标准捆绑中，并从标准捆绑中删除标准创意

* 复制包

* 删除包

>[!MORELIKETHIS]
>
>* [管理创意库](/help/creative/creative-libraries/creative-library-manage.md)
>* [将标准创意添加到创意库](creative-add-standard.md)
>* [管理创意包](bundle-manage.md)
>* [自定义您的数据视图](/help/creative/introduction/customize-data-views.md)

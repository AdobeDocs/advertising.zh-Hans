---
title: 关于您的创意库
description: 了解如何管理广告体验的创意。
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 24846adba9ff856571d117261f44aff408e70c50
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# 关于您的创意库

您的创意库允许您管理将在广告体验中使用的创意。 您可以创建多个库，每个库都包含一组创意和&#x200B;*创意包*，这些创意包是您可以作为一个单元添加到体验中的创意组。

您的库可以包括：

* **个人创意：**&#x200B;您可以直接在广告体验中包含没有定义用户目标的个人创意。 您还可以使用创意内容创建包，这些包可以包含在定向的[广告体验](/help/creative/experiences/experience-about.md)中。

   * **标准创意：**&#x200B;您可以上传和管理[各种格式的创意](#creative-creative-formats)。 对于每个创意，指定与创意相关的每个广告的默认语言，以及用户单击包含创意的广告时打开的默认登录页面。 您可以选择指定标签，以在[!DNL Creative]内的各种视图中用作过滤器，并在使用[!UICONTROL Custom Creative Report]维度时在[!UICONTROL Creative Label]中用作列值。

   * **动态创意：**&#x200B;您可以通过将广告模板中的动态变量映射到馈送文件中的值来创建动态生成的创意。 所有用户都可以预览、复制和删除现有的动态广告。

* **创意捆绑：**&#x200B;将创意分组到捆绑中，以在具有已定义用户目标的多个体验中使用。 您可以创建包含标准显示广告的&#x200B;*标准显示包*、包含标准视频广告的&#x200B;*标准视频包*&#x200B;以及包含动态生成的显示广告的&#x200B;*动态显示包*。

## 支持的Creative格式 {#creative-creative-formats}

### 标准创意内容的格式

您可以在[支持的创意大小](creative-sizes.md)中添加和管理以下创意类型。

>[!IMPORTANT]
>
>* 即使您打算将HTML5、弹性HTML5或第三方创意用于标准显示广告体验，您还必须为您使用的每个创意大小添加图像创意。
>* 每个标准显示体验都需要为分配给体验的每个创意大小提供一个默认图像创意。 当浏览器未启用JavaScript或广告服务器由于延迟而无法个性化广告时，可以使用默认图像创意。
>* 每个标准视频体验都需要为分配给该体验的每个创意持续时间提供一个默认视频创意。<!-- when is it used? -->

#### 灵活的HTML5

灵活的HTML5创意人员是HTML5创意人员，其所有图像和其他属性均作为标准HTML标记，您可以直接在[!DNL Creative]中、创意库或单个体验（这会创建原始创意内容的变体）中编辑这些内容。 在DSP中，灵活的HTML5创意适用于单个特定广告大小（以像素为单位）。 您可以选择更改在灵活的HTML5创作实例中指定的属性的默认值。 稍后，您可以为特定体验中的属性指定自定义值，这会创建父级创意内容的变体。

您可以将灵活的HTML5创意内容上传为ZIP文件，也可以使用您帐户可用的模板之一作为起点。 请参阅灵活的HTML5创意的[规范](html5-creative-specification.md)。

#### 标准显示创意

标准显示广告包括：

* HTML5创意内容已本地上传或从Adobe GenStudio for Performance Marketing上传。
* 图像文件上传到本地或从Adobe Experience Manager上传。

##### HTML5创意人员

* **GenStudio体验：**&#x200B;您可以从[GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences)中的[显示广告体验](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)导入所有广告变体作为HTML5创意。 外部链接将转换为本地引用。 HTML内容最长可达20 MB，单个图像最长可达50 MB。

  要使用此功能，GenStudio帐户和Advertising Creative帐户必须使用相同的组织ID，并且用户必须具有访问GenStudio的权限。

  导入GenStudio体验后，您可以编辑已导入创意内容的元数据（名称、语言、标记），但不能编辑创意内容。 如果您在GenStudio中编辑GenStudio体验，请在[!DNL Creative]中重新导入该体验以使用最新版本。

* **上载的文件：**&#x200B;您还可以上载简单或静态的HTML5创意（指定了所有属性和图像）作为ZIP文件。 您无法编辑任何属性或添加图像；请上传新的ZIP文件以添加新创意。 有关简单和静态的HTML5创意，请参阅[规范](html5-creative-specification.md)。

##### 图像创意

您可以采用GIF、JPEG、JPG或PNG格式包含图像创意。 您可以从Adobe Experience Manager帐户上传已批准的图像，或者从设备或网络上传已批准的图像。

每个标准显示广告体验都需要为分配给体验的每个创意大小提供一个默认图像创意。

#### 第三方创意人员

输入第三方广告服务器上托管的创意的JavaScript跟踪标记。 脚本因广告服务器而异；以下是示例：

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### 视频创意 {#creative-video-specs}

您可以从设备或网络中为Web、移动或连接的电视上传第一方视频创意。 每个标准视频广告体验都需要为分配给体验的每个创意持续时间提供一个默认视频创意。 DSP会自动将所有视频创意转换为VAST 2.0标记，以便您预览。 在[!UICONTROL Tag Manager]中，您可以选择将[特定于DSP的转码](/help/creative/experiences/experience-tag-video-transcoding.md)应用于任何视频广告体验标记。

请参阅以下视频创作要求。 **注意：**&#x200B;如果要将视频体验上传到Advertising DSP，请另外参阅DSP对高清视频Assets的[要求](https://experienceleague.adobe.com/zh-hans/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets)，这可能更有限。

**文件类型：** .mov、.mp4、.webm

**文件大小：**&#x200B;最大为512 MB

**视频宽高比：** 16:9，4:3

**视频分辨率：** 640x360(360p)，1280x720(720p)，1920x1080(1080p)

**视频长度：**&#x200B;最长90秒

**比特率：** 360p为600-1200 kbps，720p为1500-2500 kbps，1080p为3000-5000+ kbps

**视频帧速率：** 23.98 FPS。 可根据区域或发布者要求接受额外的帧速率

**视频编解码器：** H.264（行业标准）、AV1、H.265

**音频格式：** ACC （行业标准/MP4）、Opus (WebM/AV1)

**音频比特率：** 16-512 kbps

**音频采样速率：** 44100-48000 Hz

**音频速率：** 44.1kHz或48 kHz

**音频其他：**&#x200B;上传的文件必须是非交错的、混合的，并且包含一个音轨。 可能没有声音，但视频文件中必须包含音频轨道。

### 动态广告的格式

您可以将广告模板中的动态变量映射到信息源文件中的值，从而动态生成静态HTML5和动态HTML5格式的创意。 动态创意人员可能包括从旧版Adobe Advertising Dynamic Creative Optimization (DCO)体验迁移而来的创意人员。

## [!UICONTROL Creative Libraries]次查看

有关自定义每个视图的详细信息，请参阅[自定义数据视图](/help/creative/introduction/customize-data-views.md)。

### [!UICONTROL Creative Libraries]主视图

[!UICONTROL Creative Libraries]主视图显示所有创意库。 每个库的数据包括已为其分配库捆绑包的体验数量、捆绑包数量、创意内容数量、创意大小数量、默认语言目标数量、创建日期以及对库的任何元素的最后修改日期。 表格模式还包括用于广告商的列。

在卡片模式下，您可以使用&lt;和>按钮滚动浏览具有多个创意的库中的图像。

#### 可用操作

* [创建新库](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* 对于每个创意库：

   * [编辑库名称](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [打开库以查看分配给库的创意和捆绑包](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [删除库](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]视图

#### [!UICONTROL Standard Ads]

[!UICONTROL Standard Ads]选项卡显示您已创建的所有标准创意。 每个创意的数据包括创意大小、创意类型和创建日期。 表模式还包括默认语言和默认登陆页面的列。

##### 可用操作

* [将标准创意添加到库](creative-add-standard.md)

* [编辑标准创意](creative-edit-standard.md)

* [预览标准创意](creative-preview.md)

* [将标准创意添加到标准显示包，并从标准显示包中删除标准创意](creative-attach-detach-bundles.md)

* [将视频创意添加到标准视频包，并从标准视频包中删除视频创意](creative-attach-detach-bundles.md)

* [复制标准创意](creative-duplicate.md)

* [下载标准创意](creative-download.md)

* [删除标准创意](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

[!UICONTROL Dynamic Ads]选项卡显示为您的创意目录动态创建的所有动态创意，但您[从](creative-delete.md)选项卡中手动删除[!UICONTROL Dynamic Ads]的任何动态创意除外。 如果您[手动复制](creative-duplicate.md)任何动态创意<!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed -->，则该目录的创意列表也包含重复的创意。

每个创意的数据包括创意类型、创意大小、创意所属的目录数量和创建日期。 表模式还包括用于广告模板的列，通过广告模板生成创意和选件计数。

>[!NOTE]
>
>每次处理目录时，将刷新该目录的现有动态创意数据。<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### 可用操作

* [将动态创意添加到库](creative-add-dynamic.md)

* [编辑动态创意](creative-edit-dynamic.md)

* [预览动态创意](creative-preview.md)

* [将动态创意添加到动态显示捆绑包中，并从动态显示捆绑包中删除动态创意](creative-attach-detach-bundles.md)

* [复制动态创意](creative-duplicate.md)

* [删除动态创意](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]视图

[!UICONTROL Bundles]视图显示所有标准和动态捆绑包容器。 您可以查看每个捆绑包中包含的创意人员的创意名称、创意大小和语言。 在卡片模式下，可以使用&lt;和>按钮滚动浏览具有多个创意的捆绑包中的图像。

#### 可用操作

* 将标准显示、标准视频和动态显示捆绑包添加到库

* 列出并预览捆绑包中的创意

* 编辑包名称

* 将标准显示创意添加到标准显示捆绑包中，并从标准显示捆绑包中删除标准显示创意

* 将标准视频创意添加到标准视频包，并从标准视频包中删除标准视频创意

* 复制包

* 删除包

>[!MORELIKETHIS]
>
>* [管理创意库](/help/creative/creative-libraries/creative-library-manage.md)
>* [将标准创意添加到创意库](creative-add-standard.md)
>* [管理创意包](bundle-manage.md)
>* [自定义您的数据视图](/help/creative/introduction/customize-data-views.md)

---
title: 自定义视频广告体验标记的转码选项
description: 了解如何自定义视频广告标记的转码选项。
feature: Creative Experiences
exl-id: 6100213c-2e7d-4e98-a3ab-045ca10e5174
source-git-commit: 3d0d42d19c11276f13a4e003c382a2d2410ab037
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# 自定义视频广告体验标记的转码选项

*已关闭的测试版*

您可以为视频广告体验自定义转码选项，以确保跨发布者的快速播放和质量控制。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 执行以下操作之一：

* 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**。

* 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**。

1. 将光标悬停在适用的广告标记的行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Video Settings]**。

1. 在&#x200B;**[!UICONTROL Publisher specific transcodes]**&#x200B;列表中，选择转码类型。

1. 单击&#x200B;**[!UICONTROL Save Settings]**。

## 默认([!DNL Adobe] DSP)转码规范

| 文件类型 | 维度 | 视频比特率 | 视频帧速率 | 音频比特率 | 音频采样率 | 音频级别 |
|---|---|---|---|---|---|---|
| mp4 | 640x360 | 1000 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 400x300 | 1000 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 1024x768 | 500 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 640x480 | 1000 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 960x540 | 2000 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 960x720 | 2000 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 1280x720 | 2000 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 1920x1080 | 3500 kbps | 23.98 fps | 128 kbps | 44.100千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 640x360 | 800 kbps | 23.98 fps | 96 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 640x360 | 400 kbps | 23.98 fps | 128 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |
| mp4 | 1920x1080 | 16000 kbps | 23.98 fps | 256 kbps | 48.000千赫 | 24个LKFS (+/- 2.0 dB) |

>[!MORELIKETHIS]
>
>* [关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)
>* [创建具有定位功能的体验](/help/creative/experiences/experience-create-targeting.md)
>* [为适用的创意大小手动创建广告标签](experience-tag-create-manually.md)
>* [导出和实施实时体验的广告体验标记](experience-tag-export.md)

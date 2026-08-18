---
title: Creative Studio中的C2PA元数据
description: 了解如何在Creative Studio中将C2PA元数据自动附加到使用生成人工智能生成或编辑的内容中。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# [!UICONTROL Creative Studio]中的C2PA元数据

[!UICONTROL Creative Studio]自动将C2PA元数据附加到使用创作AI生成或编辑的内容，以便将广告内容的来源记录为持久的、不可见的元数据。 元数据遵循[内容来源和授权联盟](https://c2pa.org/) (C2PA)的标准。

## 内容类型及其范围 {#cc-content-types}

| 内容类型 | 受支持？ | 生成内容的AI服务 | 生成凭据的模型 |
| --- | --- | --- | --- |
| 图像 | 是的。 当使用创作AI生成或编辑图像时，附加C2PA元数据，并通过由AI助手执行的裁切和调整大小操作来保留。 | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## 附加C2PA元数据的操作

下表总结了根据[!UICONTROL Creative Studio] AI助手中执行的图像操作，何时附加C2PA元数据。

| 操作 | 描述 | 是否附加C2PA元数据？ | 用例示例 |
| --- | --- | --- | --- |
| **生成图像** | 使用文本提示创建新图像 | 因为图像是由创成式人工智能生成的。 | 使用文本提示为广告模板生成新的背景图像或徽标。<br><br>使用文本提示将广告概念中的默认图像替换为您库中上传的资产。<br><br>使用文本提示生成广告模板中背景图像的变体。 |

## 内容移动时会出现什么情况？ {#cc-content-moves}

当用户下载图像文件或发送该文件以便在广告中提供服务时，将保留完整的来源链。

## C2PA元数据包括什么内容？

对于每次GenAI的生成或更改，C2PA元数据中包含以下内容。 如果资产被多次更改，则每个操作都会显示在C2PA元数据中。

* 使用的AI系统的名称和版本信息([!DNL Adobe Firefly C2PA])
* 使用的AI模型([!DNL Gemini Flash])
* 用法：是否使用GenAI生成或编辑它
* 使用创作AI工具创建和/或修改内容的时间和日期
* 唯一标识符（可用于区分创作AI的每个用法）

## 如何查看图像的C2PA元数据？

要查看图像的完整资源历史记录，请执行以下操作：

* 在内容真实性检查工具（如https://contentauthenticity.adobe.com/inspect或https://verify.contentauthenticity.org/）中打开图像文件。

* 查看图像元数据。

* 使用浏览器的代码检查工具（通常称为[!DNL Inspect]）查看图像代码。

![映像的C2PA元数据示例](/help/creative/assets/cs-content-credentials-example.png "映像的C2PA元数据")

## 其他资源

* [[!DNL Adobe]创作AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [关于Creative Studio](/help/creative/creative-studio/creative-studio-about.md)

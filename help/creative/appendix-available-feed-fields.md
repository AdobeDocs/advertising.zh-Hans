---
title: 动态广告馈送文件的可用字段
description: 了解可在用于创建动态广告的信息源文件中包含的字段。
feature: Creative Dynamic Creatives
exl-id: 9cd3fa29-d4db-4e9f-9ffd-87b44b62a3e2
source-git-commit: 5bf0474f49160775d31dff0d434ba1e069f27959
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 附录：动态广告馈送文件的可用字段

Advertising Creative后端提供了以下信息源字段。 您可以上载使用组织特定字段名称的[信息源文件](/help/creative/feeds/asset-manage.md)。 但是，必须先将信息源文件中的每个字段映射到将用于创建目录的[信息源模板](/help/creative/feeds/catalog-manage.md)中的以下字段之一，然后才能从信息源文件创建[目录](/help/creative/feeds/feed-template-manage.md)。

您的信息源文件中唯一必须具有等效项的字段是`PART_NUM`。

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| 字段名称 | 数据类型 | 必需？ |
|------------|-----------|-----------|
| AD_SIZE | varchar(32) | 否 |
| ADDITIONAL_PRICE_1 | decimal(10,2) | 否 |
| ADDITIONAL_PRICE_2 | decimal(10,2) | 否 |
| ADDITIONAL_PRICE_3 | decimal(10,2) | 否 |
| 区域代码 | 文本 | 否 |
| AUDIENCE_SEGMENT | 文本 | 否 |
| AUDIO_1 | varchar(1024) | 否 |
| AUDIO_2 | varchar(1024) | 否 |
| AUDIO_3 | varchar(1024) | 否 |
| AUDIO_4 | varchar(1024) | 否 |
| AUDIO_5 | varchar(1024) | 否 |
| 城市 | 文本 | 否 |
| 国家/地区 | 文本 | 否 |
| Creative_ATTRIBUTE_1 | varchar(256) | 否 |
| Creative_ATTRIBUTE_2 | varchar(256) | 否 |
| Creative_ATTRIBUTE_3 | varchar(256) | 否 |
| Creative_ATTRIBUTE_4 | varchar(256) | 否 |
| Creative_ATTRIBUTE_5 | varchar(256) | 否 |
| Creative_ATTRIBUTE_6 | varchar(256) | 否 |
| Creative_ATTRIBUTE_7 | varchar(256) | 否 |
| Creative_ATTRIBUTE_8 | varchar(256) | 否 |
| Creative_ATTRIBUTE_9 | varchar(256) | 否 |
| Creative_ATTRIBUTE_10 | varchar(256) | 否 |
| DATAPAS_FILTER_1 | 文本 | 否 |
| DATAPAS_FILTER_2 | 文本 | 否 |
| DATAPASS过滤器3 | 文本 | 否 |
| DATAPASS过滤器4 | 文本 | 否 |
| DATAPASS过滤器5 | 文本 | 否 |
| DISCOUNT_PRICE | decimal(10,2) | 否 |
| DMA | 文本 | 否 |
| 图像 | varchar(1024) | 否 |
| IMAGE_1 | varchar(1024) | 否 |
| IMAGE_2 | varchar(1024) | 否 |
| IMAGE_3 | varchar(1024) | 否 |
| IMAGE_4 | varchar(1024) | 否 |
| IMAGE_5 | varchar(1024) | 否 |
| IMAGE_6 | varchar(1024) | 否 |
| IMAGE_7 | varchar(1024) | 否 |
| IMAGE_8 | varchar(1024) | 否 |
| IMAGE_9 | varchar(1024) | 否 |
| IMAGE_10 | varchar(1024) | 否 |
| IMAGE_HEIGHT | int | 否 |
| IMAGE_WIDTH | int | 否 |
| IS_DEFAULT | 枚举 | 否 |
| 语言 | 文本 | 否 |
| PART_NUM | varchar(64) | 是 |
| 价格 | decimal(10,2) | 否 |
| 产品名称 | 文本 | 否 |
| PRODUCT_URL | 文本 | 否 |
| PROFILE_FILTER_1 | 文本 | 否 |
| PROFILE_FILTER_2 | 文本 | 否 |
| PROFILE_FILTER_3 | 文本 | 否 |
| PROFILE_FILTER_4 | 文本 | 否 |
| PROFILE_FILTER_5 | 文本 | 否 |
| 排名 | int | 否 |
| 状态 | 文本 | 否 |
| TEXT_1 | 文本 | 否 |
| TEXT_2 | 文本 | 否 |
| TEXT_3 | 文本 | 否 |
| TEXT_4 | 文本 | 否 |
| TEXT_5 | 文本 | 否 |
| TEXT_6 | 文本 | 否 |
| TEXT_7 | 文本 | 否 |
| TEXT_8 | 文本 | 否 |
| TEXT_9 | 文本 | 否 |
| TEXT_10 | 文本 | 否 |
| TEXT_11 | 文本 | 否 |
| TEXT_12 | 文本 | 否 |
| TEXT_13 | 文本 | 否 |
| TEXT_14 | 文本 | 否 |
| TEXT_15 | 文本 | 否 |
| VIDEO_1 | varchar(1024) | 否 |
| VIDEO_2 | varchar(1024) | 否 |
| VIDEO_3 | varchar(1024) | 否 |
| VIDEO_4 | varchar(1024) | 否 |
| VIDEO_5 | varchar(1024) | 否 |
| ZIP | 文本 | 否 |

>[!MORELIKETHIS]
>
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理资源文件](/help/creative/feeds/asset-manage.md)
>* [管理馈送模板](/help/creative/feeds/feed-template-manage.md)
>* [管理目录](/help/creative/feeds/catalog-manage.md)

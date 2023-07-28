---
title: 归因规则的计算方式
description: 了解Adobe Advertising如何计算每种类型的归因规则。
exl-id: b61561fa-8c01-4989-9ef7-620d2b4c2c0b
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# 如何为Adobe Advertising计算归因规则

*仅具有Adobe Advertising转化跟踪的广告商*

<!-- Verify statements about cross-device events -->

广告商级别的归因规则用于在一系列导致转化的事件中归因转化数据（可能跨多个广告渠道）。

在报表、Advertising Search、Social和Commerce（Search、Social和Commerce）的默认视图和（某些用户角色）以及Search、Social和Commerce的项目组合级别模拟中，选定的规则仅用于视图、报表或模拟数据。 各种归因规则的应用如下。

>[!NOTE]
>
>* 归因规则适用于任何渠道中的付费广告点击次数，以及展示广告和社交广告的展示次数。 它们不适用于付费搜索广告的展示次数，此类展示次数无法在事件级别进行跟踪。
>* Adobe Advertising始终在转化前为每个Web浏览者存储以下事件： a)第一次付费点击； b)每个渠道最多10次点击（搜索、社交或显示），包括第一次点击；以及c)最多10次显示展示。 <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* 在Advertising DSP和Advertising Creative中，跨设备定义仅考虑所选归因规则中的事件路径。<!-- cross-device attribution via LiveRamp only -->
* 在报表和管理视图中，为某个值显示的小数位数取决于货币，但Adobe Advertising会存储更精确的值。

## 上一个事件（默认）

将转化归因于广告商的系列中的最后一次付费点击 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 或者，如果未发生付费点击，则指向广告商展示的最后一次展示 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j).

如果转换之前只有展示次数，则将此转换视为 *显示到达*，根据广告商的 [显示到达权重设置](/help/search-social-commerce/glossary.md#uv) 或 — 如所指定 — 根据报告、视图或自定义模拟参数中指定的浏览估价方法。

![上一个事件归因百分比](/help/search-social-commerce/assets/attribution-percent-last-event.png "上一个事件归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径： Click1、Click2、Click3、120美元的转化

该转换归因于Click 3，金额为120美元。

### 包含展示次数和点击次数的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、120美元转化

该转换归因于Click 1，金额为120美元。

### 具有所有展示的示例

**注意：** 仅适用于展示广告和社交广告的展示次数。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

该转化归因于展示3。 由于转化是显示到达次数，因此应用了在报表设置的“转化归因”部分中选择的显示到达估价方法：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于显示到达。 例如，如果广告商的展示权重为40%，则120 USD x 40% = 48 USD，因此48 USD归因于“展示3”。

* 如果报表参数指定使用显示到达的原始值，则显示到达权重不会应用于显示到达，并且全部120美元将归因于“展示3”。

+++

<!-- end examples as collapsible content -->

## 第一个事件

将转化归因于广告商的系列中的第一次付费点击 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 或者，如果未发生付费点击，则呈现广告商的第一印象 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j). 此规则仅适用于单个设备上的事件。

如果转换之前只有展示次数，则将此转换视为 *显示到达*，根据广告商的 [显示到达权重设置](/help/search-social-commerce/glossary.md#uv) 或 — 如所指定 — 根据报告、视图或自定义模拟参数中指定的浏览估价方法。

![第一个事件归因百分比](/help/search-social-commerce/assets/attribution-percent-first-event.png "第一个事件归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换额为120美元

该转换归因于Click 1，金额为120美元。

### 包含展示次数和点击次数的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、120美元转化

该转换归因于Click 1，金额为120美元。

### 具有所有展示的示例

**注意：** 仅适用于展示广告和社交广告的展示次数。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

该转化归因于展示1。 由于转化是显示到达，因此应用了在报表设置的“（显示促销活动）转化归因”部分中选择的显示到达估价方法：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于显示到达。 例如，如果广告商的展示权重为40%，则120 x 40% = 48美元，因此48美元归因于“展示次数1”。

* 如果报表参数指定使用显示到达的原始值，则显示到达权重不会应用于显示到达，并且全部120美元将归因于“展示1”。

+++

<!-- end examples as collapsible content -->

## 将第一个事件加权更多

将转化归因于广告商发生的一系列事件中的所有事件 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)，但给予第一个事件最大权重，而依次给予以下事件较小权重。此规则仅适用于单个设备上的事件。

如果转换之前只有展示次数，则将此转换视为 *显示到达*，根据广告商的 [显示到达权重设置](/help/search-social-commerce/glossary.md#uv) 或 — 如所指定 — 根据报告、视图或自定义模拟参数中指定的浏览估价方法。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在搜索、社交和商务中， [印象覆盖权重](/help/search-social-commerce/glossary.md#i-j)  — 在广告商的展示次数覆盖权重设置以及报表、视图或自定义模拟参数中指定 — 首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![权重第一个事件更多归因百分比](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "权重第一个事件更多归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换额为120美元

归因：单击1 = 60 USD，单击2 = 40 USD，单击3 = 20 USD（总计120 USD）

### 包含展示和点击的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### （仅限搜索、社交和商务）使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 8 USD，点击次数1 = 72 USD，展示次数2 = 4 USD，点击次数2 = 36 USD（总计120 USD）

#### 使用(仅限DSP)无展示覆盖权重或（仅限搜索、Social和Commerce）0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 80 USD，展示次数2 = 0 USD，点击次数2 = 40 USD（总计120 USD）

### 具有所有展示的示例

**注意：** 仅适用于显示广告的展示次数。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达重量为40%，则展示1 = 24 USD，展示2 = 16 USD，展示3 = 8 USD（合计48 USD）

* 如果报表参数指定使用原始值表示显示到达次数，则不会为展示应用显示到达权重，120美元全数在三种展示之间分配：展示1 = 60美元，展示2 = 40美元，展示3 = 20美元（总计120美元）

+++

<!-- end examples as collapsible content -->

## 均匀分布

>[!NOTE]
>
>此规则仅适用于单个设备上的事件。

将转化同等地归因于广告商广告中发生的系列中的每个事件 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j).

如果转换之前只有展示次数，则将此转换视为 *显示到达*，根据广告商的 [显示到达权重设置](/help/search-social-commerce/glossary.md#uv) 或 — 如所指定 — 根据报告、视图或自定义模拟参数中指定的浏览估价方法。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在搜索、社交和商务中， [印象覆盖权重](/help/search-social-commerce/glossary.md#i-j)  — 在广告商的展示次数覆盖权重设置以及报表、视图或自定义模拟参数中指定 — 首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![偶数归因百分比](/help/search-social-commerce/assets/attribution-percent-even.png "偶数归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换价格为120美元

无展示会导致转化，因此展示覆盖权重不适用，并且转化在三次点击之间平均分配：

归因：单击1 = 40 USD，单击2 = 40 USD，单击3 = 40 USD（总计120 USD）

### 包含展示和点击的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### （仅限搜索、社交和商务）使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 6 USD，点击次数1 = 54 USD，展示次数2 = 6 USD，点击次数2 = 54 USD（总计120 USD）

#### 使用(仅限Adobe Advertising DSP)无展示覆盖权重或（仅限搜索、Social和Commerce）0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 60 USD，展示次数2 = 0 USD，点击次数2 = 60 USD（总计120 USD）

## 具有所有展示的示例

**注意：** 仅适用于显示广告的展示次数。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达重量为40%，则展示1 = 16 USD，展示2 = 16 USD，展示3 = 16 USD（合计48 USD）

* 如果报表参数指定使用原始值表示显示到达次数，则不会为展示应用显示到达权重，120美元全数在三种展示之间分配：展示1 = 40美元，展示2 = 40美元，展示3 = 40美元（总计120美元）

+++

<!-- end examples as collapsible content -->

## 权重最后一个事件更多

将转化归因于广告商发生的一系列事件中的所有事件 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)，但是会为最后一个事件赋予最大权重，而为前面事件依次赋予较小的权重。

如果转换之前只有展示次数，则将此转换视为 *显示到达*，根据广告商的 [显示到达权重设置](/help/search-social-commerce/glossary.md#uv) 或 — 如所指定 — 根据报告、视图或自定义模拟参数中指定的浏览估价方法。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在搜索、社交和商务中， [印象覆盖权重](/help/search-social-commerce/glossary.md#i-j)  — 在广告商的展示次数覆盖权重设置以及报表、视图或自定义模拟参数中指定 — 首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![权重最后事件更多归因百分比](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "权重最后事件更多归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换额为120美元

归因：单击3 = 60 USD，单击2 = 40 USD，单击1 = 20 USD（总计120 USD）

### 包含展示和点击的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### （仅限搜索、社交和商务）使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 4 USD，点击次数1 = 36 USD，展示次数2 = 8 USD，点击次数2 = 72 USD（总计120 USD）

#### 使用(仅限DSP)无展示覆盖权重或（仅限搜索、Social和Commerce）0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 40 USD，展示次数2 = 0 USD，点击次数2 = 80 USD（总计120 USD）

### 具有所有展示的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1， Impression 2， Impression 3,120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达权重为40%，则将“包含所有点击的示例”中的每个值乘以40%：Impression 3 = 24 USD，Impression 2 = 16 USD，Impression 1 = 8 USD（合计48 USD）

* 如果报表参数指定使用显示到达的原始值，则完整的120 USD在展示之间平分：展示3 = 60 USD，展示2 = 40 USD，展示1 = 20 USD（总计120 USD）

+++

<!-- end examples as collapsible content -->

## U型

将转化归因于广告商发生的一系列事件中的所有事件 [单击回顾窗口](/help/search-social-commerce/glossary.md#c-d) 和 [展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)，但是会为第一个事件和最后一个事件赋予最大的权重，而对转换路径中间事件的权重则依次较低。

如果转换之前只有展示次数，则将此转换视为 *显示到达*，根据广告商的 [显示到达权重设置](/help/search-social-commerce/glossary.md#uv) 或 — 如所指定 — 根据报告、视图或自定义模拟参数中指定的浏览估价方法。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在搜索、社交和商务中， [印象覆盖权重](/help/search-social-commerce/glossary.md#i-j)  — 在广告商的展示次数覆盖权重设置以及报表、视图或自定义模拟参数中指定 — 首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![U形归因百分比](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U形归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，单击4,120美元换算

归因：单击1 = 36 USD，单击2 = 24 USD，单击3 = 24 USD，单击4 = 36 USD（总计120 USD）

### 包含展示和点击的示例

**注意：** 展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### （仅限搜索、社交和商务）使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 6 USD，点击次数1 = 54 USD，展示次数2 = 6 USD，点击次数2 = 54 USD（总计120 USD）

#### 使用(仅限DSP)无展示覆盖权重或（仅限搜索、Social和Commerce）“展示覆盖权重”为0%

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 60 USD，展示次数2 = 0 USD，点击次数2 = 60 USD（总计120 USD）

### 具有所有展示的示例

**注意：** 仅适用于显示广告的展示次数。

事件路径： Impression 1、Impression 2、Impression 3、Impression 4、120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达重量为40%，则单击1 = 14.40 USD，单击2 = 9.60 USD，单击3 = 9.60 USD，单击4 = 14.40 USD（合计48 USD）

* 如果报表参数指定使用显示到达的原始值，则完整的120 USD将在展示次数之间平分：单击1 = 36 USD，单击2 = 24 USD，单击3 = 24 USD，单击4 = 36 USD（总计120 USD）

+++

<!-- end examples as collapsible content -->

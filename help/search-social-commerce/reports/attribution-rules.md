---
title: 归因规则的计算方式
description: 了解Adobe Advertising如何计算每种类型的归因规则。
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '2716'
ht-degree: 0%

---

# 如何为Adobe Advertising计算归因规则

*仅跟踪Adobe Advertising转化情况的广告商*

<!-- Verify statements about cross-device events -->

广告商级别的归因规则用于在一系列导致转化的事件中归因转化数据（可能跨多个广告渠道）。

在Advertising Search、Social和Commerce(Search、Social和Commerce)的报表默认视图和自定义视图，以及Search、Social和Commerce的项目组合级别模拟（某些用户角色）中，选定的规则仅用于视图、报表或模拟数据。 各种归因规则的应用如下。

>[!NOTE]
>
>* 归因规则适用于任何渠道中的付费广告点击次数，以及展示广告和社交广告的展示次数。 它们不适用于付费搜索广告的展示次数，此类展示次数无法在事件级别进行跟踪。
>* Adobe Advertising始终在转化前为每个Web浏览者存储以下事件： a)第一次付费点击； b)每个渠道最多10次点击（搜索、社交或显示），包括第一次点击；以及c)最多10次显示展示。<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* 在Advertising DSP和Advertising Creative中，跨设备定义仅考虑所选归因规则中的事件路径。<!-- cross-device attribution via LiveRamp only -->
* 在报表和管理视图中，为某个值显示的小数位数取决于货币，但Adobe Advertising会存储更精确的值。

## 上一个事件（默认）

将转化归因于广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)内系列中的最后一次付费点击，如果没有发生付费点击，则归因于广告商的[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内的最后一次展示。

如果转换之前只有展示次数，则将转换视为&#x200B;*显示到达*，该转换根据广告商的[显示到达权重设置](/help/search-social-commerce/glossary.md#uv)进行加权，或者，根据指定，根据在报表、视图或自定义模拟参数中指定的显示到达估价方法进行加权。

![上一个事件归因百分比](/help/search-social-commerce/assets/attribution-percent-last-event.png "上一个事件归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径： Click1、Click2、Click3、120美元的转化

该转换归因于Click 3，金额为120美元。

### 包含展示次数和点击次数的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、120美元转化

该转换归因于Click 1，金额为120美元。

### 具有所有展示的示例

**注意：**&#x200B;仅展示广告和社交广告的展示次数适用。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

该转化归因于展示3。 由于转化是显示到达次数，因此应用了在报表设置的“转化归因”部分中选择的显示到达估价方法：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于显示到达。 例如，如果广告商的展示权重为40%，则120 USD x 40% = 48 USD，因此48 USD归因于“展示3”。

* 如果报表参数指定使用显示到达的原始值，则显示到达权重不会应用于显示到达，并且全部120美元将归因于“展示3”。

+++

<!-- end examples as collapsible content -->

## 第一个事件

将转化归因于广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)内系列中的第一次付费点击，如果没有发生付费点击，则归因于广告商的[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内的第一次展示。 此规则仅适用于单个设备上的事件。

如果转换之前只有展示次数，则转换将被视为&#x200B;*显示到达*，其根据广告商的[显示到达权重设置](/help/search-social-commerce/glossary.md#uv)进行加权，或者，根据指定，根据在报表、视图或自定义模拟参数中指定的显示到达估价方法进行加权。

![第一个事件归因百分比](/help/search-social-commerce/assets/attribution-percent-first-event.png "第一个事件归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换额为120美元

该转换归因于Click 1，金额为120美元。

### 包含展示次数和点击次数的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、120美元转化

该转换归因于Click 1，金额为120美元。

### 具有所有展示的示例

**注意：**&#x200B;仅展示广告和社交广告的展示次数适用。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

该转化归因于展示1。 由于转化是显示到达，因此在“（显示促销活动）转化”中选择的显示到达估价方法
报表设置的“归因”部分：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于显示到达。 例如，如果广告商的展示权重为40%，则120 x 40% = 48美元，因此48美元归因于“展示次数1”。

* 如果报表参数指定使用显示到达的原始值，则显示到达权重不会应用于显示到达，并且全部120美元将归因于“展示1”。

+++

<!-- end examples as collapsible content -->

## 将第一个事件加权更多

将转化归因于在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的系列中的所有事件，但给予第一个事件的权重最大，给予以下事件的权重依次较低。此规则仅适用于单个设备上的事件。

如果转换之前只有展示次数，则转换将被视为&#x200B;*显示到达*，其根据广告商的[显示到达权重设置](/help/search-social-commerce/glossary.md#uv)进行加权，或者，根据指定，根据在报表、视图或自定义模拟参数中指定的显示到达估价方法进行加权。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在Search、Social和Commerce中，[展示覆盖权重](/help/search-social-commerce/glossary.md#i-j)（在广告商的展示覆盖权重设置中以及在报表、视图或自定义模拟参数中指定）首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![加权第一个事件更多归因百分比](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "加权第一个事件更多归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换额为120美元

归因：单击1 = 60 USD，单击2 = 40 USD，单击3 = 20 USD（总计120 USD）

### 包含展示和点击的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### (仅限搜索、社交和Commerce)使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 8 USD，点击次数1 = 72 USD，展示次数2 = 4 USD，点击次数2 = 36 USD（总计120 USD）

#### 使用(仅限DSP)无展示覆盖权重或(仅限搜索、Social和Commerce)0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 80 USD，展示次数2 = 0 USD，点击次数2 = 40 USD（总计120 USD）

### 具有所有展示的示例

**注意：**&#x200B;仅展示广告的展示次数适用。

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

将转化平均归因于在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的系列中的每个事件。

如果转换之前只有展示次数，则转换将被视为&#x200B;*显示到达*，其根据广告商的[显示到达权重设置](/help/search-social-commerce/glossary.md#uv)进行加权，或者，根据指定，根据在报表、视图或自定义模拟参数中指定的显示到达估价方法进行加权。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在Search、Social和Commerce中，[展示覆盖权重](/help/search-social-commerce/glossary.md#i-j)（在广告商的展示覆盖权重设置中以及在报表、视图或自定义模拟参数中指定）首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![偶数归因百分比](/help/search-social-commerce/assets/attribution-percent-even.png "偶数归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换价格为120美元

无展示会导致转化，因此展示覆盖权重不适用，并且转化在三次点击之间平均分配：

归因：单击1 = 40 USD，单击2 = 40 USD，单击3 = 40 USD（总计120 USD）

### 包含展示和点击的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### (仅限搜索、社交和Commerce)使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 6 USD，点击次数1 = 54 USD，展示次数2 = 6 USD，点击次数2 = 54 USD（总计120 USD）

#### 使用(仅限Adobe Advertising DSP)无展示覆盖权重或(仅限搜索、Social和Commerce)0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 60 USD，展示次数2 = 0 USD，点击次数2 = 60 USD（总计120 USD）

## 具有所有展示的示例

**注意：**&#x200B;仅展示广告的展示次数适用。

事件路径： Impression 1、Impression 2、Impression 3、120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达重量为40%，则展示1 = 16 USD，展示2 = 16 USD，展示3 = 16 USD（合计48 USD）

* 如果报表参数指定使用原始值表示显示到达次数，则不会为展示应用显示到达权重，120美元全数在三种展示之间分配：展示1 = 40美元，展示2 = 40美元，展示3 = 40美元（总计120美元）

+++

<!-- end examples as collapsible content -->

## 权重最后一个事件更多

将转化归因于在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的系列中的所有事件，但将最大权重给予最后一个事件，并依次减少对前面事件的权重。

如果转换之前只有展示次数，则转换将被视为&#x200B;*显示到达*，其根据广告商的[显示到达权重设置](/help/search-social-commerce/glossary.md#uv)进行加权，或者，根据指定，根据在报表、视图或自定义模拟参数中指定的显示到达估价方法进行加权。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在Search、Social和Commerce中，[展示覆盖权重](/help/search-social-commerce/glossary.md#i-j)（在广告商的展示覆盖权重设置中以及在报表、视图或自定义模拟参数中指定）首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![加权最后事件更多归因百分比](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "加权最后事件更多归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，转换额为120美元

归因：单击3 = 60 USD，单击2 = 40 USD，单击1 = 20 USD（总计120 USD）

### 包含展示和点击的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### (仅限搜索、社交和Commerce)使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 4 USD，点击次数1 = 36 USD，展示次数2 = 8 USD，点击次数2 = 72 USD（总计120 USD）

#### 使用(仅限DSP)无展示覆盖权重或(仅限搜索、Social和Commerce)0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 40 USD，展示次数2 = 0 USD，点击次数2 = 80 USD（总计120 USD）

### 具有所有展示的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1， Impression 2， Impression 3,120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达权重为40%，则将“包含所有点击的示例”中的每个值乘以40%：Impression 3 = 24 USD，Impression 2 = 16 USD，Impression 1 = 8 USD（合计48 USD）

* 如果报表参数指定使用显示到达的原始值，则完整的120 USD在展示之间平分：展示3 = 60 USD，展示2 = 40 USD，展示1 = 20 USD（总计120 USD）

+++

<!-- end examples as collapsible content -->

## U型

将转化归因于在广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)内发生的系列中的所有事件，但将最大权重赋予第一个事件和最后一个事件，依次减少对转化路径中间事件的权重。

如果转换之前只有展示次数，则转换将被视为&#x200B;*显示到达*，其根据广告商的[显示到达权重设置](/help/search-social-commerce/glossary.md#uv)进行加权，或者，根据指定，根据在报表、视图或自定义模拟参数中指定的显示到达估价方法进行加权。

当转化路径包含付费点击和展示次数时，展示次数会因不同的Adobe Advertising产品而异：

* 在Search、Social和Commerce中，[展示覆盖权重](/help/search-social-commerce/glossary.md#i-j)（在广告商的展示覆盖权重设置中以及在报表、视图或自定义模拟参数中指定）首先应用于展示次数。

* 在DSP中，会忽略展示次数，并且只对点击进行加权。 DSP在归因中不考虑展示次数覆盖权重。

![U形归因百分比](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U形归因百分比")

<!-- start examples as collapsible content -->

+++事件计算示例

### 包含所有点击的示例

事件路径：单击1，单击2，单击3，单击4,120美元换算

归因：单击1 = 36 USD，单击2 = 24 USD，单击3 = 24 USD，单击4 = 36 USD（总计120 USD）

### 包含展示和点击的示例

**注意：**&#x200B;展示次数仅适用于显示广告和社交广告。

事件路径： Impression 1、Click 1、Impression 2、Click 2、120美元的转化

#### (仅限搜索、社交和Commerce)使用默认的“展示覆盖权重”10%

由于事件序列既包含展示次数也包含点击次数，因此展示次数覆盖权重适用于展示次数。

归因：展示次数1 = 6 USD，点击次数1 = 54 USD，展示次数2 = 6 USD，点击次数2 = 54 USD（总计120 USD）

#### 使用(仅限DSP)无展示覆盖权重或(仅限搜索、Social和Commerce)0%的“展示覆盖权重”

由于事件系列同时包含展示次数和点击次数，因此会忽略展示次数。

归因：展示次数1 = 0 USD，点击次数1 = 60 USD，展示次数2 = 0 USD，点击次数2 = 60 USD（总计120 USD）

### 具有所有展示的示例

**注意：**&#x200B;仅展示广告的展示次数适用。

事件路径： Impression 1、Impression 2、Impression 3、Impression 4、120美元转化

由于转换是一种显示转换，因此会应用显示转换估价方法（而不是展示次数覆盖权重）来确定每个展示次数的值：

* 如果报表参数指定了加权的显示到达权重，则该权重将应用于展示值。 例如，如果显示到达重量为40%，则单击1 = 14.40 USD，单击2 = 9.60 USD，单击3 = 9.60 USD，单击4 = 14.40 USD（合计48 USD）

* 如果报表参数指定使用显示到达的原始值，则完整的120 USD将在展示次数之间平分：单击1 = 36 USD，单击2 = 24 USD，单击3 = 24 USD，单击4 = 36 USD（总计120 USD）

+++

<!-- end examples as collapsible content -->

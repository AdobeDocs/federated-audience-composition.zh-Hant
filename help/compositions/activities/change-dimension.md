---
audience: end-user
title: 使用變更維度活動
description: 瞭解如何使用變更維度活動
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 41%

---


# 變更維度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="產生補充集"
>abstract="您可以使用剩餘族群 (其已因重複而排除) 產生額外的出站轉變。若要這樣做，請開啟「**產生補充集**」選項"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="變更維度活動"
>abstract="此活動可讓您在建立對象時變更目標定位維度。其會根據資料範本和輸入維度來移動軸。例如，您可以從「合約」維度切換到「客戶」維度。"

此 **變更維度** 活動可讓您在建立對象時變更目標維度。 它會根據資料範本和輸入維度來移動軸。 <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->


## 設定變更維度活動 {#configure}

請依照下列步驟設定 **變更維度** 活動：

1. 新增 **變更維度** 活動至您的構成。

1. 定義 **新增目標維度**. 在維度變更期間，會保留所有記錄。

1. 執行構成以檢視結果。 比較變更維度活動前後表格中的資料，並比較構成表格的結構。

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

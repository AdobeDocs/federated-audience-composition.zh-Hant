---
audience: end-user
title: 使用變更維度活動
description: 瞭解如何使用變更維度活動
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 18%

---


# 變更維度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="產生補集"
>abstract="您可以使用剩餘族群 (其已因重複而排除) 產生額外的出站轉變。若要這樣做，請開啟「**產生補集**」選項"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="變更維度活動"
>abstract="此活動可讓您在建立對象時變更結構（也稱為目標維度）。 它會根據資料範本和輸入結構描述來移動軸。 例如，您可以從「contracts」結構描述切換至「clients」結構描述。"

此 **變更維度** 活動可讓您在建立對象時變更結構（也稱為目標維度）。 它會根據資料範本和輸入結構描述來移動軸。

## 設定變更維度活動 {#configure}

請依照下列步驟設定 **變更維度** 活動：

1. 新增 **變更維度** 活動至您的構成。

   ![](../assets/change-dimension.png)

1. 定義 **新結構描述**. 在方案變更期間，會保留所有記錄。

1. 執行構成以檢視結果。 比較表格之前和之後的資料 **變更維度** 活動，並比較構成表格的結構。

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->
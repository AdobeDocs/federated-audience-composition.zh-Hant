---
audience: end-user
title: 建立組合
description: 瞭解如何建立組合
badge: label="限量開放使用" type="Informative"
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 59%

---

# 建立構成的主要原則 {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="構成屬性"
>abstract="在此畫面中，選擇用於建立構成的範本並指定標籤。展開「其他選項」區段以設定更多設定，例如構成內部名稱、其資料夾、時區和主管群組。強烈建議選取一個主管群組，以便在發生錯誤時警告操作者。"

## 構成內的內容 {#gs-composition-inside}

Experience Platform同盟對象構成提供視覺畫布，可讓您運用各種活動（分割、擴充等）來建立對象。

構成圖是應該發生的表示法。 它會說明要執行的各種任務以及任務如何連結在一起。

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

每個構成都包含：

* **[!UICONTROL 活動]**：活動指要執行的任務。各種活動在圖表中會以圖示表示。每種活動都有特定屬性和所有活動共有的其他屬性。
* **[!UICONTROL 轉變]**：轉變會將來源活動連結到目標活動並定義其序列。
* **[!UICONTROL 工作表]**：工作表包含轉變攜帶的所有資訊。每個構成都使用數個工作表。 這些表格中傳送的資料可在構成生命週期中使用。

## 建立組合的關鍵步驟 {#gs-composition-steps}

建立構成的主要步驟如下：

1. [建立及設定構成](../compositions/create-composition.md)
1. [協調活動](../compositions/orchestrate-activities.md)
1. [執行構成並監視其執行](../compositions/start-monitor-composition.md)

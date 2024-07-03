---
audience: end-user
title: 建立組合
description: 瞭解如何建立組合
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 36%

---


# 構成建立的主要原則 {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="組合屬性"
>abstract="在此畫面中，選擇用來建立構成並指定標籤的範本。 展開「其他OPTIONS」區段來設定更多設定，例如構成內部名稱、資料夾、時區和主管群組。 強烈建議選取一個主管群組，以便在發生錯誤時警告操作者。"

同盟資料構成提供視覺畫布，可讓您運用各種活動（分割、擴充等）來建立對象。

## 構成內有什麼？ {#gs-composition-inside}

構成圖是應該發生的表示法。 它會說明要執行的各種任務以及任務如何連結在一起。

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

每個構成都包含：

* **活動**：活動指要執行的任務。各種活動在圖表中會以圖示表示。每種活動都有特定屬性和所有活動共有的其他屬性。

  在構成圖中，特定活動可產生多個任務，尤其是當有回圈或重複動作時。

* **轉變**：轉變會將來源活動連結到目標活動並定義其序列。

* **工作表**：工作表包含轉變攜帶的所有資訊。每個構成都使用數個工作表。 這些表格中傳送的資料可在構成生命週期中使用。

## 建立組合的關鍵步驟 {#gs-composition-steps}

建立構成的主要步驟如下：

1. [建立構成](#create)
1. [設定構成設定](#starting-audience)
1. [新增和設定活動](#action-activities)
1. [執行構成並監視其執行](#save)
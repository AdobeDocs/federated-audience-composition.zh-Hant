---
audience: end-user
title: 使用查詢建模工具
description: 了解如何使用 查詢 建模器。
source-git-commit: 5d4bdbbb9c903e839b21d22455d870396ac1df7d
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

---

# 使用查詢建模工具 {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="查詢建模工具"
>abstract="定義資料庫中的收件者或任何其他綱要 （也稱為目標維度） 的篩選條件。"

查詢建模器簡化了根據各種條件篩選資料庫的過程。 此外，查詢建模器可以有效地管理非常複雜和冗長的查詢，從而提供增強的靈活性和精度。 此外，它還支持在條件內預先定義的篩選器，使您能夠輕鬆優化查詢，同時利用高級表達式和運算符進行全面的對象 目標定位和細分策略。

## 訪問 查詢 建模器

查詢建模工具適用於每個您需要定義篩選資料的規則的環境。

| 使用方式 | 範例 |
|  ---  |  ---  |
| **定義受眾**：指定要在合成中目標的人口，並毫不費力地創建適合您需求的新受眾。 | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **自定義工作流程活動**：在組合活動中應用規則，例如 **拆分** 和 **對帳**，以符合您的特定要求。 [瞭解有關作曲活動的更多資訊](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## 查詢建模器介面 {#interface}

查詢建模器提供了一個中央画布，您可以在其中版本編號查詢，右窗格提供有關查詢的信息。

![](assets/query-interface.png){zoomable="yes"}

### 中央畫布 {#canvas}

在查詢建模器中央畫布中，您可以添加和組合構建查詢的不同元件。 [了解如何版本編號查詢](build-query.md)

位於畫布右上角的工具列提供了一些選項，用於輕鬆操作查詢元件並在畫布中導航：

* **多個選擇模式**：選擇多個過濾元件以將其複製並粘貼到所選位置。
* **旋轉**：垂直切換畫布。
* **適合螢幕**&#x200B;大小：根據螢幕調整畫布縮放級別。
* **縮放出** / **縮放入**：縮放出或在畫布中。
* **顯示地圖**：打開畫布的快照，顯示您的位置。

### 規則屬性窗格 {#rule-properties}

在右側，“ **[!UICONTROL 規則屬性]** ”窗格提供有關查詢的信息。 它允許您執行各種操作來檢查查詢並確保它適合您的需求。 [了解如何檢查和驗證您的查詢](build-query.md#check-and-validate-your-query)

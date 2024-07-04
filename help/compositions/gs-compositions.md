---
audience: end-user
title: 開始使用組合
description: 瞭解如何開始使用組合
source-git-commit: 0d6930b15be5013b57b8859dd3d21a5d3367ecae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 開始使用組合 {#compositions}

## 什麼是構成？ {#what}

Adobe資料構成可讓您建立構成，其中您可以使用各種活動（分割、排除……）在視覺畫布中建立對象。 完成後，產生的受眾會與現有受眾一併儲存至Adobe Experience Platform中，並可在Journey Optimizer等目的地運用於鎖定客戶。

![](assets/composition-example.png)

## 存取及管理組合 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="構成"
>abstract="在此畫面中，您可以存取組成專案的完整清單、檢查其目前狀態、上次/下次執行日期，以及建立新組成。"

可從Adobe Experience Platform存取組合 **[!UICONTROL 受眾]** 功能表，在 **同盟組合** 標籤。

從這個畫面，您可以建立新組合併存取現有組合。 您也可以按一下現有構成名稱旁的省略符號按鈕，以複製或刪除現有構成。

![](assets/compositions-list.png)

若要精簡清單並輕鬆找到您要尋找的組合，您可以搜尋清單，並依組合的狀態或最後處理日期篩選組合。

您也可以透過新增或移除欄來自訂清單。 若要這麼做，請按一下 **設定欄** s按鈕並新增或移除所需的輸出欄。

![](assets/compositions-columns.png)

## 組合的狀態 {#status}

組合可以有多種狀態：

* **[!UICONTROL 草稿]**：構成已建立並儲存。
* **[!UICONTROL 進行中]**：構成已執行且目前正在執行。
* **[!UICONTROL 已停止]**：構成執行已停止。
* **[!UICONTROL 已暫停]**：構成執行已暫停。
* **[!UICONTROL 錯誤]**：構成執行發生錯誤。 開啟構成並存取日誌和工作以識別錯誤並加以解決。

有關如何啟動和監視構成的詳細資訊，請參閱 [本節](../compositions/start-monitor-composition.md).
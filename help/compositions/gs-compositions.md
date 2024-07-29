---
audience: end-user
title: 開始使用組合
description: 瞭解如何開始使用組合
badge: label="可用性限制" type="Informative"
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 3b891232a3a671f8ec12e06b19086f12ef849f1e
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 10%

---

# 開始使用組合 {#compositions}

## 什麼是構成 {#what}

「Adobe對象構成」可讓您建立構成，其中您可以使用各種活動（分割、排除……）到視覺畫布中建立對象。 完成後，產生的受眾會與現有受眾一併儲存至Adobe Experience Platform中，並可在Adobe Experience Platform目標和Adobe Journey Optimizer中運用於鎖定客戶。 [瞭解如何使用對象](../start/audiences.md)

![](assets/composition-example.png)

## 存取和管理構成 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="構成"
>abstract="在此畫面中，您可以存取構成的完整清單、檢查其目前狀態、上次/下次執行日期並建立新的構成。"

可透過&#x200B;**[!UICONTROL Federated Compositions]**&#x200B;索引標籤中的Adobe Experience Platform **[!UICONTROL Audiences]**&#x200B;功能表存取組合。

從這個畫面，您可以建立新組合併存取現有組合。 您也可以按一下現有構成名稱旁的省略符號按鈕，以複製或刪除現有構成。

![](assets/compositions-list.png)

若要精簡清單並輕鬆找到您要尋找的組合，您可以搜尋清單，並依組合的狀態或最後處理日期篩選組合。

您也可以透過新增或移除欄來自訂清單。 若要這麼做，請按一下**[!UICONTROL 設定資料行]**按鈕，然後新增或移除所需的輸出資料行。

![](assets/compositions-columns.png)

## 組合的狀態 {#status}

組合可以有多種狀態：

* **[!UICONTROL 草稿]**：已建立並儲存構成。
* **[!UICONTROL 進行中]**：構成已經執行，目前正在執行。
* **[!UICONTROL 已停止]**：構成執行已完成並已停止。
* **[!UICONTROL 已暫停]**：構成執行已暫停。
* **[!UICONTROL 錯誤]**：構成執行發生錯誤。 開啟構成並存取日誌和工作以識別錯誤並加以解決。

有關如何啟動和監視組合的詳細資訊，請參閱[本節](../compositions/start-monitor-composition.md)。

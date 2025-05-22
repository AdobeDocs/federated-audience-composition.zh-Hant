---
audience: end-user
title: 開始使用構成
description: 學習如何開始構成
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 90%

---

# 開始使用構成 {#compositions}

>[!AVAILABILITY]
>
>若要存取組合，您需要下列其中一項許可權：
>
>-**管理同盟組合**
>-**檢視同盟組合**
>
>如需必要許可權的詳細資訊，請參閱[Access Federated Audience Composition指南](/help/start/feature-access.md)。

## 什麼是構成 {#what}

Adobe 客群構成允許您建立構成，讓您可以透過視覺化畫布的形式進行各種活動 (分割、排除…)，以建立客群。完成後，產生的客群會與現有客群一起儲存到 Adobe Experience Platform 中，並且可以在 Adobe Experience Platform 目的地和 Adobe Journey Optimizer 中用來鎖定客戶。[學習如何使用客群](../start/audiences.md)

![](assets/composition-example.png)

## 存取和管理構成 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="構成"
>abstract="在此畫面中，您可以存取構成的完整清單、檢查其目前狀態、上次/下次執行日期並建立新的構成。"

您可以透過&#x200B;**[!UICONTROL 聯合構成]**&#x200B;索引標籤中的 Adobe Experience Platform **[!UICONTROL 客群]** 選單存取構成。

在此畫面中，您可以建立新的構成，並存取現有的構成。您也可以按一下現有構成名稱旁邊的省略符號按鈕，以複製或刪除構成。

![](assets/compositions-list.png)

若要縮小清單範圍，並輕鬆找到您想要的構成，您可以搜尋清單，並依狀態或最後處理日期篩選構成。

您也可以透過新增或移除資料欄來自訂清單。若要執行此操作，請按一下 **[!UICONTROL 設定資料欄]** 按鈕，並新增或移除所需的輸出資料欄。

![](assets/compositions-columns.png)

## 構成的狀態 {#status}

構成可以有多種狀態：

* **[!UICONTROL 草稿]**：構成已建立並儲存。
* **[!UICONTROL 進行中]**：構成已執行，且正在執行中。
* **[!UICONTROL 已停止]**：構成已執行完成並停止。
* **[!UICONTROL 暫停]**：構成已暫停執行。
* **[!UICONTROL 錯誤]**：構成執行期間發生錯誤。請開啟構成並存取相關記錄和任務，以找出並解決錯誤。

有關如何開始並監控構成的詳細資訊，請參閱本[章節](../compositions/start-monitor-composition.md)。

---
audience: end-user
title: 建立組合
description: 瞭解如何建立組合
exl-id: 7b9acfc0-99b6-4f83-b774-3652c811868c
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# 編排組合活動 {#activities}

建立構成後，您就可以開始編排將執行的不同任務。 為此，提供了視覺畫布，可讓您建構對象組合圖表。 在此圖表中，您可以新增各種活動，並依序連線它們。

## 新增活動 {#add}

在組態的這個階段中，圖表會顯示起始圖示，代表您組合的開頭。 若要新增您的第一個活動，請按一下連線到開始圖示的&#x200B;**+**&#x200B;按鈕。

可新增至圖表的活動清單隨即顯示。 可用的活動取決於您在構成圖中的位置。 例如，新增第一個活動時，您可以透過鎖定對象、分割構成路徑、設定排程器以延遲構成執行或設定&#x200B;**等待**&#x200B;活動以延遲構成執行來啟動構成。 另一方面，在&#x200B;**建立對象**&#x200B;活動後，您可以使用目標定位活動來調整目標，或使用流量控制活動來組織構成程式。

將活動新增到圖表後，右側窗格會出現，可讓您使用特定設定來設定新新增的活動。 有關如何設定每個活動的詳細資訊，請參閱[本節](activities/about-activities.md)。

![](assets/composition-create-add.png)

重複此程式，根據您希望構成執行的任務，新增所需數量的活動。 請注意，您也可以在兩個活動之間插入新活動。 若要這麼做，請按一下活動之間轉變上的&#x200B;**+**&#x200B;按鈕，選取所需的活動，並在右窗格中設定它。

>[!TIP]
>
>您可以選擇個人化每個活動之間的轉變名稱。 要執行此操作，請選取轉變並在右窗格中變更其標籤。

## 畫布工具列 {#toolbar}

位於畫布右上角的工具列提供可輕鬆操控活動並在畫布中導覽的選項。

![](assets/canvas-toolbar.png)

可用的動作包括：

* **[!UICONTROL 多個選取專案]**：選取多個活動以一次刪除所有活動，或複製並貼上這些活動。 請參閱[本節](#copy)。
* **[!UICONTROL 旋轉]**：垂直切換畫布。
* **[!UICONTROL 符合熒幕大小]**：調整畫布縮放等級以符合熒幕。
* **[!UICONTROL 縮小]** / **[!UICONTROL 放大]**：縮小或進入畫布。
* **[!UICONTROL 顯示地圖]**：開啟顯示您所在位置的畫布快照。

## 管理活動 {#manage}

新增活動時，屬性窗格中會顯示動作按鈕，可讓您執行多項作業。

![](assets/activity-actions.png)

您可以：

* 從畫布中&#x200B;**[!UICONTROL 刪除]**&#x200B;活動。
* **[!UICONTROL 停用]/[!UICONTROL 啟用]**&#x200B;活動。 執行構成時，不會在同一路徑上執行已停用的活動和下列活動，並且會停止構成。
* **[!UICONTROL 暫停]/[!UICONTROL 繼續]**&#x200B;活動。 構成執行時，會在暫停的活動中暫停。 系統不會執行對應的任務，以及在相同路徑中跟隨著該任務的所有任務。
* **[!UICONTROL 複製]**&#x200B;活動以將其貼到構成中的其他位置。 若要這麼做，請按一下轉變上的&#x200B;**+**&#x200B;按鈕，然後選取&#x200B;**[!UICONTROL 貼上X活動]**。<!-- cannot copy multiple activities ? cannot paste in another composition?-->
* 為選取的活動設定&#x200B;**[!UICONTROL 執行選項]**。 展開以下區段以進一步瞭解可用的選項。

  +++可用的執行選項

  **[!UICONTROL 屬性]**&#x200B;區段可讓您設定有關活動執行的一般設定：

   * **[!UICONTROL 執行]**：定義啟動時要執行的動作。
   * **[!UICONTROL 最長執行期間]**：指定期間，例如&quot;30s&quot;或&quot;1h&quot;。 如果活動在指定的持續時間過後仍未完成，則會觸發警報。 這不會影響組成功能的方式。
   * **[!UICONTROL 時區]**：選取活動的時區。 同盟對象構成可讓您在同一例項上管理多個國家/地區之間的時間差異。 套用的設定會在建立執行個體時進行設定。
   * **[!UICONTROL 相似性]**：強制構成活動在特定電腦上執行。 若要這麼做，您必須為相關活動指定一或多個相關性。
   * **[!UICONTROL 行為]**：定義使用非同步工作時要遵循的程式。

  **[!UICONTROL 錯誤管理]**&#x200B;區段可讓您指定活動發生錯誤時要執行的動作。

  **[!UICONTROL 初始化指令碼]**&#x200B;區段可讓您初始化變數或修改活動屬性。 按一下&#x200B;**[!UICONTROL 編輯程式碼]**&#x200B;按鈕，然後輸入要執行的程式碼片段。 當活動執行時，會呼叫指令碼。

  +++

* 存取活動的&#x200B;**記錄檔與工作**。

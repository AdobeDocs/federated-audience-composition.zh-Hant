---
audience: end-user
title: 建立組合
description: 瞭解如何建立組合
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 9%

---


# 建立並執行組合 {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="工作流程屬性"
>abstract="在此畫面中，選擇用於建立工作流程的範本並指定標籤。展開「其他選項」區段以設定更多設定，例如工作流程內部名稱、其資料夾、時區和主管群組。強烈建議選取一個主管群組，以便在發生錯誤時警告操作者。"

## 建立構成 {#create}

若要建立構成，請執行下列步驟：

1. 存取 **[!UICONTROL 受眾]** 功能表並選取 **[!UICONTROL 同盟組合]** 標籤。

1. 按一下 **[!UICONTROL 建立組合]** 按鈕。

1. 在 **[!UICONTROL 屬性]** 區段，指定組合的標籤，然後按一下 **[!UICONTROL 建立]**.

1. 組合畫布隨即顯示。 您現在可以在執行構成之前，視需要新增任意數量的活動以符合您的需求，進而設定構成。 您還可以配置其他設定，例如構成標籤或與在構成執行時的錯誤管理相關的選項。

請在以下章節瞭解更多資訊：

* [設定構成設定](#starting-audience)
* [新增活動](#action-activities)
* [執行構成並監視其執行](#save)

## 設定構成設定 {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="組合屬性"
>abstract="本節提供建立構成時也可以存取的一般構成屬性。"

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="組合分段"
>abstract="依預設，僅保留構成的最後一次執行的工作表。 您可以啟用此選項來保留工作表格以進行測試。 必須使用 **僅限** 在開發或中繼環境中。 在生產環境中絕對不可將其存回。"

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="錯誤管理設定"
>abstract="您可以在此段落中定義如何管理執行期間的錯誤。 您可以選擇暫停程式、忽略特定數目的錯誤，或停止構成執行。"

按一下 **設定** 按鈕以存取構成的其他選項：

* **[!UICONTROL 標籤]**：變更構成標籤。

* **[!UICONTROL 保留兩次執行之間的中期母體結果]**：依預設，僅保留構成的最後一次執行的工作表。 技術工作流程會清除先前執行的工作表，每天都執行。

  如果啟用此選項，即使執行構成後，也會保留工作表格。 您可以將其用於測試目的，因此必須使用 **僅限** 在開發或中繼環境中。 絕不可在生產工作流程中勾選該專案。

* **[!UICONTROL 錯誤管理]**：此區段可讓您定義構成活動發生錯誤時應採取的動作。 有三個可能的選項：

   * **[!UICONTROL 暫停處理序]**：構成會自動暫停，其狀態會變更為 **[!UICONTROL 已失敗]**. 問題解決後，請使用 **[!UICONTROL 繼續]** 按鈕。
   * **[!UICONTROL 忽略]**：觸發錯誤的工作狀態會變更為 **[!UICONTROL 已失敗]**，但構成會保留 **[!UICONTROL 已開始]** 狀態。
   * **[!UICONTROL 中止處理序]**：構成會自動停止，其狀態會變更為 **[!UICONTROL 已失敗]**. 問題解決後，請使用 **[!UICONTROL 開始]** 按鈕。

* **[!UICONTROL 連續錯誤]**：指定程式停止前可忽略的錯誤數。 達到此數字後，構成狀態會變更為 **[!UICONTROL 已失敗]**. 如果此欄位的值為0，則無論錯誤數量如何，構成都不會停止。

## 新增活動 {#activities}

構成畫布可讓您設定在構成中視需要新增許多活動，以符合您的需求。

若要這麼做，請按一下構成路徑上的+按鈕，然後新增所需的活動。 右側窗格隨即開啟，可讓您設定新新增的活動。 [進一步瞭解構成中的活動以及如何進行設定](../compositions/activities/about-activities.md)

若要從畫布移除活動，請選取該活動，然後按一下右窗格中的刪除按鈕。 如果要刪除的活動是構成中其他活動的父項，則會顯示一則訊息，允許您指定是隻刪除所選活動，還是刪除其所有子活動。

## 執行構成 {#execute}

構成準備就緒後，按一下 **[!UICONTROL 開始]** 按鈕來執行，並將產生的對象儲存到Adobe Experience Platform中。 「您可以使用監控工作流程的執行 **記錄檔** 按鈕。 有三個索引標籤可協助您監視執行：

* **[!UICONTROL 記錄檔]**：
* **[!UICONTROL 任務]**：
* **[!UICONTROL 變數]**：

---
audience: end-user
title: 開始使用組合
description: 瞭解如何開始使用組合
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 8%

---

# 開始使用組合 {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="組合屬性"
>abstract="本節提供建立構成時也可以存取的一般構成屬性。"

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="組合分段"
>abstract="依預設，僅保留構成的最後一次執行的工作表。 您可以啟用此選項來保留工作表格以進行測試。 必須使用 **僅限** 在開發或中繼環境中。 在生產環境中絕對不可將其存回。"




## 什麼是組合？ {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="構成"
>abstract="在此畫面中，您可以存取組成專案的完整清單、檢查其目前狀態、上次/下次執行日期，以及建立新組成。"


## 錯誤管理設定  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="錯誤管理設定"
>abstract="您可以在此段落中定義如何管理執行期間的錯誤。 您可以選擇暫停程式、忽略特定數目的錯誤，或停止構成執行。"

* **[!UICONTROL 錯誤管理]**：此欄位可讓您定義構成活動發生錯誤時應採取的動作。
有三個可能的選項：

   * **[!UICONTROL 暫停處理序]**：構成會自動暫停，其狀態會變更為 **[!UICONTROL 已失敗]**. 問題解決後，請使用 **[!UICONTROL 繼續]** 按鈕。
   * **[!UICONTROL 忽略]**：觸發錯誤的工作狀態會變更為 **[!UICONTROL 已失敗]**，但構成會保留 **[!UICONTROL 已開始]** 狀態。
   * **[!UICONTROL 中止處理序]**：構成會自動停止，其狀態會變更為 **[!UICONTROL 已失敗]**. 問題解決後，請使用 **[!UICONTROL 開始]** 按鈕。

* **[!UICONTROL 連續錯誤]**：此欄位可在下列情況下使用 **[!UICONTROL 忽略]** 值選取於 **[!UICONTROL 發生錯誤時]** 欄位。 您可以指定程序停止之前可以忽略的錯誤數。達到此數字後，構成狀態會變更為 **[!UICONTROL 已失敗]**. 如果此欄位的值為0，則無論錯誤數量如何，構成都不會停止。

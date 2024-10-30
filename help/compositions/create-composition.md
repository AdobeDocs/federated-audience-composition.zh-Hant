---
audience: end-user
title: Create compositions
description: Learn how to create compositions
badge: label="可用性限制" type="Informative"
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: bd3223a77f490a43487e21662d8f766d4f9b06fc
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 21%

---

# 建立和設定構成 {#create}

建立構成的第一步是定義其標籤，並視需要設定其他設定。

## Create the composition {#create-the-composition}

1. ********

1. ****

   ![](assets/composition-create.png)

1. **** Only the schemas associated to this data model will be available in your composition&#39;s activities.

   ![](assets/composition-select-schema.png)

1. 按一下 **[!UICONTROL 建立]**。The composition canvas displays. You can now configure your composition by adding as many activities as needed to suit your needs before executing it:

   * [Learn how to orchestrate activities](orchestrate-activities.md)
   * [](start-monitor-composition.md)

## 進行構成設定 {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="構成屬性"
>abstract="本區段提供一般構成屬性，在建立構成時也可以存取這些屬性。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="構成分段"
>abstract="依預設，只保留最後一次執行構成的工作表。您可以啟用此選項以保留工作表格用於測試目的。它必須&#x200B;**僅**&#x200B;在開發或中繼環境中使用。絕不能在生產環境中進行檢查。"

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="錯誤管理設定"
>abstract="在此區段中，您可以定義執行期間應如何管理錯誤。您可以選擇暫停流程、忽略一定數量的錯誤，或是停止構成執行。"

When accessing a composition, you can access advanced settings that allow you, for example, to define how the composition should behave in case of error. ****

![](assets/composition-create-settings.png)

Available settings are as follows:

* **[!UICONTROL 標籤]**：變更構成標籤。

* **[!UICONTROL 保留兩個執行之間的臨時母體結果]**：依預設，僅保留構成的最後一個執行的工作表。 Working tables from previous executions are purged by a technical composition, which runs on a daily basis.

  If this option is enabled, working tables will be kept even after the composition has been executed. **** It must never be checked in a production composition.

* **** There are three possible options:

   * ************
   * ************
   * ************

* **[!UICONTROL 連續錯誤]**：指定程式停止前可忽略的錯誤數目。 一旦達到此數目，構成狀態就會變更為&#x200B;**[!UICONTROL 失敗]**。 如果此欄位的值為0，則無論錯誤數量如何，構成都不會停止。

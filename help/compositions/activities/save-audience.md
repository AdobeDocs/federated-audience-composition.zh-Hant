---
audience: end-user
title: 使用儲存對象活動
description: 瞭解如何使用「儲存對象」活動
source-git-commit: c151cc316eb9b5df6fa1d09f01455313195dfd07
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 12%

---


# 儲存對象 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="儲存一個對象"
>abstract="使用此活動可更新現有的對象，或是從構成中的母體運算上游建立新的對象。 建立的對象將新增至對象清單中，並可透過「**對象**」選單使用。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="產生傳出轉變"
>abstract="如果您想在「**儲存對象**」活動之後新增轉變，請使用此選項。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="主要身分欄位"
>abstract="選取要用於設定檔的主要身分。"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="在Experience Platform檔案中瞭解更多"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="身分命名空間"
>abstract="選取要用於設定檔的名稱空間。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces" text="在Experience Platform檔案中瞭解更多"

此 **儲存對象** 活動可讓您更新現有的對象，或是從構成中的母體運算上游建立新的對象。 建立的對象會新增至應用程式對象清單，並可透過 **受眾** 功能表。

此活動主要用於將母體族群轉換為可重複使用的對象，讓母體族群可繼續在相同構成中運算。 將其連線到其他目標定位活動，例如 **建立對象** 或 **合併** 活動。

## 設定「儲存對象」活動 {#save-audience-configuration}

請依照下列步驟設定 **儲存對象** 活動：

1. 新增 **儲存對象** 活動至您的構成。

   ![](../assets/save-audience.png)

1. 指定要建立的對象標籤。

1. 按一下 **新增對象對應** 然後選擇來源和目標受眾欄位：

   * **Source對象欄位**：
   * **目標對象欄位**：

   重複此作業，視需要儘量新增對象對應。

1. 選取主要身分和名稱空間，以用於識別資料庫中的目標設定檔：

   * **主要身分欄位**：選取要用來識別設定檔的欄位。 例如，其電子郵件地址或電話號碼。
   * **身分名稱空間**：選取用來識別設定檔的名稱空間，也就是要用來作為識別索引鍵的資料型別。 例如，如果已選取電子郵件地址作為主要身分欄位，則身分名稱空間 **電子郵件** 應選取。 如果唯一識別碼是電話號碼，則為身分名稱空間 **電話** 應選取。

執行構成後，產生的對象會儲存在Adobe Experience Platform中，並可在中存取 **受眾** 功能表。

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->

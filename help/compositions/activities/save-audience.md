---
audience: end-user
title: 使用儲存對象活動
description: 瞭解如何使用分叉活動
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
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

1. 在 **模式** 在下拉式清單中，選取您要執行的動作：

   * **建立或更新現有對象**：定義 **對象標籤**. 如果對象已存在，則會更新，否則將建立新對象。

   * **更新現有的對象**：選擇 **對象** 您要在現有對象清單中進行更新。

1. 選取 **更新模式** 將套用至現有受眾：

   * **以新資料取代受眾內容**：所有對象內容都會被取代。 遺失舊資料。僅保留儲存對象活動之入站轉變的資料。 此選項會清除更新對象的對象型別和目標定位維度。

   * **使用新資料完成對象**：保留舊的對象內容，並新增儲存對象活動入站轉變的資料。

1. 檢查 **產生出站轉變** 選項(如果您想要在 **儲存對象** 活動。

之後著，儲存的對象內容便可在對象的詳細資料檢視中使用，您可從以下位置存取： **受眾** 功能表。 此檢視中可用的欄會與的入站轉變的欄相對應 **儲存對象** 活動。

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->

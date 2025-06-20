---
audience: end-user
title: 使用儲存設定檔活動
description: 瞭解如何使用儲存設定檔活動
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: ca975be136155f69bc84362fde8c283b1c4edffe
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 18%

---

# 儲存輪廓 {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="儲存輪廓"
>abstract="「儲存輪廓」活動，能夠與外部倉儲的資料聯合，擴充 Experience Platform 輪廓，並允許使用其他屬性增強客戶輪廓。 "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="選取Experience Platform結構描述"
>abstract="選擇輪廓的 Experience Platform 結構描述。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="選取主要身分識別欄位"
>abstract="選取主要身分識別，以識別資料庫中的目標輪廓。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="選取Experience Platform結構描述"
>abstract="選擇輪廓的 Experience Platform 結構描述。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="儲存設定檔更新模式"
>abstract="儲存設定檔活動的可用更新模式包括完整更新和增量更新。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="完整更新"
>abstract="完整更新模式會更新擴充的完整設定檔集。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="增量更新"
>abstract="增量更新模式會更新自上次擴充執行以來修改的設定檔。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="主要身分識別欄位"
>abstract="主要身分欄位會指出將設定檔合併在一起以進行擴充時的真實來源。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="必要欄位條件"
>abstract="必要欄位是在匯出資料時，必須為每個設定檔或記錄填寫的屬性。 如果缺少必填欄位，匯出將無法完成或有效。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="主要身分欄位條件"
>abstract="每個設定檔或記錄的唯一識別碼。 這樣可確保每個記錄都能被清楚辨識和比對，避免重複資料。"

**儲存設定檔**&#x200B;活動可讓您使用從外部倉儲同盟的資料，擴充Adobe Experience Platform設定檔。

此活動通常用於透過引進其他屬性和深入分析來增強客戶設定檔，而不會將資料實際移動或複製到平台中。

## 設定儲存設定檔活動 {#save-profile-configuration}

請依照下列步驟設定&#x200B;**儲存設定檔**&#x200B;活動：

1. 將&#x200B;**儲存設定檔**&#x200B;活動新增至您的組合。

   ![](../assets/save-profile.png)

1. 指定要建立的設定檔標籤。

   >[!IMPORTANT]
   >
   >對象標籤在目前沙箱中必須是唯一的。 其標籤不得與任何現有對象相同。

1. 選取您要使用的Adobe Experience Platform結構描述。

   ![](../assets/save-profile-2.png)

1. 選擇用於識別資料庫中設定檔的主要身分欄位。

1. 如果要調解其他資料屬性，請按一下[新增屬性]。**&#x200B;**

   然後，針對您要對應的每個屬性，指定&#x200B;**Source**&#x200B;欄位（外部資料）和&#x200B;**目的地**&#x200B;欄位（結構描述欄位）。

   ![](../assets/save-profile-3.png)

1. 設定之後，按一下&#x200B;**開始**。

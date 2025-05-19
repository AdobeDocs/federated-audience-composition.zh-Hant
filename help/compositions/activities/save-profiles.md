---
audience: end-user
title: 使用儲存設定檔活動
description: 瞭解如何使用儲存設定檔活動
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: fae57356b8e9f5358a39d31cad4883171a310fb6
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 29%

---

# 儲存輪廓 {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="儲存設定檔"
>abstract="儲存設定檔活動可讓您透過聯合外部倉儲的資料來擴充 Experience Platform 設定檔，進而使用其他屬性來增強客戶設定檔。 "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="選取 AEP 結構描述"
>abstract="選擇設定檔的 Experience Platform 結構描述。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="選取主要身分識別欄位"
>abstract="選取主要身分識別，以用於在資料庫中識別目標設定檔。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="選取 AEP 結構描述"
>abstract="選擇設定檔的 Experience Platform 結構描述。"

**儲存設定檔**&#x200B;活動可讓您使用從外部倉儲同盟的資料，擴充Adobe Experience Platform設定檔。

此活動通常用於透過引進其他屬性和深入分析來增強客戶設定檔，而不會將資料實際移動或複製到平台中

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

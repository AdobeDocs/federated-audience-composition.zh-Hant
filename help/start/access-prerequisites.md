---
title: 聯合客群構成的先決條件和護欄
description: 了解聯合客群構成的先決條件、權限和護欄
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
TQID: https://experienceleague.adobe.com/VBIotVn1VyiFJChb3mM0VDLUSbG9aQOmbfGnfGgqvhU
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: tm+mt
source-wordcount: 386
ht-degree: 100%

---

# 先決條件和護欄 {#fac-access}

聯合客群構成需要 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer **Prime** 或 **Ultimate** 套件。 若要存取此功能，您必須已購買聯合客群構成附加元件。

>[!AVAILABILITY]
>
>在您收到 Adobe 的歡迎電子郵件通知後，可能需要等候幾個小時，才能看到更新的介面並使用相關功能。

## 支援的系統 {#supported-systems}

聯合客群構成支援下列雲端倉儲：

* Amazon Redshift
* Azure Synapse
* Databricks
* Google BigQuery
* Snowflake
* Vertica Analytics
* Microsoft Fabric

您可以在[連線總覽](../connections/home.md)中，瞭解如何建立和這些系統之前的連線。

## 沙箱

購買聯合客群構成後，您有權使用兩個沙箱。 若有任何額外的沙箱佈建請求，請聯絡您的 Adobe 代表。

若要檢視使用中的聯合客群構成清單，請依照下列步驟操作：

1. 從聯合客群構成中，存取「**[!UICONTROL 管理]**」下方的「**[!UICONTROL 授權使用量]**」選單。

1. 請從&#x200B;**[!UICONTROL 資料輸入的總體積]**，選取 ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) 圖示 ，方便存取您的沙箱屬性。

   ![](assets/sandbox_1.png)

1. 您沙箱的相關資訊會顯示在「屬性」彈出提示框中。

   ![](assets/sandbox_2.png)

## 權限 {#permissions}

若要存取聯合客群構成，您必須將使用者新增至購買時所建立的沙箱特定產品設定檔中，並為其指派「**[!UICONTROL 管理聯合資料]**」權限。 [了解更多](/help/governance-privacy-security/access-control.md)

## IP 允許清單 {#ip}

若要安全地啟用聯合客群構成來存取您的資料庫，您必須授權將存取這些資料庫的聯合客群構成伺服器的 IP 位址。 在 Adobe Experience Platform 使用者介面中新增聯合資料庫時，這些 IP 位址便會顯示。 [了解更多](../connections/home.md)

將這些 IP 位址新增至您的允許清單，以授予聯合客群構成的存取權。

## 合併原則 {#merge-policies}

如果您的沙箱使用&#x200B;**資料集優先順序**&#x200B;合併原則，請聯絡 Adobe 客戶服務以將 `Halos UPS` 資料集新增至您的合併原則。

如需有關合併原則的詳細資訊，請參閱[合併原則概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/merge-policies/overview)。

## 護欄與限制 {#fac-guardrails}

* [Adobe Real-Time Customer Data Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails){target="_blank"}中列出的權益、產品限制及效能護欄，均適用於聯合客群構成。

* 聯合客群構成支援匯出大量客群，檔案大小可大於 1GB。 為了獲得最佳效能，建議的檔案大小上限為 20GB。

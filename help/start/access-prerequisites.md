---
title: 聯合客群構成的先決條件和護欄
description: 了解聯合客群構成的先決條件、權限和護欄
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 97bda9d08eead79e6172e3b5bb746e7516bf6d85
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 83%

---

# 先決條件和護欄 {#fac-access}

聯合客群構成需要 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer **Prime** 或 **Ultimate** 套件。若要存取此功能，您必須已購買聯合客群構成附加元件。

>[!AVAILABILITY]
>
>在您收到 Adobe 的歡迎電子郵件通知後，可能需要等候幾個小時，才能看到更新的介面並使用相關功能。

## 支援的系統 {#supported-systems}

聯合客群構成支援下列雲端倉儲：

* Amazon Redshift
* Azure Synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics
* Microsoft Fabric

若要了解如何建立與這些系統的連線，請參閱[此頁面](../connections/connections.md)。

## 沙箱

購買聯合客群構成後，您有權使用兩個沙箱。若有任何額外的沙箱佈建請求，請聯絡您的 Adobe 代表。

若要檢視使用中的同盟對象構成沙箱清單，請遵循下列步驟：

1. 從Federated Audience Composition，存取&#x200B;**[!UICONTROL 管理]**&#x200B;下的&#x200B;**[!UICONTROL 授權使用情況]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 資料輸出總量]**&#x200B;中的![](assets/do-not-localize/Smock_InfoOutline_18_N.svg)圖示以存取您的沙箱屬性。

   ![](assets/sandbox_1.png)

1. 「屬性」彈出視窗中顯示沙箱的相關資訊。

   ![](assets/sandbox_2.png)

## 權限 {#permissions}

若要存取聯合客群構成，您必須將使用者新增至購買時所建立的沙箱特定產品設定檔中，並為其指派「**[!UICONTROL 管理聯合資料]**」權限。[了解更多](feature-access.md)

## IP 允許清單 {#ip}

若要安全地啟用聯合客群構成來存取您的資料庫，您必須授權將存取這些資料庫的聯合客群構成伺服器的 IP 位址。在 Adobe Experience Platform 使用者介面中新增聯合資料庫時，這些 IP 位址便會顯示。[了解更多](../connections/connections.md)

將這些 IP 位址新增至您的允許清單，以授予聯合客群構成的存取權。

## 護欄和限制 {#fac-guardrails}

* 聯合客群構成目前不適用於[攝取健康資料](https://experienceleague.adobe.com/zh-hant/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}的客戶。[了解更多](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* [Adobe Real-Time Customer Data Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails){target="_blank"}中列出的權益、產品限制及效能護欄均適用於聯合客群構成。

<!--* Federated Audience Composition supports the export of large audiences, with file sizes greater than 1 GB. For optimal performance, the maximum recommended file size is up to 20 GB.
-->


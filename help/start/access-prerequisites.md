---
title: 聯合客群構成的先決條件和護欄
description: 了解聯合客群構成的先決條件、權限和護欄
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: ht
source-wordcount: '305'
ht-degree: 100%

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

若要了解如何建立與這些系統的連線，請參閱[此頁面](../connections/connections.md)。

## 權限 {#permissions}

當您購買聯合客群構成附加元件時，系統會為當時的每個使用中沙箱建立一個產品設定檔。此產品設定檔是在 Admin Console 中的 **Adobe Experience Platform** 產品卡下方建立，並遵循以下命名慣例：`ACP_FAC - <<SandboxName>> - admin.`。若要存取特定沙箱的聯合客群構成，您必須將使用者新增至為該沙箱建立的產品設定檔中。

例如，如果啟用名為「fac-test」的新沙箱，則會建立對應的產品設定檔「ACP_FAC - fac-test - admin」。為了使用此沙箱存取聯合客群構成，您必須將使用者新增至此產品設定檔。

## IP 允許清單 {#ip}

若要安全地啟用聯合客群構成來存取您的資料庫，請聯絡您的 Adobe 代表以取得將存取這些資料庫的聯合客群構成伺服器的 IP 位址。

將這些 IP 位址新增至您的允許清單，以授予聯合客群構成的存取權。

## 護欄和限制 {#fac-guardrails}

* 聯合客群構成目前不適用於[攝取健康資料](https://experienceleague.adobe.com/zh-hant/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}的客戶以及 Adobe Journey Optimizer Privacy and Security Shield 客戶。[了解更多](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}。

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* [Adobe Real-Time Customer Data Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails){target="_blank"}中列出的權益、產品限制和效能護欄均適用於此附加元件。

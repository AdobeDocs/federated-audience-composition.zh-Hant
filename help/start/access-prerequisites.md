---
title: 同盟對象構成的先決條件和護欄
description: 瞭解同盟對象構成的先決條件、許可權和護欄
badge: label="限量開放使用" type="Informative"
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 13%

---

# 先決條件和安全護欄 {#fac-access}

同盟對象構成需要Adobe Real-time Customer Data Platform和/或Adobe Journey Optimizer **Prime**&#x200B;或&#x200B;**Ultimate**&#x200B;套件。 若要存取此功能，您必須已購買Federated Audience Composition附加元件。

>[!AVAILABILITY]
>
>在您收到 Adobe 的歡迎電子郵件通知後，可能還需要等幾個小時，才能看到新版介面並使用相關功能。

## 權限 {#permissions}

當您購買Federated Audience Composition附加元件時，產品設定檔會於當時為每個使用中的沙箱建立。 此產品設定檔是在&#x200B;**Adobe Experience Platform**&#x200B;產品卡下的Admin Console中建立的，並遵循以下命名慣例： `ACP_FAC - <<SandboxName>> - admin.`若要存取特定沙箱的Federated Audience Composition，必須將使用者新增至為該沙箱建立的產品設定檔。

例如，如果啟動名為「fac-test」的新沙箱，則會建立對應的產品設定檔「ACP_FAC - fac-test - admin」。 若要使用此沙箱存取同盟對象構成，必須將使用者新增至此產品設定檔。

## IP允許清單 {#ip}

若要安全地啟用同盟受眾構成以存取您的資料庫，請聯絡您的Adobe代表，以取得將存取這些資料庫的同盟受眾構成伺服器的IP位址。

將這些IP位址新增至您的允許清單，以授與同盟對象構成的存取權。」

## 護欄和限制 {#fac-guardrails}

* 同盟受眾構成與Privacy &amp; Security Shield相容，可用於除醫療保健產業外的所有垂直產業。 目前，同盟對象構成無法授權給想要擷取健康情況資料的客戶。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* [Adobe Real-time Customer Data Platform檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails){target="_blank"}中列出的權益、產品限制和效能護欄適用於此附加元件。

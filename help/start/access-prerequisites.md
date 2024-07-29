---
title: 存取同盟對象構成
description: 瞭解如何存取同盟對象構成。
badge: label="可用性限制" type="Informative"
source-git-commit: 618d1675c28213d7a316f40cd624d282e01297f1
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# 存取同盟對象構成 {#fac-access}

## 套件和附加元件 {#package}

同盟對象構成需要Adobe Real-time Customer Data Platform和Adobe Journey Optimizer Prime或Ultimate套件。 若要存取此功能，您必須已購買Federated Audience Composition附加元件。

>[!AVAILABILITY]
>
>收到Adobe的歡迎電子郵件通知後，您可能需要幾個小時才能更新介面以及您可以使用的功能。

## 權限 {#permissions}

當您購買Federated Audience Composition附加元件時，產品設定檔會於當時為每個使用中的沙箱建立。 此產品設定檔是在&#x200B;**Adobe Experience Platform**&#x200B;產品卡下的Admin Console中建立的，並遵循以下命名慣例： `ACP_FAC - <<SandboxName>> - admin.`若要存取特定沙箱的Federated Audience Composition，必須將使用者新增至為該沙箱建立的產品設定檔。

例如，如果啟動名為「fac-test」的新沙箱，則會建立對應的產品設定檔「ACP_FAC - fac-test - admin」。 若要使用此沙箱存取同盟對象構成，必須將使用者新增至此產品設定檔。

## IP允許清單 {#ip}

您的IP位址必須新增至允許清單，才能啟用對資料倉儲的存取權並使用同盟對象構成。 若要將您的IP位址新增至允許清單，請聯絡您的Adobe代表。

## 護欄和限制 {#fac-guardrails}

* 同盟受眾構成與Privacy &amp; Security Shield相容，可用於除醫療保健產業外的所有垂直產業。 目前，同盟對象構成無法授權給想要擷取健康情況資料的客戶。 [了解更多](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* [Adobe Real-time Customer Data Platform檔案](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"}中列出的權益、產品限制和效能護欄適用於此附加元件。

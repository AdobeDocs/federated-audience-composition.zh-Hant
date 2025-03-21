---
title: Experience Platform 聯合客群構成的新增功能
description: 最新更新和發行說明
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 0b8781b5b33d96db7d7f23b3c399942b9cfe901f
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 93%

---

# 發行說明 {#rn-new}

[!DNL Federated Audience Composition]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都已整合在這些發行說明中。[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Federated Audience Composition] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}。

## 2025 年 2 月發行版本 {#fac-25-2}

此發行版本隨附下列變更。

* **Microsoft Fabric 支援**

  您現在可以透過聯合客群構成，建立與 Microsoft Fabric 資料庫的連線。[了解更多](../connections/federated-db.md)

* **Amazon Redshift Spectrum 支援**

  對 Amazon Redshift 資料庫的連線現已支援 Amazon Redshift Spectrum。[了解更多](../connections/federated-db.md#amazon-redshift)

* **增強的結構描述建立體驗**

  透過更新後的使用者介面，建立結構描述的程序已獲得改進，變得更直覺且更易於導覽。這些增強功能為資料從業人員提供了更順暢、更有效率的資料模型開發方法。[了解更多](../customer/schemas.md)

* **Databricks 的客群擴充支援**

  您現在可以在「讀取客群」流程中使用 Databricks，為 Databricks 資料庫啟用活動並允許將其設定為新目的地。[了解更多](../connections/destinations.md)

<!--
* **Federated Audience Composition permissions**

    Starting March release, [!DNL Federated Audience Composition] will start enforcing the access of **Federated data management** and **Federated Compositions** interfaces to user who have been granted the **Manage Federated Data** permission. 

    We recommend users to contact the administrators to have this permission added to their role in order to continue accessing the [!DNL Federated Audience Composition] user interface.

    To learn how to assign this permission, refer to the [detailed documentation](feature-access.md).
-->

## 2024 年 11 月發行版本 {#fac-24-11}

### 改進項目 {#fac-24-11-improvements}

此發行版本隨附以下改進項目。

* **IP 位址允許清單**

  在 Adobe Experience Platform 使用者介面中新增聯合資料庫時，您現在可以直接檢視與聯合客群構成執行個體關聯的 IP 位址。這可讓您輕鬆複製和授權這些 IP 以連接到您的資料庫，從而提高安全性和靈活性。[了解更多](../connections/connections.md)

## 2024 年 10 月發行版本 {#fac-24-10}

>[!AVAILABILITY]
>
>Adobe Experience Platform 聯合客群構成先前僅開放給某些組織使用 (LA)，現已向所有使用者開放 (GA)。此功能是根據您的產品而啟動，且僅會顯示相關的許可權。 [了解更多](access-prerequisites.md)
>

### 相容性 {#fac-24-10-compat}

在這個新版本中，聯合客群構成現在可與下列系統相容。

* **Databricks 支援**

  您現在可以透過聯合客群構成，建立與 Databricks 資料庫的連線。[了解更多](../connections/federated-db.md#databricks)

* **支援透過 AWS PrivateLink 安全地存取 Snowflake**

  現在支援透過私人連結，安全地存取外部 Snowflake 資料倉儲。請注意，您的 Snowflake 帳戶必須託管在 Amazon Web Services (AWS) 上，並且與您的聯合客群構成環境位於同一區域。請聯絡您的 Adobe 代表，協助您設定 Snowflake 帳戶的安全存取權。[了解更多](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless 支援**

  在這個新版本中，聯合客群構成支援 [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}。

### 改進項目 {#fac-24-10-improvements}

此發行版本隨附下列改進項目。

* **重新整理現有結構描述**

  當在聯合資料庫中建立、修改或刪除欄時，您現在可以透過按一下對應結構描述中的「**[!UICONTROL 重新整理結構描述]**」按鈕來偵測並套用變更。[了解更多](../customer/schemas.md#schema-refresh)

* **將資料模型與新構成相關聯**

  建立構成時，您現在可以選取與其關聯的資料模型。透過這個新選項，您的活動設定會更加容易，因為只有關聯資料模型的表格可以使用。[了解更多](../compositions/create-composition.md)

## 2024 年 7 月發行版本 - 聯合客群構成 (LA) {#fac-la}

同盟受眾構成可讓企業透過彈性且擴充的存取方式存取企業資料倉儲，以使用關鍵企業資料集和強大的品牌啟動及即時體驗來構成受眾。 有了這種新方法，身為 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/home){target="_blank"} 和/或 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/ajo-home){target="_blank"} 使用者，您就可以直接聯合現有資料倉儲中的客群資料，在一個系統中擴充 Adobe Experience Platform 客群。

對於需要靈活地使用倉庫資料集來構成客群的企業，聯合客群構成恰好滿足了他們不斷增長的市場需求。這使得企業能夠減少資料移動，同時向行銷團隊提供關鍵客群資料，以滿足使用案例要求並提升個人化體驗。 

如需有關聯合客群構成功能的詳細資訊，請參閱[此頁面](get-started.md)和[常見問題](faq.md)。

如需存取聯合客群構成的先決條件和目前護欄的詳細資訊，請參閱[此頁面](access-prerequisites.md)。


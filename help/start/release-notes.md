---
title: Experience Platform 聯合客群構成的新增功能
description: 最新更新和發行說明
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 90%

---

# 發行說明 {#rn-new}

[!DNL Federated Audience Composition]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都已整合在這些發行說明中。[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Federated Audience Composition] 延續了最新版本的創新和改進內容。 在[Adobe Experience Platform發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}中進一步瞭解這些變更。

## 2025 年 3 月版 {#fac-25-3}

### 改進項目 {#fac-25-3-improvements}

此版本包含下列改進項目。

* **聯合客群構成權限**

  從 3 月版開始，[!DNL Federated Audience Composition] 將會強制已獲得&#x200B;**管理聯合資料**&#x200B;權限的使用者存取&#x200B;**聯合資料管理**&#x200B;和&#x200B;**聯合構成**&#x200B;的介面。

  我們建議使用者聯絡管理員將此權限新增至他們的角色中，以便繼續存取 [!DNL Federated Audience Composition] 使用者介面。

  若要了解如何指派此權限，請參閱[詳細文件](feature-access.md)。

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    The AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. 
-->


### 相容性 {#fac-25-3-compat}

* **Databricks 連線**

  透過此一新版本，聯合客群構成現在支援透過私人連結進行 Databricks 資料庫連線，這包括透過私人連結與託管在 Amazon Web Services (AWS) 上的 Databricks 資料庫建立安全連線，以及透過 VPN 與託管在 Microsoft Azure 上的 Databricks 資料庫建立安全連線。[了解更多](../connections/federated-db.md#databricks)

* **為 B2B CDP 客戶提供支援**

  企業對企業 (B2B) 客戶資料平台 (CDP) 的客戶現在可以使用聯合客群構成來處理人員型客群使用案例。

* **Snowflake 安全連線**

  透過此一新版本，聯合客群構成現在支援使用私人連結連線至託管在 Microsoft Azure 上的 Snowflake 資料庫連線。[了解更多](../connections/federated-db.md#snowflake)

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

## 2024 年 11 月發行版本 {#fac-24-11}

### 改進項目 {#fac-24-11-improvements}

此發行版本隨附以下改進項目。

* **IP 位址允許清單**

  在 Adobe Experience Platform 使用者介面中新增聯合資料庫時，您現在可以直接檢視與聯合客群構成執行個體關聯的 IP 位址。這可讓您輕鬆複製和授權這些 IP 以連接到您的資料庫，從而提高安全性和靈活性。[了解更多](../connections/connections.md)

## 2024 年 10 月發行版本 {#fac-24-10}

>[!AVAILABILITY]
>
>Adobe Experience Platform 聯合客群構成先前僅開放給某些組織使用 (LA)，現已向所有使用者開放 (GA)。這項功能會根據您的產品啟用，而且必須具備相關權限才看得見。[了解更多](access-prerequisites.md)
>

### 相容性 {#fac-24-10-compat}

在這個新版本中，聯合客群構成現在可與下列系統相容。

* **Databricks 支援**

  您現在可以透過聯合客群構成，建立與 Databricks 資料庫的連線。[了解更多](../connections/federated-db.md#databricks)

* **支援透過 AWS PrivateLink 安全地存取 Snowflake**

  現在支援透過私人連結，安全地存取外部 Snowflake 資料倉儲。請注意，您的 Snowflake 帳戶必須託管在 Amazon Web Services (AWS) 上，並且與您的聯合客群構成環境位於同一區域。請聯絡您的 Adobe 代表，協助您設定 Snowflake 帳戶的安全存取權。[了解更多](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless 支援**

  透過此新版本，同盟對象構成支援[Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}。

### 改進項目 {#fac-24-10-improvements}

此發行版本隨附下列改進項目。

* **重新整理現有結構描述**

  當在聯合資料庫中建立、修改或刪除欄時，您現在可以透過按一下對應結構描述中的「**[!UICONTROL 重新整理結構描述]**」按鈕來偵測並套用變更。[了解更多](../customer/schemas.md#schema-refresh)

* **將資料模型與新構成相關聯**

  建立構成時，您現在可以選取與其關聯的資料模型。透過這個新選項，您的活動設定會更加容易，因為只有關聯資料模型的表格可以使用。[了解更多](../compositions/create-composition.md)

## 2024 年 7 月發行版本 - 聯合客群構成 (LA) {#fac-la}

聯合客群構成讓企業能夠用靈活存取更多企業資料倉儲，使用關鍵企業資料集來構成客群，並提升品牌主導的即時體驗。使用此新方法，身為[Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/home){target="_blank"}和/或[Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/ajo-home){target="_blank"}使用者，您可以直接從現有的資料倉儲同盟對象資料，以在一個系統中擴充Adobe Experience Platform對象。

市場上有越來越多企業希望能夠靈活地使用倉儲資料集來構成客群，而聯合客群構成滿足了這樣的需求。企業能夠藉此減少資料移動，同時讓行銷團隊能夠使用關鍵客群資料來滿足使用案例要求及提升個人化體驗。

在[本頁面](get-started.md)和[常見問題](faq.md)中進一步瞭解同盟對象構成功能。

如需存取聯合客群構成的先決條件和目前護欄的詳細資訊，請參閱[此頁面](access-prerequisites.md)。

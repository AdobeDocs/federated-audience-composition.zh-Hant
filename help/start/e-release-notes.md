---
title: Experience Platform 聯合客群構成的新增功能
description: 最新更新和發行說明
hide: true
hidefromtoc: true
source-git-commit: 59959bf01321d8062d345e1ec89538e5904a03cd
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 68%

---

# 發行說明 {#rn-new}

[!DNL Federated Audience Composition]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都已整合在這些發行說明中。[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Federated Audience Composition] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}。

## 2025年3月發行 {#fac-25-3}

### 改進項目 {#fac-25-3-improvements}

此版本隨附下列改善專案。

* **同盟對象組合許可權**

  自3月發行版本開始，[!DNL Federated Audience Composition]將開始強制將&#x200B;**同盟資料管理**&#x200B;與&#x200B;**同盟組合**&#x200B;介面存取給已授與管理同盟資料&#x200B;**許可權的使用者。**

  我們建議使用者連絡管理員，將此許可權新增至其角色，以繼續存取[!DNL Federated Audience Composition]使用者介面。

  若要瞭解如何指派此許可權，請參閱[詳細檔案](feature-access.md)。

* **資料模型畫布檢視**

  「資料模型」區段的「畫布」檢視可透過在畫布版面配置中在現有表格檢視旁邊啟用資料模型及其連結的視覺效果，進而改善體驗。 [了解更多](../data-management/gs-models.md)

* **對象匯出**

  同盟受眾構成現在支援匯出大型受眾，可處理最多20 GB的檔案大小。

### 相容性 {#fac-25-3-compat}

* **資料庫連線**

  透過此新版本，同盟對象構成現在支援Databricks資料庫連線的私人連結連線。
這樣還能安全地連線到Amazon Web Services (AWS)和Azure上託管的Databricks資料庫。 [了解更多](../connections/federated-db.md#databricks)

* **支援B2B CDP客戶**

  Federated Audience Composition現在可供B2B) Customer Data Platform (CDP)客戶用於以人物為基礎的對象使用案例。

* **Snowflake安全連線**

  透過此新版本，同盟對象構成支援與Azure上代管的Snowflake資料庫的安全私人連結連線。 [了解更多](../connections/federated-db.md#snowflake)

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

對於需要彈性來使用倉儲資料集組成受眾的企業來說，同盟受眾組成可解決其日益增長的市場需求。 這使得企業能夠減少資料移動，同時向行銷團隊提供關鍵客群資料，以滿足使用案例要求並提升個人化體驗。

如需有關聯合客群構成功能的詳細資訊，請參閱[此頁面](get-started.md)和[常見問題](faq.md)。

如需存取聯合客群構成的先決條件和目前護欄的詳細資訊，請參閱[此頁面](access-prerequisites.md)。



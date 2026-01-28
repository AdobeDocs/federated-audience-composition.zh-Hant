---
title: 常見問題
description: 有關 Adobe Experience Platform 聯合客群構成的常見問題
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 007192281ac7c853972a3405ea1d4069af847de1
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 83%

---

# 常見問題 {#faq}

以下是有關 Adobe Experience Platform 聯合客群構成的常見問題清單。[此頁面](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq){target="_blank"}也提供 Adobe Experience Platform Segmentation Service 的全球常見問題。

## 存取同盟對象構成需要哪些許可權？

+++ 回答

聯合客群構成需要 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer Prime 或 Ultimate 套件。您還需要購買聯合客群構成。

為了使用聯合客群構成，您必須將每位使用者新增至為每個沙箱建立的特定輪廓中。如需詳細資訊，請參閱[存取聯合客群構成](./start/access-prerequisites.md)頁面。

+++

## 支援哪些雲端倉庫？

+++ 回答

目前，支援的雲端倉儲如下：

* Amazon Redshift
* Azure Synapse Analytics
* Databricks
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

如需連線至Data Warehouse的詳細資訊，請閱讀[連線總覽](./connections/home.md)。

+++

## 可以在相同組合中查詢多個資料倉儲嗎？

+++ 回答

是的，您可以在同一個構成中查詢多個倉儲，並能合併來自多個來源的資料。通常，每個[構成活動](./compositions/activities.md) (查詢、擴充、分割等) 都會根據活動設定、目標資料庫 (可能同時存在多種聯合資料存取案例) 以及一或多份工作表的輸出與執行結果，執行一個或多個 SQL 陳述式。這些工作表會用來當做後續活動的輸入資料。

+++

### 我是否可以使用聯邦客群構成存取我的整個資料庫？

+++ 回答

不可以，但您可以自行設定專用或共用的資料庫/結構描述存取權。建議您為聯合客群構成建立專用結構描述，並僅複製/共用業務案例資料集。
+++

## 我是否可以存取專用綱要中的所有表格？

+++ 回答

可以，連接完成後，您就可以使用聯合客群構成，根據已定義的初始權限探索所有表格，並接著使用視覺化結構描述編輯器執行以下操作：

* 探索表格中的資料欄和主索引鍵
* 為這些表格建立一目了然的標籤
* 為每個資料欄建立一目了然的標籤
* 隱藏不需要的資料欄
* 儲存這些表格的描述
+++

## 同盟對象構成中是否有任何暫存空間？

+++ 回答

沒有，聯合客群構成只會儲存中繼資料 (結構描述)，不會傳輸任何客戶資料。<!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

## 同盟對象構成是否會儲存該人員清單的實體復本，以傳送至下游系統？

+++ 回答

聯合客群構成不會保留這類資料的實體副本。您可以在構成中設定頻率，以定義這類資料的重新整理頻率。Adobe Experience Platform 儲存生成客群資料的時間，不會超過執行客戶使用案例或動作所需的時間。

例如：

* 在客群建立的案例中，客群會在您的倉儲中建立，而您可以使用聯合客群構成執行其他構成任務和資料操作，然後再透過 Adobe Experience Platform 客群入口網站發佈產生的客群和相關屬性。客群定義和相關屬性會轉移到 Adobe Experience Platform。
請注意，外部產生的客群目前的資料過期時間為 30 天。此資料過期時間有助於減少組織內部儲存的過量資料。資料過期後，關聯的資料集仍會在資料集庫存中顯示，但您無法啟動客群，且用戶輪廓計數會顯示為零。若要了解更多資訊，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}。

* 客群擴充案例會以現有的 Adobe Experience Platform 客群做為起點。這裡可以考慮兩種情況：
   1. 從聯合資料倉儲引入額外的客群承載屬性：在此情況下，新增的額外屬性將會成為此客群定義的一部分。外部產生的客群資料過期時間同樣是 30 天，與上述相同。
   1. 您可以根據資料倉儲中的額外屬性，微調現有的 Adobe Experience Platform 客群。<!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

## 如果用於建立對象和擴充對象使用案例模式的資料沒有持續存在，如何暫時儲存？

+++ 回答

Adobe Experience Platform 或聯合客群構成所產生的客群資料不會長期保存。這些資料只會按照使用案例的需求，保留必要的時間。連同客群承載一併引入的客群屬性，只會做為客群定義的一部分保存。資料保留時間取決於任一客群的存留時間 (TTL)，預設為 30 天。

+++

## 我可以刪除對象嗎？

+++ 回答

可以，您可以在對象入口網站中刪除同盟對象構成對象。

+++

## 如果我合併來自多個來源的資料，該如何加入資料？ 是否會因此使用身分識別服務？

+++ 回答

不會，構成期間並不會使用身分識別服務。構成中所使用的各種來源的資料，是透過使用者定義的邏輯 (如底層模型所述) 相互連接，例如 CRM ID、使用者帳戶等。您必須在資料倉儲中，選取要在客群中用來當做身分識別碼的身分識別。在聯合客群構成產生的客群中，您需要為結果資料集中的身分識別指明身分識別命名空間。

+++

## 如何使用同盟受眾構成建立及管理隱私權請求？

+++ 回答

您可以透過兩種方式提交個別請求，以存取和刪除 Adobe 聯合客群構成中的客戶資料：

* 透過 Adobe Experience Platform **Privacy Service 使用者介面**。[了解更多](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant){target="_blank"}
* 透過 Adobe Experience Platform **Privacy Service API**。[了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/overview){target="_blank"}

建立和管理&#x200B;**存取請求**&#x200B;以及&#x200B;**刪除請求**&#x200B;的所有步驟，在[即時客戶輪廓文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/privacy){target="_blank"}中均有詳細說明。

+++

<!--
+++How are customer consent preferences honored for externally generated audiences that are imported into Federated Audience Composition?

As customer data is captured from multiple channels, identity stitching and merge policies allow this data to be consolidated in a single Real-Time Customer Profile. Information on the customers' consent preferences are stored and evaluated at the profile level.

Downstream Real-Time CDP and Journey Optimizer destinations check each profile for consent preferences prior to activation. Each profile's consent information is compared against consent requirements for a particular destination. If the profile does not satisfy the requirements, that profile is not sent to a destination.

When an external audience is ingested into Federated Audience Composition, it is reconciliated with existing profiles using a primary ID such as email or ECID. As a result, the existing consent policies will remain in force throughout activation.

>[!NOTE]
>
>Since the payload variables are not stored in the profile but in the data lake, you should not include consent information in externally generated audiences. Instead, use other Adobe Experience Platform ingestion channels where profile data is imported.

+++
-->

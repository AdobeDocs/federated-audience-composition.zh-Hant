---
title: 常見問題
description: 有關 Adobe Experience Platform 聯合客群構成的常見問題
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: f06414fbacc2e11a374313f3614f76a10eeadc0b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 常見問題 {#faq}

以下是有關 Adobe Experience Platform 聯合客群構成的常見問題清單。[此頁面](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq){target="_blank"}也提供了 Adobe Experience Platform Segmentation Service 的全球常見問題。


+++存取聯合客群構成需要哪些權限？

聯合客群構成需要 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer Prime 或 Ultimate 套件。您還需要購買聯合客群構成附加元件。

為了使用聯合客群構成，您必須將每位使用者新增至為每個沙箱建立的特定輪廓中。如需詳細資訊，請參閱[存取聯合客群構成](access-prerequisites.md)頁面。

+++

+++目前支援哪些雲端倉儲？

聯合客群構成支援的系統清單可在[此頁面](../start/access-prerequisites.md#supported-systems)取得。

+++


+++是否可以在同一個構成中，查詢多個資料倉儲？

是的，您可以在同一個構成中查詢多個倉儲，並能合併來自多個來源的資料。通常，每個[構成活動](../compositions/orchestrate-activities.md) (查詢、擴充、分割等) 都會根據活動設定、目標資料庫 (可能同時存在多種聯合資料存取案例) 以及一或多份工作表的輸出與執行結果，執行一個或多個 SQL 陳述式。這些工作表會用來當做後續活動的輸入資料。

+++

+++ 我是否可以使用聯邦客群構成存取我的整個資料庫？

不可以，但您可以自行設定專用或共用的資料庫/結構描述存取權。建議您為聯合客群構成建立專用結構描述，並僅複製/共用業務案例資料集。
+++

+++我是否可以存取專用結構描述中的所有表格？

可以，連接完成後，您就可以使用聯合客群構成，根據已定義的初始權限探索所有表格，並接著使用視覺化結構描述編輯器執行以下操作：

* 探索表格中的資料欄和主索引鍵
* 為這些表格建立一目了然的標籤
* 為每個資料欄建立一目了然的標籤
* 隱藏不需要的資料欄
* 儲存這些表格的描述
+++

+++聯合客群構成中是否有任何暫時儲存區？

沒有，聯合客群構成只會儲存中繼資料 (結構描述)，不會傳輸任何客戶資料。<!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++聯合客群構成是否會儲存客群名單的實體副本，以傳送至下游系統？

聯合客群構成不會保留這類資料的實體副本。您可以在構成中設定頻率，以定義這類資料的重新整理頻率。Adobe Experience Platform 儲存生成客群資料的時間，不會超過執行客戶使用案例或動作所需的時間。

例如：

* 在客群建立的案例中，客群會在您的倉儲中建立，而您可以使用聯合客群構成執行其他構成任務和資料操作，然後再透過 Adobe Experience Platform 客群入口網站發佈產生的客群和相關屬性。客群定義和相關屬性會轉移到 Adobe Experience Platform。
請注意，外部產生的客群目前的資料過期時間為 30 天。此資料過期時間有助於減少組織內部儲存的過量資料。資料過期後，關聯的資料集仍會在資料集庫存中顯示，但您無法啟動客群，且用戶輪廓計數會顯示為零。透過 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}了解更多。

* 客群擴充案例會以現有的 Adobe Experience Platform 客群做為起點。這裡可以考慮兩種情況：
   1. 從聯合資料倉儲引入額外的客群承載屬性：在此情況下，新增的額外屬性將會成為此客群定義的一部分。外部產生的客群資料過期時間同樣是 30 天，與上述相同。
   1. 您可以根據資料倉儲中的額外屬性，微調現有的 Adobe Experience Platform 客群。<!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++如果客群建立和客群擴充使用案例模式所使用的資料不會長期保存，那麼這些資料會以何種方式暫時儲存？

Adobe Experience Platform 或聯合客群構成所產生的客群資料不會長期保存。這些資料只會按照使用案例的需求，保留必要的時間。連同客群承載一併引入的客群屬性，只會做為客群定義的一部分保存。資料保留時間取決於任一客群的存留時間 (TTL)，預設為 30 天。

+++

+++我是否可以刪除自訂上傳的客群？

不可以，您無法在目前版本中刪除自訂上傳的客群。

+++

+++合併來自多個來源的資料之後，該如何連接這些資料？是否會因此使用身分識別服務？

不會，構成期間並不會使用身分識別服務。構成中所使用的各種來源的資料，是透過使用者定義的邏輯 (如底層模型所述) 相互連接，例如 CRM ID、使用者帳號等。您必須在資料倉儲中，選取要在客群中用來當做身分識別碼的身分識別。在聯合客群構成產生的客群中，您需要為結果資料集中的身分識別指明身分識別命名空間。

+++

+++如何為匯入同盟對象構成的外部產生對象遵循客戶同意偏好設定？

從多個管道擷取客戶資料時，身分拼接和合併原則可讓這些資料合併到單一即時客戶設定檔中。 有關客戶同意偏好設定的資訊會儲存並在設定檔層級進行評估。

下游Real-Time CDP和Journey Optimizer目的地會在啟用前檢查每個設定檔的同意偏好設定。 每個設定檔的同意資訊會與特定目的地的同意要求進行比較。 如果設定檔不符合需求，該設定檔將不會傳送到目的地。

將外部受眾內嵌至Federated Audience Composition時，會使用主要ID （例如電子郵件或ECID）與現有設定檔進行調解。 因此，現有的同意政策將在整個啟用期間保持有效。

>[!NOTE]
>
>由於裝載變數不會儲存在設定檔中，而是儲存在Data Lake中，因此您不應在外部產生的對象中包含同意資訊。 請改用其他已匯入設定檔資料的Adobe Experience Platform擷取管道。

+++

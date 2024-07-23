---
title: 常見問答
description: 常見問題
badge: label="可用性限制" type="Informative"
source-git-commit: 6cfd3bd85d7811e00e716042502c7d7b23fa4ad9
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 2%

---


# 常見問答 {#faq}

以下是有關同盟對象構成的常見問題清單。 在[此頁面](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}中，也有Adobe Experience Platform Segmentation Service適用的全域常見問題集。


+++存取同盟對象構成需要哪些許可權？

同盟對象構成沒有特定許可權。 存取此功能的唯一先決條件，就是已購買同盟對象構成附加元件。

+++

+++支援哪些雲端倉庫？

在此版本中，同盟對象構成相容於：

* Amazon Redshift
* azure synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++可以在相同組合中查詢多個資料倉儲嗎？

可以，可以在相同構成中查詢多個倉儲，也可以合併來自多個來源的資料。  通常每個[組合活動](../compositions/orchestrate-activities.md) （查詢、擴充、分割等） 根據活動組態、目標資料庫（可能存在多個同盟資料存取的情況）以及一個或多個工作表輸出和執行結果，執行一或多個SQL敘述句。 這些工作表會作為連續活動的輸入。

+++

+++ 我可以使用同盟對象構成存取整個資料庫嗎？

否，您可以自行設定專用或共用資料庫/綱要的存取權。 建議您為同盟對象構成建立專用結構，並僅複製/共用業務案例資料集。
+++



+++我是否可以存取專用綱要中的所有表格？

可以，連線之後，同盟對象構成可用於根據定義的初始許可權探索所有表格，然後您可以使用視覺結構編輯器來：

* 從表格中探索欄和主索引鍵
* 為這些表格建立易記標籤
* 為每個欄建立易記標籤
* 隱藏不必要的欄
* 儲存這些表格說明
+++


+++同盟對象構成中是否有任何暫存空間？

否，同盟對象構成僅儲存中繼資料（結構描述）。 沒有正在傳輸的客戶資料。 直接從Adobe Experience Platform對象入口網站（透過[目的地](../connections/destinations.md)）到客戶資料庫完成對象匯出流程。 建立和更新流程可直接從您的資料倉儲資料庫執行至Adobe Experience Platform對象入口網站。

+++

+++同盟對象構成是否會儲存該人員清單的實體復本，以傳送至下游系統？

同盟對象構成不會維護資料的實體復本。 頻率是在構成中設定，以定義此資料的重新整理頻率。 Adobe Experience Platform不會將產生的對象資料儲存到客戶使用案例或動作所需的時間。

例如：

* 若是對象細分，對象會建立於您的倉儲中，而您可以先使用同盟對象構成進行其他構成任務和資料操作，然後再透過Adobe Experience Platform對象入口網站發佈產生的對象和相關屬性。 受眾定義和相關屬性會移至Adobe Experience Platform。
請注意，外部產生的對象目前的資料到期日為30天。 此資料到期日可減少組織內儲存的過多資料量。 在資料有效期限過後，關聯的資料集仍會顯示在資料集詳細目錄內，但您無法啟用對象，且設定檔計數會顯示為零。 進一步瞭解[Adobe Experience Platform檔案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}。

* 在對象擴充的案例中，起點是現有的Adobe Experience Platform對象。 您可以在此檢視兩種情境：
   1. 從Federated Data Warehouse帶來其他受眾裝載屬性：在此情況下，新增的其他屬性將隨此受眾定義一起提供。 外部產生對象的資料有效期限與上述相同，即30天。
   1. 根據您的Data Warehouse中存在的其他屬性調整現有的Adobe Experience Platform對象。 例如，您的受眾是過去兩個月在網站上對特定產品表現出興趣的客戶。 您現在想要取用這個對象，並使用同盟對象構成來進一步區隔它，以僅包含具有高信用分數的客戶。 這些信用分數會被視為敏感，且不會從資料倉儲複製個別信用分數資料點。
+++

+++如果對象細分和對象擴充使用案例模式的資料沒有持續存在，如何暫時儲存？

產生的對象資料不會無限期保留在Adobe Experience Platform或同盟對象構成中。 保留時間不會超過使用案例所需的時間。 在對象裝載中隨附的對象屬性只會當作對象定義的一部分而持續存在。 持續性持續時間會根據任何對象的TTL而定，預設為30天。

+++

+++我可以刪除自訂上傳的對象嗎？

您可以直接在Audience Portal中刪除未用於下游啟動的受眾，只需從動作功能表中選取刪除即可。 進一步瞭解[Adobe Experience Platform檔案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}。

+++

+++如果我合併來自多個來源的資料，該如何加入資料？ 我們是否使用Identity服務？

否，組合期間並未運用Identity Service 。 構成中使用的各種來源之間的資料透過使用者定義的邏輯（如基礎模型中表示的）連結，例如CRM ID、使用者帳戶號碼等。 您必須選取身分識別，以在資料倉儲中作為選取對象的識別碼。 對於同盟對象構成產生的對象，您必須在產生的資料集中識別身分的身分名稱空間。

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
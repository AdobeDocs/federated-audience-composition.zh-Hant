---
title: 同盟對象構成概觀
description: 瞭解Adobe Federated Audience Composition，以及如何將其用於下游服務，例如Adobe Experience Platform和Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# 同盟對象構成概觀

同盟對象構成可讓您從協力廠商資料倉儲建立及擴充對象，並將對象匯入至Adobe Experience Platform。 這可提供簡單而強大的解決方案，讓您直接在Adobe Real-Time Customer Data Platform或Adobe Journey Optimizer等下游服務中連線企業資料倉儲，並對資料倉儲的表格執行查詢。 因此，您可以存取儲存在資料倉儲和雲端儲存平台(例如Amazon Redshift和Azure Synapse Analytics)的客戶資料。

## 功能 {#rn-capabilities}

聯合客群構成會透過全面的客群管理和啟用方法來擴充 Real-Time CDP 和 Journey Optimizer 的價值：

* **擴充對重要倉儲資料集的存取權，以建立高價值的對象**：您可以使用現有的資料倉儲作為主要記錄系統，同時運用同級最佳的應用程式來強化絕佳的客戶體驗。

* **全方位支援參與使用案例**：同盟對象構成，搭配Real-Time CDP或Journey Optimizer，支援同盟對象品牌啟動的個人化體驗，並提供即時事件觸發的即時體驗，加上人員屬性，以滿足跨團隊的使用案例需求。

* **將資料移動和重複最小化**：您可以從位於企業資料倉儲中的資料集建立對象，而不需要複製基礎資料來管理可操作的行銷設定檔和對象。

* **將單一系統用於體驗導向的工作流程**：您可以在Adobe Experience Platform中組織已擷取和同盟對象，並協調所有管道的傳出體驗。

* **多重版本支援**： B2C與B2B CDP客戶可以運用同盟對象構成，透過整合來自受支援企業資料倉儲的資料，建置以人物為基礎的對象。 此外，他們可以結合企業資料倉儲中可用的相關屬性，強化現有的Experience Platform以人為本的受眾，進而增強受眾設定檔，以實現更個人化且更有針對性的參與。

## 使用案例 {#use-cases}

聯合客群構成支援&#x200B;**三個**&#x200B;使用案例類別：客群建立、客群擴充和客戶輪廓擴充。

* **對象建立**：您可以從資料倉儲建立對象，並將這些對象組成至Experience Platform，以便透過行銷人員友善的拖放使用者介面用於Real-Time CDP或Journey Optimizer。 如此，您便可以查詢資料倉儲，而無需複製敏感的底層資料或複製現有資料。
   * **例如：**&#x200B;使用倉儲中的歷史交易資料來建立由高價值過往購買者組成的客群，而無需將這些交易複製到 Experience Platform 中。

* **對象擴充**：您可以使用資料倉儲中的其他資料集，並將此資訊覆蓋對象，在Experience Platform中為現有對象新增更多詳細資料，而完全無須將基礎資料複製到Experience Platform。 透過客群擴充，您便可以使用擴充的客群來提供更好的個人化。
   * **例如：**&#x200B;利用由高價值過往購買者組成的聯合客群構成客群來擴充由購物車捨棄者組成的 Experience Platform 客群，以提供有針對性的優惠。

* **設定檔擴充**：您可以從資料倉儲中選取個別客戶屬性，以增強Experience Platform設定檔。 透過將聯合資料新增至這些輪廓，您便可以更好地支援由傳入客戶訊號所觸發的即時體驗。
   * **例如：**&#x200B;利用聯合客群中的資訊來擴充 Experience Platform 輪廓。對於屬於高價值過往購買者聯合客群的網站訪客，您現在可以利用他們的網站上行為所觸發的針對性優惠來向他們推銷。

![圖表](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

如需有關聯合客群構成使用案例的詳細資訊，請參閱[聯合客群構成白皮書](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html)。

## 主要步驟 {#gs-steps}

Adobe 聯合客群構成可讓您直接從資料庫建立和更新 Adobe Experience Platform 客群，無需任何擷取程序。

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **建立連線**：將不同來源的資料彙整在一起，並將其合併到統一的資料集中。 如需將Adobe Experience Platform應用程式連線至您的企業資料倉儲、支援的資料庫以及設定連線的詳細資訊，請參閱[連線總覽](./connections/home.md)。

2. **為您的資料建立模型**：設計和建立定義資料結構、關係和限制的結構描述和資料模型。 如需結構描述的詳細資訊，請閱讀[結構描述概觀](./data-modelling/schemas.md)。 如需資料模型的詳細資訊，請閱讀[資料模型概觀](./data-modelling/models.md)。

3. **轉換您的資料**：套用資料操作技術來修改資料元素的格式、結構或值，使其相容或適用於特定的分析或應用程式。

4. **組成您的對象**：建立、協調和建立對象。 如需構成對象的詳細資訊，請閱讀[構成概觀](./compositions/home.md)。 您也可以透過 Adobe Experience Platform Audience Portal 和目標系統，更新或重複使用現有的客群。若要了解更多資訊，請參閱[此頁面](./connections/destinations.md)

>[!NOTE]
>
>在執行構成後，產生的客群將作為外部客群儲存在 Adobe Experience Platform 中，並可用於 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer。該客群可透過「**客群**」選單進行存取。[了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 治理、隱私權和安全性 {#governance-privacy-security}

### 隱私權要求 {#gov-privacy-requests}

您建立客群構成後，產生的客群會儲存至 Adobe Experience Platform。

接著，您可以透過 Adobe Experience Platform **Privacy Service** 提出隱私請求，要求存取和/或刪除與這些客群對應的輪廓資料，而這項 Privacy Service 提供[使用者介面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant){target="_blank"}以及 [RESTful API](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/overview){target="_blank"} 來協助您管理客戶資料請求。

>[!NOTE]
>
>關於 Privacy Service 的詳細資訊，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant){target="_blank"}。

您可以建立及管理要求存取和刪除 Adobe 聯合客群構成中客戶資料的個別請求。提交&#x200B;**存取請求**&#x200B;和&#x200B;**刪除請求**&#x200B;的步驟，請參閱[即時客戶輪廓文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/privacy){target="_blank"}的詳細說明。

### 稽核軌跡 {#gov-audit-trail}

稽核軌跡功能會針對即時對環境進行的所有動作和事件，提供詳細且按時間順序的記錄。 若要深入瞭解稽核軌跡，請閱讀[稽核軌跡概觀](./admin/audit-trail.md)。

## 了解更多 {#learn}

<!-- Workflow + Workflow activities-->

若要了解如何存取聯合客群構成、護欄和限制，請參閱[此頁面](./start/access-prerequisites.md)。

如需常見問題的解答，請閱讀[同盟對象構成常見問答集](./faq.md)。

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="執行設定"
>abstract="在此區段中，您可以設定與工作流程執行相關的設定，例如保留構成歷程記錄的天數。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="活動不可編輯"
>abstract="當在主控台利用其他資料設定&#x200B;**查詢**&#x200B;或&#x200B;**擴充**&#x200B;活動時，會將擴充資料納入考量，並傳遞至出站轉變，但無法編輯。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="建立連結"
>abstract="定義連結設定。"


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="增量查詢"
>abstract=" **增量查詢**&#x200B;活動可讓您使用查詢建模工具查詢資料庫。每次執行此活動時，都會排除先前執行的結果。這可讓您只鎖定新元素。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="增量查詢歷史記錄"
>abstract="增量查詢歷史記錄"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="增量查詢處理的資料"
>abstract="增量查詢處理的資料"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="增量查詢模式"
>abstract="增量查詢可讓您多次執行相同的查詢，方式是每次新執行時排除先前執行的結果。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="增量查詢模式"
>abstract="增量查詢可讓您多次執行相同的查詢，方式是每次執行時只考慮日期欄位晚於或等於增量查詢活動上次執行日期的結果。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="選取目標市場選擇維度"
>abstract="目標市場選擇維度可讓您定義作業的目標群體：收件者、合約受益人、操作者、訂閱者等。對於電子郵件和簡訊，依預設，目標是從收件者內建表格中選取。對於推播通知，預設目標市場選擇維度是訂閱者應用程式。"


---
title: 開始使用 Experience Platform 聯合客群構成
description: 了解什麼是 Adobe 聯合客群構成，以及如何在 Adobe Experience Platform 中使用此功能
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 16d307172ec6ad2d64f50b686d2d251267ce29ae
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 100%

---

# 開始使用聯合客群構成 {#gs-fac}

聯合客群構成適用於 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/home){target="_blank"} 和 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/ajo-home){target="_blank"} 環境。您可以透過聯合客群構成使用第三方資料倉儲來建置和擴充客群，並將客群匯入 Adobe Experience Platform。聯合客群構成提供簡易且強大的解決方案，可讓您直接在 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer 中連接企業資料倉儲，並針對資料倉儲中的表格執行查詢。

有了 Adobe 聯合客群構成協助，Adobe Experience Platform 應用程式使用者就能存取儲存在資料倉儲與雲端儲存平台 (如 Amazon Redshift、Azure Synapse Analytics 等) 中的客戶資料。現在，客戶資料可以存放在多個資料倉儲中，而且無需複寫，就能立即存取。[此頁面](../connections/home.md#supported-db)列出支援的平台。

>[!INFO]
>
>請遵循此[逐步指南](https://experienceleague.adobe.com/zh-hant/docs/platform-learn/tutorial-comprehensive-technical/datacollection/module13/fac)，了解如何使用聯合客群構成來建立客群。

## 功能 {#rn-capabilities}

聯合客群構成會透過全面的客群管理和啟用方法來擴充 Real-Time CDP 和 Journey Optimizer 的價值：

* 擴大對基於倉儲的關鍵資料集的存取以建立高價值客群：利用現有資料倉儲作為主要記錄系統，同時利用同級最佳的應用程式來提升卓越的客戶體驗。

* 對提高參與度使用案例的全面支援：將聯合客群構成與 Real-Time CDP 或 Journey Optimizer 搭配使用，以支援聯合客群的品牌發起的個人化體驗、提供由即時事件觸發的即時體驗，並與人員屬性結合來滿足跨團隊的使用案例要求。

* 盡量減少資料移動和複製：從企業資料倉儲的資料集中建立客群，而無需複製基礎資料來管理可操作的行銷輪廓和客群。

* 利用單一系統來實現體驗驅動的工作流程：在 Adobe Experience Platform 中管理攝取和聯合的客群，並協調所有管道的傳出體驗。

* B2C 和 B2B CDP 客戶現在可以利用聯合客群構成，透過整合受支援的企業資料倉儲中的資料來建立以人員為基礎的客群。此外，他們可以透過整合企業資料倉儲中的相關屬性來擴充現有 AEP 以人員為基礎的客群，從而增強其客群輪廓以實現更個人化和有針對性的參與。

## 使用案例 {#use-cases}

聯合客群構成支援&#x200B;**三個**&#x200B;使用案例類別：客群建立、客群擴充和客戶輪廓擴充。

* 客群建立：您可以從資料倉儲中建立客群，並將這些客群聯合到 Experience Platform 中，以便透過行銷人員易用的拖放使用者介面，在 Real-Time CDP 或 Journey Optimizer 中使用。如此，您便可以查詢資料倉儲，而無需複製敏感的底層資料或複製現有資料。
   * **例如：**&#x200B;使用倉儲中的歷史交易資料來建立由高價值過往購買者組成的客群，而無需將這些交易複製到 Experience Platform 中。

* 客群擴充：您可以使用資料倉儲中的其他資料集並利用這些資訊來覆蓋您的客群，從而為 Experience Platform 中的現有客群新增更多詳細資料，而完全無需將底層資料複製到 Experience Platform 中。透過客群擴充，您便可以使用擴充的客群來提供更好的個人化。
   * **例如：**&#x200B;利用由高價值過往購買者組成的聯合客群構成客群來擴充由購物車捨棄者組成的 Experience Platform 客群，以提供有針對性的優惠。

* 輪廓擴充：您可以從資料倉儲中選取個別的客戶屬性來改進 Experience Platform 輪廓。透過將聯合資料新增至這些輪廓，您便可以更好地支援由傳入客戶訊號所觸發的即時體驗。
   * **例如：**&#x200B;利用聯合客群中的資訊來擴充 Experience Platform 輪廓。對於屬於高價值過往購買者聯合客群的網站訪客，您現在可以利用他們的網站上行為所觸發的針對性優惠來向他們推銷。

![圖表](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

如需有關聯合客群構成使用案例的詳細資訊，請參閱[聯合客群構成白皮書](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html)。

## 主要步驟 {#gs-steps}

Adobe 聯合客群構成可讓您直接從資料庫建立和更新 Adobe Experience Platform 客群，無需任何擷取程序。

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

主要步驟：

1. **資料整合**：匯集各種來源的資料，並合併為統一的資料集。若要進一步了解如何連接 Adobe Experience Platform 應用程式和您的企業資料倉儲、支援的資料庫，以及如何設定這些資料庫，請參閱[本節](../connections/home.md)說明。

1. **資料模式**：設計並建立資料模型和結構描述，以定義資料的結構、關係和限制。若要了解更多有關結構描述的資訊，請參閱[此頁面](../customer/schemas.md)。在[此頁面](../data-management/gs-models.md)學習如何為資料模型建立連結。

1. **資料轉換**：應用資料處理技術，修改資料元素的格式、結構或值，使其相容或適用於特定的分析或應用程式。

1. **資料使用**：建立、協調及建置客群。透過[此頁面](../compositions/gs-compositions.md)了解如何構成客群。您也可以透過 Adobe Experience Platform Audience Portal 和目標系統，更新或重複使用現有的客群。若要了解更多資訊，請參閱[此頁面](../connections/destinations.md)

>[!NOTE]
>
>在執行構成後，產生的客群將作為外部客群儲存在 Adobe Experience Platform 中，並可用於 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer。該客群可透過「**客群**」選單進行存取。[了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 治理、隱私權和安全性 {#governance-privacy-security}

### 隱私請求 {#gov-privacy-requests}

您建立客群構成後，產生的客群會儲存至 Adobe Experience Platform。

接著，您可以透過 Adobe Experience Platform **Privacy Service** 提出隱私請求，要求存取和/或刪除與這些客群對應的輪廓資料，而這項 Privacy Service 提供[使用者介面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant){target="_blank"}以及 [RESTful API](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/overview){target="_blank"} 來協助您管理客戶資料請求。

>[!NOTE]
>
>關於 Privacy Service 的詳細資訊，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant){target="_blank"}。

您可以建立及管理要求存取和刪除 Adobe 聯合客群構成中客戶資料的個別請求。提交&#x200B;**存取請求**&#x200B;和&#x200B;**刪除請求**&#x200B;的步驟，請參閱[即時客戶輪廓文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/privacy){target="_blank"}的詳細說明。

### 稽核軌跡 {#gov-audit-trail}

稽核軌跡功能會針對您在環境執行的所有動作和事件，即時提供按時間順序排列的詳細記錄。[了解更多](../admin/audit-trail.md)

## 了解更多 {#learn}

<!-- Workflow + Workflow activities-->


若要了解如何存取聯合客群構成、護欄和限制，請參閱[此頁面](access-prerequisites.md)。

另請參閱[此頁面](faq.md)的常見問題。


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="執行設定"
>abstract="在此區段中，您可以設定與工作流程執行相關的設定，例如構成歷史記錄的保留天數。"

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


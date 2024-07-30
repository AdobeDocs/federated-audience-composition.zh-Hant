---
title: 開始使用Experience Platform同盟對象構成
description: 了解什麼是 Adobe 聯合客群組成，以及如何在 Adobe Experience Platform 中使用此功能
badge: label="限量開放使用" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 2a3eb92ba6d7c24e9eec7f6ff978bf9a34be34ab
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 57%

---

# 開始使用聯合客群組成 {#gs-fac}

同盟對象構成是[Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/home){target="_blank"}和[Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/ajo-home){target="_blank"}的附加功能，可讓您從協力廠商資料倉儲建立並擴充對象，並將對象匯入至Adobe Experience Platform。 聯合客群組成提供簡易且強大的解決方案，可讓您直接在 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer 中連接企業資料倉儲，並針對資料倉儲中的表格執行查詢。

有了 Adobe 聯合客群組成協助，Adobe Experience Platform 應用程式使用者就能存取儲存在資料倉儲與雲端儲存平台 (如 Amazon Redshift、Azure Synapse Analytics 等) 中的客戶資料。現在，客戶資料可以存放在多個資料倉儲中，而且無需複寫，就能立即存取。[此頁面](../connections/federated-db.md#supported-db)列出了支援的平台。

## 功能 {#rn-capabilities}

同盟受眾構成透過全面性的受眾策劃和啟用方法，進一步延伸Real-Time CDP和Journey Optimizer的價值：

* 擴充對關鍵倉儲型資料集的存取權，以建立高價值受眾：運用現有的資料倉儲作為主要記錄系統，同時運用同級最佳的應用程式來強化絕佳的客戶體驗。

* 全面支援強力參與使用案例：同盟受眾構成、搭配Real-Time CDP或Journey Optimizer支援品牌啟動的個人化體驗與同盟受眾，並提供即時事件觸發的即時體驗，加上人員屬性，以滿足跨團隊的使用案例需求。

* 將資料移動和複製最小化：從位於企業資料倉儲中的資料集建立對象，無需複製基礎資料即可管理可操作的行銷設定檔和對象。

* 針對體驗導向工作流程利用單一系統：在Adobe Experience Platform中組織內嵌和同盟對象，並協調所有管道的對外體驗。

## 使用案例 {#rn-uc}

透過行銷人員一看就懂的使用者介面，建立用來查詢資料倉儲的區段規則，找出符合行銷活動所需特定區段資格的使用者清單；存取倉儲中的現有客群並加以啟用，或使用倉儲中的其他現有資料點擴充 Adobe Experience Platform 客群。

此版本提供兩種使用案例：

1. 對象建立：從企業資料集建立新對象，而不複製基礎資料，並使用預先建立的目的地啟用這些對象&#x200B;。

1. 對象擴充：利用從企業資料倉儲已同盟的構成對象資料，擴充Adobe Experience Platform中的現有對象。 此資料不會儲存在Adobe Experience Platform客戶設定檔中。

![圖表](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## 主要步驟 {#gs-steps}

Adobe 聯合客群組成可讓您直接從資料庫建立和更新 Adobe Experience Platform 客群，無需任何擷取程序。

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

主要步驟：

1. **資料整合**：匯集各種來源的資料，並合併為統一的資料集。若要進一步了解如何連接 Adobe Experience Platform 應用程式和您的企業資料倉儲、支援的資料庫，以及如何設定這些資料庫，請參閱[本節](../connections/federated-db.md)說明。

2. **資料模式**：設計並建立資料模型和結構描述，以定義資料的結構、關係和限制。前往[此頁面](../customer/schemas.md)深入了解結構描述。前往[此頁面](../data-management/gs-models.md)學習如何為資料模型建立連結。

3. **資料轉換**：應用資料處理技術，修改資料元素的格式、結構或值，使其相容或適用於特定的分析或應用程式。

4. **資料使用**：建立、協調及建置客群。前往[此頁面](../compositions/gs-compositions.md)了解如何構成客群。您也可以透過 Adobe Experience Platform Audience Portal 和目標系統，更新或重複使用現有的客群。前往[此頁面](../connections/destinations.md)了解更多

>[!NOTE]
>
>執行構成後，產生的受眾會作為外部受眾儲存在Adobe Experience Platform中，並可供Adobe Real-Time Customer Data Platform和/或Adobe Journey Optimizer使用。 它可在&#x200B;**對象**&#x200B;功能表中存取。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 了解更多 {#learn}

<!-- Workflow + Workflow activities-->


在[此頁面](access-prerequisites.md)中瞭解如何存取同盟對象構成、護欄和限制。

另請參閱[此頁面](faq.md)中的常見問題。


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

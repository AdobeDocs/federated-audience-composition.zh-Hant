---
title: 開始使用 Experience Platform 聯合客群構成
description: 了解什麼是 Adobe 聯合客群構成，以及如何在 Adobe Experience Platform 中使用此功能
badge: label="限量開放使用" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 8b67aa9258b05a6ca239dd54ebb10273826ea550
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 97%

---

# 開始使用聯合客群構成 {#gs-fac}

聯合客群構成是 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/home){target="_blank"} 和 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/ajo-home){target="_blank"} 的附加功能，可讓您從第三方資料倉儲建立和擴充客群，並將客群匯入 Adobe Experience Platform。聯合客群構成提供簡易且強大的解決方案，可讓您直接在 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer 中連接企業資料倉儲，並針對資料倉儲中的表格執行查詢。

有了 Adobe 聯合客群構成協助，Adobe Experience Platform 應用程式使用者就能存取儲存在資料倉儲與雲端儲存平台 (如 Amazon Redshift、Azure Synapse Analytics 等) 中的客戶資料。現在，客戶資料可以存放在多個資料倉儲中，而且無需複寫，就能立即存取。[此頁面](../connections/federated-db.md#supported-db)列出了支援的平台。

## 功能 {#rn-capabilities}

聯合客群構成會透過全面的客群管理和啟用方法來擴充 Real-Time CDP 和 Journey Optimizer 的價值：

* 擴大對基於倉儲的關鍵資料集的存取以建立高價值客群：利用現有資料倉儲作為主要記錄系統，同時利用同級最佳的應用程式來提升卓越的客戶體驗。

* 對提高參與度使用案例的全面支援：將聯合客群構成與 Real-Time CDP 或 Journey Optimizer 搭配使用，以支援聯合客群的品牌發起的個人化體驗、提供由即時事件觸發的即時體驗，並與人員屬性結合來滿足跨團隊的使用案例要求。

* 盡量減少資料移動和複製：從企業資料倉儲的資料集中建立客群，而無需複製基礎資料來管理可操作的行銷輪廓和客群。

* 利用單一系統來實現體驗驅動的工作流程：在 Adobe Experience Platform 中管理攝取和聯合的客群，並協調所有管道的傳出體驗。

## 使用案例 {#rn-uc}

透過行銷人員一看就懂的使用者介面，建立用來查詢資料倉儲的區段規則，找出符合行銷活動所需特定區段資格的使用者清單；存取倉儲中的現有客群並加以啟用，或使用倉儲中的其他現有資料點擴充 Adobe Experience Platform 客群。

在此版本中，有兩個可用的使用案例：

1. 對象建立：從企業資料集建立新對象，而不複製基礎資料，並使用預先建立的目的地啟用這些對象。

1. 客群擴充：利用從企業資料倉儲聯合的構成客群資料，擴充 Adobe Experience Platform 中的現有客群。此資料將不會長期保存在 Adobe Experience Platform 客戶輪廓中。

![圖表](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## 主要步驟 {#gs-steps}

Adobe 聯合客群構成可讓您直接從資料庫建立和更新 Adobe Experience Platform 客群，無需任何擷取程序。

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

主要步驟：

1. **資料整合**：匯集各種來源的資料，並合併為統一的資料集。若要進一步了解如何連接 Adobe Experience Platform 應用程式和您的企業資料倉儲、支援的資料庫，以及如何設定這些資料庫，請參閱[本節](../connections/federated-db.md)說明。

1. **資料模式**：設計並建立資料模型和結構描述，以定義資料的結構、關係和限制。前往[此頁面](../customer/schemas.md)深入了解結構描述。前往[此頁面](../data-management/gs-models.md)學習如何為資料模型建立連結。

1. **資料轉換**：應用資料處理技術，修改資料元素的格式、結構或值，使其相容或適用於特定的分析或應用程式。

1. **資料使用**：建立、協調及建置客群。前往[此頁面](../compositions/gs-compositions.md)了解如何構成客群。您也可以透過 Adobe Experience Platform Audience Portal 和目標系統，更新或重複使用現有的客群。前往[此頁面](../connections/destinations.md)了解更多

>[!NOTE]
>
>在執行構成後，產生的客群將作為外部客群儲存在 Adobe Experience Platform 中，並可用於 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer。該客群可透過「**客群**」選單進行存取。[了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

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

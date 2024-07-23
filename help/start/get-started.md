---
title: 開始使用同盟對象構成
description: 瞭解什麼是Adobe同盟對象構成以及如何在Adobe Experience Platform中使用
badge: label="可用性限制" type="Informative"
source-git-commit: 6cfd3bd85d7811e00e716042502c7d7b23fa4ad9
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 12%

---


# 開始使用同盟對象構成 {#gs-fac}

同盟對象構成是Adobe Real-time Customer Data Platform和Adobe Journey Optimizer的附加元件，可讓您從協力廠商資料倉儲建立並擴充對象，並將對象匯入至Adobe Experience Platform。 同盟對象構成提供簡單而強大的解決方案，可直接在Adobe Real-time Customer Data Platform及/或Adobe Journey Optimizer中連線您的企業資料倉儲，並在Data Warehouse的表格上執行查詢。

Adobe同盟對象構成可協助Adobe Experience Platform應用程式使用者存取其儲存在資料倉儲和雲端儲存平台(例如Amazon Redshift、Azure synapse Analytics等)的客戶資料。 客戶資料可存放在多個資料倉儲中，現在無需複製即可立即存取。 支援的平台列於[此頁面](../connections/federated-db.md#supported-db)。

## 使用案例 {#rn-uc}

透過方便行銷的UI，建立區段規則來查詢您的資料倉儲，以取得符合行銷活動所需特定區段資格的使用者清單、存取倉儲中的現有對象以進行啟用，或利用倉儲中存在的其他資料點來擴充Adobe Experience Platform對象。

此版本提供兩種使用案例：對象細分和對象擴充。 設定檔擴充功能將於未來版本中提供。

![圖表](assets/fac-use-cases.png){zoomable="yes"}

## 主要步驟 {#gs-steps}

Adobe同盟對象構成可讓您直接從資料庫建立和更新Adobe Experience Platform對象，無需任何擷取程式。

![圖表](assets/steps-diagram.png){zoomable="yes"}

關鍵步驟：

1. **資料整合**：將各種來源的資料彙整在一起，並將它們合併到統一的資料集中。 在[本節](../connections/federated-db.md)中詳細瞭解如何連結Adobe Experience Platform應用程式和您的企業資料倉儲、支援的資料庫，以及如何設定它們。

2. **資料模型**：設計和建立定義資料結構、關係和限制的資料模型和結構描述。 在[此頁面](../customer/schemas.md)中進一步瞭解結構描述。 在[此頁面](../data-management/gs-models.md)中瞭解如何建立資料模型的連結。

3. **資料轉換**：套用資料操作技術來修改資料元素的格式、結構或值，使其相容或適用於特定的分析或應用程式。

4. **資料使用**：建立、協調和建立對象。 瞭解如何在[此頁面](../compositions/gs-compositions.md)中撰寫對象。 您也可以透過Adobe Experience Platform對象入口網站和目標，更新或重複使用現有的對象。 在[本頁](../connections/destinations.md)中進一步瞭解



## 更多詳情 {#learn}

<!-- Workflow + Workflow activities-->

請參閱[此頁面](faq.md)中的常見問題。

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="執行設定"
>abstract="您可以在此段落中設定與工作流程執行相關的設定，例如構成歷程記錄的保留天數。"




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="活動不可編輯"
>abstract="當在主控台利用其他資料設定&#x200B;**查詢**&#x200B;或&#x200B;**擴充**&#x200B;活動時，會將擴充資料納入考量，並傳遞至出站轉變，但無法編輯。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="建立連結"
>abstract="定義連結設定。"

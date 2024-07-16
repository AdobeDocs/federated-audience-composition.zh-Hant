---
title: 開始使用同盟對象構成
description: 瞭解什麼是Adobe同盟對象構成以及如何在Adobe Experience Platform中使用
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# 開始使用同盟對象構成 {#gs-fac}

Adobe同盟對象構成可協助Adobe Experience Platform應用程式使用者存取儲存在企業資料倉儲中的客戶資料。 客戶資料可存放在多個資料倉儲中，且應可立即存取，無需複製。

Adobe Experience Platform同盟對象構成提供簡單而強大的解決方案，直接在Adobe Real-time Customer Data Platform中連線您的企業資料倉儲，並對資料倉儲的表格執行查詢。

## 主要步驟 {#gs-steps}

Adobe同盟對象構成可讓您直接從資料庫建立和更新Adobe Experience Platform對象，無需任何擷取程式。

![圖表](assets/FAC-diagram.png)

關鍵步驟：

* **設定**

   1. 連線Adobe Experience Platform與您的企業資料倉儲。
支援下列資料庫：Snowflake、Google Big Query、Azure synapse、Redshift。
在[本頁](../connections/federated-db.md)中進一步瞭解
   1. 建立結構以選取應該可從使用者介面存取哪些資料。
在[本頁](../customer/schemas.md)中進一步瞭解
   1. 為您的資料模型建立連結。
在[本頁](../data-management/gs-models.md)中進一步瞭解

* **撰寫對象**

   1. 設計和執行組合以建立對象。
在[本頁](../compositions/gs-compositions.md)中進一步瞭解
   1. 透過Adobe Experience Platform對象入口網站和目的地更新或重複使用現有對象。
在[本頁](../connections/destinations.md)中進一步瞭解

## 更多詳情 {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="執行設定"
>abstract="在此區段中，您可以設定與工作流程執行相關的設定，例如工作流程歷史記錄的保留天數。"




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="活動不可編輯"
>abstract="當在主控台利用其他資料設定&#x200B;**查詢**&#x200B;或&#x200B;**擴充**&#x200B;活動時，會將擴充資料納入考量，並傳遞至出站轉變，但無法編輯。"

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="建立連結"
>abstract="定義連結設定。"

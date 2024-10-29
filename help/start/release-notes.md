---
title: Experience Platform 聯合客群構成的新增功能
description: 最新更新和發行說明
badge: label="限量開放使用" type="Informative"
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 61a70f9de0a6cf171a2ff1128b57ae6206be842c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 53%

---

# 發行說明 {#rn-new}

[!DNL Federated Audience Composition]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都整合在這些發行說明中。 [!DNL Adobe Experience Platform] 上內建的原生 [!DNL Federated Audience Composition] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2024年10月發行 {#fac-24-10}

### 相容性 {#fac-24-10-compat}

透過這個新版本，同盟對象構成現在與下列系統相容。

* **資料庫支援**

  您現在可以透過同盟對象構成來建立與Databricks資料庫的連線。 [了解更多](../connections/federated-db.md#databricks)

* **支援透過AWS PrivateLink安全存取Snowflake**

  現在支援透過私人連結安全存取外部Snowflake資料倉儲。 請注意，您的Snowflake帳戶必須託管至Amazon Web Services (AWS)，且位置與您的同盟對象構成環境相同。 請聯絡您的Adobe代表，以尋求設定安全存取您的Snowflake帳戶的協助。 [了解更多](../connections/federated-db.md#snowflake)

* **Amazon Redshift無伺服器支援**

  透過此新版本，同盟對象構成支援[Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}。

### 改進項目 {#fac-24-10-improvements}

此發行版本隨附下列改進項目。

* **重新整理現有結構描述**

  在同盟資料庫中建立、修改或刪除資料行時，您現在可以偵測並套用變更，方法是按一下對應結構描述中的&#x200B;**[!UICONTROL 重新整理結構描述]**&#x200B;按鈕。 [了解更多](../customer/schemas.md#schema-refresh)

* **將資料模型與新構成建立關聯**

  建立構成時，您現在可以選取要與其產生關聯的資料模型。 有了這個新選項，活動設定會更容易，因為只有關聯資料模型的表格可用。 [了解更多](../compositions/create-composition.md)

## 2024年7月發行版本 — 同盟對象構成(LA) {#fac-la}

>[!AVAILABILITY]
>
>Adobe Experience Platform 聯合客群構成目前僅開放給某些組織使用 (限量開放使用)。
>

聯合客群構成是一項附加功能，使企業能夠靈活地擴充對企業資料倉儲的存取，以使用關鍵企業資料集來構成客群，並提升品牌發起的即時體驗。有了這種新方法，身為 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/home){target="_blank"} 和/或 [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/ajo-home){target="_blank"} 使用者，您就可以直接聯合現有資料倉儲中的客群資料，在一個系統中擴充 Adobe Experience Platform 客群。

對於需要靈活地使用倉庫資料集來構成客群的企業，聯合客群構成恰好滿足了他們不斷增長的市場需求。這使得企業能夠減少資料移動，同時向行銷團隊提供關鍵客群資料，以滿足使用案例要求並提升個人化體驗。 

如需有關聯合客群構成功能的詳細資訊，請參閱[此頁面](get-started.md)和[常見問題](faq.md)。

如需存取聯合客群構成的先決條件和目前護欄的詳細資訊，請參閱[此頁面](access-prerequisites.md)。


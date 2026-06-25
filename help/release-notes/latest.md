---
title: 同盟對象構成發行說明
description: 同盟對象構成的最新更新和發行說明。
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
TQID: https://experienceleague.adobe.com/AqtqibUr1TNXwQ9lrtVoQ3CBNwyjSMS64e4s8y4iTSc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
source-git-commit: 8da27489f6767e837828456b2b11c8238ea6a0a4
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 12%

---

# 發行說明

[!DNL Federated Audience Composition]持續提供新功能、現有功能增強並修正錯誤。 所有變更都已整合在這些發行說明中。 [!DNL Federated Audience Composition] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年6月發行 {#fac-26-06}

6月發行的Federated Audience Composition支援下列功能：

| Google [!DNL BigQuery]的REST API聯結器具有[!DNL Apigee]閘道支援 |
| --- |
| 您現在可以使用REST API聯結器連線至Google [!DNL BigQuery]，並可以選擇在使用服務帳戶驗證時透過[!DNL Apigee]閘道路由您的連線。 如需使用[!DNL Apigee]連線的詳細資訊，請參閱[連線總覽](/help/connections/home.md#apigee)。 |

## 2026年5月發行 {#fac-26-05}

5月發行的Federated Audience Composition支援下列功能：

| Google [!DNL BigQuery]的工作負載識別同盟(WIF)驗證 |
| --- |
| 您現在可以使用WIF驗證連線到Google [!DNL BigQuery]。 如需使用WIF驗證連線的詳細資訊，請參閱[連線總覽](/help/connections/home.md#wif-configuration)。 |

### 改善 {#fac-26-05-improvements}

此版本隨附下列改善專案。

- **在Adobe Journey Optimizer讀取對象歷程中使用同盟對象構成對象的多實體鎖定目標**

  您現在可以在Journey Optimizer讀取對象歷程中善用FAC對象屬性當作補充識別碼。 這可讓您在多個實體（例如帳戶或訂閱層級）啟用對象。

  如需詳細資訊，請參閱歷程指南[&#128279;](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier)中的使用補充識別碼。

## 2026 年 4 月版 {#fac-26-04}

4月發行的Federated Audience Composition支援下列功能和改善：

### 全新功能 {#fac=26-04-feature}

| 新聯結器 — Teradata |
| --- |
| Teradata聯結器現在可與同盟對象構成搭配使用。 您可以使用Teradata聯結器來建立對象和擴充對象使用案例。 如需Teradata聯結器的詳細資訊，請閱讀[連線總覽](/help/connections/home.md)。 |

### 改善 {#fac-26-04-improvements}

此版本隨附下列改善專案。

- **Snowflake的未加密金鑰支援**

  現在，在使用金鑰組驗證來與Snowflake資料倉儲連線時，您可以使用未加密的金鑰。

  若要進一步瞭解如何搭配Snowflake使用未加密的金鑰，請參閱[連線總覽](/help/connections/home.md)。

## 2026 年 3 月發行版本 {#fac-26-03}

3月發行的Federated Audience Composition支援下列功能：

### 全新功能 {#fac-26-03-feature}

| AI支援的分段 |
| --- |
| 您現在可以在AI Assistant中自主建立同盟對象組合。 使用AI助理建立對象時，AI助理會產生一個計畫，在您核准後，該計畫將在您的瀏覽器中執行。 如需使用AI助理建立對象的詳細資訊，請閱讀[AI助理概述](/help/start/ai-assistant.md)。 |

| Operational Insights的AI助理 |
| --- |
| 您現在可以向AI助理詢問有關同盟受眾構成中操作深入分析的問題。 支援的區域包括連線、結構描述和資料模型。 此發行版本不支援&#x200B;**同盟組合**。 如需有關同盟對象構成中AI助理的詳細資訊，請閱讀[AI助理概述](/help/start/ai-assistant.md)。 |

## 2026 年 2 月版 {#fac-26-02}

2月版的Federated Audience Composition支援下列功能：

### 新功能 {#fac-26-02-feature}

| 欄位擴充支援 |
| --- |
| 您現在可以在組合中使用儲存欄位活動。 儲存欄位活動可讓您透過聯合來自外部倉庫的資料來擴充Experience Platform綱要，讓您透過其他屬性增強Experience Platform綱要。 儲存欄位活動同時支援B2B和B2C結構描述。 如需有關使用此活動的詳細資訊，請閱讀[活動概覽](../compositions/activities.md#save-fields)。 |

| Databricks的進階驗證支援 |
| --- |
| 您現在可以使用服務主要驗證或使用OAuth 2.0，以資料庫連線至同盟對象構成。 如需建立連線的詳細資訊，請參閱[連線總覽](../connections/home.md#create)。 |

## 2026 年 1 月版 {#fac-26-01}

1月發行的Federated Audience Composition支援下列新功能和改善：

### 全新功能 {#fac-26-01-feature}

| Azure Synapse服務主要驗證支援 |
| --- |
| 您現在可以使用服務主體來連線至同盟對象構成與Azure Synapse。 如需建立連線的詳細資訊，請參閱[連線總覽](../connections/home.md#create)。 |

| Amazon Web Services (AWS)上Adobe Experience Platform客戶的可用性 |
| --- |
| 如果您的Experience Platform執行個體位於AWS，您現在可以使用同盟對象構成。 如需AWS上Experience Platform的詳細資訊，請閱讀[多雲端總覽](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud)。 |

### 改善 {#fac-26-01-improvements}

此版本隨附下列改善專案。

- **對象的資料到期組態**

  在構成中使用&#x200B;**儲存對象**&#x200B;活動時，您現在可以設定資料有效期。

  若要深入瞭解同盟對象組合中的資料有效期，請參閱[活動指南](../compositions/activities.md#save-audience)。

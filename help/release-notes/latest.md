---
title: 同盟對象構成發行說明
description: 同盟對象構成的最新更新和發行說明。
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 7d12773b36cb963f3d4251a9b88486864056a0fb
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 11%

---


# 發行說明

[!DNL Federated Audience Composition]持續提供新功能、現有功能增強並修正錯誤。 所有變更都整合在這些發行說明中。[!DNL Federated Audience Composition] 原生內建於[!DNL Adobe Experience Platform]，並繼承其最新的創新和改進專案。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2026年2月發行 {#fac-26-02}

2月版的Federated Audience Composition支援下列功能：

### 新功能 {#fac-26-02-feature}

| 欄位擴充支援 |
| --- |
| 您現在可以在組合中使用儲存欄位活動。 儲存欄位活動可讓您透過聯合來自外部倉庫的資料來擴充Experience Platform綱要，讓您透過其他屬性增強Experience Platform綱要。 儲存欄位活動同時支援B2B和B2C結構描述。 如需有關使用此活動的詳細資訊，請閱讀[活動概覽](../compositions/activities.md#save-fields)。 |

| Databricks的進階驗證支援 |
| --- |
| 您現在可以使用服務主要驗證或使用OAuth 2.0，以資料庫連線至同盟對象構成。 如需建立連線的詳細資訊，請參閱[連線總覽](../connections/home.md#create)。 |

## 2026年1月發行 {#fac-26-01}

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

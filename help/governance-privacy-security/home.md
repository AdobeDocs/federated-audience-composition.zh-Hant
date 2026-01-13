---
title: 聯合客群構成中的隱私權和安全性
description: 了解聯合客群構成如何處理使用者資料的隱私權和安全性，包括資料治理、同意執行、存取控制、資料加密和隱私權合規性等功能。
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 77%

---

# 資料控管、隱私權和安全性

>[!IMPORTANT]
>
>同盟對象構成完全符合HIPAA規範，可供Healthcare Shield以及Privacy and Security Shield客戶使用。

Federated Audience Composition提供數種服務和工具，可讓您遵守業務實務、法律義務和開發流程。

這些服務可分成三個類別：

- [資料治理](#data-governance)
- [隱私權](#privacy)
- [安全性](#security)

## 資料治理 {#data-governance}

您可以使用資料控管來管理並識別客戶的資料，確保資料已正確標示，以遵守組織定義或法規的限制。

### 資料使用情況標籤 {#data-usage-labels}

您可以使用資料使用標籤，根據套用至該資料的治理原則，將資料集和欄位分類。 使用構成建立客群後，您可以在產生的結構描述上套用適當的資料標籤，以確保其符合所需的使用限制。

如需在同盟對象構成中使用資料標籤的詳細資訊，請參閱[套用存取標籤區段](../compositions/home.md#access-labels){target="_blank"}。

## 隱私權

同盟受眾構成為Adobe Experience Platform和Adobe Journey Optimizer提供同盟資料以供使用，並確保使用者資料的隱私權得到尊重。

### 隱私權服務 {#privacy-service}

由於同盟對象構成&#x200B;**不會**&#x200B;儲存任何資料倉儲的任何客戶資料，因此您可以使用Adobe Experience Platform Privacy Service來遵守資料主體和資料刪除請求。

例如，當您使用構成畫布中的儲存活動區塊建立客群時，產生的客群將作為外部客群儲存在 Experience Platform 的資料湖中。此外部客群是以其身分欄位和身分命名空間加以標記。因此，您可以使用隱私權服務來存取和刪除具有外部客群的輪廓。

或者，在使用構成畫布中的儲存輪廓活動建立輪廓擴充後，產生的擴充將作為啟用輪廓的結構描述和啟用輪廓的資料集儲存在 Experience Platform 中。此擴充資料是以身分欄位和身分命名空間加以標記。因此，您可以使用隱私權服務來存取和清理這些輪廓。

如需關於隱私權服務的詳細資訊，請詳閱[隱私權服務概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/home){target="_blank"}。

### 隱私權要求 {#privacy-requests}

在隱私權服務中，您可以建立及管理要求存取和刪除聯合客群構成中客戶資料的個別隱私權請求。隱私權服務提供[使用者介面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant){target="_blank"}和 [RESTful API](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/overview){target="_blank"}，幫助您管理客戶資料請求。

如需關於建立和管理隱私權請求的詳細資訊，請參閱[隱私權服務 UI 中的隱私權作業指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/ui/user-guide){target="_blank"}。

### 同意原則執行 {#consent}

聯合客群構成透過 Experience Platform 提供工具，讓您可以自動執行同意，確保您依據客戶提供的同意來啟動客群。

例如，當您使用構成畫布中的儲存活動區塊建立客群時，產生的客群將作為外部客群儲存在 Experience Platform 的資料湖中。Experience Platform 在啟動期間自動支援同意驗證。如需更多資訊，請詳閱[分段服務常見問題](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq#consent){target="_blank"}。

或者，在使用構成畫布中的儲存輪廓活動建立輪廓擴充後，產生的擴充將作為啟用輪廓的結構描述和啟用輪廓的資料集儲存在 Experience Platform 中。如果是現有輪廓，可用的同意屬性會在啟動期間自動生效。如果是新輪廓，在輪廓提取期間提供的同意屬性將在啟動期間自動生效。如需將同意套用於輪廓的詳細資訊，請詳閱[同意和偏好設定欄位群組指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}。

如需套用同意的詳細資訊，請詳閱[管理原則 UI 指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}。

### 資料生命週期 {#data-lifecycle}

由於聯合客群構成&#x200B;**不會**&#x200B;儲存任何資料倉儲的任何客戶資料，因此您可以使用 Experience Platform 來處理資料生命週期。透過進階資料生命週期管理，您可以在資料集和記錄層級管理資料生命週期。

例如，當您使用構成畫布中的儲存活動區塊建立客群時，產生的客群將作為外部客群儲存在 Experience Platform 的資料湖中。由於該資料&#x200B;**不會**&#x200B;儲存在聯合客群構成中，因此當在客群入口網站中刪除客群時，客群資料和對應的資料集也會自動刪除。

或者，在使用構成畫布中的儲存輪廓活動建立輪廓擴充後，產生的擴充將作為啟用輪廓的結構描述和啟用輪廓的資料集儲存在 Experience Platform 中。因此，您可以透過資料生命週期來存取和清理輪廓。

如需關於使用資料生命週期的詳細資訊，請詳閱[資料生命週期概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-lifecycle/home){target="_blank"}。

## 安全性 {#security}

資料安全性可確保您的資料在同盟對象構成中受到保護。

### 加密 {#encryption}

同盟對象構成透過靜態資料加密、傳輸中資料加密和客戶管理的金鑰提供加密。

靜態資料是指聯合客群構成中使用的客戶資料。資料由雲端服務提供者加密，並以加密形式用於聯合客群構成。

傳輸中的資料是指在聯合客群構成中從一個元件移動到另一個元件的客戶資料。資料在整個聯合客群構成元件間使用 TLS 1.3 over HTTPS 保持加密。

如需關於 Adobe 如何處理資料加密的詳細資訊，請詳閱[Experience Platform 中的資料加密](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}指南。

### 客戶自管金鑰 {#customer-managed-keys}

客戶自管金鑰可讓您使用自己的加密金鑰來加密資料，從而讓您能夠控制資料。由於聯合客群構成&#x200B;**不會**&#x200B;儲存任何客戶資料，因此您可以直接在產生的客群和擴充上使用客戶自管金鑰，因為它們將儲存在 Experience Platform 的資料湖中。

如需關於客戶自管金鑰的詳細資訊，請詳閱[客戶自管金鑰指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}。

### 稽核記錄 {#audit-log}

在聯合客群構成中執行的所有建立、讀取、更新和刪除操作都記錄在稽核記錄中。您可以使用此稽核記錄來追蹤這些操作、強化問責機制並支援合規性稽核。

若要了解更多資訊，請詳閱[稽核記錄概觀](/help/admin/audit-trail.md){target="_blank"}。

### 存取控制 {#access-control}

您可以在欄位和角色層級控制對聯合客群構成的存取。您可以使用這些存取控制來強制施行資料治理原則，限制敏感資訊的曝露，並將存取權與使用者職責相符。

如需同盟對象構成中存取控制的詳細資訊，請參閱[存取控制指南](/help/governance-privacy-security/access-control.md){target="_blank"}。

### 資料本地化 {#data-localization}

聯合客群構成&#x200B;**不會**&#x200B;儲存任何客戶資料。因此，你需要確保&#x200B;**僅**&#x200B;將外部資料庫連接至相符的沙箱區域，以將資料保存在相同區域內。如果您將不同區域的資料庫連接至沙箱，Adobe 將&#x200B;**不承擔**&#x200B;資料本地化的責任。

## 後續步驟 {#next-steps}

閱讀本指南後，您對用於同盟對象構成的資料控管、隱私權和安全性功能有了更深入的瞭解，包括資料使用標籤、隱私權法規遵循、同意執行、資料生命週期管理以及存取控制。

---
title: 聯合客群構成中的隱私權和安全性
description: 了解聯合客群構成如何處理使用者資料的隱私權和安全性，包括資料治理、同意執行、存取控制、資料加密和隱私權合規性等功能。
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 8076a7851d0cd5cd84a7c48c6f1783b452864903
workflow-type: ht
source-wordcount: '1085'
ht-degree: 100%

---

# 聯合客群構成中的隱私權和安全性

聯合客群構成遵循多種安全措施，以在處理期間保護您的資料。

## 隱私權服務 {#privacy}

聯合客群構成為 Adobe Experience Platform 和 Adobe Journey Optimizer 提供聯合資料。然而，Federated Audience Composition **不會**&#x200B;儲存任何資料倉儲的任何客戶資料。因此，您可以使用 Adobe Experience Platform 隱私權服務來遵守資料主體和資料刪除請求。

例如，當您使用構成畫布中的儲存活動區塊建立客群時，產生的客群將作為外部客群儲存在 Experience Platform 的資料湖中。此外部客群是以其身分欄位和身分命名空間加以標記。因此，您可以使用隱私權服務來存取和刪除具有外部客群的輪廓。

或者，在使用構成畫布中的儲存輪廓活動建立輪廓擴充後，產生的擴充將作為啟用輪廓的結構描述和啟用輪廓的資料集儲存在 Experience Platform 中。此擴充資料是以身分欄位和身分命名空間加以標記。因此，您可以使用隱私權服務來存取和清理這些輪廓。

如需關於隱私權服務的詳細資訊，請詳閱[隱私權服務概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/home){target="_blank"}。

### 隱私權請求 {#privacy-requests}

在隱私權服務中，您可以建立及管理要求存取和刪除聯合客群構成中客戶資料的個別隱私權請求。隱私權服務提供[使用者介面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant){target="_blank"}和 [RESTful API](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/overview){target="_blank"}，幫助您管理客戶資料請求。

如需關於建立和管理隱私權請求的詳細資訊，請參閱[隱私權服務 UI 中的隱私權作業指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/ui/user-guide){target="_blank"}。

## 同意原則執行 {#consent}

聯合客群構成透過 Experience Platform 提供工具，讓您可以自動執行同意，確保您依據客戶提供的同意來啟動客群。

例如，當您使用構成畫布中的儲存活動區塊建立客群時，產生的客群將作為外部客群儲存在 Experience Platform 的資料湖中。Experience Platform 在啟動期間自動支援同意驗證。如需更多資訊，請詳閱[分段服務常見問題](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq#consent){target="_blank"}。

或者，在使用構成畫布中的儲存輪廓活動建立輪廓擴充後，產生的擴充將作為啟用輪廓的結構描述和啟用輪廓的資料集儲存在 Experience Platform 中。如果是現有輪廓，可用的同意屬性會在啟動期間自動生效。如果是新輪廓，在輪廓提取期間提供的同意屬性將在啟動期間自動生效。如需將同意套用於輪廓的詳細資訊，請詳閱[同意和偏好設定欄位群組指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}。

如需套用同意的詳細資訊，請詳閱[管理原則 UI 指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}。

## 資料生命週期 {#data-lifecycle}

由於聯合客群構成&#x200B;**不會**&#x200B;儲存任何資料倉儲的任何客戶資料，因此您可以使用 Experience Platform 來處理資料生命週期。透過進階資料生命週期管理，您可以在資料集和記錄層級管理資料生命週期。

例如，當您使用構成畫布中的儲存活動區塊建立客群時，產生的客群將作為外部客群儲存在 Experience Platform 的資料湖中。由於該資料&#x200B;**不會**&#x200B;儲存在聯合客群構成中，因此當在客群入口網站中刪除客群時，客群資料和對應的資料集也會自動刪除。

或者，在使用構成畫布中的儲存輪廓活動建立輪廓擴充後，產生的擴充將作為啟用輪廓的結構描述和啟用輪廓的資料集儲存在 Experience Platform 中。因此，您可以透過資料生命週期來存取和清理輪廓。

如需關於使用資料生命週期的詳細資訊，請詳閱[資料生命週期概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-lifecycle/home){target="_blank"}。

## 資料使用情況標籤 {#data-usage-labels}

資料使用情況標籤可讓您根據套用於該資料的治理原則，將資料集和欄位進行分類。使用構成建立客群後，您可以在產生的結構描述上套用適當的資料標籤，以確保其符合所需的使用限制。

如需關於使用資料標籤的詳細資訊，請詳閱[資料使用情況標籤概述](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/labels/overview){target="_blank"}。

## 加密 {#encryption}

彈性客群構成透過靜態資料加密、傳輸中資料加密和客戶自管金鑰提供加密。

靜態資料是指聯合客群構成中使用的客戶資料。資料由雲端服務提供者加密，並以加密形式用於聯合客群構成。

傳輸中的資料是指在聯合客群構成中從一個元件移動到另一個元件的客戶資料。資料在整個聯合客群構成元件間使用 TLS 1.3 over HTTPS 保持加密。

如需關於 Adobe 如何處理資料加密的詳細資訊，請詳閱[Experience Platform 中的資料加密](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}指南。

### 客戶自管金鑰 {#customer-managed-keys}

客戶自管金鑰可讓您使用自己的加密金鑰來加密資料，從而讓您能夠控制資料。由於聯合客群構成&#x200B;**不會**&#x200B;儲存任何客戶資料，因此您可以直接在產生的客群和擴充上使用客戶自管金鑰，因為它們將儲存在 Experience Platform 的資料湖中。

如需關於客戶自管金鑰的詳細資訊，請詳閱[客戶自管金鑰指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}。

## 稽核記錄 {#audit-log}

在聯合客群構成中執行的所有建立、讀取、更新和刪除操作都記錄在稽核記錄中。您可以使用此稽核記錄來追蹤這些操作、強化問責機制並支援合規性稽核。

若要了解更多資訊，請詳閱[稽核記錄概觀](/help/admin/audit-trail.md){target="_blank"}。

## 存取控制 {#access-control}

您可以在欄位和角色層級控制對聯合客群構成的存取。您可以使用這些存取控制來強制施行資料治理原則，限制敏感資訊的曝露，並將存取權與使用者職責相符。

如需關於聯合客群構成存取控制的詳細資訊，請詳閱[存取聯合客群構成指南](/help/start/feature-access.md){target="_blank"}。

## 資料本地化 {#data-localization}

聯合客群構成&#x200B;**不會**&#x200B;儲存任何客戶資料。因此，你需要確保&#x200B;**僅**&#x200B;將外部資料庫連接至相符的沙箱區域，以將資料保存在相同區域內。如果您將不同區域的資料庫連接至沙箱，Adobe 將&#x200B;**不承擔**&#x200B;資料本地化的責任。

## 後續步驟 {#next-steps}

閱讀完本指南後，您將對聯合客群構成所採用的隱私權與安全性功能有更深入的了解，包括資料治理、隱私權合規性、同意執行、資料生命週期管理以及存取控制。

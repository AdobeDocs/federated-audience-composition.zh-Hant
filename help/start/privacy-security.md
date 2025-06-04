---
title: 同盟對象組合中的隱私權與安全性
description: 瞭解同盟受眾構成如何處理使用者資料的隱私和安全性，包括資料治理、同意實作、存取控制、資料加密和隱私權法規遵循等功能。
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# 同盟對象組合中的隱私權與安全性

同盟對象構成符合許多安全性實務，可在處理期間保護您的資料。

## Privacy Service {#privacy}

同盟對象構成提供Adobe Experience Platform和Adobe Journey Optimizer使用的同盟資料。 不過，同盟對象構成&#x200B;**不會**&#x200B;儲存來自任何資料倉儲的任何客戶資料。 因此，您可以使用Adobe Experience Platform Privacy Service來遵守資料主體和資料刪除請求。

例如，當您使用構成畫布中的儲存活動區塊來建立對象時，產生的對象會作為外部對象儲存在Experience Platform的資料湖中。 此外部對象會以其身分欄位和身分名稱空間標示。 因此，您可以使用Privacy Service來存取和移除具有外部對象的這些設定檔。

或者，在構成畫布中使用儲存設定檔活動建立設定檔擴充後，產生的擴充會作為啟用設定檔的結構描述和啟用設定檔的資料集儲存在Experience Platform中。 此擴充資料會以身分欄位和身分名稱空間標示。 因此，您可以使用Privacy Service來存取和清除這些設定檔。

如需Privacy Service的詳細資訊，請閱讀[Privacy Service概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/home){target="_blank"}。

### 隱私權要求 {#privacy-requests}

在Privacy Service中，您可以建立和管理個人隱私權請求，以存取和刪除同盟對象構成中的客戶資料。 Privacy Service提供[使用者介面](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant){target="_blank"}和[RESTful API](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/api/overview){target="_blank"}，協助您管理客戶資料請求。

如需建立及管理隱私權要求的詳細資訊，請參閱Privacy Service UI指南[&#128279;](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/privacy/ui/user-guide){target="_blank"}中的隱私權工作。

## 同意原則執行 {#consent}

同盟對象構成可透過Experience Platform提供可讓您自動執行同意的工具，確保您根據提供給客戶的同意來啟用對象。

例如，當您使用構成畫布中的儲存活動區塊來建立對象時，產生的對象會作為外部對象儲存在Experience Platform的資料湖中。 Experience Platform在啟用期間自動支援同意驗證。 如需詳細資訊，請參閱[Segmentation Service常見問題集](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq#consent){target="_blank"}。

或者，當您使用構成畫布中的儲存設定檔活動建立設定檔擴充後，產生的擴充會作為啟用設定檔的結構描述和啟用設定檔的資料集儲存在Experience Platform中。 對於現有的設定檔，在啟用期間會自動接受可用的同意屬性。 對於新設定檔，在啟動期間會自動遵循設定檔擷取期間提供的同意屬性。 如需將同意套用至設定檔的詳細資訊，請閱讀[同意和偏好設定欄位群組指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}。

如需套用同意的詳細資訊，請參閱[管理原則UI指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}。

## 資料生命週期 {#data-lifecycle}

由於同盟對象構成&#x200B;**不會**&#x200B;儲存來自任何資料倉儲的任何客戶資料，因此您可以使用Experience Platform處理資料生命週期。 透過進階資料生命週期管理，您可以在資料集和記錄層級管理您的資料生命週期。

例如，當您在構成畫布中使用儲存活動區塊來建立對象時，產生的對象會作為外部對象儲存在Experience Platform的資料湖中。 由於此資料是&#x200B;**非**&#x200B;儲存在同盟對象構成中，因此對象資料與對應的資料集會在對象入口網站中刪除對象時自動刪除。

或者，當您使用構成畫布中的儲存設定檔活動建立設定檔擴充後，產生的擴充會作為啟用設定檔的結構描述和啟用設定檔的資料集儲存在Experience Platform中。 因此，您可以在資料生命週期中存取及清除設定檔。

如需使用資料生命週期的詳細資訊，請參閱[資料生命週期概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-lifecycle/home){target="_blank"}。

## 資料使用情況標籤 {#data-usage-labels}

資料使用情況標籤可讓您根據套用至該資料的治理原則，將資料集和欄位分類。 使用構成建立受眾後，您可以在產生的結構描述上套用適當的資料標籤，以確保其符合必要的使用限制。

如需使用資料標籤的詳細資訊，請閱讀[資料使用標籤概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/labels/overview){target="_blank"}。

## 加密 {#encryption}

彈性的對象組合可透過靜態資料加密、傳輸中資料加密和客戶管理的金鑰提供加密。

靜態資料是指用於同盟對象構成的客戶資料。 資料會由雲端服務提供者加密，並用於加密形式的同盟對象構成。

傳輸中的資料是指在同盟對象構成中從一個元件移動到另一個元件時的客戶資料。 所有使用TLS 1.3 （透過HTTPS）的同盟受眾構成元件中的資料都會保持加密。

如需Adobe如何處理資料加密的詳細資訊，請閱讀Experience Platform中[資料加密](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}的指南。

### 客戶自控金鑰 {#customer-managed-keys}

客戶自控金鑰可讓您使用自己的加密金鑰來加密資料，進而控制資料。 由於同盟對象構成&#x200B;**不會**&#x200B;儲存任何客戶資料，因此您可以直接在產生的對象和增強專案上使用客戶自控金鑰，因為這些金鑰將會儲存在Experience Platform上的資料湖中。

如需客戶自控金鑰的詳細資訊，請參閱[客戶自控金鑰指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}。

## 稽核記錄 {#audit-log}

在Federated Audience Composition中執行的所有建立、讀取、更新和刪除操作，都會記錄到稽核軌跡。 您可以使用此稽核記錄來追蹤這些動作、強制執行責任以及支援規範遵循稽核。

如需詳細資訊，請閱讀[稽核軌跡概觀](/help/admin/audit-trail.md){target="_blank"}。

## 存取控制 {#access-control}

您可以同時在欄位和角色層級控制同盟對象構成的存取權。 您可以使用這些存取控制來強制實施資料治理原則、限制敏感資訊的曝光，以及根據使用者責任來調整存取權。

如需同盟對象構成中存取控制的詳細資訊，請參閱[存取同盟對象構成指南](/help/start/feature-access.md){target="_blank"}。

## 資料本地化 {#data-localization}

同盟對象構成&#x200B;**不**&#x200B;儲存任何客戶資料。 因此，您必須確保僅&#x200B;**將**&#x200B;外部資料庫與相符的沙箱區域連線，以將您的資料儲存在相同區域中。 如果將其他區域的資料庫連線到沙箱，Adobe會&#x200B;**不負責**&#x200B;資料本地化。

## 後續步驟 {#next-steps}

閱讀本指南後，您對用於同盟受眾構成的隱私權和安全性功能有了更深入的瞭解，包括資料治理、隱私權法規遵循、同意執行、資料生命週期管理及存取控制。

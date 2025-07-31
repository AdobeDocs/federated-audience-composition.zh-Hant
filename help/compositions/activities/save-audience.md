---
audience: end-user
title: 使用儲存客群活動
description: 瞭解如何使用「儲存對象」活動
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: c133ddb2b1d2a75e7f9614d7623fad63aa24eb55
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 25%

---

# 儲存客群 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="儲存一個對象"
>abstract="使用此活動從構成中的群體運算上游建立新的客群。建立的對象將新增至對象清單中，並可透過「**對象**」選單使用。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="產生傳出轉變"
>abstract="如果您想在「**儲存對象**」活動之後新增轉變，請使用此選項。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="主要身分識別欄位"
>abstract="選取輪廓要用的主要身分識別。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="進一步瞭解 Experience Platform 文件"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="身分識別命名空間"
>abstract="選取輪廓要用的命名空間。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces" text="進一步瞭解 Experience Platform 文件"

>[!IMPORTANT]
>
>如果您的沙箱使用&#x200B;**資料集優先順序**&#x200B;合併原則，請聯絡Adobe客戶服務以將`Halos UPS`資料集新增到合併原則中。
>
>如需有關合併原則的詳細資訊，請參閱[合併原則概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/merge-policies/overview)。

**[!UICONTROL 儲存對象]**&#x200B;活動可讓您從構成中的母體運算上游建立新的對象。 建立的對象會新增至Adobe Experience Platform對象清單，並可透過&#x200B;**對象**&#x200B;功能表使用。 [學習如何使用客群](../../start/audiences.md)

此活動主要用於將母體族群轉換為可重複使用的對象，讓母體族群可繼續在相同構成中運算。 將其連線到其他目標定位活動，例如&#x200B;**建立對象**&#x200B;或&#x200B;**合併**&#x200B;活動。

**[!UICONTROL 儲存對象]**&#x200B;活動會產生新的對象結構描述和相關資料集，其中可能包含個人識別資訊(PII)或受保護的健康資訊(PHI)。 建立對象後，請與您的管理員合作，確保根據您組織的資料原則套用適當的資料治理標籤。 如需如何套用資料使用標籤的詳細資訊，請參閱[資料使用標籤使用手冊](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/labels/user-guide)。

## 設定儲存客群活動 {#save-audience-configuration}

請按照以下步驟，設定「**儲存客群**」活動：

1. 將&#x200B;**儲存對象**&#x200B;活動新增至您的組合。

   ![](../assets/save-audience.png)

1. 指定要建立的對象標籤。

   >[!IMPORTANT]
   >
   >對象標籤在目前沙箱中必須是唯一的。 其標籤不得與任何現有對象相同。

1. 使用「對象對應」區段來選取您要與新建立的對象一起帶入的欄位。 若要這麼做，請按一下&#x200B;**新增對象對應**，然後選擇來源和目標對象欄位。

   重複此作業，視需要儘量新增對象對應。

1. 選取主要身分和名稱空間，以用於識別資料庫中的目標設定檔：

   * **主要身分欄位**：選取要用來識別設定檔的欄位。 例如，其電子郵件地址或電話號碼。
   * **識別名稱空間**：選取要用來識別設定檔的名稱空間，也就是要做為識別金鑰的資料型別。 例如，如果已選取電子郵件地址作為主要身分欄位，則應選取身分名稱空間&#x200B;**電子郵件**。 如果唯一識別碼是電話號碼，則應該選取識別名稱空間&#x200B;**電話**。

## 在 Adobe Experience Platform 中存取客群 {#access-audience}

執行構成後，產生的對象會儲存至Adobe Experience Platform作為外部對象，並可在Audience Portal的Adobe Real-Time CDP和/或Adobe Journey Optimizer中使用。 如需對象入口網站的詳細資訊，請閱讀[對象入口網站概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}。

建立的對象包含「對象對應」區段中選取的所有欄位。 您可以在Journey Optimizer中鎖定此對象，或在Adobe Experience Platform支援的任何目的地啟用它。

[請到 Adobe Experience Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}那邊，了解更多相關資訊。

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->

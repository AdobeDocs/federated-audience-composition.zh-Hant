---
title: 存取聯合客群構成
description: 了解聯合客群構成所需的權限
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 46%

---

# 存取聯合客群構成 {#feature-access}

## 管理對沙箱的存取權 {#access-sandboxes}

當您購買 Adobe Experience Platform 聯合客群構成時，系統會為當時的每個使用中沙箱建立產品設定檔。此產品設定檔是在 Admin Console 中的 **Adobe Experience Platform** 產品卡下方建立，並遵循以下命名慣例：`ACP_FAC - <<SandboxName>> - admin.`。若要存取特定沙箱的聯合客群構成，您必須將使用者新增至為該沙箱建立的產品設定檔中。

例如，如果啟用名為「fac-test」的新沙箱，則會建立對應的產品設定檔「ACP_FAC - fac-test - admin」。為了使用此沙箱存取聯合客群構成，您必須將使用者新增至此產品設定檔。

## 管理對聯合客群構成的存取權

若要存取&#x200B;**同盟對象構成**，您必須先確定您指派必要的許可權，以存取同盟對象構成的不同層面。 這些角色必須指派給需要&#x200B;**同盟對象構成**&#x200B;存取權的使用者。

請注意，只有管理員才能夠指派權限。

1. 導覽至「**[!UICONTROL 權限]**」選單。

1. 從「**[!UICONTROL 角色]**」選單中，選取您想要更新的&#x200B;**[!UICONTROL 角色]**。

   ![](assets/access_fda_1.png)

1. 選取&#x200B;**[!UICONTROL 編輯]**&#x200B;以修改您角色的許可權。

   ![](assets/access_fda_2.png)

1. 為使用者新增必要許可權。 您可以新增以下許可權來存取同盟對象構成：

   | 權限 | 說明 |
   | ---------- | ----------- |
   | 管理同盟資料 | 使用此許可權可管理同盟對象構成的各個層面。 此許可權包含管理同盟資料庫、管理同盟結構、管理同盟資料模型，以及管理同盟組成。 |
   | 管理同盟資料庫 | 使用此許可權來新增、檢視、更新和刪除您與同盟資料庫的連線。 |
   | 檢視同盟資料庫 | 使用此許可權來檢視您與同盟資料庫的連線。 |
   | 管理同盟結構描述 | 使用此許可權來建立、檢視、更新、刪除和重新整理結構描述。 |
   | 檢視同盟結構描述資料 | 使用此許可權可檢視架構區段內的資料標籤。 |
   | 檢視同盟結構描述 | 使用此許可權來檢視綱要表格。 |
   | 管理同盟資料模型 | 使用此許可權來建立、檢視、更新和刪除資料模型。 |
   | 檢視同盟資料模型 | 使用此許可權來檢視資料模型。 |
   | 檢視同盟稽核軌跡 | 使用此許可權可檢視Federated Audience Composition的稽核軌跡。 |
   | 管理同盟組合 | 使用此許可權來建立、檢視、更新和刪除同盟組合。 |
   | 檢視同盟組合 | 使用此許可權來檢視同盟組合。 |

   ![](assets/permissions.png)

1. 完成必要的變更後，請選取&#x200B;**[!UICONTROL 儲存]**。

對於任何已指派此角色的使用者，其權限都將自動更新並可存取聯合客群構成。

若要將此角色指派給新使用者：

1. 導覽至您角色儀表板中的&#x200B;**[!UICONTROL 使用者]**&#x200B;索引標籤，並選取&#x200B;**[!UICONTROL 新增使用者]**。

   ![](assets/access_fda_4.png)

1. 輸入使用者的姓名或電子郵件地址，或從可用清單中進行選取。完成後，選取&#x200B;**[!UICONTROL 儲存]**。

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

然後，使用者將會收到一封電子郵件，內含存取執行個體的指示。如果之前未建立該使用者，請參閱[此文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/abac/permissions-ui/users)。

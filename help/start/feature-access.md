---
title: 存取聯合客群構成
description: 了解聯合客群構成所需的權限
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 100%

---

# 存取聯合客群構成 {#feature-access}

## 管理對沙箱的存取權 {#access-sandboxes}

當您購買 Adobe Experience Platform 聯合客群構成時，系統會為當時的每個使用中沙箱建立產品設定檔。此產品設定檔是在 Admin Console 中的 **Adobe Experience Platform** 產品卡下方建立，並遵循以下命名慣例：`ACP_FAC - <<SandboxName>> - admin.`。若要存取特定沙箱的聯合客群構成，您必須將使用者新增至為該沙箱建立的產品設定檔中。

例如，如果啟用名為「fac-test」的新沙箱，則會建立對應的產品設定檔「ACP_FAC - fac-test - admin」。為了使用此沙箱存取聯合客群構成，您必須將使用者新增至此產品設定檔。

## 管理對聯合客群構成的存取權

若要存取&#x200B;**聯合客群構成**，您必須先確保指派所需權限以便存取聯合客群構成的所有層面。然後，您必須將這些角色指派給需要存取&#x200B;**聯合客群構成**&#x200B;的使用者。

請注意，只有管理員才能夠指派權限。

1. 導覽至「**[!UICONTROL 權限]**」選單。

1. 從「**[!UICONTROL 角色]**」選單中，選取您想要更新的&#x200B;**[!UICONTROL 角色]**。

   ![](assets/access_fda_1.png)

1. 選取「**[!UICONTROL 編輯]**」以修改您的角色權限。

   ![](assets/access_fda_2.png)

1. 新增使用者所需的權限。您可以新增以下權限以便存取聯合客群構成：

   | 權限 | 說明 |
   | ---------- | ----------- |
   | 管理聯合資料 | 使用此權限來管理聯合客群構成的所有層面。此權限包含管理聯合資料庫、管理聯合結構描述、管理聯合資料模型和管理聯合構成。 |
   | 管理聯合資料庫 | 使用此權限來新增、檢視、更新和刪除您與聯合資料庫的連線。 |
   | 檢視聯合資料庫 | 使用此權限來檢視您與聯合資料庫的連線。 |
   | 管理聯合結構描述 | 使用此權限來建立、檢視、更新、刪除和刷新結構描述。 |
   | 檢視聯合結構描述資料 | 使用此權限來檢視結構描述部分內的資料標籤。 |
   | 檢視聯合結構描述 | 使用此權限來檢視結構描述表。 |
   | 管理聯合資料模型 | 使用此權限來建立、檢視、更新和刪除資料模型。 |
   | 檢視聯合資料模型 | 使用此權限來檢視資料模型。 |
   | 檢視聯合稽核軌跡 | 使用此權限來檢視聯合客群構成的稽核軌跡。 |
   | 管理聯合構成 | 使用此權限來建立、查看、更新和刪除聯合構成。 |
   | 檢視聯合構成 | 使用此權限來檢視聯合構成。 |

   ![](assets/permissions.png)

1. 在完成必要的變更後，請選取「**[!UICONTROL 儲存]**」。

對於任何已指派此角色的使用者，其權限都將自動更新並可存取聯合客群構成。

若要將此角色指派給新使用者：

1. 導覽至「角色」儀表板內的「**[!UICONTROL 使用者]**」標籤，然後選取「**[!UICONTROL 新增使用者]**」。

   ![](assets/access_fda_4.png)

1. 輸入使用者的姓名或電子郵件地址，或從可用清單中進行選取。完成後，選取「**[!UICONTROL 儲存]**」。

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

然後，使用者將會收到一封電子郵件，內含存取執行個體的指示。如果之前未建立該使用者，請參閱[此文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/abac/permissions-ui/users)。

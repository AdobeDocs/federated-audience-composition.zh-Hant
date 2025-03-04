---
title: 存取聯合客群構成
description: 了解聯合客群構成所需的權限
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
hide: true
hidefromtoc: true
source-git-commit: 0b8781b5b33d96db7d7f23b3c399942b9cfe901f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 93%

---

# 存取聯合客群構成 {#feature-access}

## 管理對沙箱的存取權 {#access-sandboxes}

購買Adobe Experience Platform同盟對象構成時，系統會同時為每個使用中的沙箱建立產品設定檔。 此產品設定檔是在 Admin Console 中的 **Adobe Experience Platform** 產品卡下方建立，並遵循以下命名慣例：`ACP_FAC - <<SandboxName>> - admin.`。若要存取特定沙箱的聯合客群構成，您必須將使用者新增至為該沙箱建立的產品設定檔中。

例如，如果啟用名為「fac-test」的新沙箱，則會建立對應的產品設定檔「ACP_FAC - fac-test - admin」。為了使用此沙箱存取聯合客群構成，您必須將使用者新增至此產品設定檔。

## 管理對聯合客群構成的存取權

>[!AVAILABILITY]
>
>權限是作為 3 月版的一部分提供。

若要存取&#x200B;**聯合客群構成**，您必須先確保&#x200B;**管理聯合資料**&#x200B;權限已指派給適當的角色。然後，您必須將這些角色指派給需要存取&#x200B;**聯合客群構成**&#x200B;的使用者。

請注意，只有管理員才能夠指派權限。

1. 導覽至「**[!UICONTROL 權限]**」選單。

1. 從「**[!UICONTROL 角色]**」選單中，選取您想要更新的&#x200B;**[!UICONTROL 角色]**。

   ![](assets/access_fda_1.png)

1. 按一下「**[!UICONTROL 編輯]**」以修改您的角色權限。

   ![](assets/access_fda_2.png)

1. 新增&#x200B;**聯合資料**&#x200B;資源，然後從下拉式選單中選取「**[!UICONTROL 管理聯合資料]**」。

   ![](assets/access_fda_3.png)

1. 在完成必要的變更後，請按一下「**[!UICONTROL 儲存]**」。

對於任何已指派此角色的使用者，其權限都將自動更新並可存取聯合客群構成。

若要將此角色指派給新使用者：

1. 導覽至「角色」儀表板內的「**[!UICONTROL 使用者]**」標籤，然後按一下「**[!UICONTROL 新增使用者]**」。

   ![](assets/access_fda_4.png)

1. 輸入使用者的姓名或電子郵件地址，或從可用清單中進行選取。完成後，按一下「**[!UICONTROL 儲存]**」。

然後，使用者將會收到一封電子郵件，內含存取執行個體的指示。如果之前未建立該使用者，請參閱[此文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/abac/permissions-ui/users)。

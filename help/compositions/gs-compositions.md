---
audience: end-user
title: 開始使用構成
description: 學習如何開始構成
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 17%

---

# 開始使用構成 {#compositions}

>[!AVAILABILITY]
>
>若要存取作品，您需要以下權限之一：
>
>-**管理聯合構成**
>>-**檢視聯合構成**
>
>如需必要許可權的詳細資訊，請參閱[存取控制指南](/help/governance-privacy-security/access-control.md)。

同盟對象構成可讓您建立構成，其中您可以使用各種活動在視覺畫布中建立對象。 建立構成後，產生的對象會儲存至Adobe Experience Platform中，並可在Experience Platform目的地和Adobe Journey Optimizer中運用於鎖定客戶。

![範例構成工作流程顯示在同盟對象構成中。](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## 存取和管理構成 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="構成"
>abstract="在此畫面中，您可以存取構成的完整清單、檢查其目前狀態、上次/下次執行日期並建立新的構成。"

可透過&#x200B;**[!UICONTROL 客戶]**&#x200B;區段內&#x200B;**[!UICONTROL 同盟組合]**&#x200B;索引標籤中的Adobe Experience Platform **[!UICONTROL 對象]**&#x200B;功能表存取組合。

在此畫面中，您可以建立新的構成，並存取現有的構成。您也可以選取現有構成名稱旁的![省略符號](/help/assets/icons/more.png)按鈕，以複製或刪除現有構成。

您也可以檢視有關構成的相關資訊，包括名稱、狀態、建立者和上次修改日期。

| 狀態 | 說明 |
| ------ | ----------- |
| **[!UICONTROL 草稿]** | 構成已建立並儲存。 |
| **[!UICONTROL 進行中]** | 構成已執行，且目前正在執行。 |
| **[!UICONTROL 已停止]** | 構成執行完成並已停止。 |
| **[!UICONTROL 已暫停]** | 構成執行已暫停。 |
| **[!UICONTROL 錯誤]** | 構成執行發生錯誤。 若要檢視有關錯誤的詳細資訊，請開啟構成並存取記錄。 |

您可以在[開始和監視撰寫指南](./start-monitor-composition.md)中瞭解如何開始或停止撰寫。

![顯示可用的組合清單。](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

若要調整清單並尋找您要尋找的組合，您可以搜尋清單，並依組合的狀態或上次處理日期篩選組合。

您也可以透過新增或移除資料欄來自訂清單。若要這麼做，請選取&#x200B;**[!UICONTROL 設定資料行]**&#x200B;按鈕，然後新增或移除所需的輸出資料行。

![會顯示可新增至組合瀏覽頁面的可用欄清單。](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### 套用存取標籤 {#access-labels}

若要將存取權標籤套用至特定構成，請選取構成，然後選取&#x200B;**[!UICONTROL 管理存取權]**。

![構成畫布中會醒目顯示[管理存取權]按鈕。](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

**[!UICONTROL 管理存取權]**&#x200B;彈出視窗會出現。 在此頁面上，您可以將適用的存取權和資料治理標籤套用至您的構成。

![顯示[管理存取權]彈出視窗。 這會顯示您可以套用至構成的所有可用標籤清單。](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| 標籤型別 | 說明 |
| ---------- | ----------- |
| 合約標籤 | 合約標籤（「C」標籤）可用來對具有合約義務或與貴組織的資料治理原則相關的資料進行分類。 |
| 身分識別標籤 | 身分標籤（「I」標籤）可用來對可識別或聯絡特定人員的資料進行分類。 |
| 敏感標籤 | 敏感標籤（「S」標籤）可用來分類您和/或您的組織認為敏感。 |
| 合作夥伴生態系統標籤 | 合作夥伴生態系統標籤可用來對來自組織外部來源的資料進行分類。 |

如需存取和資料控管標籤的詳細資訊，請閱讀[資料使用標籤字彙表](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference)。

## 後續步驟

閱讀本指南後，您已瞭解如何存取、管理和建立構圖的存取標籤。 如需整體使用對象的詳細資訊，請參閱[對象指南](../start/audiences.md)。

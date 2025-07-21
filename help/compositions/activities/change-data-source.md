---
audience: end-user
title: 變更資料Source活動
description: 瞭解如何使用變更資料來源活動來變更構成所使用的資料來源，在構成中管理資料方面提供更大的彈性。
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# 變更資料來源

>[!IMPORTANT]
>
>**[!UICONTROL 變更維度]**&#x200B;和&#x200B;**[!UICONTROL 變更資料來源]**&#x200B;活動應該&#x200B;**不**&#x200B;新增在一列中。 如果您需要連續使用這兩個活動，請在它們之間加入&#x200B;**[!UICONTROL 擴充]**&#x200B;活動。 這可確保正確執行並防止潛在的衝突或錯誤。

**[!UICONTROL 變更資料來源]**&#x200B;活動可讓您變更構成所使用的資料來源。

## 設定 {#configure}

將&#x200B;**[!UICONTROL 變更資料來源]**&#x200B;活動新增至畫布後，您可以定義工作流程的資料來源。

![資料來源選項在同盟對象組合工作區中反白顯示。](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}{align="center"}

| 來源 | 說明 |
| ------ | ----------- |
| FDA外部帳戶 | 外部雲端資料庫已透過同盟對象構成連線至Adobe Campaign。 |

選取&#x200B;**[!UICONTROL FDA外部帳戶]**&#x200B;後，您可以選擇您要連線的外部帳戶。

![顯示外部帳戶選項的彈出視窗。](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}{align="center"}

---
title: AI助理總覽
description: 瞭解如何使用AI Assistant，包括產品知識、營運見解以及建立同盟受眾組合。
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: 226679a38d0ad17726fd743f5df3b74879a2dd32
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# AI 助理概觀 {#ai-assistant}

AI 助理是一項使用者介面功能，旨在協助您導覽和了解 Adobe 概念。 您可以使用AI Assistant來更瞭解Adobe Experience Cloud多個產品中的產品知識使用案例，包括同盟受眾構成。

>[!CAUTION]
>
>您必須同意 Adobe Experience Cloud 生成式 AI 使用者準則，然後才能使用 AI 助理。 在[AI Assistant （舊版）總覽](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home){target="_blank"}中進一步瞭解合約。

在聯合客群構成中，您可以存取產品知識來了解與流程不同部分相關的 Adobe 概念。 AI Assistant支援四種型別的使用案例： **開啟探索** （探索以Experience League檔案為基礎的產品概念）、**目標式學習與疑難排解** （詢問關於特定功能或功能的問題）、**營運深入分析** （詢問關於同盟對象組合中物件的問題）以及&#x200B;**建立同盟對象組合**。

## 存取權 {#access}

若要存取AI助理，請選取頂端列上的![AI助理圖示](/help/start/assets/ai-assistant/icon.png)。 AI 助理會顯示在畫面的右側區段。 您可以選取![潛入影像替代文字](assets/do-not-localize/Smock_FullScreen_18_N.svg "展開圖示")以展開AI助理視窗。

![AI助理圖示會反白顯示，顯示如何存取AI助理。](/help/start/assets/ai-assistant/access.png)

## 使用AI助理 {#using}

開啟AI助理後，請在畫面底部的欄位中輸入問題，然後按Enter鍵。 現在會顯示問題的答案。 您可以向上或向下使用大拇指來評價您的答案。

![顯示AI Assistant中的範例問題和答案。](/help/start/assets/ai-assistant/sample-question-answer.png)

## 範例問題 {#sample-questions}

以下查詢顯示您可以向AI助理詢問的問題型別：

| 查詢型別 | 範例問題 |
| ---------- | --------------- |
| 開啟探索 | <ul><li>什麼是聯合客群構成？</li></ul> |
| 目標式學習 | <ul><li>如何設定Snowflake同盟資料庫帳戶？</li><li>如何建立聯合構成？</li></ul> |
| 運作洞察 | <ul><li>我的沙箱中有多少同盟資料庫？</li><li>我在過去30天內建立了多少結構描述？</li></ul> |
| 建立同盟受眾構成 | <ul><li>建立居住在英國之客戶的同盟受眾。</li></ul> |

此外，您可以使用AI Assistant自動建立同盟對象構成。

## 建立客群 {#create-audience}

您可以使用AI助理使用自然語言提示建立同盟對象構成。 當您使用AI Assistant建立受眾時，AI Assistant會根據您的提示產生計畫，並使用AI支援的自動化在瀏覽器中執行。

例如，如果您要求AI Assistant「使用結構CUSTOMERS_Table為生活在英國的客戶建立同盟對象」，AI Assistant會規劃建立對象所要執行的計畫，包括導覽至Federated Compositions頁面、代理程式將如何建立構成等步驟，以及在完成之後儲存對象。

![顯示範例問題和回應。](/help/start/assets/ai-assistant/ask-create.png)

如果計畫看起來正確，您可以選取&#x200B;**[!UICONTROL 執行]**，讓代理程式通過自動化。 代理程式將在瀏覽器中自動執行在Federated Audience Composition UI中建立您請求構成的步驟。 如果您想要隨時停止自動化，請選取&#x200B;**[!UICONTROL 停止]**。

![計畫已執行，代理程式正在自動執行計畫。](/help/start/assets/ai-assistant/execute-plan.png)

目前，建立對象技能支援下列附加功能：

- 排程器
   - 您可以建立按週期性排程執行的同盟組合。 支援的值包括&#x200B;**一次**&#x200B;和&#x200B;**每日**。
- 重複資料刪除
   - 您可以在資料協調期間刪除同盟資料記錄的重複資料

## 後續步驟

如需有關AI助理的詳細資訊，包括您可以使用AI助理完成的目標範例，以及瞭解AI助理的運作方式，請閱讀[AI助理概觀](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home){target="_blank"}。

如需您可以詢問同盟對象構成的作業Insight問題的完整清單，請閱讀[作業深入分析區段](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}。

---
audience: end-user
title: 使用增量查詢活動
description: 瞭解如何使用增量查詢活動
source-git-commit: 33a1eb9d4c0c7b847e04ac3f0f9f1881317a2f83
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 18%

---

# 增量查詢 {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="增量查詢"
>abstract="此 **增量查詢** 活動可讓您使用查詢建模器查詢資料庫。 每次執行此活動時，都會排除先前執行的結果。這可讓您只鎖定新元素。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="增量查詢歷史記錄"
>abstract="增量查詢歷史記錄"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="增量查詢處理的資料"
>abstract="增量查詢處理的資料"

此 **增量查詢** 活動可讓您依排程查詢資料庫。 每次執行此活動時，都會排除先前執行的結果。這可讓您只鎖定新元素。

此 **[!UICONTROL 增量查詢]** 活動可用於各種型別的使用：

* 將個人分段以定義訊息、對象等的目標。
* 匯出資料。 例如，您可以使用活動定期匯出檔案中的新記錄檔。 如果您想要在外部報告或BI工具中使用記錄檔資料，則此功能會很有用。

先前執行已定位的母體會儲存在構成中。 這表示從相同範本開始的兩個構成不共用相同記錄。 但是，在相同的構成中，以相同的增量查詢為基礎的兩個工作使用相同的記錄。

如果在增量查詢的其中一個執行期間其結果等於0，則構成會暫停直到查詢下一次程式化執行。 因此，增量查詢之後的轉變和活動不會在後續執行之前處理。

## 設定增量查詢活動 {#incremental-query-configuration}

請依照下列步驟設定 **增量查詢** 活動：

1. 新增 **增量查詢** 活動放入構成。

1. 在 **[!UICONTROL 對象]** 區段，選擇 **目標維度** 然後按一下 **[!UICONTROL 繼續]**.

   目標定位維度可讓您定義作業的目標族群：收件者、合約受益人、操作者、訂閱者等依預設，會從收件者中選取目標。 <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. 使用查詢建模器來定義您的查詢，就像在設計新電子郵件時建立對象一樣。 <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. 在 **[!UICONTROL 已處理的資料]** 區段，選取要使用的增量模式：

   * **[!UICONTROL 排除先前執行的結果]**：每次執行活動時，都會排除先前執行的結果。

     先前執行中已定位的記錄可記錄從目標日期起的最大天數。 若要這麼做，請使用 **[!UICONTROL 歷史記錄（天）]** 欄位。 如果此值為零，收件者永遠不會從記錄中清除。

   * **[!UICONTROL 使用日期欄位]**：此選項可讓您根據特定日期欄位，從先前執行中排除結果。 若要這麼做，請從所選目標維度的可用屬性清單中選擇所需的日期欄位。 在下次執行構成時，只會擷取在上次執行日期之後修改或建立的資料。

     在第一次執行構成後， **[!UICONTROL 上次執行日期]** 欄位會變為可用。 它指定將用於下一次執行的日期，並在每次執行構成時自動更新。 您仍然可以手動輸入新值來覆寫此值，以符合您的需求。

   >[!NOTE]
   >
   >此 **[!UICONTROL 使用日期欄位]** 模式會根據選取的日期欄位，提供更大的彈性。 例如，如果指定的欄位與修改日期相對應，則日期欄位模式將可讓您擷取最近更新的資料，而其他模式將僅排除在先前執行中已定位的記錄，即使這些記錄自上次執行構成後已被修改。

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->

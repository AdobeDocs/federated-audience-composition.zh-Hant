---
audience: end-user
title: 使用分割活動
description: 瞭解如何使用分割活動
exl-id: 6346eef6-b164-40cf-9402-b5ff208af97f
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '923'
ht-degree: 75%

---

# 分割 {#split}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="分割活動"
>abstract="**分割**&#x200B;活動可讓您根據不同選擇標準 (例如篩選規則或群體大小) 將傳入群體分割到多個子集。"

**分割**&#x200B;活動可讓您根據不同選擇標準 (例如篩選規則或群體大小) 將傳入群體分割到多個子集。

## 設定分割活動 {#split-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="分割活動的區段"
>abstract="依需求新增任意數量的子集，將傳入的群體進行細分。<br/></br>執行&#x200B;**分割** 活動時，系統會依照子集新增至活動的順序，將群體細分成不同的子集。在開始構成之前，請確保已使用箭頭按鈕按照符合您需求的順序排列子集。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="分割活動篩選器"
>abstract="若要將篩選條件套用到子集，請按一下「**[!UICONTROL 建立篩選]**」並使用查詢建模工具設定所需的篩選規則。例如，於傳入族群中，將有電子郵件地址存在於資料庫的設定檔包含在內。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="分割活動限制"
>abstract="若要限制子集選取設定檔的數量，請開啟「**[!UICONTROL 啟用限制]**」選項，並指定要包含的族群數量或百分比。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="分割活動排序"
>abstract="為子集設定族群限制時，您可以用指定設定檔屬性按升序或降序順序來排列所選設定檔。為此，請開啟「**啟用排序**」選項。例如，您可以限制子集僅包含購買金額最高的前 50 個設定檔。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="分割產生補集"
>abstract="設定完所有子集後，您可以選擇與任何子集都不相符的剩餘族群，並將其包含在額外的傳出轉變中。若要這樣做，請開啟「**產生補集**」選項。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="在相同表格中產生所有子集"
>abstract="切換此選項可將所有子集歸類至單一的傳出轉換。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="省略空值轉變"
>abstract="如果傳入群體為空，則切換「**[!UICONTROL 跳過空值轉變]**」選項可停用此子集的輸出轉變。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="啟用輸出群體的重疊"
>abstract="「**[!UICONTROL 啟用輸出群體的重疊]**」選項可讓您管理屬於多個子集的群體。當未選取該方塊時，分割活動將確保收件者不能出現在多個輸出轉換中，即使其滿足多個子集的條件也是如此。它們將位於具有符合條件的第一個標籤的目標中。當選取該方塊時，符合篩選條件的收件者，會出現在多個子集中。 "

請按照以下步驟設定&#x200B;**分割**&#x200B;活動：

1. 將&#x200B;**分割**&#x200B;活動新增至您的組合。

1. 活動設定面板隨即開啟，其中包含預設子集。按一下「**新增區段**」按鈕，新增所需數量的子集，依此來分割傳入群體。

   >[!IMPORTANT]
   >
   >執行&#x200B;**分割**&#x200B;活動時，母體會依新增至活動的順序，跨不同的子集分段。 例如，如果第一個子集取得初始群體的 70%，則下一個新增的子集只能將其選擇標準套用到剩餘的 30%，依此類推。
   >
   >開始撰寫之前，請確定已依您的需求排序子集。 要執行此操作，請使用箭頭按鈕來變更子集的位置。

1. 新增子集後，活動將顯示與子集一樣多的輸出轉變。我們強烈建議變更每個子集的標籤，以便在構成畫布中輕鬆識別它們。

   ![](../assets/split.png)

1. 設定每個子集應如何篩選傳入群體。要執行此操作，請依照下列步驟執行：

   1. 展開子集以顯示其屬性。

      ![](../assets/split-subset.png)

   1. 若要將篩選條件套用到子集，請按一下「**[!UICONTROL 建立篩選]**」並使用查詢建模工具設定所需的篩選規則。例如，將傳入母體的設定檔包含在資料庫中存在其電子郵件地址。 [瞭解如何使用查詢模型工具](../../query/query-modeler-overview.md)

   1. 若要限制子集選取設定檔的數量，請開啟「**[!UICONTROL 啟用限制]**」選項，並指定要包含的族群數量或百分比。

   1. 若要在傳入母體為空時停用轉變，請開啟&#x200B;**[!UICONTROL 略過空轉變]**&#x200B;選項。 如果沒有符合子集的設定檔，構成將不會轉換為下一個活動。

   >[!NOTE]
   >
   >為子集設定族群限制時，您可以用指定設定檔屬性按升序或降序順序來排列所選設定檔。為此，請開啟「**[!UICONTROL 啟用排序]**」選項。例如，您可以限制子集僅包含購買金額最高的前 50 個設定檔。

1. 設定完所有子集後，您可以選擇與任何子集都不相符的剩餘族群，並將其包含在額外的傳出轉變中。若要這樣做，請開啟「**[!UICONTROL 產生補集]**」選項。

1. **[!UICONTROL 在相同資料表中產生所有子集]**&#x200B;選項可讓您將所有子集群組成單一輸出轉換。

1. **[!UICONTROL 啟用輸出母體重疊]**&#x200B;選項可讓您管理屬於數個子集的母體：

   * 當未選取該方塊時，分割活動將確保收件者不能出現在多個輸出轉換中，即使其滿足多個子集的條件也是如此。它們會位於具有相符條件的第一個標籤的目標中。
   * 當選取該方塊時，符合篩選條件的收件者，會出現在多個子集中。最佳實務建議使用專屬條件。

該活動現已完成設定。在執行時，母體將依照其加入活動的順序，分割成不同的子集。

<!--
## Example{#split-example}

In the following example, the **[!UICONTROL Split]** activity is used to segment an audience into distinct subsets based on the communication channel that we want to use :

* **Subset 1 "push"**: This subset comprises all profiles who have installed our mobile application.
* **Subset 2 "sms"**: Mobile phone users: For the remaining population that did not fall into Subset 1, subset 2 applies a filtering rule to select profiles with mobile phones in the database.
* **Complement transition**: This transition captures all the remaining profiles that did not match Subset 1 or Subset 2. Specifically, it includes profiles who neither installed the mobile application nor have a mobile phone, such as users who haven't installed the mobile app or lack a registered mobile number.

![](../assets/workflow-split-example.png)
-->

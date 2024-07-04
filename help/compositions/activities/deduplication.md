---
audience: end-user
title: 使用重複資料刪除活動
description: 瞭解如何使用重複資料刪除活動
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 60%

---


# 去重複化 {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="用於識別重複項目的欄位"
>abstract="在&#x200B;**用於識別重複項目的欄位**&#x200B;區段，按一下&#x200B;**新增屬性**&#x200B;按鈕以指定可允許識別重複之相同值的欄位，例如：電子郵件地址、名字、姓氏等。欄位的順序可讓您指定首要處理的條件。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="重複項目刪除活動"
>abstract="「**重複項目刪除**」活動可讓您刪除入站活動結果中的重複項目。其主要在目標定位活動之後和允許使用目標資料的活動之前使用。"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="產生補充集"
>abstract="您可以使用剩餘族群 (其已因重複而排除) 產生額外的出站轉變。若要這樣做，請開啟「**產生補充集**」選項"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="重複項目刪除設定"
>abstract="若要刪除傳入資料中的重複項目，請在以下欄位中定義重複項目刪除方法。預設只會保留一筆記錄。您還應該根據運算式或屬性選取重複項目刪除模式。預設會隨機選取要避免重複的記錄。"

此 **重複資料刪除** 活動可讓您刪除入站活動結果中的重複專案，例如收件者清單中的重複設定檔。 此 **重複資料刪除** 活動通常用於目標定位活動之後，以及允許使用目標定位資料之活動之前。

## 設定重複資料刪除活動{#deduplication-configuration}

請依照下列步驟設定 **重複資料刪除** 活動：

1. 新增 **重複資料刪除** 活動至您的構成。

1. 在&#x200B;**用於識別重複項目的欄位**&#x200B;區段，按一下&#x200B;**新增屬性**&#x200B;按鈕以指定可允許識別重複之相同值的欄位，例如：電子郵件地址、名字、姓氏等。欄位的順序可讓您指定首要處理的條件。

1. 在 **重複資料刪除設定** 區段，選取唯一數量 **要保留的重複專案**. 此欄位的預設值為 1。如果值為 0 則可讓您保留所有重複項目。

   例如，如果記錄 A 和 B 被視為記錄 Y 的重複項目，而記錄 C 被視為記錄 Z 的重複項目：

   * 如果該欄位的值為 1：僅保留 Y 和 Z 記錄。
   * 如果該欄位的值為 0：會保留所有記錄。
   * 如果該欄位的值為 2：會保留記錄 C 和 Z，並且將保留 A、B 和 Y 中的兩條記錄，這是偶然的或取決於之後所選取的重複資料刪除方法。

1. 選取 **重複資料刪除方法** 若要使用：

   * **隨機選取**：隨機選取要保留在重複專案外的記錄。
   * **使用運算式**：這可讓您保留所輸入運算式的值最小或最大的記錄。
   * **追隨值清單**：可讓您定義一或多個欄位的值優先順序。 若要定義值，請按一下 **屬性** 以選取欄位或建立運算式，然後將值新增至適當的表格。 若要定義新欄位，請按一下值清單上方的「新增」按鈕。

1. 檢查 **產生補充** 選項，以利用剩餘母體。 補充包含所有重複專案。 隨後會將其他轉變新增至活動。

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->

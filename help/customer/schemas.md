---
audience: end-user
title: 開始使用結構描述
description: 瞭解如何開始使用結構描述
badge: label="可用性限制" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: c2d4ec21f497a1c4ad9c1701b4283edd16ca0611
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 20%

---

# 開始使用結構描述 {#schemas}

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="選取表格"
>abstract="選取要為資料模式新增的表格。"

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="索引鍵"
>abstract="選取資料調和的索引鍵。"

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="結構描述的名稱"
>abstract="輸入結構描述的名稱。"


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="結構描述說明"
>abstract="結構描述說明列出了資料欄、類型和標籤。您也可以檢查結構描述的調和索引鍵。若要更新結構描述定義，請按一下鉛筆圖示。"

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="選取要篩選的來源資料庫"
>abstract="您可以根據其來源來篩選結構描述。選取一或多個同盟資料庫以顯示其綱要。"

## 什麼是結構描述 {#schema-start}

綱要代表資料庫的表格。 它是應用程式內的物件，定義資料與資料庫表格的連結方式。

透過建立結構，您可以在Experience Platform同盟對象構成中定義表格的表示法：

* 提供易記的名稱和說明，以簡化使用者的理解
* 根據每個欄位的實際使用情況決定其可見性
* 請選取其主要索引鍵，以便根據[資料模型](../data-management/gs-models.md#data-model-start)的需要連結它們之間的結構描述

>[!CAUTION]
>
>使用相同的資料庫連線多個沙箱時，必須使用不同的工作結構描述。
>

## 建立結構描述 {#schema-create}

若要在Federated Audience Composition中建立方案，請遵循下列步驟：

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;區段中，進入&#x200B;**[!UICONTROL 模型]**&#x200B;連結。 瀏覽至&#x200B;**[!UICONTROL 結構描述]**&#x200B;索引標籤，然後按一下&#x200B;**[!UICONTROL 建立結構描述]**&#x200B;按鈕。

   ![](assets/schema_create.png){zoomable="yes"}

   此步驟可讓您透過下拉式清單存取新畫面，您可以在其中找到連線到您環境的資料庫。 在[本節](../connections/connections.md#connections-fdb)中進一步瞭解資料庫連線。

1. 在清單中選取您的來源資料庫，然後按一下&#x200B;**[!UICONTROL 新增表格]**&#x200B;索引標籤。

   ![](assets/schema_tables.png){zoomable="yes"}

   然後您可以檢視資料庫中所有表格的清單。

1. 透過新增您要建立綱要的表格，您可以存取其欄位，如下所示：

   ![](assets/schema_fields.png){zoomable="yes"}

   對於每個表格，您可以：

   * 變更結構描述的標籤
   * 新增說明
   * 重新命名所有欄位，並設定其可見度
   * 選取結構描述主索引鍵

   例如，針對匯入的下清單格：

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   結構描述可以定義如下：

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## 編輯結構 {#schema-edit}

若要編輯綱要：

1. 按一下結構描述資料夾中結構描述的名稱。

1. 按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;按鈕。

   ![](assets/schema_edit.png){zoomable="yes"}

   您可以存取與[建立結構描述](#schema-create)時相同的選項。

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## 在結構描述中預覽資料 {#schema-preview}

若要預覽結構描述所代表之表格中的資料，請瀏覽至&#x200B;**[!UICONTROL 資料]**&#x200B;標籤，如下所示。

按一下&#x200B;**[!UICONTROL 計算]**&#x200B;連結以預覽錄製總數。

![](assets/schema_data.png){zoomable="yes"}

按一下&#x200B;**[!UICONTROL 設定資料行]**&#x200B;按鈕以變更資料顯示。

![](assets/schema_columns.png){zoomable="yes"}

## 刪除結構描述 {#schema-delete}

若要刪除結構描述，請按一下&#x200B;**[!UICONTROL 更多]**&#x200B;按鈕，然後選擇&#x200B;**[!UICONTROL 刪除]**。

![](assets/schema_delete.png){zoomable="yes"}

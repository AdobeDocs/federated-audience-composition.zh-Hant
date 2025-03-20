---
audience: end-user
title: 開始使用資料模型
description: 瞭解如何開始使用資料模型
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 61a7b66d16358a4a1c3d4b2ae153e856d8f682f7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 15%

---

# 開始使用資料模型 {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="使用模型"
>abstract="此畫面中列出了結構描述和資料模型。您可以透過&#x200B;**建立**&#x200B;按鈕建立結構描述和資料模型。"

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="選取結構描述"
>abstract="選取資料模型的結構描述。"


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="選取客群"
>abstract="選取資料模式的客群。"

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="資料模型屬性"
>abstract="輸入資料模型的標籤。"


## 什麼是資料模型 {#data-model-start}

資料模型是一組結構描述、對象及其之間的連結。 它可用來將對象與資料庫資料建立同盟。

深入瞭解[結構描述](../customer/schemas.md#schema-start)。

深入瞭解[對象](../start/audiences.md)。

例如，您可以在下方看到資料模型的表示法：表格及其名稱和它們之間的連結。

![](assets/datamodel.png){zoomable="yes"}

在Federated Audience Composition中，可以建立許多資料模型。

它們的建立將基於使用案例：您選擇必要的表格，並根據需求連結它們。

## 建立資料模型 {#data-model-create}

若要建立資料模型，請遵循下列步驟：

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;區段中，存取&#x200B;**[!UICONTROL 模型]**&#x200B;功能表，並瀏覽至&#x200B;**[!UICONTROL 資料模型]**&#x200B;標籤。

   按一下&#x200B;**[!UICONTROL 建立資料模型]**&#x200B;按鈕。

   ![](assets/datamodel_create.png){zoomable="yes"}

1. 定義資料模型的名稱，然後按一下&#x200B;**[!UICONTROL 建立]**&#x200B;按鈕。

1. 在資料模型儀表板中，按一下&#x200B;**[!UICONTROL 新增結構描述]**&#x200B;以選擇與資料模型關聯的結構描述。

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL 新增對象]**&#x200B;以定義您的目標群組。

1. 在資料模型中的表格之間建立連線，以確保精確的資料關係。 [了解更多](#data-model-links)

1. 完成設定後，按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以套用您的變更。

## 建立連結 {#data-model-links}

若要在資料模型的表格之間建立連結，請遵循下列步驟：

1. 按一下其中一個資料表的&#x200B;**[!UICONTROL 建立連結]**&#x200B;功能表，或按一下&#x200B;**[!UICONTROL 建立連結]**&#x200B;按鈕，然後選擇2個資料表：

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. 填寫指定表單以定義連結。

   ![](assets/datamodel_link.png){zoomable="yes"}

   **基數**

   * **1-N**：來源表格的一個出現次數可以具有多個目標表格的對應出現次數，但目標表格的一個出現次數最多可以具有來源表格的一個對應出現次數。

   * **N-1**：目標表格的一個出現次數可以有來源表格的多個對應出現次數，但來源表格的一個出現次數最多可以有目標表格的對應出現次數。

   * **1-1**：來源資料表的一個執行個體最多可以具有目標資料表的一個對應執行個體。

為您的資料模型定義的所有連結如下所列：

![](assets/datamodel_alllinks.png){zoomable="yes"}

## 操作說明影片 {#data-model-video}

透過此影片瞭解如何建立資料模型：

>[!VIDEO](https://video.tv.adobe.com/v/3432020)

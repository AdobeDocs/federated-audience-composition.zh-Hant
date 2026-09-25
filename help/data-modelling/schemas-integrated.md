---
audience: end-user
title: 結構描述概觀
description: 瞭解如何在Adobe Experience Platform UI中建立和使用同盟對象構成的結構描述。
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%
---
# 結構描述概觀 {#schemas}

>[!AVAILABILITY]
>
>新結構描述體驗僅供特定客戶使用。 如需詳細資訊，請聯絡Adobe客戶服務。
>
>如果您無法存取新的結構描述體驗，請閱讀[結構描述概觀](./schemas.md)。
>
>若要存取方案，您需要下列其中一項許可權：
>
>-**管理同盟結構描述**
>-**檢視同盟結構描述**
>
>如需有關必要權限的詳細資訊，請參閱[存取控制指南](/help/governance-privacy-security/access-control.md)。

綱要代表資料庫的表格。 它是應用程式內的物件，定義資料與資料庫表格的連結方式。

透過建立結構，您可以在Experience Platform同盟對象構成中定義表格的表示法：

* 提供易記的名稱和說明，以簡化使用者的理解
* 根據每個欄位的實際使用情況決定其可見性
* 請選取其主要索引鍵，以便根據[資料模型](../data-modelling/models.md#data-model-start)的需要連結它們之間的結構描述

>[!CAUTION]
>
>使用相同資料庫連線多個沙箱時，必須使用不同的工作結構描述。

## 建立結構描述 {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="管理設定"
>abstract="暫時的空白內容。"

若要在Federated Audience Composition中建立結構描述，請在Experience Platform UI的&#x200B;**[!UICONTROL 資料管理]**&#x200B;區段中選取&#x200B;**[!UICONTROL 結構描述]**。 在結構描述UI中，選取&#x200B;**[!UICONTROL 建立結構描述]**。

![結構描述UI中的「結構描述」和「建立結構描述」按鈕都會反白顯示。](/help/data-modelling/assets/integrated/select-create-schema.png)

「建立結構描述」彈出視窗出現後，請選取&#x200B;**[!UICONTROL 關聯式]**，然後選取&#x200B;**[!UICONTROL 探索結構描述]**&#x200B;和&#x200B;**[!UICONTROL 下一步]**，以建立同盟對象組合的結構描述。

![[建立關聯式結構描述]彈出視窗中會醒目顯示[探索結構描述]按鈕。](/help/data-modelling/assets/integrated/select-discover-schemas.png)

出現&#x200B;**[!UICONTROL 選取同盟資料庫]**&#x200B;彈出視窗。 在此彈出視窗上，您可以選取[來源資料庫](/help/connections/home.md)，然後選取&#x200B;**[!UICONTROL 下一步]**。

![顯示[選取同盟資料庫]彈出視窗。](/help/data-modelling/assets/integrated/select-federated-database.png)

## 定義結構描述 {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="複合索引鍵"
>abstract="由多個結構描述欄組成的結構描述索引鍵。 標示要用作複合索引鍵的欄。"

選擇同盟資料庫後，您現在可以定義架構。 **[!UICONTROL 新增資料]**&#x200B;畫面隨即顯示。 您可以在此頁面選取&#x200B;**[!UICONTROL 新增資料表]**，以選擇要新增至結構描述的資料表。

![[新增資料表]按鈕在[新增資料]畫面中反白顯示。](/help/data-modelling/assets/integrated/select-add-table.png)

**[!UICONTROL 選取資料表]**&#x200B;彈出視窗會出現。 在此彈出視窗中，您可以選取要用來建立綱要的表格。

![顯示[選取資料表]彈出視窗。](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

每個選取的表格都會產生具有所選欄的綱要。 對於每個表格，您可以變更綱要的標籤、新增說明、重新命名欄位標籤、設定欄位標籤可見度，以及選取綱要主索引鍵。

![選取的資料表會顯示在[新增資料]頁面中。](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>如果您選擇&#x200B;**[!UICONTROL 複合索引鍵]**，但只選取一個要使用的索引鍵，則會將該索引鍵視為標準結構描述主索引鍵。

此外，您可以建立由多個結構描述欄組成的索引鍵。 選取&#x200B;**[!UICONTROL 複合金鑰]**，並標籤您要用來作為複合金鑰的金鑰。

![已同時選取組合鍵切換及結構描述。](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

完成設定後，請選取&#x200B;**[!UICONTROL 完成]**&#x200B;以完成建立結構描述。

## 編輯結構 {#schema-edit}

若要編輯結構描述，請在&#x200B;**結構描述**&#x200B;頁面上選取您先前建立的結構描述旁的![省略符號圖示](/help/assets/icons/more.png)，接著選取&#x200B;**[!UICONTROL 編輯]**。

![[編輯結構描述]按鈕已反白顯示。](/help/data-modelling/assets/integrated/edit-schema.png)

在&#x200B;**[!UICONTROL 編輯結構描述]**&#x200B;視窗上，您可以看到結構描述編輯器。 如需有關使用結構描述編輯器的詳細資訊，請閱讀[結構描述UI指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/ui/resources/schemas#customize-schema)。

![顯示結構描述編輯器。](/help/data-modelling/assets/integrated/schema-editor.png)

### 編輯關係 {#relationship-edit}

若要編輯結構描述的關係，請在結構描述編輯器中選取&#x200B;**[!UICONTROL 檢視實體圖表]**。

![檢視實體圖表按鈕已反白顯示。](/help/data-modelling/assets/integrated/view-entity-diagram.png)

實體圖表頁面隨即顯示。 您可以在此頁面上建立連結，以建立方案之間的關係。

![實體圖表已顯示。](/help/data-modelling/assets/integrated/entity-diagram.png)

如需建立連結的詳細資訊，請閱讀[資料模型概觀](/help/data-modelling/models.md#data-model-links)的「畫布檢視」標籤。

## 在結構描述中預覽資料 {#schema-preview}

若要預覽結構描述所代表之資料表中的資料，請移至&#x200B;**[!UICONTROL 資料集]**&#x200B;區段，然後選取&#x200B;**[!UICONTROL 瀏覽]**。

![資料集和瀏覽按鈕會反白顯示。](/help/data-modelling/assets/integrated/datasets-browse.png)

選取![三個點](/help/assets/icons/more.png)，然後選取&#x200B;**[!UICONTROL 預覽資料集]**，以檢視結構描述中的資料預覽。

![預覽資料集按鈕已反白顯示。](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## 重新整理結構描述 {#schema-refresh}

可以更新、新增或移除同盟資料庫中的表格。 在這種情況下，您必須重新整理Adobe Experience Platform中的結構以符合最新變更。 若要重新整理結構描述，請選取&#x200B;**[!UICONTROL 更多]**&#x200B;按鈕，然後選取&#x200B;**[!UICONTROL 管理組態]**。

![[管理設定]按鈕已反白顯示。](/help/data-modelling/assets/integrated/manage-configuration.png)

**[!UICONTROL 編輯組態]**&#x200B;彈出視窗會出現。 選取&#x200B;**[!UICONTROL 重新整理]**&#x200B;以重新整理結構描述。

![[重新整理結構描述]按鈕已反白顯示。](/help/data-modelling/assets/integrated/refresh-schema.png)

## 刪除結構描述 {#schema-delete}

若要刪除結構描述編輯器中的結構描述，請選取&#x200B;**[!UICONTROL 更多]**，然後選取&#x200B;**[!UICONTROL 刪除]**。

![[刪除結構描述]按鈕已反白顯示。](/help/data-modelling/assets/integrated/delete-schema.png)

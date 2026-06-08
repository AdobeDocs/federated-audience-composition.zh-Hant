---
audience: end-user
title: 在Adobe Journey Optimizer中使用同盟受眾構成受眾的多實體鎖定目標
description: 瞭解如何在Adobe Journey Optimizer歷程中鎖定同盟對象構成對象中的設定檔。
source-git-commit: 79f05c5a1b025b522a1b88615973d9fe383e3720
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# 使用Adobe Journey Optimizer中的同盟受眾構成受眾進行多實體鎖定目標

透過多實體鎖定目標，您可以使用同盟對象構成對象屬性做為Adobe Journey Optimizer歷程中的補充識別碼。 這些屬性可讓您在多個實體（例如帳戶或訂閱層級）啟用對象。

## 在同盟對象構成中建立您的對象 {#create}

若要從多實體鎖定目標開始，您首先需要在同盟對象構成中建立並儲存對象。

在對象構成UI中，新增&#x200B;**建立對象**&#x200B;活動以在同盟構成畫布中建立對象，並新增&#x200B;**儲存對象**&#x200B;活動以設定對象的對應、主要身分和資料有效期。

![已顯示Federated Audience Composition UI，顯示對象。](/help/connections/assets/multi-entity-targeting/build-activity.png)

完成對象的設定後，請選取&#x200B;**開始**&#x200B;以開始撰寫的執行。 此對象及其對應的資料集可在Experience Platform中使用。

如需在同盟對象構成中建立構成的詳細資訊，請參閱[建立構成指南](/help/compositions/create-composition.md)。

## 在Adobe Journey Optimizer中啟用對象 {#activate}

構成執行完成後，您可以在Journey Optimizer中啟用對象。 在Adobe Journey Optimizer的&#x200B;**歷程管理**&#x200B;區段中，選取&#x200B;**歷程**，然後選取&#x200B;**建立歷程**&#x200B;以開啟歷程使用者介面。

![Adobe Journey Optimizer中的「建立歷程」按鈕會醒目提示。](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

在歷程介面中，新增&#x200B;**讀取對象**&#x200B;節點。 您可以提供標籤並選取您先前建立的對象，以設定此節點。

![讀取對象節點會顯示在Journey Optimizer UI中。](/help/connections/assets/multi-entity-targeting/read-journey.png)

選擇先前建立的對象後，啟用&#x200B;**使用補充識別碼**。

![[使用補充識別碼]核取方塊已反白顯示。](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

您現在可以選擇補充識別碼。 在選取器畫面中，選取&#x200B;**進階模式**&#x200B;並導覽至&#x200B;**Experience Platform**。 在此頁面中，選取您先前建立的對象名稱，並選擇要用於對象的補充識別碼。

![已顯示運算式編輯器。](/help/connections/assets/multi-entity-targeting/add-expression.png)

## 設定歷程條件 {#configure-journey}

現在您已啟動並設定對象設定，您可以繼續設定歷程的其餘條件。 在此使用案例中，您會在&#x200B;**讀取對象**&#x200B;節點之後新增&#x200B;**最佳化程式**&#x200B;節點，接著新增&#x200B;**動作**&#x200B;節點。

在設定剩餘的節點後，選取&#x200B;**發佈**&#x200B;以完成歷程建立。

![已反白發佈按鈕。](/help/connections/assets/multi-entity-targeting/select-publish.png)

您的歷程現在會根據&#x200B;**補充識別碼**&#x200B;來鎖定對象設定檔，而非主要識別碼。 使用此功能，您現在可以鎖定多個實體（例如訂閱ID、帳戶ID或訂單ID）並啟用至您想要的管道。

## 後續步驟 {#next-steps}

閱讀本指南後，您現在瞭解如何在Journey Optimizer歷程中使用同盟對象構成對象的補充識別碼。 如需有關使用補充歷程的詳細資訊，請參閱歷程指南[&#128279;](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier)中的使用補充識別碼。


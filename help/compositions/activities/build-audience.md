---
audience: end-user
title: 使用建立對象活動
description: 瞭解如何使用建立對象活動
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 37%

---


# 建置對象 {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="建置對象活動"
>abstract="此 **建立對象** 活動可讓您定義將進入構成的對象。"

此 **建立對象** 活動可讓您定義將進入構成的對象。

若要定義對象族群，您可以：

<!--* Select an existing audience, created as a list in the client console.-->
* 選取 Adobe Experience Platform 對象。
* 定義並結合篩選條件，以使用查詢建模器建立器建立新對象。

此 **建立對象** 活動可放置在構成的開頭或任何其他活動之後。 任何活動都可以放在 **建立對象**.

## 設定建置對象活動 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="對象"
>abstract="選取您的對象。"

請按照以下步驟設定「**建置對象**」活動：

1. 新增「**建置對象**」活動。
1. 定義標籤。
1. 定義對象類型：「**建立您自己的**」或是「**讀取對象**」。
1. 請依照下列標籤中詳述的步驟設定您的對象。

>[!BEGINTABS]

>[!TAB 建立您自己的（查詢）]

若要建立自己的查詢，請依照下列步驟進行：

1. 選取「**建立您自己的 (查詢)**」。
1. 選擇「**目標定位維度**」。目標定位維度可讓您定義作業的目標族群：收件者、合約受益人、操作者、訂閱者等依預設，會從收件者中選取目標。<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. 按一下&#x200B;**繼續**。
1. 使用查詢建模器來定義您的查詢，就像在設計新電子郵件時建立對象一樣。 <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB 讀取閱聽眾]

若要選取現有對象，請依照以下步驟進行：

1. 選取「**讀取對象**」。
1. 按一下&#x200B;**繼續**。
1. 選取您的對象，就像在設計新傳送時使用對象一樣。 <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->

---
audience: end-user
title: 配合對象
description: 瞭解如何使用受眾
badge: label="可用性限制" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: 4b7645e45b68a7316d9ddc09af1a8253b4e4dd62
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 2%

---

# 配合對象 {#gs-audiences}

Experience Platform同盟對象構成可讓您[建立構成](../compositions/gs-compositions.md)，您可以在視覺畫布中運用各種活動來建立對象，並將其儲存至Adobe Experience Platform對象入口網站。

然後，您可以對Adobe Experience Platform支援的任何目的地啟用這些對象。

## 使用組合建立對象 {#creation}

若要使用同盟對象構成建立對象，您必須建立包含&#x200B;**[!UICONTROL 儲存對象]**&#x200B;活動的構成。 此活動可讓您將對象儲存至Audience Portal，並從外部資料庫中選取要包含在對象中的欄位。 [瞭解如何設定儲存對象活動](../compositions/activities/save-audience.md)

使用Adobe同盟資料構成建立的對象包含&#x200B;**[!UICONTROL 儲存對象]**&#x200B;活動中選取的所有欄位，並與所有Adobe Experience Platform對象一起儲存在對象入口網站中。

執行構成後，產生的受眾會作為外部受眾儲存在Adobe Experience Platform中，並可供Adobe Real-Time Customer Data Platform和/或Adobe Journey Optimizer使用。

您可以對Adobe Experience Platform支援的任何目的地啟用這些對象。 [瞭解如何使用目的地](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home)

>[!NOTE]
>
>無法編輯使用Adobe同盟對象構成所建立的對象。 若要修改其中一個對象，您需要使用構成來建立新對象。

## 在Adobe Experience Platform中存取您的對象 {#access-audience}

使用同盟對象構成建立的對象可在Audience Portal中存取，該入口網站可從&#x200B;**對象**&#x200B;功能表存取。

**[!UICONTROL 瀏覽]**&#x200B;索引標籤會列出儲存至Adobe Experience Platform的所有現有對象。 您可以使用&#x200B;**[!UICONTROL Origin]**&#x200B;欄或左窗格中可用的篩選器，識別清單中的同盟對象構成對象。

![](assets/audiences-list.png)

如需如何在Adobe Experience Platform中使用對象的詳細資訊，請參閱[對象入口網站檔案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal)

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->
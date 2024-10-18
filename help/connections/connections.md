---
audience: end-user
title: 建立和管理與同盟資料庫的連線
description: 瞭解如何建立和管理與同盟資料庫的連線
badge: label="可用性限制" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: c2d4ec21f497a1c4ad9c1701b4283edd16ca0611
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 16%

---

# 建立連線 {#connections-fdb}

Experience Platform 聯合客群構成可讓客戶從第三方資料倉儲中建立和擴充客群，並將客群匯入 Adobe Experience Platform。

若要使用同盟資料庫和Adobe Experience Platform，您必須先建立連線。 此連線設定於Adobe Experience Platform使用者介面提供的專用使用者介面，如本頁所述。

若要設定與資料庫的連線，請執行下列步驟：

1. 在左側邊欄瀏覽至&#x200B;**[!UICONTROL 同盟資料]**&#x200B;區段。

1. 在&#x200B;**[!UICONTROL 同盟資料庫]**&#x200B;連結中，按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**&#x200B;按鈕。

   ![](assets/connections_list.png){zoomable="yes"}

1. 使用資料庫名稱和型別設定連線&#x200B;**[!UICONTROL Properties]**。

   ![](assets/connections_name.png){zoomable="yes"}

   選取其型別可讓您存取要填寫的其他屬性。 在此瞭解更多有關[此頁面](federated-db.md)中支援的資料庫。

   ![](assets/connections_details.png){zoomable="yes"}

   組態設定取決於資料庫的型別。 瀏覽下列連結以存取設定連線所需的詳細資訊：

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. 填寫詳細資料後，按一下&#x200B;**[!UICONTROL 測試連線]**&#x200B;按鈕，再按一下&#x200B;**[!UICONTROL 部署函式]**&#x200B;按鈕。

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;按鈕，完成連線的建立。

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   您有同盟資料庫連線的概觀，如下所示：

   ![](assets/connections_overview.png){zoomable="yes"}

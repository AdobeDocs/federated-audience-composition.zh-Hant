---
audience: end-user
title: 建立和管理與同盟資料庫的連線
description: 瞭解如何建立和管理與同盟資料庫的連線
badge: label="可用性限制" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# 建立連線 {#connections-fdb}

直接在AEP中使用同盟資料庫表示要與其建立連線。

若要設定與資料庫的連線，請移至&#x200B;**[!UICONTROL 同盟資料]**&#x200B;區段，然後在&#x200B;**[!UICONTROL 同盟資料庫]**&#x200B;連結中，按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**&#x200B;按鈕。

![](assets/connections_list.png){zoomable="yes"}

您將存取連線&#x200B;**[!UICONTROL 屬性]**&#x200B;的視窗，其名稱與資料庫的型別。

![](assets/connections_name.png){zoomable="yes"}

選取其型別可讓您存取要填寫的其他屬性。 [在此深入瞭解支援的資料庫](federated-db.md)。

![](assets/connections_details.png){zoomable="yes"}

根據您資料庫的型別，在下列連結中瞭解設定連線所需的資訊：

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [azure synapse](federated-db.md#azure-synapse-redshift)
* [Google Big Query](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

填寫詳細資料後，按一下&#x200B;**[!UICONTROL 測試連線]**&#x200B;按鈕，再按一下&#x200B;**[!UICONTROL 部署函式]**按鈕。
按一下**[!UICONTROL 儲存]**&#x200B;按鈕，完成連線的建立。

![](assets/connections_testdeploy.png){zoomable="yes"}

您將會有同盟資料庫連線的概觀，如下所示：

![](assets/connections_overview.png){zoomable="yes"}

---
audience: end-user
title: 開始使用同盟資料庫
description: 瞭解如何建立和管理您的同盟資料庫
badge: label="可用性限制" type="Informative"
exl-id: b8c0589d-4150-40da-ac79-d53cced236e8
source-git-commit: 866dbeb39f2d3cc73d21edea170a3861f91a4802
workflow-type: tm+mt
source-wordcount: '1467'
ht-degree: 6%

---

# 開始使用同盟資料庫 {#federated-db}

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="同盟資料庫"
>abstract="此畫面中列出了與同盟資料庫的現有連接。若要建立新連接，請按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**&#x200B;按鈕。"

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="同盟資料庫屬性"
>abstract="輸入新同盟資料庫的名稱，然後選取其類型。"

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="同盟資料庫詳細資料"
>abstract="輸入連接到新同盟資料庫的設定。使用&#x200B;**[!UICONTROL 測試連接]**&#x200B;按鈕驗證您的設定。"

Experience Platform同盟對象構成可讓客戶從協力廠商資料倉儲建立並豐富對象，並將對象匯入至Adobe Experience Platform。

在此頁面瞭解如何建立、設定、測試及儲存外部資料庫的連線。

## 支援的資料庫 {#supported-db}

透過同盟對象構成，您可以連線至下列資料庫。 每個資料庫的設定詳述如下。

* [Amazon Redshift](#amazon-redshift)
* [azure synapse](#azure-synapse-redshift)
* [Google Big Query](#google-big-query)
* [Snowflake](#snowflake)
* [Vertica Analytics](#vertica-analytics)

## Amazon Redshift {#amazon-redshift}

使用同盟資料庫來處理儲存在外部資料庫中的資訊。 請依照下列步驟設定Amazon Redshift的存取權。

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;功能表下，選取&#x200B;**[!UICONTROL 同盟資料庫]**。

1. 按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**。

   ![](assets/federated_database_1.png)

1. 輸入同盟資料庫的&#x200B;**[!UICONTROL 名稱]**。

1. 從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中，選取Amazon Redshift。

   ![](assets/federated_database_6.png)

1. 設定Amazon Redshift驗證設定：

   * **[!UICONTROL 伺服器]**：新增DNS的名稱。

   * **[!UICONTROL 帳戶]**：新增使用者名稱。

   * **[!UICONTROL 密碼]**：新增帳戶密碼。

   * **[!UICONTROL 資料庫]**：如果未在DSN中指定資料庫名稱。 若在DSN中指定，可保留空白

   * **[!UICONTROL 工作結構描述]**：工作結構描述的名稱。 [了解更多](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

1. 選取&#x200B;**[!UICONTROL 測試連線]**&#x200B;選項以驗證您的組態。

1. 按一下&#x200B;**[!UICONTROL 部署函式]**&#x200B;按鈕以建立函式。

1. 完成設定後，按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以建立同盟資料庫。

## azure synapseRedshift {#azure-synapse-redshift}

使用同盟資料庫來處理儲存在外部資料庫中的資訊。 請依照下列步驟設定對Azure synapseRedshift的存取權。

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;功能表下，選取&#x200B;**[!UICONTROL 同盟資料庫]**。

1. 按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**。

   ![](assets/federated_database_1.png)

1. 輸入同盟資料庫的&#x200B;**[!UICONTROL 名稱]**。

1. 從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中，選取Azure synapseRedshift。

   ![](assets/federated_database_4.png)

1. 設定Azure synapseRedshift驗證設定：

   * **[!UICONTROL 伺服器]**：輸入Azure synapse伺服器的URL。

   * **[!UICONTROL 帳戶]**：輸入使用者名稱。

   * **[!UICONTROL 密碼]**：輸入帳戶密碼。

   * **[!UICONTROL 資料庫]** （選擇性）：如果未在DSN中指定，請輸入資料庫名稱。

   * **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

1. 選取&#x200B;**[!UICONTROL 測試連線]**&#x200B;選項以驗證您的組態。

1. 按一下&#x200B;**[!UICONTROL 部署函式]**&#x200B;按鈕以建立函式。

1. 完成設定後，按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以建立同盟資料庫。

| 選項 | 說明 |
|---|---|
| 驗證 | 聯結器支援的驗證型別。 目前支援的值： ActiveDirectoryMSI。 如需詳細資訊，請參閱[SQL檔案](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings) （連線字串n°8範例） |


## Google Big Query {#google-big-query}

使用同盟資料庫來處理儲存在外部資料庫中的資訊。 請依照下列步驟設定對Google Big Query的存取權。

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;功能表下，選取&#x200B;**[!UICONTROL 同盟資料庫]**。

1. 按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**。

   ![](assets/federated_database_1.png)

1. 輸入同盟資料庫的&#x200B;**[!UICONTROL 名稱]**。

1. 從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中，選取Google Big Query。

   ![](assets/federated_database_3.png)

1. 設定Google Big Query驗證設定：

   * **[!UICONTROL 服務帳戶]**：輸入您&#x200B;**[!UICONTROL 服務帳戶]**&#x200B;的電子郵件。 如需詳細資訊，請參閱[Google Cloud檔案](https://cloud.google.com/iam/docs/creating-managing-service-accounts)。

   * **[!UICONTROL 專案]**：輸入您&#x200B;**[!UICONTROL 專案]**&#x200B;的名稱。 如需詳細資訊，請參閱[Google Cloud檔案](https://cloud.google.com/resource-manager/docs/creating-managing-projects)。

   * **[!UICONTROL 資料集]**：輸入&#x200B;**[!UICONTROL 資料集]**&#x200B;的名稱。 如需詳細資訊，請參閱[Google Cloud檔案](https://cloud.google.com/bigquery/docs/datasets-intro)。

   * **[!UICONTROL 金鑰檔案路徑]**：將您的金鑰檔案上傳至伺服器。 僅接受.json檔案。

   * **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

1. 選取&#x200B;**[!UICONTROL 測試連線]**&#x200B;選項以驗證您的組態。

1. 按一下&#x200B;**[!UICONTROL 部署函式]**&#x200B;按鈕以建立函式。

1. 完成設定後，按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以建立同盟資料庫。

| 選項 | 說明 |
|---|---|
| ProxyType | 用來透過ODBC和SDK聯結器連線至BigQuery的Proxy型別。 目前支援</br>HTTP （預設）、http_no_tunnel、socks4和socks5。 |
| ProxyHost | 可連線到Proxy的主機名稱或IP位址。 |
| ProxyPort | 執行Proxy的連線埠號碼，例如8080 |
| ProxyUid | 用於已驗證Proxy的使用者名稱 |
| proxypwd | ProxyUid密碼 |
| bqpath | 請注意，這僅適用於大量載入工具(Cloud SDK)。 </br>若要避免使用PATH變數或必須將google-cloud-sdk目錄移至其他位置，您可以使用此選項指定伺服器上cloud sdk bin目錄的精確路徑。 |
| GCloudConfigName | 請注意，這適用於7.3.4版開始並僅適用於大量載入工具(Cloud SDK)。</br> Google Cloud SDK使用設定將資料載入BigQuery表格。 名為`accfda`的組態儲存用來載入資料的引數。 不過，此選項可讓使用者為組態指定不同的名稱。 |
| GCloudDefaultConfigName | 請注意，這適用於7.3.4版開始並僅適用於大量載入工具(Cloud SDK)。</br>必須先將作用中的標籤傳輸至新的設定，才能刪除作用中的Google Cloud SDK設定。 此暫時設定是重新建立載入資料的主要設定所必需的。 暫存組態的預設名稱為`default`，如有需要，可以變更此名稱。 |
| GCloudRecreateConfig | 請注意，這適用於7.3.4版開始並僅適用於大量載入工具(Cloud SDK)。</br>設為`false`時，大量載入機制不會嘗試重新建立、刪除或修改Google Cloud SDK設定。 相反地，它會使用電腦上現有的設定繼續進行資料載入。 當其他作業取決於Google Cloud SDK設定時，此功能很有價值。 </br>如果使用者在沒有適當組態的情況下啟用此引擎選項，大量載入機制將會發出警告訊息： `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`。 為避免進一步的錯誤，它會恢復為使用預設的ODBC陣列插入大量載入機制。 |


## Snowflake {#snowflake}

使用同盟資料庫來處理儲存在外部資料庫中的資訊。 請依照下列步驟設定對Snowflake的存取權。

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;功能表下，選取&#x200B;**[!UICONTROL 同盟資料庫]**。

1. 按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**。

   ![](assets/federated_database_1.png)

1. 輸入同盟資料庫的&#x200B;**[!UICONTROL 名稱]**。

1. 從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中，選取Snowflake。

   ![](assets/federated_database_2.png)

1. 設定Snowflake驗證設定：

   * **[!UICONTROL 伺服器]**：輸入您的伺服器名稱。

   * **[!UICONTROL 使用者]**：輸入您的使用者名稱。

   * **[!UICONTROL 密碼]**：輸入您的帳戶密碼。

   * **[!UICONTROL 資料庫]** （選擇性）：如果未在DSN中指定，請輸入資料庫名稱。

   * **[!UICONTROL 工作結構描述]** （選擇性）：輸入工作結構描述的名稱。

   * **[!UICONTROL 私密金鑰]**：按一下&#x200B;**[!UICONTROL 私密金鑰]**&#x200B;欄位，從地區設定資料夾中選取您的.pem檔案。

   * **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

1. 選取&#x200B;**[!UICONTROL 測試連線]**&#x200B;選項以驗證您的組態。

1. 按一下&#x200B;**[!UICONTROL 部署函式]**&#x200B;按鈕以建立函式。

1. 完成設定後，按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以建立同盟資料庫。

聯結器支援下列選項：

| 選項 | 說明 |
|---|---|
| 工作綱要 | 用於工作表的資料庫綱要 |
| 倉儲 | 要使用的預設倉儲名稱。 它會覆寫使用者的預設值。 |
| 時區名稱 | 預設為空白，這表示會使用Campaign Classic應用程式伺服器的系統時區。 選項可用來強制TIMEZONE工作階段引數。 <br>如需詳細資訊，請參閱[此頁面](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone)。 |
| weekstart | WEEK_START階段作業引數。 預設為0。 <br>如需詳細資訊，請參閱[此頁面](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start)。 |
| UseCachedResult | USE_CACHED_RESULTS工作階段引數。 預設為TRUE。 此選項可用來停用Snowflake快取結果。 <br>如需詳細資訊，請參閱[此頁面](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html)。 |
| bulkThread | 用於Snowflake大量載入器的執行緒數量，執行緒越多，批次載入量越大，效能就越好。 預設為1。 根據機器執行緒計數，數字可以調整。 |
| chunkSize | 決定大量載入器區塊的檔案大小。 預設為128MB。 可以修改以獲得最佳效能（當與bulkThreads一起使用時）。 同時作用中的執行緒越多，效能就越好。 <br>如需詳細資訊，請參閱[Snowflake檔案](https://docs.snowflake.net/manuals/sql-reference/sql/put.html)。 |
| 階段名稱 | 預先布建的內部階段名稱。 它將用於大量載入，而不是建立新的臨時階段。 |


## Vertica Analytics {#vertica-analytics}

使用同盟資料庫來處理儲存在外部資料庫中的資訊。 請依照下列步驟設定對Vertica analytics的存取權。

1. 在&#x200B;**[!UICONTROL 同盟資料]**&#x200B;功能表下，選取&#x200B;**[!UICONTROL 同盟資料庫]**。

1. 按一下&#x200B;**[!UICONTROL 新增同盟資料庫]**。

   ![](assets/federated_database_1.png)

1. 輸入同盟資料庫的&#x200B;**[!UICONTROL 名稱]**。

1. 從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中，選取Vertica analytics。

   ![](assets/federated_database_5.png)

1. 設定Vertica Analytics驗證設定：

   * **[!UICONTROL 伺服器]**：新增[!DNL Vertica Analytics]伺服器的URL。

   * **[!UICONTROL 帳戶]**：新增使用者名稱。

   * **[!UICONTROL 密碼]**：新增帳戶密碼。

   * **[!UICONTROL 資料庫]** （選擇性）：如果未在DSN中指定，請輸入資料庫名稱。

   * **[!UICONTROL 工作結構描述]** （選擇性）：輸入工作結構描述的名稱。

   * **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

1. 選取&#x200B;**[!UICONTROL 測試連線]**&#x200B;選項以驗證您的組態。

1. 按一下&#x200B;**[!UICONTROL 部署函式]**&#x200B;按鈕以建立函式。

1. 完成設定後，按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以建立同盟資料庫。

聯結器支援下列選項：

| 選項 | 說明 |
|---|---|
| 時區名稱 | 預設為空白，這表示會使用Campaign Classic應用程式伺服器的系統時區。 選項可用來強制TIMEZONE工作階段引數。 |

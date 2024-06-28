---
audience: end-user
title: 開始使用同盟資料庫
description: 瞭解如何建立和管理您的同盟資料庫
source-git-commit: 847da9a5eeb28199010f8491f7eebba4a60a83f1
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 2%

---

# 開始使用同盟資料庫 {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="同盟資料庫"
>abstract="此畫面中列出現有的同盟資料庫連線。 若要建立新連線，請按一下 **新增同盟資料庫** 按鈕。"


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="同盟資料庫屬性"
>abstract="輸入新同盟資料庫的名稱，並選取其型別。"


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="同盟資料庫詳細資料"
>abstract="輸入設定以連線到新的同盟資料庫。 使用 **測試連線** 按鈕以驗證您的設定。"

建立、設定、測試並儲存外部資料庫的連線。

支援的外部資料庫：

* Snowflake
* Google Big Query
* azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL 伺服器]**：

* **[!UICONTROL 使用者]**：使用者名稱。

* **[!UICONTROL 密碼]**：使用者帳戶密碼。

* **[!UICONTROL 資料庫]**：

* **[!UICONTROL 工作結構描述]**：

* **[!UICONTROL 私密金鑰]**：僅接受.pem檔案

* **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

| 選項 | 說明 |
|---|---|
| 工作綱要 | 用於工作表的資料庫綱要 |
| 倉儲 | 要使用的預設倉儲名稱。 它會覆寫使用者的預設值。 |
| 時區名稱 | 預設為空白，這表示會使用Campaign Classic應用程式伺服器的系統時區。 選項可用來強制TIMEZONE工作階段引數。 <br>有關詳細資訊，請參閱 [此頁面](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| weekstart | WEEK_START階段作業引數。 預設為0。 <br>有關詳細資訊，請參閱 [此頁面](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start). |
| UseCachedResult | USE_CACHED_RESULTS工作階段引數。 預設為TRUE。 此選項可用來停用Snowflake快取結果。 <br>有關詳細資訊，請參閱 [此頁面](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThread | 用於Snowflake大量載入器的執行緒數量，執行緒越多，批次載入量越大，效能就越好。 預設為1。 根據機器執行緒計數，數字可以調整。 |
| chunkSize | 決定大量載入器區塊的檔案大小。 預設為128MB。 可以修改以獲得最佳效能（當與bulkThreads一起使用時）。 同時作用中的執行緒越多，效能就越好。 <br>有關詳細資訊，請參閱 [Snowflake檔案](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| 階段名稱 | 預先布建的內部階段名稱。 它將用於大量載入，而不是建立新的臨時階段。 |

## Google Big Query {#google-big-query}

* **[!UICONTROL 服務帳戶]**：您的電子郵件 **[!UICONTROL 服務帳戶]**. 如需詳細資訊，請參閱 [Google Cloud檔案](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL 專案]**：您的名稱 **[!UICONTROL 專案]**. 如需詳細資訊，請參閱 [Google Cloud檔案](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL 資料集]**：您的名稱 **[!UICONTROL 資料集]**. 如需詳細資訊，請參閱 [Google Cloud檔案](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL 金鑰檔案路徑]**：將您的金鑰檔案上傳至伺服器。 僅接受.json檔案。

* **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

| 選項 | 說明 |
|:-:|:-:|
| ProxyType | 用來透過ODBC和SDK聯結器連線至BigQuery的Proxy型別。 </br>目前支援HTTP （預設）、http_no_tunnel、socks4和socks5。 |
| ProxyHost | 可連線到Proxy的主機名稱或IP位址。 |
| ProxyPort | 執行Proxy的連線埠號碼，例如8080 |
| ProxyUid | 用於已驗證Proxy的使用者名稱 |
| proxypwd | ProxyUid密碼 |
| bqpath | 請注意，這僅適用於大量載入工具(Cloud SDK)。 </br> 若要避免使用PATH變數或google-cloud-sdk目錄必須移至其他位置，您可以使用此選項指定伺服器上cloud sdk bin目錄的精確路徑。 |
| GCloudConfigName | 請注意，這適用於7.3.4版開始並僅適用於大量載入工具(Cloud SDK)。</br> Google Cloud SDK會使用設定將資料載入BigQuery表格。 已命名的設定 `accfda` 儲存用來載入資料的引數。 不過，此選項可讓使用者為組態指定不同的名稱。 |
| GCloudDefaultConfigName | 請注意，這適用於7.3.4版開始並僅適用於大量載入工具(Cloud SDK)。</br> 必須先將作用中的標籤傳輸至新設定，才能刪除作用中的Google Cloud SDK設定。 此暫時設定是重新建立載入資料的主要設定所必需的。 暫存組態的預設名稱為 `default`，如有需要，可加以變更。 |
| GCloudRecreateConfig | 請注意，這適用於7.3.4版開始並僅適用於大量載入工具(Cloud SDK)。</br> 當設定為 `false`，大量載入機制不會嘗試重新建立、刪除或修改Google Cloud SDK設定。 相反地，它會使用電腦上現有的設定繼續進行資料載入。 當其他作業取決於Google Cloud SDK設定時，此功能很有價值。 </br> 如果使用者在沒有適當設定的情況下啟用此引擎選項，大量載入機制將會發出警告訊息： `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. 為避免進一步的錯誤，它會恢復為使用預設的ODBC陣列插入大量載入機制。 |

## azure synapseRedshift {#azure-synapse-redshift}

* **[!UICONTROL 伺服器]**：Azure synapse伺服器的URL

* **[!UICONTROL 帳戶]**：使用者名稱

* **[!UICONTROL 密碼]**：使用者帳戶密碼

* **[!UICONTROL 資料庫]**：資料庫名稱

* **[!UICONTROL 選項]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL 伺服器]**：的URL [!DNL Vertica Analytics] 伺服器

* **[!UICONTROL 帳戶]**：使用者名稱

* **[!UICONTROL 密碼]**：使用者帳戶密碼

* **[!UICONTROL 資料庫]**：資料庫名稱

* **[!UICONTROL 工作結構描述]**：工作結構描述的名稱。

* **[!UICONTROL 選項]**：聯結器支援下表詳述的選項。

聯結器支援下列選項：

| 選項 | 說明 |
|---|---|
| 時區名稱 | 預設為空白，這表示會使用Campaign Classic應用程式伺服器的系統時區。 選項可用來強制TIMEZONE工作階段引數。 |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL 伺服器]**：DNS的名稱

* **[!UICONTROL 帳戶]**：使用者名稱

* **[!UICONTROL 密碼]**：使用者帳戶密碼

* **[!UICONTROL 資料庫]**：未在DSN中指定的資料庫名稱。 若在DSN中指定，可保留空白

* **[!UICONTROL 工作結構描述]**：工作結構描述的名稱。 [了解更多](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)


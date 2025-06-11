---
title: 存取外部資料庫的許可權
description: 瞭解您需要在每個資料庫引擎上存取和執行工作的許可權
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: 530a8709a67fabec1a36e1661b922f3e9a9e6996
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---

# 同盟資料存取(FDA)許可權矩陣 {#fda-rights}

下表概述每個系統所需的資料庫許可權，可讓您透過同盟資料存取(FDA)對外部資料庫執行作業。

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **正在連線到遠端資料庫** | `USAGE ON WAREHOUSE`、`USAGE ON DATABASE`和`USAGE ON SCHEMA`許可權 | 建立連結至AWS帳戶的使用者 | 建立服務帳戶並授與專案的主要存取權 | 目錄的`USE CATALOG`許可權和SQL倉儲的`CAN_USE`許可權 |
| **正在建立資料表** | `CREATE TABLE ON SCHEMA`許可權 | `CREATE`許可權 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`和`bigquery.tables.create`許可權 | `USE SCHEMA`和`CREATE TABLE`許可權 |
| **正在建立索引** | 不適用 | `CREATE`許可權 | BigQuery僅支援搜尋索引。 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`、`bigquery.tables.getData`和`bigquery.tables.createIndex`許可權 | 不適用 |
| **正在建立函式** | `CREATE FUNCTION ON SCHEMA`許可權 | `USAGE ON LANGUAGE plpythonu`許可權以呼叫外部Python指令碼 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`和`bigquery.routines.create`許可權 | `CREATE FUNCTION`許可權 |
| **正在建立程式** | 不適用 | `USAGE ON LANGUAGE plpythonu`許可權以呼叫外部Python指令碼 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`和`bigquery.routines.create`許可權 |  不適用 |
| **移除物件（表格、索引、函式、程式）** | 擁有物件 | 擁有物件或成為超級使用者 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`、`bigquery.routines.delete`、`bigquery.tables.delete`和`bigquery.tables.deleteIndex`許可權 | 不適用 |
| **監視執行** | 必要物件的`MONITOR`許可權 | 使用`EXPLAIN`命令不需要許可權 | `monitoring.viewer`角色 | `CAN_VIEW`許可權 |
| **正在寫入資料** | `INSERT`和/或`UPDATE`許可權（視寫入作業而定） | `INSERT`和`UPDATE`許可權 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`和`bigquery.tables.updateData` | `MODIFY`許可權 |
| **正在將資料載入資料表** | 目標資料表許可權上的`CREATE STAGE ON SCHEMA`、`SELECT`和`INSERT` | `SELECT`和`INSERT`許可權 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`、`bigquery.tables.getData`和`bigquery.tables.updateData` | `SELECT`和`MODIFY`許可權 |
| **正在存取使用者端資料** | `SELECT on (FUTURE) TABLE(S)`或`VIEW(S)`許可權 | `SELECT`許可權 | 指派給服務帳戶的角色必須包含： `bigquery.jobs.create`和`bigquery.tables.getData` （針對資料表或`bigquery.dataViewer`角色） | `SELECT`許可權 |
| **存取中繼資料** | `SELECT on INFORMATION_SCHEMA SCHEMA`許可權 | `SELECT`許可權 | `bigquery.metadataViewer`角色 |  `SELECT on INFORMATION_SCHEMA SCHEMA`許可權 |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **正在連線到遠端資料庫** | 讀取（預設）許可權 | `CONNECT`許可權 | 不需要許可權 |
| **正在建立資料表** | `CREATE TABLE ON DATABASE` （倉儲）和`ALTER ON SCHEMA` | `CREATE TABLE`許可權 | `CREATE ON SCHEMA`許可權 |
| **正在建立索引** | 不適用 | `ALTER`許可權 | 不適用 |
| **正在建立函式** | 不適用 | `CREATE FUNCTION`許可權 | `CREATE ON SCHEMA`許可權 |
| **正在建立程式** | `CREATE PROCEDURE ON DATABASE` （倉儲）和`ALTER ON SCHEMA` | `CREATE PROCEDURE`許可權 | `CREATE ON SCHEMA`許可權 |
| **移除物件（表格、索引、函式、程式）** | `ALTER ON SCHEMA` | `ALTER`許可權 | 擁有物件或物件的`DROP`許可權 |
| **監視執行** | Workspace貢獻者或以上許可權(`queryinsights.exec_requests_history`) | `CONTROL`許可權 | 使用`EXPLAIN`陳述式不需要許可權 |
| **正在寫入資料** | `INSERT`和/或`UPDATE ON OBJECT` | `INSERT`和`UPDATE`許可權 | `INSERT`和`UPDATE`許可權 |
| **正在將資料載入資料表** | `SELECT ON OBJECT` 和 `INSERT ON OBJECT` | `CREATE TABLE`、`EXECUTE`、`SELECT`、`INSERT`、`UPDATE`和`ALTER`許可權 | 資料表的`INSERT`許可權，結構描述的`USAGE`許可權 |
| **正在存取使用者端資料** | `SELECT ON OBJECT` | `SELECT`許可權 | `SELECT`許可權 |
| **存取中繼資料** | `SELECT ON INFORMATION_SCHEMA` | 不需要許可權來說明表格 | `USAGE ON SCHEMA`、`SELECT on TABLE`以及表格`v_catalog.columns`和`v_catalog.view_columns`的許可權 |

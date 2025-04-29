---
title: 存取外部資料庫的許可權
description: 瞭解每個資料庫引擎的特定許可權
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 3%

---

# FDA許可權矩陣 {#fda-rights}

下表概述每個系統所需的資料庫許可權，讓使用者可透過FDA在外部資料庫執行作業。

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **正在連線到遠端資料庫** | 倉儲使用量、資料庫使用量和綱要許可權使用量 | 建立連結至AWS帳戶的使用者 | 建立服務帳戶並授與專案的主要存取權 | 對目錄使用CATALOG許可權，以及對SQL倉儲使用CAN_USE許可權 |
| **正在建立資料表** | 依據綱要許可權建立表格 | CREATE許可權 | 指派給服務帳戶的角色必須包含： bigquery.jobs.create和bigquery.tables.create許可權 | 使用綱要許可權和CREATE TABLE許可權 |
| **正在建立索引** | 不適用 | CREATE許可權 | BigQuery僅支援搜尋索引。 指派給服務帳戶的角色必須包含： bigquery.jobs.create、bigquery.tables.getData和bigquery.tables.createIndex許可權 | 不適用 |
| **正在建立函式** | 在綱要許可權上建立函式 | 使用LANGUAGE PLYTHONU許可權可呼叫外部Python指令碼 | 指派給服務帳戶的角色必須包含： bigquery.jobs.create和bigquery.routines.create許可權 | CREATE函式許可權 |
| **正在建立程式** | 不適用 | 使用LANGUAGE PLYTHONU許可權可呼叫外部Python指令碼 | 指派給服務帳戶的角色必須包含： bigquery.jobs.create和bigquery.routines.create許可權 |  不適用 |
| **移除物件（表格、索引、函式、程式）** | 擁有物件 | 擁有物件或成為超級使用者 | 指派給服務帳戶的角色必須包含：bigquery.jobs.create、bigquery.routines.delete、bigquery.tables.delete和bigquery.tables.deleteIndex許可權 |
| **監視執行** | 必要物件的MONITOR許可權 | 使用EXPLAIN命令不需要許可權 | monitoring.viewer角色 | CAN_VIEW許可權 |
| **正在寫入資料** | INSERT和/或UPDATE許可權（視寫入作業而定） | INSERT和UPDATE許可權 | 指派給服務帳戶的角色必須包含： bigquery.jobs.create和bigquery.tables.updateData |  MODIFY許可權 |
| **正在將資料載入資料表** | 在綱要上建立階段，選取並在目標表格上插入許可權 | SELECT和INSERT許可權 | 指派給服務帳戶的角色必須包含： bigquery.jobs.create、bigquery.tables.getData和bigquery.tables.updateData | SELECT與MODIFY許可權 |
| **正在存取使用者端資料** | 選取（未來的）表格或檢視許可權 | SELECT許可權 | 指派給服務帳戶的角色必須包含：表格的bigquery.jobs.create和bigquery.tables.getData或bigquery.dataViewer角色 |  SELECT許可權 |
| **存取中繼資料** | 選取INFORMATION_SCHEMA綱要許可權 | SELECT許可權 | bigquery.metadataViewer角色 |  選取INFORMATION_SCHEMA綱要許可權 |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **正在連線到遠端資料庫** | 讀取（預設）許可權 | CONNECT許可權 | 不需要許可權 |
| **正在建立資料表** | 在資料庫（倉儲）上建立表格並在綱要上變更 | 建立表格許可權 | 建立在綱要上的許可權 |
| **正在建立索引** | 不適用 | ALTER許可權 | 不適用 |
| **正在建立函式** | 不適用 | 建立函式許可權 | 建立在綱要上的許可權 |
| **正在建立程式** | 在資料庫（倉儲）上建立程式，並在綱要上變更 | 建立程式許可權 | 建立在綱要上的許可權 |
| **移除物件（表格、索引、函式、程式）** | 在方案上變更 | ALTER許可權 | 擁有物件或物件的DROP許可權 |
| **監視執行** | Workspace貢獻者或以上許可權(queryinsights.exec_requests_history)  | 控制許可權 | 使用EXPLAIN陳述式不需要任何許可權 |
| **正在寫入資料** | 在物件上插入和/或更新 | 插入和更新許可權 | INSERT和UPDATE許可權 |
| **正在將資料載入資料表** | 在物件上選取並插入在物件上 | 建立表格、執行、選取、插入、更新、變更許可權 | 表格的INSERT許可權，綱要的USAGE許可權 |
| **正在存取使用者端資料** | 在物件上選取 | 選取許可權 | SELECT許可權 |
| **存取中繼資料** | 在INFORMATION_SCHEMA上選取 | 不需要許可權來說明表格 | 使用於綱要、SELECT on TABLE以及表格v_catalog.columns和v_catalog.view_columns的許可權 |

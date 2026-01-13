---
title: 同盟對象構成發行說明
description: 同盟對象構成的最新更新和發行說明。
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: e82f1c237927af983a32c848cb9d45d84f9cf3fe
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 95%

---

# 發行說明 {#rn-new}

[!DNL Federated Audience Composition]持續提供新功能、現有功能增強並修正錯誤。所有變更都已整合在這些發行說明中。[!DNL Federated Audience Composition] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-hant){target="_blank"}。

## 2025 年 10 月發行版本 {#fac-25-10}

### 全新功能 {#fac-25-10-feature}

<!-- 
<table>
<thead>
<tr>
<th><strong>Availability for Adobe Experience Platform customers on Amazon Web Services (AWS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use Federated Audience Composition if your Experience Platform instance is on AWS.</p>
<p>For more information about Experience Platform on AWS, please read the <a href="https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/multi-cloud">multi-cloud overview</a>.</p>
</br>
</td>
</tr>
</tbody>
</table> 
-->

<table>
<thead>
<tr>
<th><strong>適用於 Google BigQuery 和 Snowflake 的 OAuth 驗證</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用 OAuth 連線至 Google BigQuery 和 Snowflake。</p>
<p>如需有關建立連線的更多資訊，請參閱<a href="../connections/home.md#create">連線概觀</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

## 2025 月 8 月版 {#fac-25-8}

### 全新功能 {#fac-25-08-feature}

<table>
<thead>
<tr>
<th><strong>結構描述探索中的複合索引鍵支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在您可以將欄組合在一起來為您的結構描述建立複合索引鍵。</p>
<p>如需有關結構描述的詳細資訊，請參閱<a href="../data-modelling/schemas.md#create">結構描述概觀</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在模型的連結中新增多個聯結</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將多個聯結一起新增到您的模型的單一連結中。</p>
<p>如需有關模型的詳細資訊，請閱讀<a href="../data-modelling/models.md#create">模型概觀</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

### 改善 {#fac-25-8-improvements}

此版本包含下列改善項目：

* **已新增的 `StringAgg` 函數**

  您現在可以將 `StringAgg` 函數用於 Amazon Redshift Spectrum 資料庫。使用運算式編輯器。

* **`Replace`函數**

  該 `Replace` 函數的描述和語法已經在文件中闡明。

### 相容性 {#fac-25-8-compatibility}

* **Azure Synapse 資料庫**

  現在您可以使用 PrivateLink 或 VPN 安全地連線到 Azure Synapse 資料庫。如需詳細資訊，請和 Adobe 客戶服務聯絡。

* **Oracle 資料庫**

  您現在可以安全地連線至 Oracle 資料庫。如需詳細資訊，請和 Adobe 客戶服務聯絡。

如需有關聯合客群構成的詳細資訊，請閱讀[連線概觀](../connections/home.md)。

## 2025 年 7 月版 {#fac-25-7}

### 全新功能 {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>新連接器 - Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Oracle 連接器現在可與聯合客群構成搭配使用。</p>
<p>您可以將 Oracle 連接器用於客群建立和客群擴充使用案例。</p>
<p>如需有關 Oracle 連線的詳細資訊，請參閱<a href="../connections/home.md#create">連線概觀</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>構成警報</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以訂閱警報，以了解您的構成執行成功和失敗的資訊</p>
<p>如需訂閱構成執行通知的詳細資訊，請參閱<a href="../compositions/create-composition.md#alerts">建立構成指南</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

### 改善 {#fac-25-07-improvements}

此版本包含下列改善項目：

* **增加了伺服器字元長度**

  在設定您的聯合資料庫時，您現在最多可以使用 255 個字元，而不是先前的 80 個字元。

## 2025 年 6 月版 {#fac-25-6}

### 改善 {#fac-25-06-improvements}

此版本包含下列改善項目：

* **對 Adobe Healthcare Shield 客戶的全面發佈**

  在 6 月底以前，Adobe Healthcare Shield 客戶將可以將聯合客群構成用於客群建立、擴充以及輪廓擴充使用案例。

  如需有關聯合客群構成中的隱私權和安全性的詳細資訊，請參閱[資料治理、隱私權和安全性指南](/help/governance-privacy-security/home.md)。

* **物件層級的存取控制**

  聯合客群構成現在支援物件層級的存取控制，以便將存取標籤套用至您指定的構成。

  如需有關使用物件層級存取標籤的詳細資訊，請參閱[構成指南](/help/compositions/home.md)。

* **預設角色**

  您現在可以使用其中一個預設角色來管理聯合客群構成存取的使用者權限。

  如需有關預設角色的詳細資訊，請參閱[存取聯合客群構成指南](/help/governance-privacy-security/access-control.md)。

* **輪廓擴充使用案例中的漸進式更新**

  儲存輪廓活動現在支援漸進式更新。透過漸進式更新，您就可以查詢及更新增量資料，同時使用外部資料倉儲中的資料來擴充輪廓。

  有關使用儲存設定檔活動的詳細資訊，請參閱活動指南[的](/help/compositions/activities.md#save-profiles)儲存設定檔區段。

## 2025 年 5 月版 {#fac-25-5}

### 全新功能 {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>資料模型畫布檢視 - 一般適用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>具備晝布檢視的資料模型現在可供所有客戶使用！</p>
<p>除了現有的表格檢視以外，資料模型區段的畫布檢視可透過在畫布版面中啟用資料模型的視覺化及其連結，藉此改善使用體驗。 </p>
<p>有關畫布檢視的更多資訊，請閱讀「<a href="../data-modelling/models.md">資料模型概觀</a>」。</p>
</br>
</td>
</tr>
</tbody>
</table>

### 改善 {#fac-25-5-improvements}

此版本包含下列改善項目。

* **角色型存取控制**

  從 5 月版本開始，[!DNL Federated Audience Composition] 支援存取控制的全新精細度權限。使用者可以將這些權限指派給使用者角色，以便更精確存取[!DNL Federated Audience Composition]。

  若要了解有關新權限的更多資訊，請閱讀「[聯合客群構成存取指南](/help/governance-privacy-security/access-control.md)」。

## 2025 年 4 月發行版本 {#fac-25-4}

### 全新功能 {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>資料模型畫布檢視 - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了現有的表格檢視以外，資料模型區段的畫布檢視可透過在畫布版面中啟用資料模型的視覺化及其連結，藉此改善使用體驗。 </p>
<p>具有畫布檢視的資料模型目前僅供特定使用者作為 Beta 版使用。</p>
<p>如需詳細資訊，請參閱<a href="../data-modelling/models.md">詳細文件</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 助理對產品知識的支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 助理是一項使用者介面功能，旨在協助您導覽和了解 Adobe 的概念，並獲取指定環境的運作洞察。 其適用於 Adobe Experience Cloud 的多項產品，包括聯合客群構成。</p>
<p>如需詳細資訊，請參閱<a href="../start/ai-assistant.md">詳細文件</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>儲存輪廓活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> 聯合客群構成現在支援輪廓擴充使用案例，可讓客戶利用來自其外部資料倉儲的資料來增強現有的 Experience Platform 輪廓。
</p>
<p>如需詳細資訊，請參閱<a href="../compositions/activities.md#save-profiles">詳細說明文件</a>。</p>
</br>
</td>
</tr>
</tbody>
</table>

### 改善 {#fac-25-4-improvements}

此版本包含下列改善項目：

* **資料模型名稱**

  在「客群」選單中，「**聯合構成**」索引標籤現在顯示資料模型名稱而非 ID，從而提高清晰度和整體可用性。

* **客群**

  現在，當使用者選取沒有關聯客群的資料模型時，「客群」選單會顯示所選資料模型的名稱或標籤。

* **大量客群匯出**

  聯合客群構成現在支援匯出大量客群，檔案大小可大於 1GB。

* **儲存客群活動**

  **儲存客群**&#x200B;活動中新增了一則注意事項，提醒使用者與資料管理員協作，以便將治理標籤套用至在客群建立和擴充期間所建立的新結構描述和資料集。
  [深入了解資料使用標籤](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/data-governance/labels/user-guide)

### 相容性 {#fac-25-4-compat}

* **Amazon Redshift 安全連線**

  透過這個新版本，聯合客群構成可支援與 Amazon Redshift 資料庫建立安全的私人連結連線。[了解更多](../connections/home.md#amazon-redshift)

* **Google BigQuery**

  透過這個新版本，聯合客群構成可支援與 Google BigQuery 資料庫建立安全的 VPN 連線。[了解更多](../connections/home.md#google-bigquery)

## 2025 年 3 月發行版本 {#fac-25-3}

### 改善 {#fac-25-3-improvements}

此版本包含下列改善項目：

* **聯合客群構成權限**

  從 3 月版開始，[!DNL Federated Audience Composition] 將會強制已獲得&#x200B;**管理聯合資料**&#x200B;權限的使用者存取&#x200B;**聯合資料管理**&#x200B;和&#x200B;**聯合構成**&#x200B;的介面。

  我們建議使用者聯絡管理員將此權限新增至他們的角色中，以便繼續存取 [!DNL Federated Audience Composition] 使用者介面。

  若要了解如何指派此權限，請參閱[詳細說明文件](/help/governance-privacy-security/access-control.md)。

### 相容性 {#fac-25-3-compat}

* **Databricks 連線**

  透過此一新版本，聯合客群構成現在支援透過私人連結進行 Databricks 資料庫連線，這包括透過私人連結與託管在 Amazon Web Services (AWS) 上的 Databricks 資料庫建立安全連線，以及透過 VPN 與託管在 Microsoft Azure 上的 Databricks 資料庫建立安全連線。[了解更多](../connections/home.md#databricks)

* **為 B2B CDP 客戶提供支援**

  企業對企業 (B2B) 客戶資料平台 (CDP) 的客戶現在可以使用聯合客群構成來處理人員型客群使用案例。

* **Snowflake 安全連線**

  透過此一新版本，聯合客群構成現在支援使用私人連結連線至託管在 Microsoft Azure 上的 Snowflake 資料庫連線。[了解更多](../connections/home.md#snowflake)

## 2025 年 2 月發行版本 {#fac-25-2}

此版本隨附下列變更：

* **Microsoft Fabric 支援**

  您現在可以透過聯合客群構成，建立與 Microsoft Fabric 資料庫的連線。[了解更多](../connections/home.md)

* **Amazon Redshift Spectrum 支援**

  對 Amazon Redshift 資料庫的連線現已支援 Amazon Redshift Spectrum。[了解更多](../connections/home.md#amazon-redshift)

* **增強的結構描述建立體驗**

  透過更新後的使用者介面，建立結構描述的程序已獲得改善，變得更直覺且更易於導覽。這些增強功能為資料從業人員提供了更順暢、更有效率的資料模型開發方法。[了解更多](../data-modelling/schemas.md)

* **Databricks 的客群擴充支援**

  您現在可以在「讀取客群」流程中使用 Databricks，為 Databricks 資料庫啟用活動並允許將其設定為新目的地。[了解更多](../connections/destinations.md)

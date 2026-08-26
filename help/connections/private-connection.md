---
title: 使用私人連線來連線到同盟對象構成
description: 瞭解如何使用私人連線來設定並連線至同盟對象構成。 這包括PrivateLink或站台對站台VPN。
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# 與同盟對象構成的私人連線

同盟對象構成支援與多個資料庫的私人連線。 私人連線可讓您連線到客戶代管的資料倉儲，而不需周遊公用網際網路。

## 支援的資料庫 {#supported-databases}

下列資料庫支援與同盟對象構成的私人連線：

| 資料庫 | 雲端 | 私人連線型別 |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink （VPC介面端點） |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink （私人端點） |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink （Managed VPC端點） |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink （VPC介面端點） |
| [!DNL Databricks] | [!DNL Microsoft Azure] | 站台對站台VPN |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | 站台對站台VPN |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | 站台對站台VPN |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | 站台對站台VPN |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>若要搭配[!DNL Snowflake]使用私人連線，您&#x200B;**必須**&#x200B;至少在[!DNL Snowflake]上的Business Critical層或更高。 如需與[!DNL Snowflake]的私人連線詳細資訊，請參閱Snowflake檔案[&#128279;](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound)中的私人連線指南。

與[!DNL Snowflake]搭配使用私人連線視您[!DNL Snowflake]執行個體所在的雲端提供者而定。

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>在繼續之前，請務必從Adobe客戶服務取得您的AWS帳戶ID。 取得AWS帳戶ID後，請連絡[!DNL Snowflake]支援，讓[!DNL Snowflake]可以授權您的AWS帳戶使用PrivateLink。

在您的AWS帳戶獲得授權可與[!DNL Snowflake]一起使用後，您將需要取得包括`privatelink-vpce-id`、`privatelink-account-url`和`privatelink_ocsp-url`的值，才能取得VPC介面端點。

您可以在您的[!DNL Snowflake]帳戶中以ACCOUNTADMIN身分執行下列命令，以取得這些值：

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

執行這些命令後，您可以將完整的SQL輸出傳送至Adobe客戶服務，讓Adobe可以為您建立VPC介面端點。

如需使用AWS建立PrivateLink連線的詳細資訊，請參閱[AWS PrivateLink指南](https://docs.snowflake.com/en/user-guide/admin-security-privatelink)。

如果您想要授權PrivateLink以便與內部中繼環境搭配使用，請聯絡Adobe客戶服務以啟用該環境。

如需有關為內部測試環境建立與AWS的PrivateLink連線的詳細資訊，請閱讀[內部測試環境的AWS VPC介面端點指南](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws)。

### Microsoft Azure {#snowflake-azure}

若為Microsoft Azure，您必須取得包括`privatelink-pls-id`、`privatelink-account-url`和`privatelink_ocsp-url`在內的值，才能建立Azure私人端點。

您可以在Snowflake帳戶中執行下列命令，以取得這些值：

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

執行這些命令後，您可以將完整的SQL輸出傳送至Adobe客戶服務，讓Adobe可以為您建立Azure私人端點。

Adobe建立Azure私人端點後，您就可以取得私人端點資源ID。 現在您已擁有私人端點資源識別碼，請連絡[!DNL Snowflake]支援人員，在提供資源識別碼的同時，授權您的[!DNL Snowflake]帳戶。

如需使用Azure建立PrivateLink連線的詳細資訊，請參閱[Azure PrivateLink指南](https://docs.snowflake.com/en/user-guide/privatelink-azure)。

如果您要授權PrivateLink以便與內部中繼環境搭配使用，請在[!DNL Snowflake]中執行下列命令，同時提供Adobe客戶服務提供的內部中繼資源ID：

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

如需有關為內部測試環境建立與Azure的PrivateLink連線的詳細資訊，請閱讀[內部測試環境的Azure私人端點指南](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure)。

## Amazon Redshift {#amazon-redshift}

布建的叢集和Redshift無伺服器都支援具有同盟對象構成的私人連線。

>[!IMPORTANT]
>
>開始之前，請聯絡Adobe客戶服務，接收您的Amazon Web Services (AWS)帳戶ID和虛擬私人雲端(VPC) ID。 您將需要&#x200B;**兩個**&#x200B;這些值才能取得跨帳戶端點存取權。 如需授與VPC存取權的詳細資訊，請參閱[授與VPC存取權指南](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html)。

取得AWS和VPC ID後，請前往AWS Management Console授與受管理VPC端點的跨帳戶存取權。

針對已布建的叢集，請記下&#x200B;**Redshift叢集識別碼**&#x200B;和&#x200B;**叢集擁有者AWS帳戶ID**&#x200B;的值。 若是Redshift Server無伺服器，請同時記下&#x200B;**工作群組名稱**&#x200B;和&#x200B;**擁有者AWS帳戶ID**&#x200B;值。

取得這些值後，請將這些詳細資料與Adobe客戶服務共用，讓Adobe可以建立受管理的VPC端點。 然後Adobe會與您共用下列連線詳細資料： **Redshift端點URL**、**Redshift JDBC URL**&#x200B;和&#x200B;**Redshift ODBC URL**。

## Databricks {#databricks}

>[!AVAILABILITY]
>
>若要搭配Databricks使用私人連線，您&#x200B;**必須**&#x200B;屬於Databricks的企業計畫。 如需有關Databricks私人連線的詳細資訊，請參閱[私人連結概念指南](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts)。

搭配Databricks使用私人連線取決於您的Databricks執行個體所在的雲端提供者。

### Amazon Web Services {#databricks-aws}

使用Amazon Web Services設定之前，請聯絡Adobe客戶服務，讓他們建立指向Databricks的前端（傳入） VPC介面端點。 此端點涵蓋Federated Audience Composition與您的Databricks工作區的ODBC連線。

從Adobe客戶服務取得您的VPC端點ID和AWS區域後，您需要使用Adobe提供的資訊註冊VPC端點。

註冊VPC端點後，您需要建立私人存取設定(PAS)物件。 當您建立端點時，請將&#x200B;**私人存取層級**&#x200B;設定為&#x200B;**端點**&#x200B;層級，並選取先前建立的VPC端點。 如需建立私人存取設定的詳細資訊，請參閱[設定入站PrivateLink指南](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings)。

在設定您的私人存取設定後，您可以將VPC端點附加至您的工作區。 如需使用PrivateLink建立工作區的詳細資訊，請參閱[設定傳入的PrivateLink指南](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects)。

現在所有設定均已設定完畢，您可以與Adobe客戶服務共用您的Databricks工作區URL。 在您共用Databricks工作區URL後，Adobe可以設定將請求路由至工作區端點所需的DNS設定。

### Microsoft Azure {#databricks-azure}

站台對站台VPN可用來安全地從Adobe連線至Azure上的Databricks工作區。 您必須設定Azure VPN閘道，以建立VPN通道，將資料安全地傳輸至Adobe。

設定Azure VPN閘道和Databricks私人端點後，請與您的Adobe客戶服務代表共用下列詳細資料： **Azure虛擬網路閘道**、**Databricks私人端點IP**、**Databricks Workspace URL**&#x200B;和&#x200B;**自治系統號碼(ASN)**。

有了這些詳細資訊，Adobe可以建立您的連線所需的VPN通道。 建立VPN通道後，Adobe會提供&#x200B;**VPN通道公用和私用IP位址**、**預先共用金鑰**&#x200B;以及&#x200B;**自治系統號碼**。

您現在可以在Azure VNet閘道中設定VPN通道。 如需詳細資訊，請參閱[使用VPN閘道連線AWS和Azure](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp)。

### Google Cloud Platform {#databricks-gcp}

站台對站台VPN可用來從Adobe安全地連線至Google Cloud平台上的Databricks工作區。 您需要設定Google Cloud Platform High Availability VPN閘道和雲端路由器，以建立VPN通道，將您的資料安全地傳輸至Adobe。

設定GCP HA VPN閘道和雲端路由器後，請與您的Adobe客戶服務代表分享下列詳細資料： **GCP HA VPN閘道**、**Databricks Workspace URL**、**Private Service Connect (PSC) IP**&#x200B;以及&#x200B;**自治系統號碼(ASN)**。

有了這些詳細資訊，Adobe可以建立您的連線所需的VPN通道。 建立VPN通道後，Adobe會提供&#x200B;**VPN通道公用和私用IP位址**、**預先共用金鑰**&#x200B;以及&#x200B;**自治系統號碼**。

您現在可以在Google Cloud Platform帳戶中設定VPN通道。 如需詳細資訊，請閱讀[建立HA VPN連線指南](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws)。

## Azure Synapse Analytics {#azure-synapse}

若要與Azure Synapse Analytics連線，您必須先建立Azure虛擬網路閘道和Synapse私人端點。 Azure虛擬網路閘道可讓您在Azure虛擬網路之間傳送加密的流量至Synapse，而Synapse私人端點則可讓您透過私人連線安全地傳輸資料。

設定Azure虛擬網路閘道和Synapse私人端點後，請與您的Adobe客戶服務代表共用下列詳細資料： **Azure虛擬網路閘道**、**Synapse私人端點IP**、**Synapse Workspace URL**&#x200B;和&#x200B;**自治服務號碼(ASN)**。

有了這些詳細資訊，Adobe可以建立您的連線所需的VPN通道。 建立VPN通道後，Adobe會提供&#x200B;**VPN通道配對**、**預先共用金鑰**&#x200B;以及&#x200B;**自治系統號碼**。

您現在可以在Azure VNet閘道中設定VPN通道。 如需詳細資訊，請參閱[使用VPN閘道連線AWS和Azure](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp)。

## Google Big Query {#gbq}

若要與Google Big Query連線，您必須先建立Google Cloud Platform High Availability VPN閘道和雲端路由器。

設定GCP HA VPN閘道和雲端路由器後，請與您的Adobe客戶服務代表共用下列詳細資料： **GCP HA VPN閘道**、**私人服務連線(PSC) IP**&#x200B;以及&#x200B;**自治系統號碼(ASN)**。

有了這些詳細資訊，Adobe可以建立您的連線所需的VPN通道。 建立VPN通道後，Adobe會提供&#x200B;**VPN通道公用和私用IP位址**、**預先共用金鑰**&#x200B;以及&#x200B;**自治系統號碼**。

您現在可以在Google Cloud Platform帳戶中設定VPN通道。 如需詳細資訊，請閱讀[建立HA VPN連線指南](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws)。

---
audience: end-user
title: 將受眾傳送至Adobe同盟受眾構成
description: 瞭解如何將Adobe Experience Platform對象傳送至同盟對象構成
badge: label="可用性限制" type="Informative"
source-git-commit: 553db3ad6d318e7bddcede352178427255d41781
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 5%

---

# 傳送Adobe Experience Platform至Adobe同盟對象構成 {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="建立目的地"
>abstract="輸入連接到新同盟資料庫的設定。使用&#x200B;**[!UICONTROL 連結到目的地]**&#x200B;按鈕驗證您的設定。"

Adobe Experience Platform可讓您從受眾入口網站傳送受眾，以Adobe同盟受眾構成。 如此一來，您就可以將現有的對象運用到組合中，並將其與外部資料庫的資料結合，以建立新對象或更新現有的對象。

若要這麼做，您需要在Adobe Experience Platform中設定與Adobe同盟對象構成目的地的新連線。 您可以使用排程器以固定頻率傳送特定對象，選擇要與對象一起傳送的欄位，例如ID以調解資料。 如果您已將治理和隱私權政策套用至對象，則會在對象更新後保留並傳回對象入口網站。

將Adobe Experience Platform對象傳送至Adobe同盟對象構成的主要步驟如下：

1. 存取Adobe Experience Platform目的地目錄，並選取同盟對象構成目的地。

   在右窗格中選取&#x200B;**[!UICONTROL 設定新的目的地]**。

   ![](assets/destination-new.png)

1. 提供新連線的名稱，並選擇要使用的&#x200B;**[!UICONTROL 連線型別]**&#x200B;以及要連線的&#x200B;**[!UICONTROL 同盟資料庫]**，然後按一下[下一步]****。

   ![](assets/destination-configure.png)

   **[!UICONTROL 警示]**&#x200B;區段可讓您啟用警示，以接收有關您目的地之資料流狀態的通知。 如需警示的詳細資訊，請參閱[使用UI訂閱目的地警示](../../ui/alerts.md)的指南。

1. **[!UICONTROL 治理原則與執行動作]**&#x200B;步驟，您可以定義您的資料治理原則，並確保在傳送和啟用對象時，所使用的資料是合規的。

   當您完成選取目的地所需的行銷動作時，請按一下[建立]。****

1. 會建立與目的地的新連線。 您現在可以啟用對象以傳送至目的地。 若要這麼做，請從清單中選取它，然後按一下[下一步] ****

   ![](assets/destination-activate.png)

1. 選取您要傳送的所要對象，然後按一下[下一步] ****。

1. 為選取的對象設定檔案名稱和匯出排程。

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >有關如何設定排程和檔案名稱的詳細資訊，請參閱Adobe Experience Platform檔案：
   >* [排程對象匯出](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling)
   >* [設定檔案名稱](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names)

1. 在&#x200B;**[!UICONTROL 對應]**&#x200B;步驟中，選取要為對象匯出的屬性和身分欄位。 如需詳細資訊，請參閱Adobe Experience Platform檔案中的[對應步驟](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping)。

   ![](assets/destination-attributes.png)

1. 檢閱目的地組態和對象設定，然後按一下[完成]。****

   ![](assets/destination-review.png)

現在為新連線啟用選取的對象。 您可以導覽回&#x200B;**[!UICONTROL 啟用對象]**&#x200B;頁面，新增更多要透過此連線傳送的對象。 對象啟動後，您就無法移除對象。

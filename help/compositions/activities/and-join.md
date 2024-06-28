---
audience: end-user
title: 使用AND — 聯結活動
description: 瞭解如何使用AND — 加入活動
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 66%

---

# 合併連結 {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join 活動"
>abstract="此 **合併連結** 活動可讓您同步撰寫的多個執行分支。 一旦所有前面的活動完成，就會觸發此活動。這可讓您在繼續執行構成之前，先確定某些活動已完成。"

此 **合併連結** 活動可讓您同步撰寫的多個執行分支。

此活動只會在所有傳入轉變啟動後，才會觸發其傳出轉變，換句話說，會在所有之前的活動完成後觸發。這可讓您在繼續執行構成之前，先確定某些活動已完成。

## 設定 And-join 活動 {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="設定 AND-join 活動"
>abstract="選取您要參加的活動。在「**主要集合**」下拉選單中，選擇您要保留的傳入轉變族群。"

請按照以下步驟設定「**合併連結**」活動：

1. 新增多個活動，例如「管道」活動，以形成至少兩個不同的執行分支。
1. 新增「**合併連結**」活動至任何分支。
1. 在「**合併選項**」一節中，勾選您之前希望加入的所有活動。
1. 在「**主要集合**」下拉選單中，選擇您要保留的傳入轉變母體。傳出轉變只能包含其中一個傳入轉變母體。


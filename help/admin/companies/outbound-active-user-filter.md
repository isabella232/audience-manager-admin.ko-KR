---
description: 다음 지침에 따라 최근 활성 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 사이트 내 타깃팅 시스템에 푸시하거나 DSP로 파일 크기를 제한하도록 필터링할 수 있습니다. 증분 동기화에는 이 필터를 사용할 수 없습니다.
seo-description: 다음 지침에 따라 최근 활성 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 사이트 내 타깃팅 시스템에 푸시하거나 DSP로 파일 크기를 제한하도록 필터링할 수 있습니다. 증분 동기화에는 이 필터를 사용할 수 없습니다.
seo-title: 활성 사용자만 아웃바운드 데이터 필터링
title: 활성 사용자만 아웃바운드 데이터 필터링
uuid: A 2 B 4 A 385-EEE 3-458 C-B 978-09509 CACB 397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 활성 사용자만 아웃바운드 데이터 필터링 {#filter-outbound-data-by-active-users-only}

다음 지침에 따라 최근 활성 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 사이트 내 타깃팅 시스템에 푸시하거나 DSP로 파일 크기를 제한하도록 필터링할 수 있습니다. 증분 동기화에는 이 필터를 사용할 수 없습니다.

>[!NOTE]
>
>방문자는 선택한 고객 사이트나 광고 트래픽에 대해 "활성" 로 분류할 필요가 없습니다. [!DNL Audience Manager] 고객 또는 파트너가 "활성" 로 분류할 수 있습니다.

활성 사용자만 필터링하려면 다음을 수행하십시오.

1. 클릭 **[!UICONTROL Companies]**.
1. 작업할 회사를 선택하고 **[!UICONTROL Destinations]**&#x200B;를 클릭합니다.
1. [!UICONTROL Batch Data] 섹션에서 다음 옵션을 설정합니다.

   * **[!UICONTROL Sync Type]**: **[!UICONTROL Customer]** 또는 **[!UICONTROL Platform]**&#x200B;을 선택합니다.
   * **[!UICONTROL Sync Type Lookback Period]**: 이 시간 간격은 데이터 파일의 범위를 정의합니다. 선택 사항은 **[!UICONTROL 24 hours]****[!UICONTROL 7 days]****[!UICONTROL 30 days]**, 입니다.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: **[!UICONTROL Never]** Select. 이 필터는 전체 동기화 파일에만 적용됩니다.
   * **[!UICONTROL Full Sync Scheduled Run]**: 이 파일 수신 빈도를 결정합니다. 선택 사항에는 **[!UICONTROL 24 hours]****[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**&#x200B;또는 **[!UICONTROL Never]** (비활성화) 이 포함됩니다.

1. 클릭 **[!UICONTROL Save]**.

---
description: 이 지침에 따라 최근에 활성화된 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 사이트 내 타깃팅 시스템에 푸시하도록 필터링하거나 DSP로 전송된 파일의 크기를 제한하도록 할 수 있습니다. 증분 동기화에 이 필터를 사용할 수 없습니다.
seo-description: 이 지침에 따라 최근에 활성화된 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 사이트 내 타깃팅 시스템에 푸시하도록 필터링하거나 DSP로 전송된 파일의 크기를 제한하도록 할 수 있습니다. 증분 동기화에 이 필터를 사용할 수 없습니다.
seo-title: 활성 사용자로만 아웃바운드 데이터 필터링
title: 활성 사용자로만 아웃바운드 데이터 필터링
uuid: a2b4a385-eee3-458c-b978-09509cacb397
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 8%

---


# 활성 사용자로만 아웃바운드 데이터 필터링 {#filter-outbound-data-by-active-users-only}

이 지침에 따라 최근에 활성화된 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 사이트 내 타깃팅 시스템에 푸시하도록 필터링하거나 DSP로 전송된 파일의 크기를 제한하도록 할 수 있습니다. 증분 동기화에 이 필터를 사용할 수 없습니다.

>[!NOTE]
>
>방문자를 선택한 고객 사이트 또는 광고 트래픽에서 &quot;활성&quot;으로 간주할 필요는 없습니다. 모든 [!DNL Audience Manager] 고객 또는 파트너가 &quot;활성&quot;으로 자격을 얻을 수 있습니다.

활성 사용자로만 필터링하려면

1. 클릭 **[!UICONTROL Companies]**.
1. 작업할 회사를 선택하고 을 클릭합니다 **[!UICONTROL Destinations]**.
1. 섹션에서 [!UICONTROL Batch Data] 다음 옵션을 설정합니다.

   * **[!UICONTROL Sync Type]**: 또는 **[!UICONTROL Customer]** 를 선택합니다 **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: 이 시간 간격은 데이터 파일의 범위를 정의합니다. 선택 사항에는 **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**&#x200B;등이 포함됩니다.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 이 필터는 전체 동기화 파일에만 적용됩니다.
   * **[!UICONTROL Full Sync Scheduled Run]**: 이 파일을 받는 빈도를 결정합니다. 선택 사항에는 **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]****[!UICONTROL 30 days]**&#x200B;또는 **[!UICONTROL Never]** (비활성화)가 포함됩니다.

1. 클릭 **[!UICONTROL Save]**.

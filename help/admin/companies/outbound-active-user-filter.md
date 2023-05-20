---
description: 다음 지침에 따라 최근 활성 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 온사이트 타겟팅 시스템에 푸시하도록 필터링하거나 DSP에 전송되는 파일 크기를 제한할 수 있습니다. 증분 동기화에는 이 필터를 사용할 수 없습니다.
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: 활성 사용자로만 아웃바운드 데이터 필터링
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%

---

# 활성 사용자로만 아웃바운드 데이터 필터링 {#filter-outbound-data-by-active-users-only}

다음 지침에 따라 최근 활성 사용자만 포함하는 전체 동기화 파일을 생성합니다. 활성 사용자가 관련 데이터를 온사이트 타겟팅 시스템에 푸시하도록 필터링하거나 DSP에 전송되는 파일 크기를 제한할 수 있습니다. 증분 동기화에는 이 필터를 사용할 수 없습니다.

>[!NOTE]
>
>방문자를 선택한 고객 사이트 또는 해당 광고 트래픽에서 볼 필요가 없어 &quot;활성&quot;으로 분류할 수 있습니다. 이 조각은 누구나 볼 수 있습니다. [!DNL Audience Manager] 고객 또는 파트너가 &quot;활성&quot;으로 평가되는 경우

활성 사용자만 필터링하려면 다음을 수행합니다.

1. 클릭 **[!UICONTROL Companies]**.
1. 작업할 회사를 선택하고 을(를) 클릭합니다 **[!UICONTROL Destinations]**.
1. 다음에서 [!UICONTROL Batch Data] 섹션에서 다음 옵션을 설정합니다.

   * **[!UICONTROL Sync Type]**: 선택 **[!UICONTROL Customer]** 또는 **[!UICONTROL Platform]**.
   * **[!UICONTROL Sync Type Lookback Period]**: 이 시간 간격은 데이터 파일의 범위를 정의합니다. 선택 사항에는 다음이 포함됩니다. **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**.
   * **[!UICONTROL Incremental Sync Scheduled Run]**: Select **[!UICONTROL Never]**. 이 필터는 전체 동기화 파일에만 적용됩니다.
   * **[!UICONTROL Full Sync Scheduled Run]**: 이 파일의 수신 빈도를 결정합니다. 선택 사항에는 다음이 포함됩니다. **[!UICONTROL 24 hours]**, **[!UICONTROL 7 days]**, **[!UICONTROL 30 days]**, 또는 **[!UICONTROL Never]** (비활성화하려면).

1. 클릭 **[!UICONTROL Save]**.

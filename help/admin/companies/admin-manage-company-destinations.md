---
description: Audience Manager 대상을 만들고, 편집하고, 삭제합니다.
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 회사 대상 관리
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 1%

---

# 회사 대상 관리 {#manage-company-destinations}

Audience Manager 대상을 만들고, 편집하고, 삭제합니다.

<!-- t_company_destinations.xml -->

자세한 내용은 [대상](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html) 다음에서 *Audience Manager 사용 안내서*.

## 회사 대상 만들기 또는 편집 {#create-edit-company-destinations}

섹션을 스크롤하여 새로 만드는 방법에 대한 단계별 지침을 확인하십시오 [!DNL Audience Manager] 대상 또는 기존 대상을 편집합니다.

<!-- create-edit-company-destinations.xml -->

다음 방문: [Experience Cloud 파트너 통합 페이지](https://wiki.corp.adobe.com/x/mPIMPw) 대상을 설정하기 전에 이 페이지에는 각 라이브러리에 대해 채워야 하는 특정 정보가 포함되어 있습니다 [!DNL Audience Manager] 파트너 통합.

클라이언트에서 을 사용하려는 경우 [!DNL Adobe Media Optimizer] 의 대상으로서 [!DNL Audience Manager] , 다음에서 이 작업을 설정해야 합니다. [!DNL Adobe Media Optimizer].

## 대상 탭으로 이동합니다. {#navigate-destinations}

1. 클릭 **[!UICONTROL Companies]**&#x200B;를 클릭하고 원하는 회사를 찾아 클릭하여 해당 회사를 표시합니다 [!UICONTROL Profile] 페이지를 가리키도록 업데이트하는 중입니다. 다음을 사용할 수 있습니다. [!UICONTROL Search] 목록 하단의 상자 또는 페이지 매김 컨트롤을 사용하여 원하는 회사를 찾을 수 있습니다. 원하는 열의 헤더를 클릭하여 각 열을 오름차순 또는 내림차순으로 정렬할 수 있습니다.
1. 다음을 클릭합니다. **[!UICONTROL Destinations]** 탭.
1. 새 대상을 만들려면 다음을 클릭하십시오. **[!UICONTROL Add Destination]**. 기존 대상을 편집하려면 **[!UICONTROL Name]** 열.

## 기본 설정 {#basic-settings}

의 필드를 채웁니다. **[!UICONTROL Basic Settings]** 창.

* **[!UICONTROL Name]:** (필수) 이 대상의 이름을 지정합니다.
* **[!UICONTROL Description]:** 이 대상에 대한 설명 정보를 지정합니다.
* **[!UICONTROL Type]:** (필수) 원하는 대상 유형을 선택합니다.
   * **[!UICONTROL Bulk ID]**: 다른 플랫폼 간에 ID를 동기화합니다.
   * **[!UICONTROL Bulk Trait]**: 트레이트 정보를 대량으로 다른 플랫폼에 보냅니다.
   * **[!UICONTROL Bulk Segment]**: 세그먼트 정보를 여러 플랫폼으로 일괄적으로 보냅니다.
   * **[!UICONTROL S2S]**: 서버 간 대상을 사용하여 실시간 및 배치 데이터를 다른 플랫폼으로 전송합니다.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] 만 해당) 옵션을 선택합니다.
   * **[!UICONTROL Segment ID]:** 이 설정을 선택하면 대상 값 매핑이 [!DNL Audience Manager] 세그먼트 ID.
   * **[!UICONTROL Integration Code Value]:** 이 설정을 선택하면 대상 값 매핑이 [!DNL Audience Manager] 세그먼트 통합 코드.
* **[!UICONTROL User ID Key]:** (필수) 드롭다운 목록에서 이 대상에 대해 원하는 사용자 ID 키를 선택합니다.

이 ID는 마스터 데이터 소스 ID로 사용됩니다. 파일에서 아웃바운드 사용자 ID를 결정합니다.

>[!NOTE]
>
>의 경우 [!UICONTROL Bulk ID] 대상 유형, [!DNL Audience Manager] [!UICONTROL User ID] 또는 [!DNL Adobe Experience Cloud] ID

데이터 소스 ID인 경우( [!UICONTROL DPID])가 드롭다운 목록에 표시되지 않으면 **[!UICONTROL Outbound]** 의 데이터 소스 수준에서 확인란 [데이터 소스 설정 페이지](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]:** (필수) 드롭다운 목록에서 이 대상에 대해 원하는 데이터 소스를 선택합니다. 이 설정을 사용하면 아웃바운드 데이터의 레이블을 지정할 수 있으므로 클라이언트 측에서 별도의 시스템으로 수집할 수 있습니다.
* **[!UICONTROL Foreign Account ID]:** 이 대상에 대한 외부 계정 ID를 지정하십시오. 이는 아웃바운드 데이터에 대한 수신자 시스템의 식별 값입니다.
* **[!UICONTROL Outbound Sample Rate Denominator]:** 반환되는 데이터의 총 양을 알 수 없는 경우 이 설정을 사용하여 전체 양이 아닌 샘플 양의 데이터만 반환합니다. 데이터의 일부를 나타내려면 여기서 숫자를 조정하십시오(예: 값 &#39;100&#39;은 데이터의 정규 양의 1/100을 반환하고, 값 &#39;10&#39;은 데이터의 정규 양의 1/10을 반환). 기본값은 모든 데이터를 반환하는 &#39;1&#39;입니다.

## 실시간 데이터(S2S 대상용) {#realtime-s2s}

다음을 만드는 경우 [!UICONTROL S2S] 대상, 아래 필드를 채웁니다.

**[!UICONTROL Servers]**: 원하는 을 선택합니다 `HTTP` 이 대상에 대한 서버입니다.
**[!UICONTROL Format]**: 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!UICONTROL HTTP only].

>[!NOTE]
>
>대상 [!DNL S2S] 다음 중 하나를 활성화하거나 비활성화할 수 있습니다. [!UICONTROL Realtime] 또는 [!UICONTROL Batch] 온스크린 꺼짐/켜짐 슬라이더를 사용하는 대상. 두 옵션을 모두 비활성화할 수는 없습니다.

## 일괄 데이터 {#batch-data}

대상 [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] 또는 [!UICONTROL Bulk Segment] 대상, 아래 필드를 채웁니다.

* **[!UICONTROL Protocol]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 프로토콜을 선택합니다.
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 서버를 선택합니다.
* **[!UICONTROL Format]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!DNL HTTP] 또는 위에서 선택한 프로토콜에 따라 파일 형식도 선택할 수 있습니다.
* **[!UICONTROL Sync Type]**: (필수) 이 대상에 대해 원하는 동기화 유형을 선택합니다. 이는 클라이언트가 아웃바운드 주문에 포함할 사용자 활동 수준을 나타냅니다. 선택 **[!UICONTROL Customer]** 고객이 속성에서 세그먼트 자격 분석에만 관심이 있는 경우. 선택 **[!UICONTROL Platform]** 모든 활동에 대해 오프사이트 활동의 세그먼트 자격을 포함하려는 경우 [!DNL Audience Manager] 고객.
* **[!UICONTROL Customer]**: 파일에는 클라이언트의 속성(클라이언트의 속성과 연계됨)에만 트레이트 구현이 1개 이상 있는 활성 사용자가 포함되어 있습니다. [!UICONTROL PID])을 선택합니다. 클라이언트는 이 옵션을 사용하여 *실시간* 대상에 대한 세그먼트 자격 조건.
* **[!UICONTROL Platform]**: 파일에는 ID 동기화 또는 트레이트 실현과 같은 최소 1개의 실시간 상호 작용이 있는 활성 사용자가 포함되어 있습니다 [!DNL Audience Manager] 선택한 기간 동안 클라이언트의 속성(모든 클라이언트 PID와 연결됨)입니다. 클라이언트는 이 옵션을 사용하여 *합계* 대상에 대한 세그먼트 자격 조건.
* **[!UICONTROL Lifetime]**: 파일의 어디에나 표시되는 활성 사용자가 포함되어 있습니다 [!DNL Audience Manager] 대상 생성 이후 클라이언트의 속성.
* **[!UICONTROL Sync Type Lookback Period]**: 를 선택하는 경우 [!UICONTROL Customer] 또는 [!UICONTROL Platform]을(를) 클릭하고 기간을 선택합니다. 파일에는 선택한 기간 동안의 활성 사용자가 포함되어 있습니다.
그런 다음 주문 유형을 선택합니다. 이는 파트너와의 각 아웃바운드 통합의 빈도 및 범위를 나타냅니다. 증분 및 전체 주문 중에서 선택합니다.
* **[!UICONTROL Incremental Scheduled Run]**: 실행할 때마다, [!DNL Audience Manager] 은(는) 이전 아웃바운드 순서 이후 자격을 얻은 순 신규 사용자만 아웃바운드 합니다. 원하는 기간을 선택합니다 [!DNL Audience Manager] 을 클릭하여 증분 동기화 프로세스를 수행합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 절대 안 함을 선택할 수 있습니다.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>첫 번째 증분 순서는 이전 사용자를 대상으로 보내지 않았기 때문에 전체 순서와 동일합니다.

* **[!UICONTROL Full Sync Scheduled Run]**: 실행할 때마다, [!DNL Audience Manager] 대상이 처음 설정된 이후 모든 활성 사용자를 아웃바운드 합니다. 원하는 일정을 선택합니다 [!DNL Audience Manager] 를 사용하여 전체 동기화 프로세스를 수행합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 절대 안 함을 선택할 수 있습니다.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>전체 동기화보다 증분 동기화를 더 자주 사용하는 것이 좋습니다. 증분 동기화는 새 트레이트 실현 또는 ID 동기화가 포함된 파일만 전송합니다. 전체 동기화는 새 구현이나 ID 동기화를 포함하는지 여부에 관계없이 모든 파일을 전송합니다. 다음 항목만 사용 [!UICONTROL Full Sync Scheduled Run] 아웃바운드 데이터 볼륨을 줄이기 위해 클라이언트가 모든 사용자의 전체 복사본을 필요로 하는 경우의 구성.

## 데이터 소스 구성 {#configure-data-sources}

대상 [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] 또는 [!UICONTROL Bulk Segment] 대상, 아래 필드를 채웁니다. 이러한 설정을 사용하면 데이터 소스와 연결된 모든 데이터(선택한 유형에 따라 트레이트, 세그먼트 또는 ID)를 전송할 수 있습니다.

* **[!UICONTROL All Unrestricted First Party Data]**: 모든 자사 데이터 소스를 사용하려면 선택합니다. 이 옵션을 선택하면 [!UICONTROL Available Data Sources] 옵션이 비활성화됩니다.
* **[!UICONTROL Available Data Sources]**: 화살표를 사용하여 데이터 소스를 **[!UICONTROL Available Data Sources]** 및 **[!UICONTROL In File Data Sources]** 상자.

## 저장 및 완료 {#save-and-finalize}

다음 **[!UICONTROL Save]** 모든 필수 필드를 입력한 후 버튼이 활성화됩니다. 클릭 **[!UICONTROL Save]** 대상 생성 프로세스를 완료합니다.

## 회사 대상 삭제 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

대상을 삭제하려면

1. 클릭 **[!UICONTROL Companies]**&#x200B;를 클릭하고 원하는 회사를 찾아 클릭한 다음 **[!UICONTROL Destinations]** 탭.
1. 클릭  ![](assets/icon_delete.png) 다음에서 **[!UICONTROL Actions]** 원하는 대상의 열입니다.
1. 클릭 **[!UICONTROL OK]** 삭제 확인.

>[!NOTE]
>
>매핑된 세그먼트가 있는 대상은 삭제할 수 없습니다.

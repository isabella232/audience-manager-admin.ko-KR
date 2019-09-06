---
description: Audience Manager 대상을 만들고, 편집하고, 삭제합니다.
seo-description: Audience Manager 대상을 만들고, 편집하고, 삭제합니다.
seo-title: 회사 대상 관리
title: 회사 대상 관리
uuid: D 9 A 6 BFB 1-7629-44 E 0-B 7 D 7-ECE 44 F 65 EA 2 B
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 회사 대상 관리 {#manage-company-destinations}

Audience Manager 대상을 만들고, 편집하고, 삭제합니다.

<!-- t_company_destinations.xml -->

자세한 내용은 Audience Manager 사용자 안내서의 [대상을](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) **&#x200B;참조하십시오.

## 회사 대상 만들기 또는 편집 {#create-edit-company-destinations}

섹션을 스크롤하여 새 [!DNL Audience Manager] 대상을 만들거나 기존 대상을 편집하는 방법에 대한 단계별 지침을 참조하십시오.

<!-- create-edit-company-destinations.xml -->

대상을 설정하기 전에 [Experience Cloud 파트너 통합 페이지를](https://wiki.corp.adobe.com/x/mPIMPw) 참조하십시오. 이 페이지에는 [!DNL Audience Manager] 각 파트너 통합에 대해 채워야 하는 특정 정보가 들어 있습니다.

클라이언트가 대상의 대상으로 사용하려는 [!DNL Adobe Media Optimizer][!DNL Audience Manager] 경우 이 설정을 [!DNL Adobe Media Optimizer]설정해야 합니다.

## Navigate to the Destinations Tab {#navigate-destinations}

1. 을 클릭하고 **[!UICONTROL Companies]**&#x200B;원하는 회사를 찾아 클릭하여 [!UICONTROL Profile] 해당 페이지를 표시합니다. 목록 하단의 [!UICONTROL Search] 상자 또는 페이지 매김 컨트롤을 사용하여 원하는 회사를 찾을 수 있습니다. 원하는 열의 헤더를 클릭하여 오름차순 또는 내림차순으로 각 열을 정렬할 수 있습니다.
1. **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 새 대상을 만들려면 **[!UICONTROL Add Destination]**&#x200B;을 클릭합니다. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## 기본 설정 {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]:** (필수) 이 대상의 이름을 지정합니다.
* **[!UICONTROL Description]:** 이 대상에 대한 설명 정보를 지정합니다.
* **[!UICONTROL Type]:** (필수) 원하는 대상 유형을 선택합니다.
   * **[!UICONTROL Bulk ID]**: 여러 플랫폼에서 ID 동기화
   * **[!UICONTROL Bulk Trait]**: 트레이트 정보를 다른 플랫폼으로 일괄 전송합니다.
   * **[!UICONTROL Bulk Segment]**: 세그먼트 정보를 다른 플랫폼으로 일괄 전송합니다.
   * **[!UICONTROL S2S]**: 서버 간 타겟을 사용하여 실시간 데이터를 다른 플랫폼으로 전송할 수 있습니다.
* **[!UICONTROL Auto-Fill Destination Mapping]:** ( [!UICONTROL S2S] 전용) 옵션을 선택합니다.
   * **[!UICONTROL Segment ID]:** 이 설정을 선택하면 대상 값 매핑이 [!DNL Audience Manager] 세그먼트 ID로 채워집니다.
   * **[!UICONTROL Integration Code Value]:** 이 설정을 선택하면 대상 값 매핑이 [!DNL Audience Manager] 세그먼트 통합 코드로 채워집니다.
* **[!UICONTROL User ID Key]:** (필수) 드롭다운 목록에서 이 대상에 대해 원하는 사용자 ID 키를 선택합니다.

이 ID는 마스터 데이터 소스 ID로 사용됩니다. 이렇게 하면 파일에 묶어질 사용자 ID가 결정됩니다.

>[!NOTE]
>
>[!UICONTROL Bulk ID] 대상 유형의 경우 [!DNL Audience Manager][!UICONTROL User ID] 또는 [!DNL Adobe Experience Cloud] ID를 사용할 수 없습니다.

데이터 소스 ID ( [!UICONTROL DPID]) 가 드롭다운 목록에 표시되지 않으면 데이터 소스 설정 페이지의 데이터 소스 수준에서 **[!UICONTROL Outbound]**[확인란을 선택해야](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)합니다.

* **[!UICONTROL Target Data Source]:** (필수) 드롭다운 목록에서 이 대상에 대해 원하는 데이터 소스를 선택합니다. 이 설정을 사용하면 분리된 데이터에 레이블을 지정할 수 있으므로 클라이언트의 측에서 별도의 시스템에 들어갈 수 있습니다.
* **[!UICONTROL Foreign Account ID]:** 이 대상에 대한 외부 계정 ID를 지정합니다. 이 값은 이 경계를 벗어난 데이터에 대한 수신자 시스템의 ID 값입니다.
* **[!UICONTROL Outbound Sample Rate Denominator]:** 반환된 데이터의 총 금액을 알 수 없는 경우 이 설정을 사용하여 전체 금액이 아닌 샘플 금액만 반환합니다. 여기에서 숫자를 조정하여 데이터의 일부를 표시합니다 (예:' 100 ' 값이 일정한 양의 데이터의 1/100 반환, 값 ' 10 ' 는 일정한 양의 데이터 1/10 반환). 기본값은 모든 데이터를 반환하는 ' 1 ' 입니다.

## Realtime 데이터 (S 2 S 대상의 경우) {#realtime-s2s}

[!UICONTROL S2S] 대상을 만드는 경우 아래 필드를 채웁니다.

**[!UICONTROL Servers]**: 이 대상에 대해 원하는 `HTTP` 서버를 선택합니다.
**[!UICONTROL Format]**: 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!UICONTROL HTTP only].

>[!NOTE]
>
>화면상의 끄기/ [!DNL S2S] 슬라이더를 사용하여 [!UICONTROL Realtime] 하나 또는 [!UICONTROL Batch] 여러 대상을 활성화하거나 비활성화할 수 있습니다. 두 옵션을 모두 비활성화할 수는 없습니다.

## 일괄 데이터 {#batch-data}

for [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] or [!UICONTROL Bulk Segment] destination, filled in the fields below:

* **[!UICONTROL Protocol]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 프로토콜을 선택합니다.
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 서버를 선택합니다.
* **[!UICONTROL Format]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!DNL HTTP] 또는 파일 유형을 선택합니다.
* **[!UICONTROL Sync Type]**: (필수) 이 대상에 대해 원하는 동기화 유형을 선택합니다. 이것은 클라이언트가 아웃바운드 주문에 포함하려는 사용자 활동 수준을 나타냅니다. 클라이언트가 속성에서만 세그먼트 자격 조건을 분석하려는 **[!UICONTROL Customer]** 경우에 선택합니다. 모든 **[!UICONTROL Platform]**[!DNL Audience Manager] 고객에 걸쳐 오프라인 활동에서 세그먼트 자격을 포함하려는 경우 선택합니다.
* **[!UICONTROL Customer]**: 파일에는 선택한 기간 동안 클라이언트의 속성 (클라이언트와 연관된) 에서만 최소 1 개의 특성 구현이 있는 [!UICONTROL PID]활성 사용자가 포함됩니다. 클라이언트는 이 옵션을 *사용하여 실시간* 세그먼트 자격을 대상으로 발송해야 합니다.
* **[!UICONTROL Platform]**: 파일에는 선택한 기간 동안 모든 [!DNL Audience Manager] 클라이언트의 속성 (모든 클라이언트 PIDS와 연관된) 에 관계없이, 최소 1 개의 실시간 상호 작용이 있는 활성 사용자가 포함됩니다. 클라이언트는 이 옵션을 사용하여 *전체* 세그먼트 자격 조건을 대상으로 아웃바운드해야 합니다.
* **[!UICONTROL Lifetime]**: 파일에는 대상을 만든 이후 [!DNL Audience Manager] 모든 클라이언트의 속성에서 볼 수 있는 활성 사용자가 포함됩니다.
* **[!UICONTROL Sync Type Lookback Period]**: 기간을 선택하거나 [!UICONTROL Customer][!UICONTROL Platform]선택한 경우 기간을 선택합니다. 파일에는 선택한 기간 동안 활성 사용자가 포함됩니다.
그런 다음 주문 유형을 선택합니다. 이것은 파트너와 각 아웃바운드 통합의 빈도 및 범위를 나타냅니다. 증분 및 전체 주문 중에서 선택합니다.
* **[!UICONTROL Incremental Scheduled Run]**: Each run with each run, [!DNL Audience Manager] will only outbound the net new users qualified since the previous outbound order. 증분 동기화 프로세스를 [!DNL Audience Manager] 수행하려는 기간을 선택합니다. 예를 들어, 24 시간, 7 일, 30 일 또는 절대로 사용하지 않을 수 있습니다.

>[!NOTE] {importance = "high"}
>
>첫 번째 증분 주문은 이전 사용자를 대상으로 보내지 않았기 때문에 전체 주문과 같습니다.

* **[!UICONTROL Full Sync Scheduled Run]**: Each run with each run, [!DNL Audience Manager] will outbound all active users since the destination was first set. 전체 동기화 프로세스를 수행하는 [!DNL Audience Manager] 데 사용할 원하는 일정을 선택합니다. 예를 들어, 24 시간, 7 일, 30 일 또는 절대로 사용하지 않을 수 있습니다.

>[!NOTE] {importance = "high"}
>
>전체 동기화보다 증분 동기화를 사용하는 것이 좋습니다. 증분 동기화는 새로운 특성 실현 또는 ID 동기화가 포함된 파일만 전송합니다. 전체 동기화는 새로운 개념이나 ID 동기화 여부에 관계없이 모든 파일을 전송합니다. 아웃바운드 데이터 볼륨을 줄이기 위해 클라이언트가 모든 사용자의 전체 복사본이 필요할 때에만 [!UICONTROL Full Sync Scheduled Run] 구성을 사용합니다.

## 데이터 소스 구성 {#configure-data-sources}

for [!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] or [!UICONTROL Bulk Segment] destination, filled in the fields below. 이러한 설정을 사용하면 데이터 소스와 연결된 모든 데이터 (선택한 유형에 따라 트레이트, 세그먼트 또는 ID) 를 보낼 수 있습니다.

* **[!UICONTROL All Unrestricted First Party Data]**: 모든 퍼스트 파티 데이터 소스를 사용하려면 선택합니다. 이 옵션을 선택하면 [!UICONTROL Available Data Sources] 옵션이 비활성화됩니다.
* **[!UICONTROL Available Data Sources]**: 화살표를 사용하여 **[!UICONTROL Available Data Sources]** AND **[!UICONTROL In File Data Sources]** 상자 간에 데이터 소스를 이동합니다.

## 저장 및 마무리 {#save-and-finalize}

필요한 모든 필드를 채운 후 **[!UICONTROL Save]** 단추가 활성화됩니다. 을 클릭하여 **[!UICONTROL Save]** 대상 만들기 프로세스를 완료합니다.

## 회사 대상 삭제 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

대상을 삭제하려면 다음을 수행하십시오.

1. 을 클릭하고 **[!UICONTROL Companies]**&#x200B;원하는 회사를 찾아 클릭한 다음 **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 원하는 ![](assets/icon_delete.png) 대상의 **[!UICONTROL Actions]** 열을 클릭합니다.
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>세그먼트가 매핑된 세그먼트가 있으면 대상을 삭제할 수 없습니다.
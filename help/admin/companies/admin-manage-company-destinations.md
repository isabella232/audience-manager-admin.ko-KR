---
description: Audience Manager 대상을 만들고, 편집하고, 삭제합니다.
seo-description: Audience Manager 대상을 만들고, 편집하고, 삭제합니다.
seo-title: 회사 대상 관리
title: 회사 대상 관리
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: f247457004a624297ddc8847dd256dbb7d8da418
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 1%

---


# 회사 대상 관리 {#manage-company-destinations}

Audience Manager 대상을 만들고, 편집하고, 삭제합니다.

<!-- t_company_destinations.xml -->

자세한 내용은 *Audience Manager 사용자 안내서*&#x200B;의 [대상](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html)을 참조하십시오.

## 회사 대상 만들기 또는 편집 {#create-edit-company-destinations}

섹션을 스크롤하여 새 [!DNL Audience Manager] 대상을 만들거나 기존 대상을 편집하는 방법에 대한 단계별 지침을 확인하십시오.

<!-- create-edit-company-destinations.xml -->

대상을 설정하기 전에 [Experience Cloud 파트너 통합 페이지](https://wiki.corp.adobe.com/x/mPIMPw)를 방문하십시오. 이 페이지에는 각 [!DNL Audience Manager] 파트너 통합에 대해 입력해야 하는 특정 정보가 포함되어 있습니다.

클라이언트가 [!DNL Audience Manager]의 대상으로 [!DNL Adobe Media Optimizer]을(를) 사용하려면 [!DNL Adobe Media Optimizer]에서 설정해야 합니다.

## 대상 탭 {#navigate-destinations}으로 이동합니다.

1. **[!UICONTROL Companies]**&#x200B;을 클릭한 다음 원하는 회사를 찾아 클릭하여 [!UICONTROL Profile] 페이지를 표시합니다. 목록 맨 아래의 [!UICONTROL Search] 상자나 페이지 매김 컨트롤을 사용하여 원하는 회사를 찾을 수 있습니다. 원하는 열의 헤더를 클릭하여 각 열을 오름차순이나 내림차순으로 정렬할 수 있습니다.
1. **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 새 대상을 만들려면 **[!UICONTROL Add Destination]**&#x200B;을 클릭합니다. 기존 대상을 편집하려면 **[!UICONTROL Name]** 열에서 대상의 이름을 클릭합니다.

## 기본 설정 {#basic-settings}

**[!UICONTROL Basic Settings]** 창의 필드를 채웁니다.

* **[!UICONTROL Name]:** (필수) 이 대상의 이름을 지정합니다.
* **[!UICONTROL Description]:** 이 대상에 대한 설명 정보를 지정합니다.
* **[!UICONTROL Type]:** (필수) 원하는 대상 유형을 선택합니다.
   * **[!UICONTROL Bulk ID]**:다른 플랫폼 간 ID 동기화
   * **[!UICONTROL Bulk Trait]**:특성 정보를 여러 플랫폼으로 일괄 전송
   * **[!UICONTROL Bulk Segment]**:세그먼트 정보를 여러 플랫폼으로 일괄 전송
   * **[!UICONTROL S2S]**:서버 간 대상을 사용하여 데이터를 실시간으로 전송하고 여러 플랫폼에 일괄적으로 전송할 수 있습니다.
* **[!UICONTROL Auto-Fill Destination Mapping]:** (  [!UICONTROL S2S] 전용) 옵션을 선택합니다.
   * **[!UICONTROL Segment ID]:** 이 설정을 선택하면 대상 값 매핑이 세그먼트  [!DNL Audience Manager] ID로 채워집니다.
   * **[!UICONTROL Integration Code Value]:** 이 설정을 선택하면 대상 값 매핑이  [!DNL Audience Manager] 세그먼트 통합 코드로 채워집니다.
* **[!UICONTROL User ID Key]:** (필수) 드롭다운 목록에서 이 대상에 대해 원하는 사용자 ID 키를 선택합니다.

이 ID는 마스터 데이터 소스 ID로 사용됩니다. 이 값은 파일에서 경계를 해제할 사용자 ID를 결정합니다.

>[!NOTE]
>
>[!UICONTROL Bulk ID] 대상 유형의 경우 [!DNL Audience Manager] [!UICONTROL User ID] 또는 [!DNL Adobe Experience Cloud] ID를 사용할 수 없습니다.

데이터 소스 ID( [!UICONTROL DPID])가 드롭다운 목록에 표시되지 않으면 [데이터 소스 설정 페이지](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html)의 데이터 소스 수준에서 **[!UICONTROL Outbound]** 확인란을 선택해야 합니다.

* **[!UICONTROL Target Data Source]:** (필수) 드롭다운 목록에서 이 대상에 대해 원하는 데이터 소스를 선택합니다. 이 설정은 클라이언트의 개별 시스템에 데이터를 수집할 수 있도록 하는 경계 데이터 레이블을 활성화합니다.
* **[!UICONTROL Foreign Account ID]:** 이 대상에 대한 외래 계정 ID를 지정합니다. 이 경계 데이터의 수신자 시스템에서 식별 값입니다.
* **[!UICONTROL Outbound Sample Rate Denominator]:** 반환된 데이터의 총량을 알 수 없는 경우 이 설정을 사용하여 전체 양이 아닌 샘플 양의 데이터만 반환합니다. 데이터의 일부를 나타내도록 여기에서 숫자를 조정합니다(예: &#39;100&#39; 값은 정규 데이터 금액의 100분의 1을 반환하고, &#39;10&#39; 값은 일반 데이터의 1/10을 반환합니다.). 기본값은 모든 데이터를 반환하는 &#39;1&#39;입니다.

## 실시간 데이터(S2S 대상) {#realtime-s2s}

[!UICONTROL S2S] 대상을 만드는 경우 아래 필드를 입력합니다.

**[!UICONTROL Servers]**:이 대상에 대해 원하는  `HTTP` 서버를 선택합니다.
**[!UICONTROL Format]**:드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!UICONTROL HTTP only].

>[!NOTE]
>
>[!DNL S2S]만 화면의 해제/켜기 슬라이더를 사용하여 [!UICONTROL Realtime] 또는 [!UICONTROL Batch] 대상을 활성화하거나 비활성화할 수 있습니다. 두 옵션을 모두 비활성화할 수 없습니다.

## 배치 데이터 {#batch-data}

[!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] 또는 [!UICONTROL Bulk Segment] 대상의 경우 아래 필드를 채웁니다.

* **[!UICONTROL Protocol]**:(필수) 드롭다운 목록에서 이 대상에 대해 원하는 프로토콜을 선택합니다.
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:(필수) 드롭다운 목록에서 이 대상에 대해 원하는 서버를 선택합니다.
* **[!UICONTROL Format]**:(필수) 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!DNL HTTP] 또는 파일 유형을 선택합니다.
* **[!UICONTROL Sync Type]**:(필수) 이 대상에 대해 원하는 동기화 유형을 선택합니다. 이것은 클라이언트가 아웃바운드 주문에 포함하려는 사용자 활동 수준을 나타냅니다. 클라이언트가 속성에서 세그먼트 자격 조건을 분석하는 경우에만 관심이 있는 경우 **[!UICONTROL Customer]**&#x200B;을 선택합니다. 모든 [!DNL Audience Manager] 고객의 외부 활동에서 세그먼트 자격 조건을 포함하려면 **[!UICONTROL Platform]**&#x200B;을 선택합니다.
* **[!UICONTROL Customer]**:파일에는 선택한 기간 동안 클라이언트의 속성(클라이언트 속성과 연관된)에만 최소 1개의 트레이트 구현이 있는 활성 사용자 [!UICONTROL PID]가 포함되어 있습니다. 클라이언트는 이 옵션을 사용하여 해당 *실시간* 세그먼트 자격 조건을 대상으로 발송해야 합니다.
* **[!UICONTROL Platform]**:파일에는 선택한 기간 동안 모든  [!DNL Audience Manager] 클라이언트의 속성(모든 클라이언트 PID와 관련)에 관계없이 ID를 동기화하거나 트레이트 실현과 같은 최소 1개의 실시간 상호 작용을 가진 활성 사용자가 포함되어 있습니다. 클라이언트는 이 옵션을 사용하여 해당 *총* 세그먼트 자격 조건을 대상으로 발송해야 합니다.
* **[!UICONTROL Lifetime]**:파일에는 대상을 만든 이후 모든  [!DNL Audience Manager] 클라이언트의 속성에 걸쳐 표시되는 활성 사용자가 포함됩니다.
* **[!UICONTROL Sync Type Lookback Period]**:또는 [!UICONTROL Customer] 를 선택한  [!UICONTROL Platform]경우 기간을 선택합니다. 파일에는 선택한 기간에 대한 활성 사용자가 포함됩니다.
그런 다음 주문 유형을 선택합니다. 이는 파트너와의 각 아웃바운드 통합의 빈도 및 범위를 나타냅니다. 증분 주문 및 전체 주문 중에서 선택합니다.
* **[!UICONTROL Incremental Scheduled Run]**:각 실행 시 이전 아웃바운드 주문 이후 자격이 있는 순 새 사용자만  [!DNL Audience Manager] 아웃바운드합니다. 증분 동기화 프로세스를 수행할 원하는 기간을 선택합니다. [!DNL Audience Manager] 예를 들어 24시간마다, 7일마다, 30일마다 또는 선택하지 않을 수 있습니다.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>이전에 대상에 보낸 사용자가 없기 때문에 첫 번째 증분 주문은 전체 주문과 같습니다.

* **[!UICONTROL Full Sync Scheduled Run]**:각 실행 시 대상이 처음 설정된 이후 모든 활성 사용자가  [!DNL Audience Manager] 아웃바운드됩니다. 전체 동기화 프로세스를 수행하는 데 사용할 [!DNL Audience Manager] 일정을 선택합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 선택하지 않을 수 있습니다.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>전체 동기화보다 증분 동기화를 더 자주 사용하는 것이 좋습니다. 증분 동기화는 새로운 특성 인식 또는 ID 동기화가 포함된 파일만 전송합니다. 전체 동기화는 새로운 관계 또는 ID 동기화가 포함되어 있는지 여부에 관계없이 모든 파일을 전송합니다. 클라이언트가 모든 사용자의 전체 복사본을 필요로 하는 경우에만 아웃바운드 데이터 볼륨을 줄이기 위해 [!UICONTROL Full Sync Scheduled Run] 구성을 사용하십시오.

## 데이터 소스 구성 {#configure-data-sources}

[!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] 또는 [!UICONTROL Bulk Segment] 대상의 경우 아래 필드를 채웁니다. 이러한 설정을 사용하면 데이터 소스와 연관된 모든 데이터(선택한 유형을 기준으로 트레이트, 세그먼트 또는 ID)를 전송할 수 있습니다.

* **[!UICONTROL All Unrestricted First Party Data]**:모든 자사 데이터 소스를 사용하려면 선택합니다. 이 옵션을 선택하면 [!UICONTROL Available Data Sources] 옵션이 비활성화됩니다.
* **[!UICONTROL Available Data Sources]**:화살표를 사용하여  **[!UICONTROL Available Data Sources]** 및  **[!UICONTROL In File Data Sources]** 상자 간에 데이터 소스를 이동할 수 있습니다.

## {#save-and-finalize} 저장 및 완료

필요한 모든 필드를 채운 후 **[!UICONTROL Save]** 단추가 활성화됩니다. 대상 만들기 프로세스를 완료하려면 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

## 회사 대상 삭제 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

대상을 삭제하려면

1. **[!UICONTROL Companies]**&#x200B;을 클릭하고 원하는 회사를 찾아 클릭한 다음 **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 원하는 대상의 **[!UICONTROL Actions]** 열에서 ![](assets/icon_delete.png)을 클릭합니다.
1. **[!UICONTROL OK]**&#x200B;을 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>대상에 매핑된 세그먼트가 있으면 대상을 삭제할 수 없습니다.
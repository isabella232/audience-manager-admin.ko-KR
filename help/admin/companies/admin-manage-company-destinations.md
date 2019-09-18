---
description: Audience Manager 대상 만들기, 편집 및 삭제
seo-description: Audience Manager 대상 만들기, 편집 및 삭제
seo-title: ' 회사 대상 관리'
title: ' 회사 대상 관리'
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# 회사 대상 관리 {#manage-company-destinations}

Audience Manager 대상 만들기, 편집 및 삭제

<!-- t_company_destinations.xml -->

자세한 내용은 Audience [Manager](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html) 사용 안내서의 *대상을 참조하십시오*.

## 회사 대상 만들기 또는 편집 {#create-edit-company-destinations}

섹션을 스크롤하여 새 [!DNL Audience Manager] 대상을 만들거나 기존 대상을 편집하는 방법에 대한 단계별 지침을 확인하십시오.

<!-- create-edit-company-destinations.xml -->

대상을 [설정하기 전에 Experience Cloud 파트너 통합 페이지를](https://wiki.corp.adobe.com/x/mPIMPw) 방문하십시오. 이 페이지에는 각 [!DNL Audience Manager] 파트너 통합에 대해 입력해야 하는 특정 정보가 포함되어 있습니다.

클라이언트가 에서 [!DNL Adobe Media Optimizer] 대상으로 사용하려는 [!DNL Audience Manager] 경우 에서 설정해야 합니다 [!DNL Adobe Media Optimizer].

## Navigate to the Destinations Tab {#navigate-destinations}

1. 을 **[!UICONTROL Companies]**&#x200B;클릭한 다음 원하는 회사를 찾아 클릭하여 해당 [!UICONTROL Profile] 페이지를 표시합니다. 목록 맨 아래의 [!UICONTROL Search] 상자나 페이지 매김 컨트롤을 사용하여 원하는 회사를 찾을 수 있습니다. 원하는 열의 머리글을 클릭하여 각 열을 오름차순이나 내림차순으로 정렬할 수 있습니다.
1. Click the **[!UICONTROL Destinations]** tab.
1. 새 대상을 만들려면 을 클릭합니다 **[!UICONTROL Add Destination]**. To edit an existing destination, click the destination's name in the **[!UICONTROL Name]** column.

## 기본 설정 {#basic-settings}

Fill in the fields in the **[!UICONTROL Basic Settings]** window.

* **[!UICONTROL Name]** :(필수) 이 대상의 이름을 지정합니다.
* **[!UICONTROL Description]** :이 대상에 대한 설명 정보를 지정합니다.
* **[!UICONTROL Type]** :(필수) 원하는 대상 유형을 선택합니다.
   * **[!UICONTROL Bulk ID]**:다른 플랫폼 간 ID 동기화
   * **[!UICONTROL Bulk Trait]**:트레이트 정보를 여러 플랫폼으로 일괄 전송
   * **[!UICONTROL Bulk Segment]**:세그먼트 정보를 여러 플랫폼으로 일괄 전송
   * **[!UICONTROL S2S]**:서버 간 대상을 사용하여 데이터를 실시간으로 전송하고 여러 플랫폼에 일괄 처리할 수 있습니다.
* **[!UICONTROL Auto-Fill Destination Mapping]** :( [!UICONTROL S2S] 전용) 옵션을 선택합니다.
   * **[!UICONTROL Segment ID]** :이 설정을 선택하면 대상 값 매핑이 세그먼트 ID로 [!DNL Audience Manager] 채워집니다.
   * **[!UICONTROL Integration Code Value]** :이 설정을 선택하면 대상 값 매핑이 세그먼트 통합 코드로 [!DNL Audience Manager] 채워집니다.
* **[!UICONTROL User ID Key]** :(필수) 드롭다운 목록에서 이 대상에 대해 원하는 사용자 ID 키를 선택합니다.

이 ID 파섹 그러면 파일에서 경계를 해제할 사용자 ID가 결정됩니다.

>[!NOTE]
>
>대상 [!UICONTROL Bulk ID] 유형의 경우 [!DNL Audience Manager] 또는 [!UICONTROL User ID] ID를 사용할 수 [!DNL Adobe Experience Cloud] 없습니다.

데이터 소스 ID( [!UICONTROL DPID])가 드롭다운 목록에 표시되지 않으면 데이터 소스 설정 페이지의 **[!UICONTROL Outbound]** 데이터 소스 수준에서 [확인란을 선택해야 합니다](https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/data-sources/manage-datasources.html).

* **[!UICONTROL Target Data Source]** :(필수) 드롭다운 목록에서 이 대상에 대해 원하는 데이터 소스를 선택합니다. 이 설정을 사용하면 아웃바운드된 데이터에 대한 레이블을 지정할 수 있으며, 이를 통해 클라이언트 측에서 별도의 시스템에 데이터를 통합할 수 있습니다.
* **[!UICONTROL Foreign Account ID]** :이 대상에 대한 외래 계정 ID를 지정합니다. 이것은 이 아웃바운드 데이터에 대한 수신자 시스템의 식별 값입니다.
* **[!UICONTROL Outbound Sample Rate Denominator]** :반환된 데이터의 전체 양을 알 수 없는 경우 이 설정을 사용하여 전체 금액이 아닌 샘플 양의 데이터만 반환합니다. 여기에서 숫자를 조정하여 데이터의 일부를 표시합니다(예를 들어 '100' 값은 정규 데이터의 1/100을 반환하고 '10' 값은 정규 데이터의 1/10을 반환합니다). 기본값은 모든 데이터를 반환하는 '1'입니다.

## 실시간 데이터(S2S 대상) {#realtime-s2s}

대상을 만드는 [!UICONTROL S2S] 경우 아래 필드를 채웁니다.

**[!UICONTROL Servers]**:이 대상에 대해 원하는 `HTTP` 서버를 선택합니다.
**[!UICONTROL Format]**:드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다. [!UICONTROL HTTP only]Adobe

>[!NOTE]
>
>의 [!DNL S2S] 경우 화면상의 꺼짐/켜짐 슬라이더를 사용하여 [!UICONTROL Realtime] 또는 [!UICONTROL Batch] 대상을 활성화하거나 비활성화할 수 있습니다. 두 옵션을 모두 비활성화할 수 없습니다.

## 일괄 처리 데이터 {#batch-data}

목적지 [!UICONTROL Bulk ID]또는 [!UICONTROL Bulk Trait] [!UICONTROL Bulk Segment] 목적지의 경우 아래 필드를 채우십시오.

* **[!UICONTROL Protocol]**:(필수) 드롭다운 목록에서 이 대상에 대해 원하는 프로토콜을 선택합니다.
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**:(필수) 드롭다운 목록에서 이 대상에 대해 원하는 서버를 선택합니다.
* **[!UICONTROL Format]**:(필수) 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다.또는 위에서 선택한 프로토콜에 따라 [!DNL HTTP] 파일 유형을 지정할 수 있습니다.
* **[!UICONTROL Sync Type]**:(필수) 이 대상에 대해 원하는 동기화 유형을 선택합니다. 이는 클라이언트가 아웃바운드 주문에 포함하려는 사용자 활동 수준을 나타냅니다. 클라이언트가 속성에서 세그먼트 자격 조건을 분석하는 데만 관심이 있는 **[!UICONTROL Customer]** 경우 선택합니다. 모든 **[!UICONTROL Platform]** [!DNL Audience Manager] 고객의 오프라인 활동에서 세그먼트 자격 조건을 포함하려는 경우 선택합니다.
* **[!UICONTROL Customer]**:파일에는 선택한 기간 동안 클라이언트의 속성(클라이언트 속성과 연관됨)에서만 최소 1개의 트레이트 구현이 있는 활성 사용자가 포함되어 [!UICONTROL PID]있습니다. 클라이언트는 이 옵션을 사용하여 *실시간* 세그먼트 자격 조건을 대상으로 발송해야 합니다.
* **[!UICONTROL Platform]**:파일에는 선택한 기간 동안 모든 클라이언트의 속성(모든 클라이언트 PID와 연관된)에 관계없이 ID 동기화 또는 트레이트 실현과 같은 실시간 상호 작용을 가진 활성 사용자가 포함되어 있습니다. [!DNL Audience Manager] 클라이언트는 이 옵션을 사용하여 *총* 세그먼트 자격 조건을 대상으로 발송해야 합니다.
* **[!UICONTROL Lifetime]**:파일은 대상을 만든 이후 모든 [!DNL Audience Manager] 클라이언트의 속성에서 볼 수 있는 활성 사용자를 포함합니다.
* **[!UICONTROL Sync Type Lookback Period]**:또는 를 선택한 [!UICONTROL Customer] 경우 기간을 [!UICONTROL Platform]선택합니다. 파일에는 선택한 기간 동안 활성 사용자가 포함됩니다.
그런 다음 주문 유형을 선택합니다. 이는 파트너와 각 아웃바운드 통합의 빈도 및 범위를 나타냅니다. 증분 주문 및 전체 주문 중에서 선택합니다.
* **[!UICONTROL Incremental Scheduled Run]**:각 실행에서는 이전 아웃바운드 주문 이후 자격이 있는 순 신규 사용자만 [!DNL Audience Manager] 아웃바운드합니다. 증분 동기화 프로세스를 [!DNL Audience Manager] 수행할 기간을 선택합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 선택하지 않을 수 있습니다.

>[!NOTE] {importance="high"}
>
>이전 사용자가 대상에 전송되지 않았으므로 최초 증분 주문은 전체 주문과 같습니다.

* **[!UICONTROL Full Sync Scheduled Run]**:각 실행에서는 대상이 처음 설정된 이후 모든 활성 사용자가 아웃바운드됩니다. [!DNL Audience Manager] 전체 동기화 프로세스를 [!DNL Audience Manager] 수행하는 데 사용할 일정을 선택합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 선택하지 않을 수 있습니다.

>[!NOTE] {importance="high"}
>
>전체 동기화보다 증가분 동기화를 더 자주 사용하는 것이 좋습니다. Incremental은 새로운 트레이트 실현이나 ID 동기화가 포함된 파일만 전송합니다. 전체 동기화는 새로운 관계 또는 ID 동기화 여부에 관계없이 모든 파일을 전송합니다. 클라이언트가 모든 사용자의 전체 복사본을 필요로 하는 경우에만 [!UICONTROL Full Sync Scheduled Run] 구성을 사용하여 아웃바운드 데이터 볼륨을 줄입니다.

## 데이터 소스 구성 {#configure-data-sources}

또는 [!UICONTROL Bulk ID]목적지의 경우 아래 필드를 [!UICONTROL Bulk Trait] [!UICONTROL Bulk Segment] 입력합니다. 이러한 설정을 사용하면 데이터 소스와 관련된 모든 데이터(선택한 유형을 기준으로 트레이트, 세그먼트 또는 ID)를 전송할 수 있습니다.

* **[!UICONTROL All Unrestricted First Party Data]**:모든 자사 데이터 소스를 사용하려면 선택합니다. 이 옵션을 선택하면 [!UICONTROL Available Data Sources] 옵션이 비활성화됩니다.
* **[!UICONTROL Available Data Sources]**:화살표를 사용하여 **[!UICONTROL Available Data Sources]** 및 **[!UICONTROL In File Data Sources]** 상자 간에 데이터 소스를 이동할 수 있습니다.

## 저장 및 완료 {#save-and-finalize}

모든 필수 필드를 채운 후 **[!UICONTROL Save]** 단추가 활성화됩니다. 을 **[!UICONTROL Save]** 클릭하여 대상 만들기 프로세스를 완료합니다.

## 회사 대상 삭제 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

대상을 삭제하려면 다음을 수행합니다.

1. 을 **[!UICONTROL Companies]**&#x200B;클릭하고 원하는 회사를 찾아 클릭한 다음 **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 원하는 ![](assets/icon_delete.png) 대상의 **[!UICONTROL Actions]** 열을 클릭합니다.
1. Click **[!UICONTROL OK]** to confirm the deletion.

>[!NOTE]
>
>대상에 매핑된 세그먼트가 있으면 대상을 삭제할 수 없습니다.
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

자세한 내용은 *Audience Manager 사용 안내서*&#x200B;에서 [대상](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html)을 참조하십시오.

## 회사 대상 만들기 또는 편집 {#create-edit-company-destinations}

섹션을 스크롤하여 새 [!DNL Audience Manager] 대상을 만들거나 기존 대상을 편집하는 방법에 대한 단계별 지침을 제공합니다.

<!-- create-edit-company-destinations.xml -->

대상을 설정하기 전에 [Experience Cloud 파트너 통합 페이지](https://wiki.corp.adobe.com/x/mPIMPw)를 방문하십시오. 페이지에는 각 [!DNL Audience Manager] 파트너 통합에 대해 입력해야 하는 특정 정보가 포함되어 있습니다.

클라이언트가 [!DNL Audience Manager]에서 [!DNL Adobe Media Optimizer]을 대상으로 사용하려는 경우 [!DNL Adobe Media Optimizer]에서 설정해야 합니다.

## 대상 탭으로 이동합니다. {#navigate-destinations}

1. **[!UICONTROL Companies]** 을 클릭한 다음 원하는 회사를 찾아 클릭하여 [!UICONTROL Profile] 페이지를 표시합니다. 목록 하단의 페이지 매김 컨트롤을 사용하여 원하는 회사를 찾을 수 있습니다. [!UICONTROL Search] 원하는 열의 헤더를 클릭하여 각 열을 오름차순이나 내림차순으로 정렬할 수 있습니다.
1. **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 새 대상을 만들려면 **[!UICONTROL Add Destination]** 을 클릭합니다. 기존 대상을 편집하려면 **[!UICONTROL Name]** 열에서 대상 이름을 클릭합니다.

## 기본 설정 {#basic-settings}

**[!UICONTROL Basic Settings]** 창의 필드를 채웁니다.

* **[!UICONTROL Name]:**  (필수) 이 대상의 이름을 지정합니다.
* **[!UICONTROL Description]:** 이 대상에 대한 수사적 정보를 지정합니다.
* **[!UICONTROL Type]:**  (필수) 원하는 대상 유형을 선택합니다.
   * **[!UICONTROL Bulk ID]**: 다른 플랫폼 간에 ID 동기화.
   * **[!UICONTROL Bulk Trait]**: 트레이트 정보를 여러 플랫폼으로 일괄적으로 전송합니다.
   * **[!UICONTROL Bulk Segment]**: 세그먼트 정보를 다른 플랫폼으로 일괄적으로 전송합니다.
   * **[!UICONTROL S2S]**: 서버 간 대상을 사용하여 다양한 플랫폼에 실시간 및 배치 데이터를 전송합니다.
* **[!UICONTROL Auto-Fill Destination Mapping]:** (  [!UICONTROL S2S] 전용) 옵션을 선택합니다.
   * **[!UICONTROL Segment ID]** : 이 설정을 선택하면 대상 값 매핑이 세그먼트  [!DNL Audience Manager] ID로 채워집니다.
   * **[!UICONTROL Integration Code Value]** : 이 설정을 선택하면 대상 값 매핑이 세그먼트  [!DNL Audience Manager] 통합 코드로 채워집니다.
* **[!UICONTROL User ID Key]**  : (필수) 드롭다운 목록에서 이 대상에 대해 원하는 사용자 ID 키를 선택합니다.

이 ID는 마스터 데이터 소스 ID로 사용됩니다. 이에 따라 파일에서 출력할 사용자 ID가 결정됩니다.

>[!NOTE]
>
>[!UICONTROL Bulk ID] 대상 유형의 경우 [!DNL Audience Manager] [!UICONTROL User ID] 또는 [!DNL Adobe Experience Cloud] ID를 사용할 수 없습니다.

데이터 소스 ID( [!UICONTROL DPID])가 드롭다운 목록에 표시되지 않으면 [데이터 소스 설정 페이지](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html)의 데이터 소스 수준에서 **[!UICONTROL Outbound]** 확인란을 선택해야 합니다.

* **[!UICONTROL Target Data Source]**  : (필수) 드롭다운 목록에서 이 대상에 대해 원하는 데이터 소스를 선택합니다. 이 설정을 사용하면 아웃바운드 데이터에 레이블을 지정할 수 있으며 이를 통해 클라이언트 측의 별도의 시스템으로 수집할 수 있습니다.
* **[!UICONTROL Foreign Account ID]** : 이 대상에 대한 외부 계정 ID를 지정합니다. 이것은 이러한 아웃바운드 데이터에 대한 수신자 시스템의 식별 값입니다.
* **[!UICONTROL Outbound Sample Rate Denominator]** : 반환된 데이터의 총 양을 알 수 없는 경우 이 설정을 사용하여 전체 양이 아닌 샘플 양의 데이터만 반환합니다. 데이터의 일부를 나타내도록 여기에서 수를 조정합니다(예: &#39;100&#39; 값은 일반 데이터 양의 1/100을 반환하고 &#39;10&#39; 값은 일반 데이터 양의 1/10을 반환합니다.). 기본값은 &#39;1&#39;이며, 모든 데이터를 반환합니다.

## 실시간 데이터(S2S 대상) {#realtime-s2s}

[!UICONTROL S2S] 대상을 만드는 경우 아래 필드를 채우십시오.

**[!UICONTROL Servers]**: 이 대상에  `HTTP` 대해 원하는 서버를 선택합니다.
**[!UICONTROL Format]**: 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다.  [!UICONTROL HTTP only].

>[!NOTE]
>
>[!DNL S2S]의 경우에만 화면 해제/설정 슬라이더를 사용하여 [!UICONTROL Realtime] 또는 [!UICONTROL Batch] 대상을 활성화하거나 비활성화할 수 있습니다. 두 옵션을 모두 비활성화할 수 없습니다.

## 배치 데이터 {#batch-data}

[!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] 또는 [!UICONTROL Bulk Segment] 대상의 경우 아래 필드를 채우십시오.

* **[!UICONTROL Protocol]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 프로토콜을 선택합니다.
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 서버를 선택합니다.
* **[!UICONTROL Format]**: (필수) 드롭다운 목록에서 이 대상에 대해 원하는 형식을 선택합니다.  [!DNL HTTP] 또는 위에서 선택한 프로토콜에 따라 파일 유형을 지정합니다.
* **[!UICONTROL Sync Type]**: (필수) 이 대상에 대해 원하는 동기화 유형을 선택합니다. 이는 클라이언트가 아웃바운드 주문에 포함할 사용자 활동 수준을 나타냅니다. 클라이언트가 해당 속성에서 세그먼트 자격을 분석하는 데만 관심이 있는 경우 **[!UICONTROL Customer]** 을 선택합니다. 모든 [!DNL Audience Manager] 고객에 대해 오프사이트 활동에서 세그먼트 자격을 포함하려면 **[!UICONTROL Platform]** 을 선택합니다.
* **[!UICONTROL Customer]**: 파일에는 선택한 기간 동안 클라이언트의 속성(클라이언트의 속성과 연관된)에 대해서만 1개 이상의 트레이트 실현이 있는 활성  [!UICONTROL PID]사용자가 포함되어 있습니다. 클라이언트는 이 옵션을 사용하여 *실시간* 세그먼트 자격을 대상으로 아웃바운드해야 합니다.
* **[!UICONTROL Platform]**: 파일에는 선택한 기간 동안 모든 클라이언트의 속성(모든 클라이언트 PID와 연관된)에서 ID 동기화 또는 트레이트 실현과 같은 실시간 상호 작용이  [!DNL Audience Manager] 1개 이상 있는 활성 사용자가 포함되어 있습니다. 클라이언트는 이 옵션을 사용하여 *total* 세그먼트 자격을 대상으로 아웃바운드해야 합니다.
* **[!UICONTROL Lifetime]**: 파일은 대상을 만든 후 모든  [!DNL Audience Manager] 클라이언트의 속성에서 나타나는 활성 사용자를 포함합니다.
* **[!UICONTROL Sync Type Lookback Period]**: 또는 [!UICONTROL Customer] 를  [!UICONTROL Platform]선택하는 경우 기간을 선택합니다. 파일에 선택한 기간 동안 활성 사용자가 포함됩니다.
그런 다음 주문 유형을 선택합니다. 이는 파트너와의 각 아웃바운드 통합의 빈도 및 범위를 나타냅니다. 증분 주문 및 전체 주문 중에서 선택합니다.
* **[!UICONTROL Incremental Scheduled Run]**: 를 실행할 때마다  [!DNL Audience Manager] 는 이전 아웃바운드 주문 이후 자격을 얻은 순 신규 사용자만 아웃바운드 아웃바운드합니다. [!DNL Audience Manager]에서 증분 동기화 프로세스를 수행할 원하는 기간을 선택합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 선택하지 않을 수 있습니다.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>첫 번째 증분 순서는 이전 사용자가 대상에 전송되지 않았으므로 전체 주문과 같습니다.

* **[!UICONTROL Full Sync Scheduled Run]**: 를  [!DNL Audience Manager] 실행할 때마다 는 대상이 처음 설정된 이후 모든 활성 사용자를 아웃바운드 아웃바운드합니다. 전체 동기화 프로세스를 수행하는 데 [!DNL Audience Manager]에 사용할 일정을 선택합니다. 예를 들어 24시간마다, 7일마다, 30일마다 또는 선택하지 않을 수 있습니다.

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>전체 동기화보다 증가분 동기화를 더 자주 사용하는 것이 좋습니다. 증분 동기화는 새로운 트레이트 실현 또는 ID 동기화를 포함하는 파일만 보냅니다. 전체 동기화는 새 실현 또는 ID 동기화를 포함하는지 여부에 관계없이 모든 파일을 보냅니다. 클라이언트에서 모든 사용자의 전체 복사본이 필요한 경우에만 [!UICONTROL Full Sync Scheduled Run] 구성을 사용하여 아웃바운드 데이터 볼륨을 줄입니다.

## 데이터 소스 구성 {#configure-data-sources}

[!UICONTROL Bulk ID], [!UICONTROL Bulk Trait] 또는 [!UICONTROL Bulk Segment] 대상의 경우 아래 필드를 채우십시오. 이러한 설정을 사용하여 데이터 소스와 연결된 모든 데이터(선택한 유형에 따라 트레이트, 세그먼트 또는 ID)를 전송할 수 있습니다.

* **[!UICONTROL All Unrestricted First Party Data]**: 모든 자사 데이터 소스를 사용하려면 을(를) 선택합니다. 이 옵션을 선택하면 [!UICONTROL Available Data Sources] 옵션이 비활성화됩니다.
* **[!UICONTROL Available Data Sources]**: 화살표를 사용하여  **[!UICONTROL Available Data Sources]** 및  **[!UICONTROL In File Data Sources]** 상자 간에 데이터 소스를 이동합니다.

## 저장 및 완료 {#save-and-finalize}

모든 필수 필드를 채운 후 **[!UICONTROL Save]** 단추가 활성화됩니다. **[!UICONTROL Save]** 을 클릭하여 대상 만들기 프로세스를 완료합니다.

## 회사 대상 삭제 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

대상을 삭제하려면

1. **[!UICONTROL Companies]** 을 클릭하고 원하는 회사를 찾아 클릭한 다음 **[!UICONTROL Destinations]** 탭을 클릭합니다.
1. 원하는 대상의 **[!UICONTROL Actions]** 열에서 ![](assets/icon_delete.png) 을 클릭합니다.
1. **[!UICONTROL OK]** 을 클릭하여 삭제를 확인합니다.

>[!NOTE]
>
>매핑된 세그먼트가 있으면 대상을 삭제할 수 없습니다.

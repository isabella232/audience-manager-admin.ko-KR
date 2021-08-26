---
description: 장치 그래프 옵션은 Adobe Experience Cloud Device Co-op에 참여하는 회사에서 사용할 수 있습니다. 고객이 또한 Audience Manager과 통합된 타사 장치 그래프 공급자와의 계약 관계가 있는 경우, 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 회사 > 회사 이름 > 프로필 > 장치 그래프 옵션에 있습니다.
seo-description: The Device Graph Options are available to companies that participate in the Adobe Experience Cloud Device Co-op. If a customer also has a contractual relationship with a third-party device graph provider that is integrated with Audience Manager, this section will show options for that device graph. These options are located in Companies > company name > Profile > Device Graph Options.
seo-title: Device Graph Options for Companies
title: 회사를 위한 장치 그래프 옵션
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
exl-id: 2502f3d2-b43c-410c-acb6-03c2a2ba2c1d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# 회사를 위한 장치 그래프 옵션 {#device-graph-options-for-companies}

[!UICONTROL Device Graph Options]은 [!DNL Adobe Experience Cloud Device Co-op]에 참여하는 회사에서 사용할 수 있습니다. 고객이 또한 Audience Manager과 통합된 타사 장치 그래프 공급자와의 계약 관계가 있는 경우, 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 [!UICONTROL Companies] > 회사 이름 > [!UICONTROL Profile] > [!UICONTROL Device Graph Options]에 있습니다.

![](assets/adminUIdataSource.png)

이 그림에서는 타사 장치 그래프 옵션에 대한 일반 이름을 사용합니다. 프로덕션에서 이러한 이름은 장치 그래프 제공자에서 가져오며 여기에 표시된 이름과 다를 수 있습니다. 예를 들어, [!DNL LiveRamp] 옵션은 일반적으로 다음과 같습니다(항상 그렇지는 않음).

*  &quot;[!DNL LiveRamp]&quot;
* 다양한 중간 이름을 포함합니다
* &quot;[!UICONTROL - Household]&quot; 또는 &quot;[!UICONTROL -Person]&quot;로 끝남

## 정의된 장치 그래프 옵션 {#device-graph-options-defined}

여기서 선택하는 장치 그래프 옵션은 [!DNL Audience Manager] 고객이 [!UICONTROL Profile Merge Rule]를 만들 때 사용할 수 있는 [!UICONTROL Device Options] 선택 사항을 표시하거나 숨깁니다.

### Co-op 장치 그래프 {#co-op-graph}

[Adobe Experience Cloud Device Co-op](https://experienceleague.adobe.com/docs/device-co-op/using/about/overview.html?lang=en)에 참여하는 고객은 이러한 옵션을 사용하여 [결정론적 및 확률론적 데이터](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en)와 함께 [!UICONTROL Profile Merge Rule]를 만듭니다. [!DNL Corporate Provisioning Team] 은 백 엔드 [!DNL API] 호출을 통해 이 옵션을 활성화하고 비활성화합니다. [!DNL Admin UI]에서는 이 상자를 선택하거나 지울 수 없습니다. 또한 **[!UICONTROL Co-op Device Graph]** 및 **[!UICONTROL Company Device Graph]** 옵션은 함께 사용할 수 없습니다. 고객이 하나 또는 다른 하나를 활성화하도록 요청할 수 있지만 둘 다 활성화하지는 않습니다. 이 옵션을 선택하면 [!UICONTROL Profile Merge Rule]에 대한 [!UICONTROL Device Options] 설정에 **[!UICONTROL Co-op Device Graph]** 컨트롤이 표시됩니다.

![](assets/adminUI1.png)

### 회사 장치 그래프 {#company-graph}

이 옵션은 [!DNL Analytics] 보고서 세트에서 [!UICONTROL People] 지표를 사용하는 [!DNL Analytics] 고객을 위한 것입니다. [!DNL Corporate Provisioning Team] 은 백 엔드 [!DNL API] 호출을 통해 이 옵션을 활성화하고 비활성화합니다. [!DNL Admin UI]에서는 이 상자를 선택하거나 지울 수 없습니다. 또한 **[!UICONTROL Company Device Graph]** 및 **[!UICONTROL Co-op Device Graph]** 옵션은 함께 사용할 수 없습니다. 고객이 하나 또는 다른 하나를 활성화하도록 요청할 수 있지만 둘 다 활성화하지는 않습니다. 선택 시:

* 이 장치 그래프는 구성 중인 회사에 속하는 결정적 데이터를 사용합니다(확률적 데이터 없음).
* [!DNL Audience Manager] 라는  [!UICONTROL Data Source] 파트너  `*`이름을 자동으로 만듭니다`*-Company Device Graph-Person`. [!UICONTROL Data Source] 세부 정보 페이지에서 [!DNL Audience Manager] 고객은 파트너 이름, 설명을 변경하고 [데이터 내보내기 컨트롤](https://experienceleague.adobe.com/docs/device-co-op/using/device-graph/links.html?lang=en)을 이 데이터 소스에 적용할 수 있습니다.
* [!DNL Audience Manager] 고객 *은* 의 섹션에 새로운  [!UICONTROL Device Options] 설정이 표시되지  [!UICONTROL Profile Merge Rule]않습니다.

### LiveRamp 장치 그래프(개인 또는 가구) {#liveramp-device-graph}

이러한 확인란은 파트너가 [!UICONTROL Data Source]을(를) 만들고 **[!UICONTROL Use as an Authenticated Profile]** 및/또는 **[!UICONTROL Use as a Device Graph]**&#x200B;을(를) 선택하면 [!DNL Admin UI]에서 활성화됩니다. 이러한 설정의 이름은 타사 장치 그래프 공급자(예: [!DNL LiveRamp], [!DNL TapAd] 등)에 의해 결정됩니다. 이 필드를 선택하면 구성할 회사에서 이 장치 그래프에서 제공하는 데이터를 사용하게 됩니다.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [정의된 프로필 병합 규칙 옵션](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/merge-rule-definitions.html?lang=en)
>* [데이터 소스 설정 및 메뉴 옵션](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=en)


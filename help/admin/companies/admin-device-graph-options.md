---
description: 장치 그래프 옵션은 Adobe Experience Cloud Device Co-op에 참여하는 회사에서 사용할 수 있습니다. 고객이 Audience Manager과 통합된 타사 장치 그래프 제공자와 계약상 관계가 있는 경우에도 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 회사 > 회사 이름 > 프로필 > 장치 그래프 옵션에 있습니다.
seo-description: 장치 그래프 옵션은 Adobe Experience Cloud Device Co-op에 참여하는 회사에서 사용할 수 있습니다. 고객이 Audience Manager과 통합된 타사 장치 그래프 제공자와 계약상 관계가 있는 경우에도 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 회사 > 회사 이름 > 프로필 > 장치 그래프 옵션에 있습니다.
seo-title: 회사를 위한 장치 그래프 옵션
title: 회사를 위한 장치 그래프 옵션
uuid: a8ced843-710c-4a8f-a0d7-ea89d010a7a5
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 4%

---


# 회사를 위한 장치 그래프 옵션 {#device-graph-options-for-companies}

이 [!UICONTROL Device Graph Options] 는 해당 회사에 참여하는 회사가 사용할 수 [!DNL Adobe Experience Cloud Device Co-op]있습니다. 고객이 Audience Manager과 통합된 타사 장치 그래프 제공자와 계약상 관계가 있는 경우에도 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 [!UICONTROL Companies] > > 회사 이름 > [!UICONTROL Profile] > [!UICONTROL Device Graph Options]에 있습니다.

![](assets/adminUIdataSource.png)

이 그림에서는 타사 장치 그래프 옵션에 대한 일반 이름을 사용합니다. 제작 과정에서 이러한 이름은 장치 그래프 제공업체에서 제공하며 여기에 표시된 이름과 다를 수 있습니다. 예를 들어, [!DNL LiveRamp] 옵션은 대개 다음과 같습니다.

*  &quot;[!DNL LiveRamp]&quot;
* 다양한 가운데 이름 포함
* &quot;[!UICONTROL - Household]&quot; 또는 &quot;[!UICONTROL -Person]&quot;로 끝남

## 장치 그래프 옵션 정의 {#device-graph-options-defined}

여기에서 선택하는 장치 그래프 옵션은 고객이 장치 [!UICONTROL Device Options] 를 만들 때 사용할 수 있는 선택 사항을 표시하거나 [!DNL Audience Manager] 숨깁니다 [!UICONTROL Profile Merge Rule].

### Co-op 장치 그래프 {#co-op-graph}

Adobe [Experience Cloud Device Co-op에](https://marketing.adobe.com/resources/help/en_US/mcdc/) 참여하는 고객은 이러한 옵션을 사용하여 [!UICONTROL Profile Merge Rule] 결정적이고 확률적인 데이터 [를 만듭니다](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html). 이 [!DNL Corporate Provisioning Team] 옵션은 백엔드 [!DNL API] 호출을 통해 이 옵션을 활성화하고 비활성화합니다. 이 상자들은 에서 확인하거나 지울 수 없습니다 [!DNL Admin UI]. 또한, **[!UICONTROL Co-op Device Graph]** 및 **[!UICONTROL Company Device Graph]** 옵션은 상호 배타적입니다. 고객은 한 가지 또는 다른 두 가지 모두를 활성화하도록 요청할 수 있습니다. 이 확인란을 선택하면 에 대한 설정 **[!UICONTROL Co-op Device Graph]** 에 [!UICONTROL Device Options] 컨트롤이 표시됩니다 [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### 회사 장치 그래프 {#company-graph}

이 옵션은 보고서 세트에서 [!DNL Analytics] 지표를 [!UICONTROL People] 사용하는 [!DNL Analytics] 고객을 위한 것입니다. 이 [!DNL Corporate Provisioning Team] 옵션은 백엔드 [!DNL API] 호출을 통해 이 옵션을 활성화하고 비활성화합니다. 이 상자들은 에서 확인하거나 지울 수 없습니다 [!DNL Admin UI]. 또한, **[!UICONTROL Company Device Graph]** 및 **[!UICONTROL Co-op Device Graph]** 옵션은 상호 배타적입니다. 고객은 한 가지 또는 다른 두 가지 모두를 활성화하도록 요청할 수 있습니다. 선택 시:

* 이 장치 그래프는 구성 중인 회사에 속하는 결정적 데이터를 사용합니다(확률적 데이터 없음).
* [!DNL Audience Manager] 자동으로 [!UICONTROL Data Source] 이름이 `*`파트너 이름을 만듭니다`*-Company Device Graph-Person`. 세부 정보 페이지에서 [!UICONTROL Data Source] 고객은 파트너 이름, 설명을 변경하고 [!DNL Audience Manager] 데이터 내보내기 제어 [](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) 기능을 이 데이터 소스에 적용할 수 있습니다.
* [!DNL Audience Manager] 고객은 *특정* 항목에 대한 [!UICONTROL Device Options] 섹션에 새로운 설정이 표시되지 않습니다 [!UICONTROL Profile Merge Rule].

### LiveRamp 장치 그래프(개인 또는 가구) {#liveramp-device-graph}

이러한 확인란은 파트너가 만들고 [!DNL Admin UI] 및/또는 [!UICONTROL Data Source] **[!UICONTROL Use as an Authenticated Profile]** **[!UICONTROL Use as a Device Graph]**&#x200B;를 선택할 때 활성화됩니다. 이러한 설정의 이름은 타사 장치 그래프 공급자(예:, [!DNL LiveRamp]등)에 의해 [!DNL TapAd]결정됩니다. 이 확인란을 선택하면 구성 중인 회사가 이러한 장치 그래프에서 제공하는 데이터를 사용하게 됩니다.

![](assets/adminUI2.png)

>[!MORELIKETHIS]
>
>* [정의된 프로필 병합 규칙 옵션](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [데이터 소스 설정 및 메뉴 옵션](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)


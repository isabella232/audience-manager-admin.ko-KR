---
description: 장치 그래프 옵션은 Adobe Experience Cloud Device Co-op에 참여하는 회사가 사용할 수 있습니다. 고객이 Audience Manager와 통합된 타사 장치 그래프 공급자와의 계약을 맺은 경우에도 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 회사 > 회사 이름 > 프로필 > 장치 그래프 옵션에 있습니다.
seo-description: 장치 그래프 옵션은 Adobe Experience Cloud Device Co-op에 참여하는 회사가 사용할 수 있습니다. 고객이 Audience Manager와 통합된 타사 장치 그래프 공급자와의 계약을 맺은 경우에도 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 회사 > 회사 이름 > 프로필 > 장치 그래프 옵션에 있습니다.
seo-title: 기업을 위한 디바이스 그래프 옵션
title: 기업을 위한 디바이스 그래프 옵션
uuid: A 8 CED 843-710 C -4 A 8 F-A 0 D 7-EA 89 D 010 A 7 A 5
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 기업을 위한 디바이스 그래프 옵션 {#device-graph-options-for-companies}

에 [!UICONTROL Device Graph Options] 있는은에 참여할 수 [!DNL Adobe Experience Cloud Device Co-op]있습니다. 고객이 Audience Manager와 통합된 타사 장치 그래프 공급자와의 계약을 맺은 경우에도 이 섹션에는 해당 장치 그래프에 대한 옵션이 표시됩니다. 이러한 옵션은 [!UICONTROL Companies] &gt; 회사 이름 &gt; [!UICONTROL Profile] &gt; [!UICONTROL Device Graph Options]에 있습니다.

![](assets/adminUIdataSource.png)

이 그림은 타사 장치 그래프 옵션에 대한 일반 이름을 사용합니다. 제작 과정에서 이러한 이름은 장치 그래프 제공업체에서 가져온 이름이며 여기에 표시된 내용과 다를 수 있습니다. 예를 들어 [!DNL LiveRamp] , 일반적으로 옵션은 (항상 아님) 다음과 같습니다.

*  "[!DNL LiveRamp]"
* 다른 이름이 포함된 가운데 이름 포함
* "[!UICONTROL - Household]Or "로 끝남[!UICONTROL -Person]

## 정의된 장치 그래프 옵션 {#device-graph-options-defined}

여기에서 선택하는 장치 그래프 옵션은 [!UICONTROL Device Options][!DNL Audience Manager] 고객이 A [!UICONTROL Profile Merge Rule]를 만들 때 사용할 수 있는 선택 사항을 표시하거나 숨깁니다.

### Co-op 장치 그래프 {#co-op-graph}

[Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/en_US/mcdc/) 에 참여하는 고객은 이러한 옵션을 사용하여 deterministic 및 probabilistic 데이터를 [!UICONTROL Profile Merge Rule] 함께 [만듭니다](https://marketing.adobe.com/resources/help/en_US/mcdc/mcdc-links.html). 는 [!DNL Corporate Provisioning Team] 백엔드 [!DNL API] 호출을 통해 이 옵션을 활성화하고 비활성화합니다. 에서 이러한 상자를 확인하거나 지울 수 [!DNL Admin UI]없습니다. 또한 **[!UICONTROL Co-op Device Graph]** 및 **[!UICONTROL Company Device Graph]** 옵션은 함께 사용할 수 없습니다. 고객은 Adobe에 활성화를 요청할 수 있습니다. 선택하면 이 설정은 A에 대한 설정의 **[!UICONTROL Co-op Device Graph]** 컨트롤을 [!UICONTROL Device Options] 노출합니다 [!UICONTROL Profile Merge Rule].

![](assets/adminUI1.png)

### 회사 장치 그래프 {#company-graph}

이 옵션은 보고서 [!DNL Analytics] 세트에서 [!UICONTROL People] 지표를 사용하는 고객을 [!DNL Analytics] 위한 것입니다. 는 [!DNL Corporate Provisioning Team] 백엔드 [!DNL API] 호출을 통해 이 옵션을 활성화하고 비활성화합니다. 에서 이러한 상자를 확인하거나 지울 수 [!DNL Admin UI]없습니다. 또한 **[!UICONTROL Company Device Graph]** 및 **[!UICONTROL Co-op Device Graph]** 옵션은 함께 사용할 수 없습니다. 고객은 Adobe에 활성화를 요청할 수 있습니다. 선택 시:

* 이 장치 그래프는 구성하고 있는 회사에 속하는 결정 데이터 (확률적 데이터 없음) 를 사용합니다.
* [!DNL Audience Manager] 자동으로 [!UICONTROL Data Source]`*`파트너 이름이 만들어집니다`*-Company Device Graph-Person`. [!UICONTROL Data Source] 세부 사항 페이지에서 [!DNL Audience Manager] , 고객은 파트너 이름, 설명 및 [데이터 내보내기 컨트롤을](https://marketing.adobe.com/resources/help/en_US/aam/c_dec.html) 이 데이터 소스에 적용할 수 있습니다.
* [!DNL Audience Manager] 고객은 *A에 대한 섹션에 새 설정이* 표시되지 [!UICONTROL Device Options] 않습니다 [!UICONTROL Profile Merge Rule].

### Liveramp 장치 그래프 (개인 또는 가족) {#liveramp-device-graph}

파트너가 A [!DNL Admin UI][!UICONTROL Data Source] 를 만들고/ **[!UICONTROL Use as an Authenticated Profile]** OR **[!UICONTROL Use as a Device Graph]**&#x200B;를 선택하면 이 확인란이 활성화됩니다. 이러한 설정의 이름은 타사 장치 그래프 공급자 (예: [!DNL LiveRamp], 등 [!DNL TapAd]) 에 의해 결정됩니다. 이 확인란을 선택하면 구성하려는 회사가 이러한 장치 그래프에 의해 제공되는 데이터를 사용하게 됩니다.

![](assets/adminUI2.png)

>[!MORE_ like_ this]
>
>* [정의된 프로필 병합 규칙 옵션](https://marketing.adobe.com/resources/help/en_US/aam/merge-rule-definitions.html)
>* [데이터 소스 설정 및 메뉴 옵션](https://marketing.adobe.com/resources/help/en_US/aam/datasource-settings-definitions.html)


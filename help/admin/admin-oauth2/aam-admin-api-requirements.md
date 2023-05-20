---
description: 고객이 Audience Manager API를 사용할 때 인식하도록 권장해야 하는 사항.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API 요구 사항 및 권장 사항
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# API 요구 사항 및 권장 사항 {#api-requirements-and-recommendations}

고객이 Audience Manager을 사용하여 작업할 때 인식하도록 권장해야 하는 사항 [!DNL API]s.

## 요구 사항 {#requirements}

을 사용하여 작업할 때 다음 사항을 참고하십시오 [!DNL Audience Manager] [!DNL API] 코드:

* **요청 매개 변수:** 별도로 지정하지 않는 한 모든 요청 매개 변수가 필요합니다.
* **[!DNL JSON]컨텐츠 유형:** 지정 `content-type: application/json` *및* `accept: application/json` 코드를 입력합니다.

* **요청 및 응답:** 적절한 형식의 요청을 보냅니다. [!DNL JSON] 개체. [!DNL Audience Manager] 다음으로 응답: [!DNL JSON] 형식이 지정된 데이터입니다. 서버 응답에는 요청된 데이터, 상태 코드 또는 두 가지 모두 포함될 수 있습니다.

* **액세스:** 사용자 [!DNL Audience Manager] 컨설턴트는 다음을 수행할 수 있는 클라이언트 ID와 키를 제공합니다. [!DNL API] 요청.

* **설명서 및 코드 샘플:** 텍스트 입력 *기울임체* 만들거나 받을 때 제공하거나 전달하는 변수를 나타냅니다 [!DNL API] 데이터. 바꾸기 *기울임꼴* 고유한 코드, 매개 변수 또는 기타 필수 정보가 있는 텍스트입니다.

## Recommendations: 일반 API 사용자 만들기 {#recommendations}

Audience Manager 작업을 위해 별도의 기술 사용자 계정을 만드는 것이 좋습니다 [!DNL API]s. 이는 클라이언트 조직의 특정 사용자와 연결되거나 연결되지 않은 일반 계정입니다. 이 유형의 [!DNL API] 사용자 계정은 다음 두 가지 작업을 수행하는 데 도움이 됩니다.

* 어떤 서비스가 를 호출하는지 확인합니다. [!DNL API] (예: [!DNL API]s 또는 일괄 변경 시).
* 에 중단 없이 액세스 제공 [!DNL API]s. 특정 직원에 연결된 계정은 퇴사할 때 삭제될 수 있습니다. 이렇게 하면 고객이 사용 가능한 로 작업할 수 없습니다 [!DNL API] 코드. 특정 직원에게 연결되지 않은 일반 계정은 이 문제를 방지하는 데 도움이 됩니다.

이 유형의 계정에 대한 예나 사용 사례로서, 다음과 같이 고객이 한 번에 많은 세그먼트를 변경하려고 한다고 가정해 보겠습니다. [벌크 관리 도구](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en). 이를 위해서는 다음이 필요합니다 [!DNL API] 액세스 권한. 특정 사용자에게 권한을 추가하는 대신 비특정 [!DNL API] 적절한 자격 증명, 키 및 암호가 있는 사용자 계정 [!DNL API] 호출. 이 기능은 를 사용하는 자체 애플리케이션을 개발하는 경우에도 유용합니다 [!DNL Audience Manager] [!DNL API]s.

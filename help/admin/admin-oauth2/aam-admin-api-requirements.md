---
description: 클라이언트가 Audience Manager API를 사용하여 작업할 때 알아야 하는 사항입니다.
seo-description: 클라이언트가 Audience Manager API를 사용하여 작업할 때 알아야 하는 사항입니다.
seo-title: API 요구 사항 및 권장 사항
title: API 요구 사항 및 권장 사항
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# API 요구 사항 및 권장 사항 {#api-requirements-and-recommendations}

고객이 Audience Manager을 사용하여 작업할 때 알아야 할 사항 [!DNL API]을 참조하십시오.

## 요구 사항 {#requirements}

코드 작업 시 다음을 [!DNL Audience Manager] [!DNL API] 참고하십시오.

* **요청 매개 변수:** 별도로 명시되지 않는 한 모든 요청 매개 변수가 필요합니다.
* **[!DNL JSON]콘텐트 유형:**코드에`content-type: application/json`and *를*`accept: application/json`지정합니다.

* **요청 및 응답:** 요청을 올바른 형식으로 [!DNL JSON] 보냅니다. [!DNL Audience Manager] 형식이 지정된 데이터로 [!DNL JSON] 응답합니다. 서버 응답에는 요청된 데이터, 상태 코드 또는 둘 다를 포함할 수 있습니다.

* **액세스:** 컨설턴트는 요청을 할 수 있는 클라이언트 ID와 키를 [!DNL Audience Manager] [!DNL API] 제공합니다.

* **설명서 및 코드 샘플:** 기울임꼴의 *텍스트는* 데이터를 만들거나 수신할 때 제공하거나 전달하는 변수를 [!DNL API] 나타냅니다. 기울임체 *가* 지정된 텍스트를 고유한 코드, 매개 변수 또는 기타 필수 정보로 바꿀 수 있습니다.

## 권장 사항: 일반 API 사용자 만들기 {#recommendations}

Audience Manager에서 작업할 수 있도록 별도의 기술 사용자 계정을 만드는 것이 [!DNL API]좋습니다. 이 계정은 클라이언트 조직의 특정 사용자에게 연결되어 있거나 연결되어 있지 않은 일반 계정입니다. 이 유형의 [!DNL API] 사용자 계정은 다음 두 가지 작업을 수행하는 데 도움이 됩니다.

* 어떤 서비스가 호출되는지 [!DNL API] 확인합니다(예: Adobe를 사용하거나 벌크 변경 [!DNL API]을 수행하는 클라이언트 앱의 호출).
* 중단 없는 액세스를 [!DNL API]제공합니다. 특정 직원과 연결된 계정은 퇴사할 때 삭제될 수 있습니다. 이렇게 하면 고객이 사용 가능한 [!DNL API] 코드를 사용할 수 없습니다. 특정 직원과 연결되지 않은 일반 계정은 이 문제를 방지하는 데 도움이 됩니다.

이러한 유형의 계정에 대한 예제 또는 사용 사례로서 고객이 벌크 관리 도구를 사용하여 한 번에 많은 세그먼트를 변경하려고 한다고 [가정합니다](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). 이를 위해서는 액세스 권한이 [!DNL API] 필요합니다. 특정 사용자에게 권한을 추가하는 대신 적절한 자격 증명, 키 및 암호를 가진 [!DNL API] 사용자 계정을 만들어 [!DNL API] 호출합니다. 이 기능은 클라이언트가 이 응용 프로그램을 사용하는 응용 프로그램을 개발할 경우에도 [!DNL Audience Manager] [!DNL API]유용합니다.

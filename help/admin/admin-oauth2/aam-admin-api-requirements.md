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

클라이언트가 Audience Manager [!DNL API]을(를) 사용할 때 알아야 할 사항입니다.

## 요구 사항 {#requirements}

[!DNL Audience Manager] [!DNL API] 코드를 사용하여 작업할 때는 다음을 참고하십시오.

* **요청 매개 변수:** 별도로 지정하지 않는 한 모든 요청 매개 변수가 필요합니다.
* **[!DNL JSON]컨텐츠 유형:** 코드 `content-type: application/json` ** `accept: application/json` 를 지정합니다.

* **요청 및 응답:** 요청을 올바른 형식의  [!DNL JSON] 개체로 전송합니다. [!DNL Audience Manager] 형식이 지정된 데이터로  [!DNL JSON] 응답합니다. 서버 응답에는 요청된 데이터, 상태 코드 또는 둘 다를 포함할 수 있습니다.

* **액세스:** 컨설턴트는  [!DNL Audience Manager] 요청을  [!DNL API] 할 수 있는 클라이언트 ID와 키를 제공합니다.

* **설명서 및 코드 샘플:** 기울임꼴로 된  ** 텍스트는  [!DNL API] 데이터를 만들거나 수신할 때 제공하거나 전달하는 변수를 나타냅니다. *기울임꼴* 텍스트를 자체 코드, 매개 변수 또는 기타 필요한 정보로 바꿉니다.

## Recommendations:일반 API 사용자 {#recommendations} 만들기

Audience Manager [!DNL API]에서 작업할 수 있도록 별도의 기술 사용자 계정을 만드는 것이 좋습니다.이 계정은 클라이언트 조직의 특정 사용자에게 연결되어 있거나 연결되어 있지 않은 일반 계정입니다. 이 유형의 [!DNL API] 사용자 계정은 다음 두 가지 작업을 수행하는 데 도움이 됩니다.

* [!DNL API]을(를) 호출하는 서비스를 식별합니다(예: [!DNL API]s를 사용하거나 벌크 변경을 수행하는 클라이언트 앱의 호출).
* [!DNL API]s에 대한 중단 없는 액세스를 제공합니다.특정 직원과 연결된 계정은 퇴사할 때 삭제될 수 있습니다. 이로 인해 고객이 사용 가능한 [!DNL API] 코드를 사용할 수 없게 됩니다. 특정 직원과 연결되지 않은 일반 계정은 이 문제를 방지하는 데 도움이 됩니다.

이러한 유형의 계정에 대한 예제 또는 사용 사례로서 고객이 [벌크 관리 도구](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)를 사용하여 한 번에 많은 세그먼트를 변경하려고 한다고 가정해 봅시다. 이를 위해서는 [!DNL API] 액세스가 필요합니다. 특정 사용자에게 권한을 추가하는 대신 해당 자격 증명, 키 및 암호를 가진 특정하지 않은 [!DNL API] 사용자 계정을 만들어 [!DNL API] 호출을 만듭니다. 이 기능은 클라이언트가 [!DNL Audience Manager] [!DNL API]s를 사용하는 자체 애플리케이션을 개발하는 경우에도 유용합니다.

---
description: 고객이 Audience Manager API를 사용하여 작업할 때 이를 인식하도록 권장해야 합니다.
seo-description: 고객이 Audience Manager API를 사용하여 작업할 때 이를 인식하도록 권장해야 합니다.
seo-title: API 요구 사항 및 권장 사항
title: API 요구 사항 및 권장 사항
uuid: EBA 9 CF 92-F 0 C 8-4394-8532-0 DE 9 A 2 E 7 B 103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# API 요구 사항 및 권장 사항 {#api-requirements-and-recommendations}

고객이 Audience Manager [!DNL API]S를 사용하여 작업할 때 이를 인식하도록 권장해야 합니다.

## 요구 사항 {#requirements}

코드를 사용하여 작업하는 경우 다음을 [!DNL Audience Manager][!DNL API] 참고하십시오.

* **요청 매개 변수:** 달리 지정되지 않은 한 모든 요청 매개 변수가 필요합니다.
* **[!DNL JSON]컨텐츠 유형:** 코드를 지정합니다 `content-type: application/json`**`accept: application/json` .

* **요청 및 응답:** 요청을 적절하게 서식이 지정된 [!DNL JSON] 개체로 보냅니다. [!DNL Audience Manager] 서식이 지정된 데이터로 [!DNL JSON] 응답합니다. 서버 응답에는 요청된 데이터, 상태 코드 또는 둘 다를 포함할 수 있습니다.

* **액세스:** [!DNL Audience Manager] 컨설턴트가 [!DNL API] 요청할 수 있는 클라이언트 ID와 키를 제공합니다.

* **설명서 및 코드 샘플:** *기울임꼴로* 된 텍스트는 데이터를 만들거나 수신할 [!DNL API] 때 제공하거나 전달하는 변수를 나타냅니다. *기울임꼴로 된* 텍스트를 사용자 고유의 코드, 매개 변수 또는 기타 필요한 정보로 바꿉니다.

## 권장 사항: 일반 API 사용자 만들기 {#recommendations}

Audience Manager [!DNL API]S를 사용하기 위해 별도의 기술 사용자 계정을 만드는 것이 좋습니다. 이 계정은 클라이언트 조직의 특정 사용자와 연결되어 있지 않거나 연결되어 있지 않은 일반 계정입니다. 이 유형의 [!DNL API] 사용자 계정은 다음 2 가지 작업을 수행하는 데 도움이 됩니다.

* 호출하는 서비스 식별 (예: [!DNL API][!DNL API]Adobe S를 사용하는 클라이언트 응용 프로그램의 호출 또는 대량 변경을 수행할 때)
* [!DNL API]s. 특정 종업원과 연결된 계정은 퇴사한 경우 삭제될 수 있습니다. 이렇게 하면 고객이 사용 가능한 [!DNL API] 코드를 사용할 수 없게 됩니다. 특정 직원에게 연결되지 않은 일반 계정은 이 문제를 피하는 데 도움이 됩니다.

이 유형의 계정에 대한 예제 또는 사용 사례로서 고객이 [벌크 관리 도구를 사용하여 한 번에 많은 세그먼트를 변경한다고](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html)가정해 보겠습니다. 이를 위해서는 액세스 권한이 필요합니다. [!DNL API] 특정 사용자에게 권한을 추가하는 대신 해당 자격 증명, 키 및 비밀이 있는 특수한 [!DNL API] 사용자 계정을 만들어 [!DNL API] 호출을 수행할 수 있습니다. 이 기능은 클라이언트가 s를 사용하는 자체 애플리케이션을 개발할 때도 유용합니다 [!DNL Audience Manager][!DNL API].

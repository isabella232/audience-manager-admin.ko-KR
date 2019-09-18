---
description: 고객이 Audience Manager API를 사용하여 작업할 때 알아야 하는 사항입니다.
seo-description: 고객이 Audience Manager API를 사용하여 작업할 때 알아야 하는 사항입니다.
seo-title: ' API 요구 사항 및 권장 사항'
title: ' API 요구 사항 및 권장 사항'
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# API 요구 사항 및 권장 사항 {#api-requirements-and-recommendations}

고객이 Adobe Audience Manager를 사용하여 작업할 때 알아야 하는 [!DNL API]사항입니다.

## 요구 사항 {#requirements}

코드 작업 시 [!DNL Audience Manager] 다음을 [!DNL API] 참고하십시오.

* **** 요청 매개 변수:별도로 지정하지 않는 한 모든 요청 매개 변수가 필요합니다.
* **[!DNL JSON]** 콘텐트 유형:코드에 `content-type: application/json` and ** `accept: application/json` 를 지정합니다.

* **** 요청 및 응답:요청을 올바른 형식의 [!DNL JSON] 개체로 보냅니다. [!DNL Audience Manager] 이에 대한 [!DNL JSON] 답변은 서식이 지정된 데이터로 이루어집니다. 서버 응답에는 요청된 데이터, 상태 코드 또는 두 가지 모두를 포함할 수 있습니다.

* **** 액세스:컨설턴트가 [!DNL Audience Manager] 클라이언트 ID와 [!DNL API] 요청을 할 수 있는 키를 제공합니다.

* **** 설명서 및 코드 샘플:기울임꼴의 *텍스트는* [!DNL API] 데이터를 만들거나 수신할 때 제공하거나 전달하는 변수를 나타냅니다. 기울임꼴 ** 텍스트를 고유한 코드, 매개 변수 또는 기타 필수 정보로 바꿀 수 있습니다.

## 권장 사항:일반 API 사용자 만들기 {#recommendations}

Adobe에서는 Audience Manager를 사용하여 별도의 기술 사용자 계정을 만드는 것이 [!DNL API]좋습니다.이 계정은 클라이언트 조직의 특정 사용자와 연결되어 있지 않거나 연결되어 있지 않은 일반 계정입니다. 이 유형의 [!DNL API] 사용자 계정은 다음 두 가지 작업을 수행하는 데 도움이 됩니다.

* 어떤 서비스가 호출되는지 [!DNL API] 확인합니다(예: Adobe의 [!DNL API]서비스를 사용하거나 벌크 변경을 수행하는 클라이언트 앱의 호출).
* 중단 없이 [!DNL API]s에 액세스특정 직원에게 연결된 계정은 퇴사할 때 삭제될 수 있습니다. 이렇게 하면 고객이 사용 가능한 [!DNL API] 코드를 사용할 수 없습니다. 특정 직원과 연결되지 않은 일반 계정은 이 문제를 해결하는 데 도움이 됩니다.

이러한 유형의 계정의 예 또는 사용 사례로서 벌크 관리 도구를 사용하여 고객이 한 번에 많은 세그먼트를 변경하려고 [한다고 가정합니다](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/bult-management-tools/bulk-management-intro.html). 이를 위해서는 [!DNL API] 액세스 권한이 필요합니다. 특정 사용자에게 권한을 추가하는 대신 적절한 자격 증명, 키 및 암호를 가진 비특정 [!DNL API] 사용자 계정을 만들어 [!DNL API] 호출합니다. 이 기능은 클라이언트가 [!DNL Audience Manager] [!DNL API]s를 사용하는 자체 애플리케이션을 개발한 경우에도 유용합니다.

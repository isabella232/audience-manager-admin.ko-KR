---
description: Audience Manager 구성에 있는 OAuth2 클라이언트 목록을 보려면 OAuth2 클라이언트 페이지를 사용합니다. 적절한 사용자 역할이 할당되도록 기존 클라이언트를 편집 또는 삭제하거나 새 클라이언트를 만들 수 있습니다.
seo-description: Audience Manager 구성에 있는 OAuth2 클라이언트 목록을 보려면 OAuth2 클라이언트 페이지를 사용합니다. 적절한 사용자 역할이 할당되도록 기존 클라이언트를 편집 또는 삭제하거나 새 클라이언트를 만들 수 있습니다.
seo-title: OAuth2 클라이언트
title: OAuth2 클라이언트
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
translation-type: tm+mt
source-git-commit: 2998dc049971b2fac8c45ca6e3118ea607ae3f92
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 2%

---


# OAuth2 클라이언트 {#oauth-clients}

구성 [!UICONTROL OAuth2 Clients] 의 클라이언트 목록을 [!UICONTROL OAuth2] 보려면 이 [!DNL Audience Manager] 페이지를 사용합니다. 적절한 사용자 역할이 할당되도록 기존 클라이언트를 편집 또는 삭제하거나 새 클라이언트를 만들 수 있습니다.

## 개요 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>고객이 [!DNL Audience Manager 사용자 안내서에서 [OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 설명서를 읽어야 합니다.

[!DNL OAuth2] 은 리소스 소유자를 대신하여 리소스에 대한 안전한 액세스 권한을 제공하는 권한 [!DNL Audience Manager] 의 개방형 표준입니다.

![](assets/oauth.png)

원하는 열의 헤더를 클릭하여 각 열을 오름차순이나 내림차순으로 정렬할 수 있습니다.

목록 맨 아래의 [!UICONTROL Search] 상자나 페이지 매김 컨트롤을 사용하여 원하는 클라이언트를 찾습니다.

## OAuth2 클라이언트 만들기 또는 편집 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Audience Manager 도구 [!UICONTROL OAuth2 Clients] 의 [!UICONTROL Admin] 페이지를 사용하여 새 [!UICONTROL Oauth2] 클라이언트를 만들거나 기존 클라이언트를 편집합니다.

1. 새 [!UICONTROL OAuth2] 클라이언트를 만들려면 **[!UICONTROL OAuth2 Clients]** > 을 클릭합니다 **[!UICONTROL Add OAuth2 Client]**. 기존 [!UICONTROL OAuth2] 클라이언트를 편집하려면 열에서 원하는 클라이언트를 **[!UICONTROL Client ID]** 클릭합니다.
1. 이 [!UICONTROL OAuth2] 클라이언트의 원하는 이름을 지정합니다. 레코드 전용 이름입니다.
1. 클라이언트의 [!UICONTROL OAuth2] 이메일 주소를 지정합니다. 하나의 이메일 주소로 제한됩니다.
1. 드롭다운 **[!UICONTROL Partner]** 목록에서 원하는 파트너를 선택합니다.
1. 상자에서 원하는 ID를 **[!UICONTROL Client ID]** 지정합니다. 요청을 제출할 때 사용되는 [!DNL API] 값입니다. 이전 단계의 드롭다운 목록에서 접두사를 선택한 후 입력을 시작하면 접두어 자동 [!UICONTROL Partner] 이 채워집니다. 올바른 형식은 &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>입니다.
1. 원하는 대로 확인란을 **[!UICONTROL Restrict to Partner Users]** 선택하거나 선택 취소합니다. 이 확인란을 선택하면 사용자가 선택한 파트너의 [!DNL Audience Manager] 사용자여야 합니다. 이 옵션을 선택하는 것이 좋습니다.
1. 섹션에서 **[!UICONTROL Scope]** 원하는 대로 **[!UICONTROL Read]** 및 **[!UICONTROL Write]** 확인란을 선택하거나 선택 취소합니다.
1. 섹션에서 **[!UICONTROL Grant Type]** 원하는 인증 방법을 선택합니다. 기본 설정 [!UICONTROL Password] 및 [!UICONTROL Refresh-token] 옵션을 사용하는 것이 좋습니다.

   * **[!UICONTROL Implicit]**: 이 옵션을 선택하면 [!UICONTROL Redirect URI] 상자가 활성화됩니다. 인증된 후 사용자에게 자동 액세스 토큰이 주어지고 즉시 리디렉션으로 전송됩니다 [!DNL URI].
   * **[!UICONTROL Authorization Code]**: 이 옵션을 선택하면 [!UICONTROL Redirect URI] 상자가 활성화됩니다. 사용자는 인증된 후 클라이언트로 반환되고 리디렉션으로 전송됩니다 [!DNL URI].
   * **[!UICONTROL Password]**: 인증 서버를 통한 자동 유효성 검사 시도가 아닌 사용자가 입력한 암호로 사용자가 인증을 받습니다.
   * **[!UICONTROL Refresh_token]**: 장기간 만료된 액세스 토큰을 새로 고치는 데 사용됩니다.

1. 상자에서 원하는 **[!UICONTROL Redirect URI]** 항목을 지정합니다 [!DNL URI]. 이 옵션은 **[!UICONTROL Implicit]** 및 **[!UICONTROL Authorization_code]** 부여 유형을 선택한 경우에만 사용할 수 있습니다. 이 **[!UICONTROL Redirect URI]** 상자를 사용하면 허용 가능한 값의 쉼표로 구분된 값을 지정할 수 [!DNL URI] 있습니다. 클라이언트 [!DNL URI] 사용자가 클라이언트 액세스 권한을 승인한 후 리디렉션됩니다 [!DNL API] .
1. 액세스 및 새로 고침 토큰 만료에 대해 원하는 만료 시간(초)을 지정합니다.

   * **[!UICONTROL Access Token Expiration Time]**: 액세스 토큰을 발행한 후 유효한 시간(초)입니다. 플랫폼 기본값(12시간)을 사용하려면 null일 수 있습니다. 액세스 토큰이 만료되지 않았음을 나타내려면 -1일 수도 있습니다.
   * **[!UICONTROL Refresh Token Expiration Time]**: 새로 고침 토큰이 발급된 후 유효한 시간(초)입니다. 플랫폼 기본값(30일)을 사용하려면 null일 수 있습니다.

1. 클릭 **[!UICONTROL Save]**.

클라이언트를 삭제하려면 [!UICONTROL OAuth2] 클릭한 다음 원하는 클라이언트 **[!UICONTROL OAuth2 Clients]**&#x200B;의 ![](assets/icon_delete.png) **[!UICONTROL Actions]** 열을 클릭합니다.

>[!MORELIKETHIS]
>
>* [API 요구 사항 및 권장 사항](../admin-oauth2/aam-admin-api-requirements.md)


---
description: '[OAuth 2 클라이언트] 페이지를 사용하여 Audience Manager 구성에서 OAuth 2 클라이언트 목록을 봅니다. 해당 사용자 역할을 할당받았음을 제공하면서 기존 클라이언트를 편집하거나 삭제하거나 새 클라이언트를 만들 수 있습니다.'
seo-description: '[OAuth 2 클라이언트] 페이지를 사용하여 Audience Manager 구성에서 OAuth 2 클라이언트 목록을 봅니다. 해당 사용자 역할을 할당받았음을 제공하면서 기존 클라이언트를 편집하거나 삭제하거나 새 클라이언트를 만들 수 있습니다.'
seo-title: OAuth 2 클라이언트
title: OAuth 2 클라이언트
uuid: 3 e 654053-fb 2 f -4 d 8 f-a 53 c-b 5 c 3 b 8 dbdaaa
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# OAuth 2 클라이언트 {#oauth-clients}

구성에 [!UICONTROL OAuth2 Clients] 있는 [!UICONTROL OAuth2] 클라이언트 목록을 보려면 페이지를 [!DNL Audience Manager] 사용합니다. 해당 사용자 역할을 할당받았음을 제공하면서 기존 클라이언트를 편집하거나 삭제하거나 새 클라이언트를 만들 수 있습니다.

## 개요 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>고객이 [[](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) ! DNL Audience Manager 사용 안내서를 참조하십시오.

[!DNL OAuth2] 리소스 소유자를 대신하여 [!DNL Audience Manager] 리소스에 대한 보안 위임된 액세스를 제공하기 위한 개방형 표준입니다.

![](assets/oauth.png)

원하는 열의 헤더를 클릭하여 오름차순 또는 내림차순으로 각 열을 정렬할 수 있습니다.

목록 아래쪽의 [!UICONTROL Search] 상자 또는 페이지 매김 컨트롤을 사용하여 원하는 클라이언트를 찾습니다.

## OAuth 2 클라이언트 만들기 또는 편집 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Audience [!UICONTROL OAuth2 Clients] Manager [!UICONTROL Admin] 도구의 페이지를 사용하여 새 [!UICONTROL Oauth2] 클라이언트를 만들거나 기존 클라이언트를 편집합니다.

1. [!UICONTROL OAuth2] 새 클라이언트를 만들려면 **[!UICONTROL OAuth2 Clients]** &gt; **[!UICONTROL Add OAuth2 Client]**&#x200B;를 클릭합니다. 기존 [!UICONTROL OAuth2] 클라이언트를 편집하려면 **[!UICONTROL Client ID]** 열에서 원하는 클라이언트를 클릭합니다.
1. 이 [!UICONTROL OAuth2] 클라이언트에 대해 원하는 이름을 지정합니다. 이 이름은 레코드에만 사용됩니다.
1. [!UICONTROL OAuth2] 클라이언트의 이메일 주소를 지정합니다. 하나의 이메일 주소 제한이 있습니다.
1. 드롭다운 **[!UICONTROL Partner]** 목록에서 원하는 파트너를 선택합니다.
1. **[!UICONTROL Client ID]** 상자에 원하는 ID를 지정합니다. 요청을 제출할 [!DNL API] 때 사용되는 값입니다. 이전 단계의 드롭다운 목록에서 A [!UICONTROL Partner] 를 선택한 후 입력을 시작하면 접두사가 자동으로 채워집니다. 올바른 형식은 &lt; *`partner subdomain`*&gt; - &lt; *`Audience Manager username`*&gt; 입니다.
1. 원하는 대로 **[!UICONTROL Restrict to Partner Users]** 확인란을 선택하거나 선택 취소합니다. 이 확인란을 선택하면 사용자가 선택한 파트너에 대해 나열된 [!DNL Audience Manager] 사용자여야 합니다. 이 옵션을 선택하는 것이 좋습니다.
1. **[!UICONTROL Scope]** 섹션에서 원하는 **[!UICONTROL Read]** 대로 및 **[!UICONTROL Write]** 확인란을 선택 또는 선택 취소합니다.
1. **[!UICONTROL Grant Type]** 섹션에서 원하는 인증 수단을 선택합니다. 기본 설정 및 [!UICONTROL Password][!UICONTROL Refresh-token] 옵션은 사용하는 것이 좋습니다.

   * **[!UICONTROL Implicit]**: 이 옵션을 선택하면 [!UICONTROL Redirect URI] 상자가 활성화됩니다. 사용자에게 인증 후 자동 액세스 토큰이 할당되고 리디렉션으로 [!DNL URI]즉시 전송됩니다.
   * **[!UICONTROL Authorization Code]**: 이 옵션을 선택하면 [!UICONTROL Redirect URI] 상자가 활성화됩니다. 사용자가 인증된 후 클라이언트에 반환되면 리디렉션으로 [!DNL URI]전송됩니다.
   * **[!UICONTROL Password]**: 사용자는 인증 서버를 통한 자동 유효성 검사 시도가 아닌 사용자가 입력한 암호로 인증됩니다.
   * **[!UICONTROL Refresh_token]**: 장기간 만료된 액세스 토큰을 새로 고치는 데 사용됩니다.

1. **[!UICONTROL Redirect URI]** 상자에 [!DNL URI]원하는 대로 지정합니다. 이 옵션은 [유형] 를 **[!UICONTROL Implicit]** 선택하고 **[!UICONTROL Authorization_code]** [허용] 를 선택하는 경우에만 활성화됩니다. **[!UICONTROL Redirect URI]** 이 상자를 사용하면 쉼표로 구분된 [!DNL URI] 값의 쉼표로 구분된 값을 지정할 수 있습니다. 액세스 권한을 [!DNL URI] 받기 위해 [!DNL API] 클라이언트를 승인한 후 클라이언트의 사용자가 리디렉션된 것입니다.
1. 토큰 만료 및 새로 고침 토큰 만료에 대한 원하는 만료 시간 (초) 를 지정합니다.

   * **[!UICONTROL Access Token Expiration Time]**: 발행 후 액세스 토큰이 유효한 시간 (초). 플랫폼 기본값 (12 시간) 를 사용하려면 null 이 될 수 있습니다. 또한 액세스 토큰이 만료되지 않음을 나타내는 -1 이 있을 수 있습니다.
   * **[!UICONTROL Refresh Token Expiration Time]**: 발급된 후 새로 고침 토큰이 유효한 시간 (초) 입니다. 플랫폼 기본값 (30 일) 를 사용하려면 null 이 될 수 있습니다.

1. 클릭 **[!UICONTROL Save]**.

[!UICONTROL OAuth2] 클라이언트를 삭제하려면을 클릭하고 **[!UICONTROL OAuth2 Clients]**&#x200B;원하는 ![](assets/icon_delete.png) 클라이언트에 대한 **[!UICONTROL Actions]** 열을 클릭합니다.

>[!MORE_ like_ this]
>
>* [API 요구 사항 및 권장 사항](../admin-oauth2/aam-admin-api-requirements.md)


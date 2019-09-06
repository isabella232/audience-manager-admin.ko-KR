---
description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 HTTP 서버를 만들거나 기존 서버를 편집할 수 있습니다.
seo-description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 HTTP 서버를 만들거나 기존 서버를 편집할 수 있습니다.
seo-title: HTTP 서버 만들기 또는 편집
title: HTTP 서버 만들기 또는 편집
uuid: 1 EF 0 E 751-E 239-4 DC 6-A 4 F 6-73 CC 05686807
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# HTTP 서버 만들기 또는 편집 {#create-or-edit-an-http-server}

Audience Manager 관리 도구의 [!UICONTROL Servers] 페이지를 사용하여 새 HTTP 서버를 만들거나 기존 서버를 편집합니다.

>[!NOTE]
>
>새 서버를 만들거나 기존 서버를 편집하려면 [!UICONTROL DEXADMIN] 역할이 있어야 합니다.

1. 새 서버를 만들려면 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**&#x200B;로 이동합니다. 기존 서버를 편집하려면 **[!UICONTROL Label]** 열에서 원하는 서버를 클릭합니다.
1. 이 서버에 대해 원하는 레이블을 지정합니다.
1. 드롭다운 **[!UICONTROL Protocol]** 목록에서 원하는 프로토콜을 선택합니다. [!DNL HTTP].
1. 다음 필드를 채웁니다.

   * **[!UICONTROL Domain]:** 이 서버에 대해 원하는 도메인 (호스트) 를 지정합니다.
   * **[!UICONTROL Port]:** 이 서버에 대해 원하는 포트를 지정합니다. 각 암호화 유형에 대해 기본 포트가 표시됩니다. 필요한 경우 기본 포트를 변경할 수 있습니다.
   * **[!UICONTROL Maximum Users Per Request]:** 이 서버에 대해 허용되는 요청당 최대 사용자 수를 지정합니다.
   * **[!UICONTROL URL Prefix]:** 이 서버에 사용할 [!DNL URL] 접두사를 지정합니다.
   * **[!UICONTROL Authentication URL]:** 이 서버의를 [!UICONTROL Authentication URL]`HTTP` 지정합니다.
   * **[!UICONTROL Authentication]:** 원하는 인증 방법을 지정합니다. **[!UICONTROL None]**, **[!UICONTROL Username/Password]**&#x200B;또는 **[!UICONTROL SSH Key]**.
   * **[!UICONTROL HTTP Signature Header]:** 고객이 서명 키를 포함하는 [!DNL HTTP] 헤더의 [!DNL HTTP] 이름. 기본값은 아래 [!UICONTROL X-Signature]예에서 보듯이 입니다.

      ```
      * Connected to partner.website.com (127.0.0.1) port 80 (#0)
      > POST /webpage HTTP/1.1
      > Host: partner.host.com
      > Accept: */*
      > Content-Type: application/json
      > Content-Length: 20
      > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
      POST message content
      ```

   * **[!UICONTROL HTTP Signature Key]:** 고객이 [!DNL HTTP] 요청한 요청에 서명하는 데 사용되는 키.
   * **[!UICONTROL Show Signature Key]:** 브라우저에서 서명을 표시할지 여부를 전환합니다.
   * **[!UICONTROL HTTP Signature Encryption Method]:** 서명을 암호화하는 데 사용하는 방법을 지정합니다. 고객이 달리 원하지 [!UICONTROL SHA1] 않는 한 사용합니다.
   >[!NOTE]
   >
   >파트너의 실시간 데이터 전송에 [대해 OAuth 2.0 인증을](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html) 활성화하려면 아래 표와 같이 필드를 입력합니다. *기울임꼴로* 된 필드는 표와 정확하게 작성해야 합니다.

   | 이름 | 값 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *승인&#x200B;*] |
   | [!UICONTROL Password] | your_ password_ here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 새 서버를 만드는 **[!UICONTROL Create]** 경우를 클릭하거나 기존 서버를 편집하는 **[!UICONTROL Update]** 경우를 클릭합니다.
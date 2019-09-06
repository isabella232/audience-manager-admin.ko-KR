---
description: 베타 환경은 Audience Manager 구현을 테스트하는 데 사용됩니다. 베타에서 변경한 내용은 프로덕션 데이터에 영향을 주지 않습니다. Audience Manager 베타 환경은 제작 환경의 독립 실행형 독립 실행형 버전입니다. 테스트하려는 모든 데이터는 이 환경에서 입력하고 수집해야 합니다.
seo-description: 베타 환경은 Audience Manager 구현을 테스트하는 데 사용됩니다. 베타에서 변경한 내용은 프로덕션 데이터에 영향을 주지 않습니다. Audience Manager 베타 환경은 제작 환경의 독립 실행형 독립 실행형 버전입니다. 테스트하려는 모든 데이터는 이 환경에서 입력하고 수집해야 합니다.
seo-title: 베타 환경
solution: Audience Manager
title: 베타 환경
uuid: 6 A 253 F 4 E -96 E 7-4395-A 783-A 8 EB 213 B 7 DAF
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27

---


# 베타 환경 {#beta-environment}

베타 환경은 Audience Manager 구현을 테스트하는 데 사용됩니다. 베타에서 변경한 내용은 프로덕션 데이터에 영향을 주지 않습니다. Audience Manager 베타 환경은 제작 환경의 독립 실행형 독립 실행형 버전입니다. 테스트하려는 모든 데이터는 이 환경에서 입력하고 수집해야 합니다.

## 개요 {#overview}

<!-- beta_environment_admin.xml -->

| service | URL/호스트 이름 | 프로비저닝하기 위한 단계 |
|--- |--- |--- |
| S3 |  | Amazon S 3 버킷 [프로비저닝을 참조하십시오](admin-beta-environment.md#provision-s3-buckets). |
| DCS | https &amp; amp; 콜론; (/dcs-beta.demdex.net/.. | 추가 단계가 필요하지 않습니다. 베타 환경에서 DCS [에 액세스를 참조하십시오](admin-beta-environment.md#access-dcs-beta-environment). |
| UI | https &amp; amp; 콜론; //bank-beta.demdex.com | 데이터는 프로덕션에서 매월 베타 환경으로 복사됩니다. 프로덕션 자격 증명은 베타 버전에 유효합니다. |
| API | https &amp; amp; 콜론; (/api-beta.demdex.com/.. | 데이터는 프로덕션에서 매월 베타 환경으로 복사됩니다. 프로덕션 자격 증명은 베타 버전에 유효합니다. |

## Amazon S 3 버킷 프로비저닝 {#provision-s3-buckets}

>[!NOTE]
>
>[!DNL FTP/SFTP]Adobe는 그 사용 방식에서 벗어나고 있습니다. 또한 베타 환경에서는 아웃바운드 데이터 전송이 작동하지 않습니다.

인바운드 데이터에 [!DNL S3] 대한 버킷을 프로비저닝하려면:

1. [**SKMS 요청 techops 도움말**](https://skms.adobe.com/) 기능을 사용합니다.
1. 왼쪽 **[!UICONTROL Request TechOps Help]** 탐색 레일에서 이동합니다.
1. 에서 **[!UICONTROL Request Search]**&#x200B;검색 필드에 Audience Manager를 입력합니다.
1. 검색 결과에서 아래로 스크롤하고 Audience Manager - **S 3 인바운드/아웃바운드 계정 프로비저닝을 클릭합니다**.
1. [프로비저닝] 창의 필드를 채우고 필드에 **샌드박스 환경을** **[!UICONTROL Environment]** 지정합니다.

>[!NOTE]
>
>우리는 사용을 권장하지 않으며 [!DNL FTP/SFTP][!UICONTROL Amazon S3]사용을 권장한다. Amazon S 3의 사용을 권장하는 이유는 [!UICONTROL Amazon S3][다음과 같습니다.](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)About.

## 베타 환경에서 DCS 액세스 {#access-dcs-beta-environment}

베타 환경에서에 [!UICONTROL DCS] 액세스하려면:

1. 명령을 사용하여 [!UICONTROL DCS][!DNL curl][전화를 겁니다](https://curl.haxx.se/docs/manpage.html). [!DNL Curl] 는 지원되는 많은 프로토콜 중 하나를 사용하여 서버와 데이터를 전송하는 도구입니다.

   예: `curl -v https://dcs-beta.demdex.net/event`

1. request by your request was serve by the beta [!UICONTROL DCS] by looking "[!DNL sandbox]in the [!UICONTROL DCS] response header.

   예:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
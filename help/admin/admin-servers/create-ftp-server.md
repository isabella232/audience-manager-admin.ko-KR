---
description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: FTP 서버 만들기 또는 편집
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 79415eba732c2a6d50f04124774664f788ccc78c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# FTP 서버 만들기 또는 편집 {#create-or-edit-an-ftp-server}

사용 [!UICONTROL Servers] 새 FTP 서버를 만들거나 기존 서버를 편집할 수 있는 Audience Manager 관리 도구의 페이지입니다.

>[!NOTE]
>
>다음을 보유해야 합니다. [!UICONTROL DEXADMIN] 새 서버를 만들거나 기존 서버를 편집하는 역할입니다.

1. 새 서버를 만들려면 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**. 기존 서버를 편집하려면 **[!UICONTROL Label]** 열.
1. 이 서버에 대해 원하는 레이블을 지정합니다.
1. 다음에서 **[!UICONTROL Protocol]** 드롭다운 목록에서 원하는 프로토콜을 선택합니다. **FTP**.

   >[!NOTE]
   >
   >모범 사례로서 다음을 사용하는 것이 좋습니다. [!DNL Amazon S3] 을(를) 통해 파일을 가져오고 파트너에게 파일을 전달하는 방법입니다. [!DNL Amazon S3] 는 웹의 어디에서나 언제든지 원하는 양의 데이터를 저장하고 검색하는 데 사용할 수 있는 간단한 웹 서비스 인터페이스를 제공합니다. 자세한 내용은 [Amazon S3 정보](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html) 다음에서 *Audience Manager 사용 안내서*.

1. 다음 필드를 채웁니다.

   * **[!UICONTROL Type]:** 원하는 암호화 유형을 선택합니다. **[!UICONTROL SFTP]** 또는 **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** 이 서버에 대해 원하는 도메인(호스트)을 지정하십시오.
   * **[!UICONTROL Port]:** 이 서버에 대해 원하는 포트를 지정하십시오. 기본 포트는 각 암호화 유형에 대해 표시됩니다. 필요한 경우 기본 포트를 변경할 수 있습니다.
   * **[!UICONTROL Remote Path]:** 이 서버에 대해 원하는 원격 경로를 지정하십시오. 이 필드를 비워 두면 Audience Manager은 파일을 기본 디렉터리에 배치합니다.
   * **[!UICONTROL .tmp File Rename on Completion]:** 이 옵션을 활성화하면 `.tmp` 완료 시 파일입니다.
   * **[!UICONTROL Filename Suffix]:** 파일을 전송할 텍스트를 지정합니다.
   * **[!UICONTROL Moved to When Finished]:** 완료 시 전송 파일을 이동할 위치에 대한 경로를 지정합니다.
   * **[!UICONTROL Authentication]:** 원하는 서버 인증 방법을 지정합니다. **[!UICONTROL Username/Password]** 또는 **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >이그레스 추가 [!DNL FTP] [!DNL IP] 을(를) 허용된 IP 목록에 추가합니다. **52.44.29.204**.

1. 대상 **[!UICONTROL SSH Key]** 인증:
   >[!NOTE]
   >
   >SSH 키 인증을 구성할 때는 항상 OpenSSH 형식으로만 공개 및 개인 키를 생성해야 합니다.
   1. 다음 위치에서 공개/개인 키 쌍 생성 [!DNL Linux] 또는 [!DNL Mac] 기계입니다.
   1. 다음을 제공합니다. **공개 키** 를 업데이트하기 위해 클라이언트에 [!DNL SFTP] 서버입니다. 다음을 포함하여 서버의 공개 키에 있는 모든 텍스트를 포함해야 합니다. `-----BEGIN RSA PRIVATE KEY-----` 및  `-----END RSA PRIVATE KEY-----` . 대신 키를 설치할 사용자 이름을 제공해야 합니다.
   1. 사용자 이름 필드를 클라이언트가 제공한 로 업데이트하고 키 필드를 **개인 키**.
1. 클릭 **[!UICONTROL Create]** 새 서버를 만드는 경우 **[!UICONTROL Update]** 기존 서버를 편집하는 경우

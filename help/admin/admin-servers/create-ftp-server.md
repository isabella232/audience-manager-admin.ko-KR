---
description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집할 수 있습니다.
seo-description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집할 수 있습니다.
seo-title: FTP 서버 만들기 또는 편집
title: FTP 서버 만들기 또는 편집
uuid: 9273 ABB 2-963 D -4 D 83-BF 5 A-B 3817 F 0 B 90 E 6
translation-type: tm+mt
source-git-commit: 57d7a92265e565b6c411e4cfa5c579e40eb837b3

---


# FTP 서버 만들기 또는 편집 {#create-or-edit-an-ftp-server}

Audience Manager 관리 도구의 [!UICONTROL Servers] 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.

>[!NOTE]
>
>새 서버를 만들거나 기존 서버를 편집하려면 [!UICONTROL DEXADMIN] 역할이 있어야 합니다.

1. 새 서버를 만들려면 **[!UICONTROL Servers]** &gt; **[!UICONTROL Create Server]**&#x200B;를 클릭합니다. 기존 서버를 편집하려면 **[!UICONTROL Label]** 열에서 원하는 서버를 클릭합니다.
1. 이 서버에 대해 원하는 레이블을 지정합니다.
1. 드롭다운 **[!UICONTROL Protocol]** 목록에서 원하는 프로토콜을 선택합니다. **** FTP.

   >[!NOTE]
   >
   >파일을 가져오고 파트너에게 [!DNL Amazon S3] 파일을 전달하는 방법을 사용하는 것이 좋습니다. [!DNL Amazon S3] 웹 어디서나 언제 어디서나 데이터를 저장하고 검색하는 데 사용할 수 있는 간단한 웹 서비스 인터페이스를 제공합니다. 자세한 내용은 Audience Manager [사용자 안내서의 Amazon S 3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html) *정보를*&#x200B;참조하십시오.

1. 다음 필드를 채웁니다.

   * **[!UICONTROL Type]:** 원하는 암호화 유형을 선택합니다. **[!UICONTROL SFTP]** **[!UICONTROL FTPs/TLS]**&#x200B;또는
   * **[!UICONTROL Domain]:** 이 서버에 대해 원하는 도메인 (호스트) 를 지정합니다.
   * **[!UICONTROL Port]:** 이 서버에 대해 원하는 포트를 지정합니다. 각 암호화 유형에 대해 기본 포트가 표시됩니다. 필요한 경우 기본 포트를 변경할 수 있습니다.
   * **[!UICONTROL Remote Path]:** 이 서버에 대해 원하는 원격 경로를 지정합니다. 이 필드를 비워 두면 Audience Manager가 파일을 기본 디렉토리에 배치합니다.
   * **[!UICONTROL .tmp File Rename on Completion]:** 완료 시 `.tmp` 파일의 이름을 변경하려면 이 옵션을 활성화합니다.
   * **[!UICONTROL Filename Suffix]:** 파일을 전송할 텍스트를 지정합니다.
   * **[!UICONTROL Moved to When Finished]:** 완료 시 파일을 이동할 위치 경로를 지정합니다.
   * **[!UICONTROL Authentication]:** 원하는 서버 인증 방법을 지정합니다. **[!UICONTROL Username/Password]** **[!UICONTROL SSH Key]**&#x200B;또는
   >[!NOTE]
   >
   >Adobe의 수신을 허용 목록에 추가하십시오 [!DNL FTP][!DNL IP]. **52.44.29.204**.

1. **[!UICONTROL SSH Key]** 인증의 경우:
   1. [!DNL Linux] 모든 또는 [!DNL Mac] 컴퓨터에서 공개/개인 키 쌍을 생성합니다.
   1. 클라이언트가 서버에서 업데이트할 **공개 키를** [!DNL SFTP] 지정합니다. 여기에는 `-----BEGIN RSA PRIVATE KEY-----` AND `-----END RSA PRIVATE KEY-----` 를 포함하여 서버의 공개 키에 있는 모든 텍스트를 포함해야 합니다. Exchange 에서는 사용자가 키를 설치하는 사용자 이름을 제공해야 합니다.
   1. 클라이언트가 제공한 사용자 이름 필드와 **개인 키가 있는 키 필드를 업데이트합니다**.
1. 새 서버를 만드는 **[!UICONTROL Create]** 경우를 클릭하거나 기존 서버를 편집하는 **[!UICONTROL Update]** 경우를 클릭합니다.

---
description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.
seo-description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.
seo-title: FTP 서버 만들기 또는 편집
title: FTP 서버 만들기 또는 편집
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
translation-type: tm+mt
source-git-commit: 78d694670e7abdc18938c5be729ad499e2647825
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 5%

---


# FTP 서버 만들기 또는 편집 {#create-or-edit-an-ftp-server}

Audience Manager 관리 도구의 [!UICONTROL Servers] 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.

>[!NOTE]
>
>새 서버를 만들거나 기존 서버를 편집하려면 [!UICONTROL DEXADMIN] 역할이 있어야 합니다.

1. 새 서버를 만들려면 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**&#x200B;을 클릭합니다. 기존 서버를 편집하려면 **[!UICONTROL Label]** 열에서 원하는 서버를 클릭합니다.
1. 이 서버에 원하는 레이블을 지정합니다.
1. **[!UICONTROL Protocol]** 드롭다운 목록에서 원하는 프로토콜을 선택합니다.**FTP**

   >[!NOTE]
   >
   >파일 가져오기 및 파트너에 파일 전달 방법으로 [!DNL Amazon S3]을 사용하는 것이 좋습니다. [!DNL Amazon S3] 웹 사이트 어디에서나 모든 양의 데이터를 저장 및 검색하는 데 사용할 수 있는 간단한 웹 서비스 인터페이스를 제공합니다. 자세한 내용은 *Audience Manager 사용 안내서*&#x200B;의 [Amazon S3](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)을 참조하십시오.

1. 다음 필드를 채웁니다.

   * **[!UICONTROL Type]:** 원하는 암호화 유형을 선택합니다. **[!UICONTROL SFTP]** 또는 **[!UICONTROL FTPs/TLS]**.
   * **[!UICONTROL Domain]:** 이 서버에 대해 원하는 도메인(호스트)을 지정합니다.
   * **[!UICONTROL Port]:** 이 서버에 대해 원하는 포트를 지정합니다. 각 암호화 유형에 대해 기본 포트가 표시됩니다. 필요한 경우 기본 포트를 변경할 수 있습니다.
   * **[!UICONTROL Remote Path]:** 이 서버에 대해 원하는 원격 경로를 지정합니다. 이 필드를 비워 두면 Audience Manager이 파일을 기본 디렉토리에 배치합니다.
   * **[!UICONTROL .tmp File Rename on Completion]:** 완료 시  `.tmp` 파일 이름을 변경하려면 이 옵션을 활성화합니다.
   * **[!UICONTROL Filename Suffix]:** 파일을 전송하는 데 추가할 텍스트를 지정합니다.
   * **[!UICONTROL Moved to When Finished]:** 전송 파일이 완료될 때 이동할 위치의 경로를 지정합니다.
   * **[!UICONTROL Authentication]:** 원하는 서버 인증 방법을 지정합니다. **[!UICONTROL Username/Password]** 또는 **[!UICONTROL SSH Key]**.

   >[!NOTE]
   >
   >허용되는 IP 목록에 [!DNL FTP] [!DNL IP] 주소를 추가해야 합니다.**52.44.29.204**.

1. **[!UICONTROL SSH Key]** 인증의 경우:
   >[!NOTE]
   >
   >SSH 키 인증을 구성할 때는 항상 공개 및 개인 키를 OpenSSH 형식으로만 생성해야 합니다.
   1. [!DNL Linux] 또는 [!DNL Mac] 컴퓨터에서 공개/개인 키 쌍을 생성합니다.
   1. **공개 키**&#x200B;를 클라이언트에 제공하여 [!DNL SFTP] 서버에서 업데이트합니다. 이러한 파일에는 `-----BEGIN RSA PRIVATE KEY-----` 및 `-----END RSA PRIVATE KEY-----`을 포함하여 서버의 공개 키의 모든 텍스트가 포함되어야 합니다. 대신 키를 설치하는 사용자 이름을 제공해야 합니다.
   1. 클라이언트에서 제공한 사용자 이름 필드와 **개인 키**&#x200B;로 키 필드를 업데이트합니다.
1. 새 서버를 만드는 경우 **[!UICONTROL Create]**&#x200B;을 클릭하고 기존 서버를 편집하는 경우 **[!UICONTROL Update]**&#x200B;를 클릭합니다.

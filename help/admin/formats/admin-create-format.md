---
description: Audience Manager 관리 도구의 형식 페이지를 사용하여 새 형식을 만들거나 기존 형식을 편집합니다.
seo-description: Audience Manager 관리 도구의 형식 페이지를 사용하여 새 형식을 만들거나 기존 형식을 편집합니다.
seo-title: 포맷 만들기 또는 편집
title: 포맷 만들기 또는 편집
uuid: CA 1 B 1 Feb-BCD 3-4 A 41-B 1 E 8-80565 F 6 C 23 AE
translation-type: tm+mt
source-git-commit: 71bf4cec222428686c1eab0998f66887db06da68

---


# 포맷 만들기 또는 편집 {#create-or-edit-a-format}

Audience Manager 관리 도구의 [!UICONTROL Formats] 페이지를 사용하여 새 형식을 만들거나 기존 형식을 편집합니다.

<!-- t_create_format.xml -->

>[!TIP]
>
>전공 데이터 형식을 선택할 때 기존 형식을 다시 사용하는 것이 가장 좋습니다. 이미 입증된 포맷을 사용하면 아웃바운드 데이터가 성공적으로 생성됩니다. 기존 포맷의 형식을 정확하게 확인하려면 메뉴 모음에서 [!UICONTROL Formats] 옵션을 클릭하고 이름이나 ID 번호별로 형식을 검색합니다. 형식에서 형식이 잘못된 형식이나 매크로를 사용하면 서식이 잘못 지정된 출력이 제공되거나 정보가 완전히 출력되지 않습니다.

1. 새 형식을 만들려면 **[!UICONTROL Formats]** &gt; **[!UICONTROL Add Format]**&#x200B;를 클릭합니다. 기존 형식을 편집하려면 **[!UICONTROL Name]** 열에서 원하는 형식을 클릭합니다.

   ![](assets/create_format.png)

1. 다음 필드를 채웁니다.
   * **이름:** (필수) 형식에 설명형 이름을 입력합니다.
   * **유형:** (필수) 원하는 형식을 선택합니다.
      * **[!UICONTROL File]**: 파일을 통해 [!DNL FTP] 데이터를 전송합니다.
      * **[!UICONTROL HTTP]**: 래퍼의 데이터를 [!DNL JSON] 포함합니다.

1. (조건부) 선택한 경우 **[!UICONTROL File]**&#x200B;필드를 채웁니다.

   >[!NOTE]
   >
   >사용 가능한 매크로 목록은 [파일 형식 매크로](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 및 [HTTP 포맷 매크로를 참조하십시오](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE).

   * **[!UICONTROL File Name]:** 데이터 전송 파일의 파일 이름을 지정합니다.
   * **header:** 데이터 전송 파일의 첫 번째 행에 나타나는 텍스트를 지정합니다.
   * **[!UICONTROL Data Row]:** 파일의 맨 앞에 있는 각 행에 나타나는 텍스트를 지정합니다.
   * **[!UICONTROL Maximum File Size (In MB)]:** 데이터 전송 파일의 최대 파일 크기를 지정합니다. 압축된 파일은 100 MB 보다 작아야 합니다. 압축되지 않은 파일 크기에는 제한이 없습니다.
   * **[!UICONTROL Compression]:** 원하는 압축 유형을 선택합니다. 데이터 파일의 GZ 또는 ZIP. 배달하려면.gz [!UICONTROL AWS S3]또는 압축되지 않은 파일을 사용해야 합니다.
   * **[!UICONTROL .info Receipt]:** transfer-control ([!DNL .info]) 파일이 생성되도록 지정합니다. 파일은 파트너가 [!DNL .info] Audience Manager에서 파일 전송을 올바르게 처리했는지 확인할 수 있도록 파일 전송에 대한 메타데이터 정보를 제공합니다. 자세한 내용은 로그 파일 전송을 위한 [전송 제어 파일을 참조하십시오](https://marketing.adobe.com/resources/help/en_US/aam/c_s2s_add_transfer_control_files.html).
   * **[!UICONTROL MD5 Checksum Receipt]:** [!DNL MD5] 체크섬 영수증이 생성되도록 지정합니다. 파트너가 Audience Manager에서 전체 전송을 올바르게 처리했는지 확인할 수 있도록 [!DNL MD5] 체크섬 영수증이 표시됩니다.

1. (조건부) 선택한 경우 **[!UICONTROL HTTP]**&#x200B;필드를 채웁니다.

   * **[!UICONTROL Method]:** 전송 프로세스에 사용할 [!DNL API] 방법을 선택합니다.
      * **[!UICONTROL POST]:** 선택하는 경우 [!DNL POST]컨텐츠 유형 ([!DNL XML] 또는 [!DNL JSON]) 를 선택한 다음 요청 본문을 지정합니다.
      * **[!UICONTROL GET]:** 선택하는 경우 [!DNL GET]쿼리 매개 변수를 지정합니다.

1. 새 형식을 만드는 **[!UICONTROL Create]** 경우를 클릭하거나 기존 형식을 편집하는 **[!UICONTROL Save Updates]** 경우 클릭합니다.

## 형식 삭제 {#delete-format}

1. 클릭 **[!UICONTROL Formats]**.
2. 원하는 ![](assets/icon_delete.png) 형식의 **[!UICONTROL Actions]** 열을 클릭합니다.
3. Click **[!UICONTROL OK]** to confirm the deletion.

---
description: Audience Manager 관리 도구의 형식 페이지에서 새 형식을 만들거나 기존 형식을 편집할 수 있습니다.
seo-description: Use the Formats page in the Audience Manager Admin tool to create a new format or to edit an existing format.
seo-title: Create or Edit a Format
title: 형식 만들기 또는 편집
uuid: ca1b1feb-bcd3-4a41-b1e8-80565f6c23ae
exl-id: 3c97d1e9-8093-4181-a1fd-fb1816cdaa3d
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 3%

---

# 형식 만들기 또는 편집 {#create-or-edit-a-format}

Audience Manager 관리 도구의 [!UICONTROL Formats] 페이지를 사용하여 새 형식을 만들거나 기존 형식을 편집합니다.

<!-- t_create_format.xml -->

>[!TIP]
>
>아웃바운드 데이터에 대한 형식을 선택할 때는 기존 형식을 다시 사용하는 것이 좋습니다. 이미 검증된 포맷을 사용하면 아웃바운드 데이터가 성공적으로 생성됩니다. 기존 형식의 형식을 정확하게 확인하려면 메뉴 모음에서 [!UICONTROL Formats] 옵션을 클릭하고 이름이나 ID 번호로 형식을 검색합니다. 형식이 잘못된 형식이나 형식으로 사용된 매크로가 잘못된 형식의 출력을 제공하거나 정보가 완전히 출력되지 않도록 합니다.

1. 새 형식을 만들려면 **[!UICONTROL Formats]** > **[!UICONTROL Add Format]** 를 클릭하십시오. 기존 형식을 편집하려면 **[!UICONTROL Name]** 열에서 원하는 형식을 클릭합니다.

   ![](assets/create_format.png)

1. 다음 필드를 채웁니다.
   * **이름:**  (필수) 형식을 설명하는 이름을 입력합니다.
   * **유형:** (필수) 원하는 형식을 선택합니다.
      * **[!UICONTROL File]**: 파일을 통해 데이터를  [!DNL FTP] 전송합니다.
      * **[!UICONTROL HTTP]**: 래퍼에 데이터를  [!DNL JSON] 포함합니다.

1. (조건부) **[!UICONTROL File]**&#x200B;을 선택한 경우 다음 필드를 채웁니다.

   >[!NOTE]
   >
   >사용 가능한 매크로 목록을 보려면 [파일 형식 매크로](../formats/file-formats.md#concept_A867101505074418A58DE325949E5089) 및 [HTTP 형식 매크로](../formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE)를 참조하십시오.

   * **[!UICONTROL File Name]:** 데이터 전송 파일의 파일 이름을 지정합니다.
   * **헤더:** 데이터 전송 파일의 첫 번째 행에 표시되는 텍스트를 지정합니다.
   * **[!UICONTROL Data Row]** : 파일의 아웃바운드 행에 표시되는 텍스트를 지정합니다.
   * **[!UICONTROL Maximum File Size (In MB)]:** 데이터 전송 파일의 최대 파일 크기를 지정합니다. 압축된 파일은 100MB보다 작아야 합니다. 압축되지 않은 파일 크기에는 제한이 없습니다.
   * **[!UICONTROL Compression]:** 원하는 압축 유형을 선택합니다. 데이터 파일의 gz 또는 zip. [!UICONTROL AWS S3]에 배달하려면 .gz 또는 압축되지 않은 파일을 사용해야 합니다.
   * **[!UICONTROL .info Receipt]** : 전송 제어([!DNL .info]) 파일이 생성되도록 지정합니다. [!DNL .info] 파일은 Audience Manager이 처리된 파일이 올바르게 전송되는지 파트너가 확인할 수 있도록 파일 전송에 대한 메타데이터 정보를 제공합니다. 자세한 내용은 [로그 파일 전송을 위한 전송 제어 파일](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/transfer-control-files.html?lang=en)을 참조하십시오.
   * **[!UICONTROL MD5 Checksum Receipt]:** 체크섬  [!DNL MD5] 영수증을 생성하도록 지정합니다. 파트너가 전체 전송을 올바르게 처리했는지 확인할 수 있도록 [!DNL MD5] 체크섬 확인.

1. (조건부) **[!UICONTROL HTTP]**&#x200B;을 선택한 경우 다음 필드를 채웁니다.

   * **[!UICONTROL Method]:** 전송  [!DNL API] 프로세스에 사용할 방법을 선택합니다.
      * **[!UICONTROL POST]** :  [!DNL POST]을 선택하는 경우 컨텐츠 유형([!DNL XML]  또는  [!DNL JSON])을 선택한 다음, 요청 본문을 지정합니다.
      * **[!UICONTROL GET]:** 선택하는 경우  [!DNL GET]쿼리 매개 변수를 지정합니다.

1. 새 형식을 만드는 경우 **[!UICONTROL Create]** 을 클릭하고, 기존 형식을 편집하는 경우 **[!UICONTROL Save Updates]** 를 클릭합니다.

## 형식 삭제 {#delete-format}

1. 클릭 **[!UICONTROL Formats]**.
2. 원하는 형식의 **[!UICONTROL Actions]** 열에서 ![](assets/icon_delete.png) 을 클릭합니다.
3. **[!UICONTROL OK]** 을 클릭하여 삭제를 확인합니다.

---
description: Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.
seo-description: Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.
seo-title: 대상 설정 문제 해결
title: 대상 설정 문제 해결
uuid: 04080 FB 9-6 C 7 B -4 DE 7-960 E -54482 BE 2 DE 83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee

---


# 대상 설정 문제 해결 {#destination-setup-troubleshooting}

Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.

## 대상을 설정했는데 파일이 표시되지 않았습니다. 어디에 있습니까? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

일반적인 대상 구성 문제에는 다음과 같은 문제가 포함됩니다.

### 잘못 구성된 대상

* **[!UICONTROL UserID]잘못된 키:** [!UICONTROL UserID] 키는 이 대상의 대상이며, 경계를 벗어나는 [!UICONTROL MasterDPID] ID 값에 대한 기준입니다. 드롭다운 목록을 통해 [!UICONTROL UserID] 키를 선택할 수 있더라도 이 값에 매핑된 ID/트레이트가 있음을 의미하지는 않습니다. 프로세스 (대상이 만들어진 후 실행되는 [!UICONTROL Outbound] 프로세스) 가 이 [!UICONTROL UserID] 키에 매핑된 사용자를 찾지 못하면 데이터가 제한되지 않습니다.
* **NO IN FILE DATA SOURCES SELECTED:** 다른 [!UICONTROL S2S]대상 유형을 선택할 때 레이블이 지정된 화면 하단에 섹션이 나타납니다 [!UICONTROL Configure Data Sources]. 이 섹션이 처음 나타나면 값이 선택되지 않습니다. [!UICONTROL All First Party] 확인란을 클릭하거나 [!UICONTROL Available Data Sources] 창에서 데이터 소스를 개별적으로 선택하는 경우 데이터가 제한되지 않습니다.

### 잘못된 형식

전공 데이터 형식을 선택할 때 기존 형식을 다시 사용하는 것이 가장 좋습니다. 이미 입증된 포맷을 사용하면 아웃바운드 데이터가 성공적으로 생성됩니다. 기존 포맷의 형식을 정확하게 확인하려면 메뉴 모음에서 [!UICONTROL Formats] 옵션을 클릭하고 이름이나 ID 번호별로 형식을 검색합니다. 형식에서 형식이 잘못된 형식이나 매크로를 사용하면 서식이 잘못 지정된 출력이 제공되거나 정보가 완전히 출력되지 않습니다.

포맷 설정 및 매크로 사용에 대한 자세한 내용은 [파일 포맷 매크로](formats/file-formats.md#) 및 [HTTP 포맷 매크로를 참조하십시오](formats/web-formats.md).

### 잘못 구성된 서버

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 호스트 이름에 접두사를 입력하지 마십시오. 계정이 [!DNL ftp://hello.com]주어지면 이 필드에 입력합니다 [!DNL hello.com] .
   * **[!UICONTROL Port/Type Combination]**
      * [!DNL FTP] 전송에 대해 기본 전송 유형은 [!DNL SFTP]입니다.
      * [!DNL SFTP] 유형을 선택할 때 포트는 거의 항상 22 입니다.
      * [!DNL FTPs/TLS] 유형을 선택할 때 포트는 거의 항상 21 입니다.
      * [!DNL FTPs/TLS] 이 유형은 일반 [!DNL FTP] 양식과 다릅니다. Adobe는 일반 (비보안) [!DNL FTP] 양도를 지원하지 않습니다.
   * **[!UICONTROL Remote Path]**
      * 원격 하위 경로를 선택할 때는 맨 앞의 슬래시 없이 입력해야 합니다.
      * 전송된 파일을 [!DNL (root)/inbound] 하위 폴더에 배치해야 하는 경우 원격 경로에 [!DNL inbound] 대해서만 추가하면 [!DNL /inbound]됩니다.
      * 여러 디렉토리를 경로로 보낼 경우 각 디렉토리 사이에 슬래시를 입력합니다. 위치가 주어지면 [!DNL /inbound/subdirectory1/subdirectory2]이 필드에 입력해야 [!DNL inbound/subdirectory1/subdirectory2] 합니다.
      * 파일을 외부 서버에 의해 자동으로 라우팅되는 디렉토리에 배치해야 하는 경우 이 공간을 비워 둘 수 있습니다. 마침표 (. ), 슬래시 (/) 또는 기타 모든 것

* **[!DNL S3]**
   * [!DNL S3] 는 기본 전송 프로토콜 (over [!DNL FTP] or [!DNL HTTP]) 입니다.
      * **[!UICONTROL Bucket]**
         * 버킷 이름은 슬래시, 접두어, 접미어 등이 없어야 합니다. 이 필드에 추가하기만 [!DNL s3://your-bucket][!DNL your-bucket] 하면 됩니다.
      * **[!UICONTROL Directory]**
         * 데이터가 배치될 하위 디렉토리를 구체적으로 지정하지 않은 경우 이 필드를 비워 두십시오. 주소를 [!DNL s3://your-bucket/your-subdirectory]받은 경우 필드에 입력하면 [!DNL your-bucket][!UICONTROL Bucket][!DNL your-subdirectory][!UICONTROL Directory] 필드에 추가해야 합니다. 이전 슬래시를 추가하지 마십시오.
         * 경로 아래로 여러 디렉토리를 이동해야 하는 경우 슬래시를 구분 문자로 사용해야 합니다. 따라서 필드의 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 위치가 [!DNL your-bucket][!UICONTROL Bucket] 필드에 입력되어 [!DNL your-subdirectory1/your-subdirectory2][!UICONTROL Directory] 필드에 입력됩니다.
      * **[!UICONTROL Access / Secret Keys]**
         * 에서 [!DNL TechOps] 버킷을 만들고 컨설턴트에 액세스/비밀 키를 제공하는 경우 이러한 자격 증명은 일반적으로 `READ-ONLY` 클라이언트로 전달되어야 하는 자격 증명입니다. 이러한 자격 증명을 [!UICONTROL Access / Secret Key] 필드에 입력하면 안 됩니다. 이러한 자격 증명은 읽기 전용이며 쓰기 가능하지 않기 때문에 전송이 실패하게 됩니다. 버킷을 [!DNL TechOps] 만들고 자격 증명을 제공하는 경우 컨설턴트는 이 버킷에 파일을 쓸 수 있도록 Adobe 키 쌍을 클라이언트에 요청하지 않아야 합니다. 이 키는 이러한 필드에 추가해야 합니다.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 항목에 대한 접두사 정보를 [!DNL HTTP] 입력합니다. 계정이 [!DNL https://superduper.com]주어지면 이 필드에 [!DNL https://superduper.com] 입력합니다.
      * **[!UICONTROL URL Prefix]**
         * [!DNL URL] 접두사를 추가할 때는 위의 슬래시 표시를 끕니다. 필드에 [!DNL https://hello.com/r/x/y/z][!DNL https://hello.com] 입력한 주소가 필드에 [!UICONTROL Domain][!DNL r/x/y/z] 입력되어 [!UICONTROL URL Prefix] 있어야 합니다.
         * if a is [!UICONTROL URL Prefix] not need, leave this value blank.
      * **[!UICONTROL Authentication - SSH Key]**
         * 정확한 암호화/키 저장을 위해 머리글, 바닥글 및 줄 바꿈을 포함하여 이 상자에 전체 `SSH PRIVATE` 키 값을 입력합니다.

### 아웃바운드 생성을 위한 충분한 시간 아님

outbounding 프로세스는 하루에 두 번 실행되며, 여러 프로세스 (outborder, publishing, push to external locations 등) 는 파일을 최종 대상에 푸시하기 전에 실행해야 합니다. 올바른 규칙은 데이터가 외부 위치로 푸시되도록 하기 전에 적어도 24 시간 전에 대상을 완전히 구성해야 한다는 것입니다.

### 파일 분할 크기가 너무 큽니다.

대상으로 파일을 보낼 때 더 큰 아웃바운드 파일을 파일 청크로 분할할 수 있습니다. 개별 파일 청크는 10 GB를 초과하지 않아야 합니다. [아웃바운드 데이터 파일 이름 참조: 구문 및 예입니다](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## 아웃바운드 데이터 파일에서 Experience Cloud ID, 고객 ID 또는 Audience Manager ID 내보내기 대상을 설정하는 방법 {#set-up-destinations-export}

이 페이지에서는 원하는 ID 유형에서 데이터를 키잉할 대상을 설정하는 대상을 설정하는 방법을 보여줍니다 [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

고객은 고객을 대상으로 디지털 채널을 통해 데이터를 활성화할 수 있습니다. 예를 들어, 고객 데이터를 다른 [!DNL Adobe Experience Cloud] 솔루션 ([!DNL Target], [!DNL Campaign]등) 로 내보낼 수 있습니다. 또는 Audience Manager와 [!UICONTROL DSP][!UICONTROL SSP]통합된 모든 플랫폼에 데이터를 보낼 수 있습니다. Adobe는 통합 Wiki 페이지에서 협력하는 파트너 [목록을 보관합니다](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>관리 UI에서 대상을 만드는 방법에 대한 자세한 연습을 보려면 회사 [대상](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 만들기 또는 편집 아티클을 참조하십시오.

고객은 대상에 따라 다른 ID 유형을 내보내고자 합니다. 아래의 구성 차트는 다른 ID 유형과 관련된 프로필 정보를 내보내도록 선택해야 하는 옵션을 보여줍니다. Audience Manager의 ID [색인을 참조하는](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html)것이 좋습니다. 고려해야 할 중요한 설정은 세 [!UICONTROL User ID Key][!UICONTROL Data Source Type][!UICONTROL Format]가지가 있습니다. Adobe는 아래의 모든 사항을 자세히 설명합니다.

* [!UICONTROL User ID Key] 구문을 사용하는 키-값 쌍으로 전달됩니다. [!UICONTROL Admin UI]**[!UICONTROL Companies]**&#x200B;에서로 이동합니다. 고객 회사를 검색하여 클릭합니다. **[!UICONTROL Destinations]** 탭을 찾아 **[!UICONTROL Add Destination]**&#x200B;누릅니다. **[!UICONTROL Add Destination]** 워크플로우에서 [!UICONTROL User ID Key]를 선택합니다. 는 [!UICONTROL User ID Key] Target 데이터 소스에서 들어오는 ID를 필터링하고 ID만 전달하도록 허용합니다.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type] 구문을 사용하는 키-값 쌍으로 전달됩니다. Audience Manager UI에서 대상을 만들 때 이 옵션을 선택합니다. 먼저, 선택한 [!UICONTROL Inbound]다음 원하는 ID 유형을 선택합니다. 옵션은 다음과 같습니다.

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format] 구문을 사용하는 키-값 쌍으로 전달됩니다. 이 옵션은 내보낼 파일 형식을 결정합니다. **[!UICONTROL Add Destination]** 워크플로우에서 **[!UICONTROL Batch Data]**&#x200B;형식을 선택합니다.

형식을 검사하려면 해당 요소를 **[!UICONTROL Admin UI > Formats]** 찾아 [!UICONTROL Data Row] 찾습니다. This element contains a macro of the file format, &lt; mcid &gt; in the example below.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 구성 아니요. </th> 
   <th colname="col1" class="entry"> <p>사용자 키 </p> </th> 
   <th colname="col2" class="entry"> <p>데이터 소스 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>형식 </p> </th> 
   <th colname="col4" class="entry"> <p>내보낸 ID 유형 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt; dp_ uuid &gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt; dp_ uuid &gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID (회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>&lt; dp_ uuid &gt; </p> </td> 
   <td colname="col4"> <p>고객 ID (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID (회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID (회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Customer ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID (회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt; dp_ uuid &gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID (회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID (회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용 사례

Audience Manager 와 [!DNL Campaign] 고객 데이터를 실행 가능한 상태로 만들려면 [!DNL Campaign][!UICONTROL Experience Cloud IDs]내보내기를 수행합니다. 이 경우 구성 번호 3를 사용해야 합니다.
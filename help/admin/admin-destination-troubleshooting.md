---
description: Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.
seo-description: Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.
seo-title: 대상 설정 문제 해결
title: 대상 설정 문제 해결
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
translation-type: tm+mt
source-git-commit: 118e8fa3f35bc77846c6518268448d57d779a2ee
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 4%

---


# 대상 설정 문제 해결 {#destination-setup-troubleshooting}

Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.

## 목적지를 설정했지만 파일이 하나도 없습니다. 해당 세그먼트는 어디 있습니까? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

일반적인 대상 구성 문제는 다음과 같습니다.

### 잘못 구성된 대상

* **잘못된[!UICONTROL UserID]키:** 키 [!UICONTROL UserID] 는 이 [!UICONTROL MasterDPID] 대상의 개념이며, 범위를 벗어나는 ID 값의 기준입니다. 드롭다운 목록을 통해 [!UICONTROL UserID] 키를 선택할 수 있더라도 이 값에 매핑된 ID/트레이트/세그먼트가 있다는 의미는 아닙니다. 대상을 만든 후에 실행되는 [!UICONTROL Outbound] 프로세스가 이 키에 매핑된 사용자를 찾지 못하면 데이터가 [!UICONTROL UserID] 아웃바운드되지 않습니다.
* **선택한 파일 데이터 소스 없음:** 다른 대상 유형을 선택할 때 [!UICONTROL S2S]는 레이블이 지정된 화면 하단에 섹션이 나타납니다 [!UICONTROL Configure Data Sources]. 이 섹션이 처음 나타나면 선택한 값이 없습니다. 확인란을 클릭하지 않거나 [!UICONTROL All First Party] 창에서 데이터 소스를 개별적으로 선택하지 않으면 데이터가 [!UICONTROL Available Data Sources] 아웃바운드되지 않습니다.

### 잘못 구성된 형식

경계 데이터의 형식을 선택할 때는 기존 형식을 다시 사용하는 것이 좋습니다. 이미 검증된 형식을 사용하면 아웃바운드 데이터가 성공적으로 생성됩니다. 기존 포맷의 형식을 정확하게 확인하려면 메뉴 모음에서 [!UICONTROL Formats] 옵션을 클릭하고 이름이나 ID 번호로 형식을 검색합니다. 형식이 잘못된 형식 또는 매크로는 형식이 잘못된 출력을 제공하거나 정보가 완전히 출력되지 않도록 합니다.

서식 설정 및 매크로 사용에 대한 자세한 내용은 [파일 형식 매크로](formats/file-formats.md#) 및 [HTTP 형식 매크로](formats/web-formats.md)를 참조하십시오.

### 잘못 구성된 서버

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 호스트 이름에 접두사를 입력하지 마십시오. 계정 [!DNL ftp://hello.com]을 부여받은 경우 이 [!DNL hello.com] 필드에 입력하기만 하면 됩니다.
   * **[!UICONTROL Port/Type Combination]**
      * 양도의 경우 [!DNL FTP] 기본 양도 유형이 사용됩니다 [!DNL SFTP].
      * 유형을 선택할 때 [!DNL SFTP] 포트는 거의 항상 22입니다.
      * 유형을 선택할 때 [!DNL FTPs/TLS] 포트는 거의 항상 21입니다.
      * 이 [!DNL FTPs/TLS] 유형은 일반 [!DNL FTP] 전송과 같지 않습니다. Adobe는 일반(비보안) 전송을 지원하지 않습니다 [!DNL FTP] .
   * **[!UICONTROL Remote Path]**
      * 원격 하위 경로를 선택할 때는 슬래시 없이 입력해야 합니다.
      * 전송된 파일을 하위 폴더에 [!DNL (root)/inbound] 배치하려면 원격 경로 [!DNL inbound] 에 대해 추가만 하면 됩니다 [!DNL /inbound].
      * 파일을 경로에 여러 개의 디렉토리를 전송하는 경우 각 디렉토리 사이에 슬래시를 입력합니다. 위치 정보를 받은 경우 이 필드 [!DNL /inbound/subdirectory1/subdirectory2]에 [!DNL inbound/subdirectory1/subdirectory2] 입력해야 합니다.
      * 외부 서버에 의해 자동으로 라우팅되는 디렉토리에 파일을 배치해야 하는 경우 이 공백을 비워 둘 수 있습니다. 마침표( . ), 슬래시( / ), 기타 모든 것.

* **[!DNL S3]**
   * [!DNL S3] 는 기본 전송 프로토콜(over [!DNL FTP] 또는 [!DNL HTTP])입니다.
      * **[!UICONTROL Bucket]**
         * 버킷 이름에는 슬래시, 접두어, 접미어 등이 없어야 합니다. 주소를 받은 경우 이 필드 [!DNL s3://your-bucket] 에 간단히 추가해야 [!DNL your-bucket] 합니다.
      * **[!UICONTROL Directory]**
         * 데이터를 배치할 하위 디렉토리를 특별히 지정하지 않으면 이 필드를 비워 둡니다. 주소를 받은 경우 [!DNL s3://your-bucket/your-subdirectory]필드에 [!DNL your-bucket][!UICONTROL Bucket] 을 입력하고 [!DNL your-subdirectory] 필드에 [!UICONTROL Directory] 추가해야 합니다. 앞의 슬래시를 추가하지 마십시오.
         * 경로를 따라 여러 개의 디렉토리를 이동해야 하는 경우에는 슬래시를 구분 문자로 사용해야 합니다. 따라서 필드 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 에 위치 [!DNL your-bucket] 가 있고 [!UICONTROL Bucket] 필드에 [!DNL your-subdirectory1/your-subdirectory2] 입력될 수 [!UICONTROL Directory] 있습니다.
      * **[!UICONTROL Access / Secret Keys]**
         * 버킷을 [!DNL TechOps] `READ-ONLY` 만들고 컨설턴트에게 액세스/비밀 키를 제공하면 이러한 자격 증명은 일반적으로 클라이언트에 전달되어야 하는 자격 증명입니다. 이 자격 증명은 읽기 전용이므로 [!UICONTROL Access / Secret Key] 필드에 입력할 수 없습니다. 이 경우 전송 실패가 발생합니다(해당 자격 증명은 쓰기 불가능하므로). 버킷을 만들고 자격 증명을 제공하는 경우 컨설턴트는 또한 Adobe 키 쌍(클라이언트에 제공되지 않음)을 요청해야 하며, 이 버킷에 파일을 작성할 수 있습니다. [!DNL TechOps] 이 필드에 해당 키를 추가해야 합니다.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 항목의 접두사 정보를 [!DNL HTTP] 입력하십시오. 계정 [!DNL https://superduper.com]을 부여받은 경우 이 [!DNL https://superduper.com] 필드에 입력합니다.
      * **[!UICONTROL URL Prefix]**
         * 접두사를 추가할 때 [!DNL URL] 앞의 슬래시를 두십시오. 주소를 [!DNL https://hello.com/r/x/y/z] 필드에 [!DNL https://hello.com] 입력하고 여기에 [!UICONTROL Domain] 입력했어야 [!DNL r/x/y/z] 합니다 [!UICONTROL URL Prefix] .
         * If a [!UICONTROL URL Prefix] is not required, leave this value.
      * **[!UICONTROL Authentication - SSH Key]**
         * 정확한 암호화/키 저장을 위해 머리글, 바닥글 및 줄 바꿈을 포함하여 이 상자에 전체 `SSH PRIVATE` 키 값을 입력합니다.

### 아웃바운드 생성 시간이 부족합니다.

아웃경계 프로세스는 하루에 두 번 실행되며 여러 프로세스(경계, 게시, 외부 위치로 푸싱 등)가 파일을 최종 대상으로 푸시하기 전에 실행해야 합니다. 경험상 적절한 규칙은 데이터가 외부 위치로 푸시될 것으로 예상하기 전에 적어도 24시간 전에 대상을 완전히 구성해야 한다는 것입니다.

### 파일 분할 크기가 너무 큼

대상에 대한 경계 파일을 내보낼 때 대용량 아웃바운드 파일을 파일 단위로 분할할 수 있습니다. 개별 파일 청크가 10GB를 초과하지 않도록 하십시오. See also, [Outbound Data File Name: Syntax and Examples](https://docs.adobe.com/help/en/audience-manager/user-guide/implemenation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html).


## 아웃바운드 데이터 파일에서 Experience Cloud ID, 고객 ID 또는 Audience Manager ID를 내보낼 대상을 설정하는 방법 {#set-up-destinations-export}

This page shows you how to set up destinations to export data keyed off the ID type you want in [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

목적지는 고객이 다양한 디지털 채널에서 데이터를 활성화할 수 있도록 허용합니다. 예를 들어 대상 데이터를 다른 [!DNL Adobe Experience Cloud] 솔루션([!DNL Target], [!DNL Campaign]등)으로 내보낼 수 있습니다. 또는 Audience Manager과 통합된 [!UICONTROL DSP]모든 플랫폼 [!UICONTROL SSP]으로 데이터를 전송할 수 있습니다. 통합 [Wiki 페이지에 파트너 목록이 있습니다](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>관리자 UI에서 대상을 만드는 방법에 대한 자세한 설명은 회사 대상 [만들기 또는 편집 문서를](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 참조하십시오.

고객은 대상에 따라 다양한 ID 유형을 내보내려고 합니다. 아래 구성 차트는 다양한 ID 유형과 관련된 프로필 정보를 내보내기 위해 선택해야 하는 옵션을 보여줍니다. Audience Manager의 ID [색인도 참조하는 것이 좋습니다](https://marketing.adobe.com/resources/help/en_US/aam/ids-in-aam.html). 고려해야 할 세 가지 중요한 설정, [!UICONTROL User ID Key]the, [!UICONTROL Data Source Type] and [!UICONTROL Format]the 우리는 그 모든 것들을 아래와 같이 자세히 기술한다.

* [!UICONTROL User ID Key]. In the [!UICONTROL Admin UI]go to **[!UICONTROL Companies]**. 고객의 회사를 검색하여 클릭합니다. 탭을 찾아 **[!UICONTROL Destinations]** 누릅니다 **[!UICONTROL Add Destination]**. 워크플로우에서 **[!UICONTROL Add Destination]** 을 선택합니다 [!UICONTROL User ID Key]. 대상 데이터 소스에서 들어오는 ID를 필터링하고 ID만 전달하도록 [!UICONTROL User ID Key] 합니다.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Audience Manager UI에서 대상을 만들 때 선택합니다. 먼저 선택한 다음 원하는 ID 유형 [!UICONTROL Inbound]을 선택합니다. 옵션은 다음과 같습니다.

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. 이 옵션은 내보낼 파일 형식을 결정합니다. 워크플로우의 **[!UICONTROL Add Destination]** 아래에서 형식 **[!UICONTROL Batch Data]**&#x200B;을 선택합니다.

포맷을 검사하려면 해당 요소 **[!UICONTROL Admin UI > Formats]** 로 이동하여 [!UICONTROL Data Row] 찾습니다. 이 요소에는 아래 예제의 &lt;MCID> 파일 형식의 매크로가 포함되어 있습니다.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 구성 번호. </th> 
   <th colname="col1" class="entry"> <p>사용자 키 </p> </th> 
   <th colname="col2" class="entry"> <p>데이터 소스 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>형식 </p> </th> 
   <th colname="col4" class="entry"> <p>내보낸 ID 유형 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager(0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID(회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>고객 ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID(회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID(회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID(회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID(회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID(회사가 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용 사례

Audience Manager을 사용하고 있다고 가정해 봅시다 [!DNL Campaign]. 고객 데이터를 실행 가능하도록 하려면 내보내기를 [!DNL Campaign]선택합니다 [!UICONTROL Experience Cloud IDs]. 이 경우 구성 번호 3을 사용해야 합니다.
---
description: Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: 대상 설정 문제 해결
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# 대상 설정 문제 해결 {#destination-setup-troubleshooting}

Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.

## 대상을 설정했는데 파일이 없습니다. 해당 세그먼트는 어디 있습니까? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

일반적인 대상 구성 문제에는 다음 문제가 포함됩니다.

### 잘못 구성된 대상

* **잘못됨 [!UICONTROL UserID] 키:** 다음 [!UICONTROL UserID] 키: [!UICONTROL MasterDPID] 및 는 아웃바운드 ID 값의 기초입니다. 다음과 같은 경우에도 [!UICONTROL UserID] 드롭다운 목록을 통해 키를 선택할 수 있지만, 반드시 이 값에 매핑된 ID/트레이트/세그먼트가 있음을 의미하지는 않습니다. 다음과 같은 경우 [!UICONTROL Outbound] 대상이 만들어진 후 실행되는 프로세스에서 이 작업에 매핑된 사용자를 찾을 수 없습니다. [!UICONTROL UserID] 키, 데이터 유출을 막을 수 없습니다.
* **선택한 파일 데이터 소스에 없음:** 이외의 대상 유형을 선택할 때 [!UICONTROL S2S], 화면 하단에 레이블이 지정된 섹션이 나타납니다 [!UICONTROL Configure Data Sources]. 이 섹션이 처음 나타나면 값이 선택되지 않습니다. 을(를) 클릭하는 것을 잊은 경우 [!UICONTROL All First Party] 확인란을 선택하거나 다음에서 데이터 소스를 개별적으로 선택합니다. [!UICONTROL Available Data Sources] 창, 아웃바운드 데이터는 없습니다.

### 잘못된 포맷

아웃바운드된 데이터의 형식을 선택할 때는 가능하면 기존 형식을 다시 사용하는 것이 좋습니다. 이미 검증된 형식을 사용하면 아웃바운드 데이터가 성공적으로 생성됩니다. 기존 형식의 서식을 정확하게 확인하려면 [!UICONTROL Formats] 메뉴 모음의 옵션을 선택하고 이름 또는 ID 번호로 형식을 검색합니다. 형식에 사용된 형식이 잘못된 형식 또는 매크로는 잘못된 형식의 출력을 제공하거나 정보가 완전히 출력되지 않도록 합니다.

형식 설정 및 매크로 사용에 대한 자세한 내용은 [파일 형식 매크로](formats/file-formats.md#) 및 [HTTP 형식 매크로](formats/web-formats.md).

### 잘못 구성된 서버

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 호스트 이름에 접두사를 입력하지 마십시오. 계정이 있는 경우 [!DNL ftp://hello.com], 간단히 입력 [!DNL hello.com] 이 필드에서 을(를) 참조하십시오.
   * **[!UICONTROL Port/Type Combination]**
      * 의 경우 [!DNL FTP] 이전, 기본 전송 유형은 다음과 같습니다. [!DNL SFTP].
      * 을(를) 선택할 때 [!DNL SFTP] 를 입력하면 포트는 거의 항상 22입니다.
      * 을(를) 선택할 때 [!DNL FTPs/TLS] 를 입력하면 포트는 거의 항상 21입니다.
      * 다음 [!DNL FTPs/TLS] 유형이 일반과 다릅니다. [!DNL FTP] 전송. 일반(비보안)은 지원하지 않습니다. [!DNL FTP] 전송.
   * **[!UICONTROL Remote Path]**
      * 원격 하위 경로를 선택할 때는 앞에 슬래시 없이 입력해야 합니다.
      * 전송된 파일이 [!DNL (root)/inbound] 하위 폴더, 간단히 추가 [!DNL inbound] 원격 경로용(아님) [!DNL /inbound].
      * 여러 디렉토리를 경로에 전송하는 경우 각 디렉토리 사이에 슬래시를 입력합니다. 의 위치가 지정되면 [!DNL /inbound/subdirectory1/subdirectory2]을 입력하여 다음을 수행해야 합니다. [!DNL inbound/subdirectory1/subdirectory2] 이 필드에서 을(를) 참조하십시오.
      * 파일을 외부 서버에서 자동으로 라우팅되는 디렉토리에 배치해야 하는 경우 이 공백을 비워 둘 수 있습니다. 마침표( )를 입력하지 마십시오. ), 슬래시( / ) 또는 기타 다른 형식으로 프로필 스크립트에서 참조할 수 있습니다.

* **[!DNL S3]**
   * [!DNL S3] 기본 전송 프로토콜입니다( [!DNL FTP] 또는 [!DNL HTTP]).
      * **[!UICONTROL Bucket]**
         * 버킷 이름에는 슬래시, 접두사, 접미사 등이 없어야 합니다. 주소를 알고 계시면 [!DNL s3://your-bucket] 다음을 추가하기만 하면 됩니다 [!DNL your-bucket] 이 필드에 전송됩니다.
      * **[!UICONTROL Directory]**
         * 데이터를 배치해야 하는 하위 디렉토리가 구체적으로 제공되지 않는 한 이 필드를 비워 둡니다. 주소를 알고 계시면 [!DNL s3://your-bucket/your-subdirectory], 입력 [!DNL your-bucket] 다음에서 [!UICONTROL Bucket] 필드 및 [!DNL your-subdirectory] 을(를) 다음에 추가해야 합니다. [!UICONTROL Directory] 필드. 이전 슬래시를 추가하지 마십시오.
         * 경로를 따라 여러 디렉토리를 이동해야 하는 경우에는 슬래시를 구분 기호로 사용해야 합니다. 위치: [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 이(가) 다음을 가질 수 있습니다. [!DNL your-bucket] 다음에서 [!UICONTROL Bucket] 필드 및 [!DNL your-subdirectory1/your-subdirectory2] 에 입력됨 [!UICONTROL Directory] 필드.
      * **[!UICONTROL Access / Secret Keys]**
         * 날짜 [!DNL TechOps] 버킷을 만들고 컨설턴트에게 액세스/비밀 키를 제공합니다. 이러한 자격 증명은 일반적으로 다음과 같습니다. `READ-ONLY` 클라이언트에게 전달될 자격 증명입니다. 이러한 자격 증명을 [!UICONTROL Access / Secret Key] 필드를 만들 수 있습니다. 이 경우 전송이 실패합니다(해당 자격 증명이 읽기 전용이며 쓰기 가능하지 않기 때문). 다음의 경우에 [!DNL TechOps] 버킷을 만들고 자격 증명을 제공합니다. 컨설턴트는 이 버킷에 파일을 작성할 수 있는 Adobe 키 쌍(클라이언트에 제공되지 않음)도 요청해야 합니다. 해당 키를 이러한 필드에 추가해야 합니다.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * 다음에 대한 접두사 정보 입력 [!DNL HTTP] 항목. 계정이 있는 경우 [!DNL https://superduper.com], 입력 [!DNL https://superduper.com] 이 필드에서 을(를) 참조하십시오.
      * **[!UICONTROL URL Prefix]**
         * 를 추가할 때 [!DNL URL] 접두사, 앞에 있는 슬래시를 해제하십시오. 주소 [!DNL https://hello.com/r/x/y/z] 이(가) 있어야 함 [!DNL https://hello.com] 다음에 입력됨: [!UICONTROL Domain] 필드 및 [!DNL r/x/y/z] 다음에 입력함: [!UICONTROL URL Prefix] 필드.
         * 다음과 같은 경우 [!UICONTROL URL Prefix] 가 필요하지 않습니다. 이 값을 비워 두십시오.
      * **[!UICONTROL Authentication - SSH Key]**
         * 전체 입력 `SSH PRIVATE` 정확한 암호화/키 저장을 위해 머리글, 바닥글 및 줄 바꿈을 포함한 이 상자의 키 값입니다.

### 아웃바운드 생성에 필요한 시간이 충분하지 않음

아웃바운드 프로세스는 매일 두 번 실행되며, 여러 프로세스(아웃바운드, 게시, 외부 위치로 푸시 등) 은(는) 파일을 최종 대상으로 푸시하기 전에 실행해야 합니다. 일반적으로 최소 24시간 전에 대상을 완전히 구성해야 데이터가 외부 위치로 푸시될 수 있습니다.

### 파일 분할 크기가 너무 큼

파일을 대상으로 아웃바운딩할 때 큰 아웃바운드 파일을 파일 청크로 분할할 수 있습니다. 개별 파일 청크가 10GB를 초과하지 않도록 합니다. 다음을 참조하십시오. [아웃바운드 데이터 파일 이름: 구문 및 예](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## 아웃바운드 데이터 파일에서 Experience Cloud ID, 고객 ID 또는 Audience Manager ID를 내보내도록 대상을 설정하는 방법 {#set-up-destinations-export}

이 페이지에서는 원하는 ID 유형의 데이터를 내보내는 대상을 설정하는 방법을 보여 줍니다 [!UICONTROL Outbound Data Files].

<!-- set-up-destinations-mcid-aamid.xml -->

대상은 고객이 다양한 디지털 채널에서 데이터를 활성화할 수 있습니다. 예를 들어 대상 데이터를 다른 대상으로 내보낼 수 있습니다 [!DNL Adobe Experience Cloud] 솔루션 ([!DNL Target], [!DNL Campaign]등). 또는 로 데이터를 전송할 수 있습니다. [!UICONTROL DSP]s, [!UICONTROL SSP]s 또는 Audience Manager과 통합된 모든 플랫폼. 우리는 함께 일하는 파트너 목록을 [통합 Wiki 페이지](https://wiki.corp.adobe.com/display/MCPI).

>[!NOTE]
>
>관리 UI에서 대상을 만드는 방법에 대한 자세한 내용은 [회사 대상 만들기 또는 편집](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 기사.

고객은 대상에 따라 다른 ID 유형을 내보내고 싶어합니다. 아래 구성 차트에서는 다른 ID 유형과 관련된 프로필 정보를 내보내기 위해 선택해야 하는 옵션을 보여 줍니다. 또한 다음을 참조하는 것이 좋습니다. [Audience Manager 내 ID 색인](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en). 고려해야 할 세 가지 중요한 설정이 있습니다. [!UICONTROL User ID Key], [!UICONTROL Data Source Type] 및 [!UICONTROL Format]. 우리는 아래에 그들 모두를 자세히 설명합니다.

* [!UICONTROL User ID Key]. 다음에서 [!UICONTROL Admin UI]로 이동합니다. **[!UICONTROL Companies]**. 고객의 회사를 검색하고 클릭합니다. 다음 항목을 찾습니다. **[!UICONTROL Destinations]** 탭하고 누르기 **[!UICONTROL Add Destination]**. 다음에서 **[!UICONTROL Add Destination]** 워크플로우에서 [!UICONTROL User ID Key]. 다음 [!UICONTROL User ID Key] 대상 데이터 소스에서 들어오는 ID를 필터링하고 ID만 전달할 수 있도록 합니다.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Audience Manager UI에서 대상을 만들 때 이 옵션을 선택합니다. 우선 다음을 선택합니다. [!UICONTROL Inbound]을(를) 클릭한 후 원하는 ID 유형을 선택합니다. 옵션은 다음과 같습니다.

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. 이 옵션은 내보낼 파일 형식을 결정합니다. 다음에서 **[!UICONTROL Add Destination]** 워크플로우, 아래 **[!UICONTROL Batch Data]**&#x200B;형식을 선택합니다.

형식을 검사하려면 **[!UICONTROL Admin UI > Formats]** 다음을 찾습니다. [!UICONTROL Data Row] 요소를 생성하지 않습니다. 이 요소는 파일 형식의 매크로를 포함합니다. &lt;mcid> 아래 예제에서.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 구성 번호 </th> 
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
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGER UUID </p> </td> 
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
   <td colname="col2"> <p>AUDIENCE MANAGER ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGER UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGER ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGER ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGER UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>고객 ID (DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGER UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGER ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGER UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGER ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>AUDIENCE MANAGER ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>AUDIENCE MANAGER UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용 사례

Audience Manager 및 [!DNL Campaign]. 에서 고객 데이터를 실용적으로 만들기 위해 [!DNL Campaign], 내보내려고 합니다. [!UICONTROL Experience Cloud IDs]. 이 경우 구성 번호 3을 사용해야 합니다.

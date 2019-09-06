---
description: HTTP 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. HTTP는 JSON 형식으로 데이터를 전송합니다.
seo-description: HTTP 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. HTTP는 JSON 형식으로 데이터를 전송합니다.
seo-title: HTTP 포맷 매크로
title: HTTP 포맷 매크로
uuid: 91021 f 60-75 d 0-4 b 1 d -86 ca -91 c 9 dadafac 1
translation-type: tm+mt
source-git-commit: 1a547e421346a6bf281e2b3ff3a0bcb5cf1d78df

---


# HTTP 포맷 매크로 {#http-format-macros}

데이터 파일을 만드는 [!DNL HTTP] 데 사용할 수 있는 매크로를 나열합니다. [!DNL HTTP] 형식으로 데이터를 [!DNL JSON] 전송합니다.

목록과 일반적으로 사용되는 일부 매크로 조합의 예는 [HTTP 형식 매크로 예제를](../formats/web-format-examples.md) 참조하십시오.

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 메서드 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>aam_ uuid</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> Audience Manager </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>dp_ uuid</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>데이터 파트너 고유 사용자 ID. 이 매크로는 ID가 <span class="keyword"> Audience Manager </span> 장치 ID와 이미 동기화된 경우 사용자에게 할당한 ID를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>dpid</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code>라고 합니다 </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>generation_ time</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>UNIX UTC 타임스탬프. 내부 타임스탬프는 AAM 이 S 2 대상을 <span class="wintitle"></span> 파트너에게 게시하라는 알림을 받았습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자의 IP 주소. </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID. (MCID는 Experience Cloud의 기존 이름인 Marketing Cloud를 나타냄) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>num_ removed_ segments</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 속해 있지 않은 세그먼트의 숫자 (정수) 입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>num_ segments</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 속하는 세그먼트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>order_ id</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>주문 또는 대상 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>pid_ alias</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>파트너 ID에 대한 별칭. 외국 계정 ID 라고도 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>임의</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>무작위 숫자를 생성합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>region_ id_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>활동이 시작된 <a href="https://docs.adobe.com/help/en/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html"> Audience </a> Manager DCS 지역입니다.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>removed_ segment_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 자격이 없는 세그먼트 ID의 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>removed_ segments</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 자격을 부여하지 않는 세그먼트 목록입니다. 다음을 포함한 특정 세그먼트 필드도 반환할 수 있습니다. </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>Traitalias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>Legacysegmentid (이전 segmentid)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>Newsegmentid</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>dateTime</code> </li> 
     </ul> </p> <p>다음 예와 같이 배열에서 이러한 필드를 지정합니다. </p> <p> <code>[&lt; removed_ segments: {seg|&lt; open_ bracket &gt; "매핑": &lt; seg. traitalias &gt;, "status: " &lt; seg. status &gt;, "time": &lt; seg. dateTime &gt; "legacysegmentid": &lt; seg. legacysegmentid &gt; "newsegmentid": &lt; seg. newsegmentid &gt; &lt; close_ bracket &gt;}; " separator = "," &gt;]</code> </p> <p>HTTP 포맷 매크로 예제도 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"></a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>removed_ time_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> 사용자가 더 이상 자격을 부여하지 않는 세그먼트에 대한 마지막 개요 목록입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>removed_ traitalias_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 자격을 부여하지 않는 세그먼트의 별칭이 지정된 이름 목록입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>segment_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>세그먼트 ID 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>세그먼트</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 자격을 갖춘 세그먼트 목록입니다. 다음을 포함한 특정 세그먼트 필드도 반환할 수 있습니다. </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>Traitalias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>Legacysegmentid (이전 segmentid)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>Newsegmentid</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>dateTime</code> </li> 
     </ul> </p> <p>다음 예와 같이 배열에서 이러한 필드를 지정합니다. </p> <p> <code>[&lt; 세그먼트: {seg|&lt; open_ bracket &gt; "매핑": &lt; seg. traitalias &gt;, "status: " &lt; seg. status &gt;, "time": &lt; seg. dateTime &gt; "legacysegmentid": &lt; seg. legacysegmentid &gt; "newsegmentid": &lt; seg. newsegmentid &gt; &lt; close_ bracket &gt;}; " separator = "," &gt;]</code> </p> <p>HTTP 포맷 매크로 예제도 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"></a>참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>time_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>마지막 realizations 목록입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>timestamp</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>UNIX, UTC 타임스탬프. 세그먼트에 대한 마지막 구현을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>traitalias_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>특정 세그먼트에 대한 별칭이 있는 이름 목록입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>user_ agent</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자 에이전트의 사용자 에이전트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>user_ list</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p><span class="keyword"> Audience Manager </span> 사용자 ID 목록입니다. 다음을 포함하는 특정 필드를 반환할 수도 있습니다. </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user. aamuuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user. dpuuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user. segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user. removedsegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user. useragent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user. ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user. dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user. timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user. random</code> </li>
     <li><code>user. regionid</code></li> 
    </ul> <p>다음 예와 같이 이러한 필드를 지정합니다. </p> <p> 
     <codeblock>
       " aam_ uuid ": " &lt; user. aamuuid &gt; "" 
datapartner_ uuid ": " &lt; user. dpuuid &gt; " 
     </codeblock> </p> <p>전체 예제는 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP 형식 매크로 예제도 </a> 참조하십시오. </p> </td> 
  </tr>
 </tbody>
</table>
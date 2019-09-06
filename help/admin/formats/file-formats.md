---
description: FTP 기반 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. 일부 매크로는 모든 데이터 파일 필드 및 행에 사용할 수 있습니다. 다른 매크로는 헤더 및 데이터 행에만 고유합니다.
seo-description: FTP 기반 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. 일부 매크로는 모든 데이터 파일 필드 및 행에 사용할 수 있습니다. 다른 매크로는 헤더 및 데이터 행에만 고유합니다.
seo-title: 파일 형식 매크로
title: 파일 형식 매크로
uuid: f 91 c 91 b 6-6581-4 ed 7-8 d 7 f-f 8532 bd 41 df 9
translation-type: tm+mt
source-git-commit: e1122a7f3d3e8c2d67616eb56cb186a4750ed29b

---


# 파일 형식 매크로 {#file-format-macros}

를 사용하여 기반 데이터 파일을 만드는 [!DNL FTP]데 사용할 수 있는 매크로를 나열합니다. 일부 매크로는 모든 데이터 파일 필드 및 행에 사용할 수 있습니다. 다른 매크로는 헤더 및 데이터 행에만 고유합니다.

## 일반 매크로 {#common-macros}

이러한 매크로는 모든 형식 필드에서 사용할 수 있습니다. 예를 들어 [파일 형식 매크로 예제를 참조하십시오](../formats/file-format-examples.md).

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_ SOH</code> </p> </td> 
   <td colname="col2"> <p>인쇄할 수 없는 ASCII 문자입니다. 이것은 행 또는 컨텐츠 섹션의 시작을 나타냅니다. 파일의 데이터 열을 구분하는 데에도 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>dpid</code> </p> </td> 
   <td colname="col2"> <p>타겟 데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>master_ dpid</code> </p> </td> 
   <td colname="col2"> <p>사용자 ID 주요 데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>order_ id</code> </p> </td> 
   <td colname="col2"> <p>주문/대상 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Pidalias</code> </p> </td> 
   <td colname="col2"> <p>주문/대상 ID에 대한 별칭. </p> <p>이 별칭에 대한 값은 대상의 <span class="wintitle"> 외부 계정 ID </span> 필드에 설정됩니다 ( <span class="wintitle"> 기본 설정 </span> 섹션). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>sync_ mode</code> </p> </td> 
   <td colname="col2"> <p>동기화 유형을 가리킵니다. 다음 선택적 변수를 수락합니다. </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>전체</code>: 전체 동기화. </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>Iter</code>: 증분 동기화. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>sync_ type</code> </p> </td> 
   <td colname="col2"> <p>데이터 전송 방법을 나타냅니다. 다음 선택적 변수를 수락합니다. </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>FTP</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>timestamp</code> </p> </td> 
   <td colname="col2"> <p>10 자리, UTC, Unix 타임스탬프. </p> <p>또한 Java 날짜/타임스탬프 서식 규칙 다음에 <code>yyyymmddhhmmss</code> 로 형식이 지정될 수도 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 헤더 필드 매크로 {#header-field-macros}

헤더 필드에서만 사용되는 매크로입니다. 예를 들어 [파일 형식 매크로 예제를 참조하십시오](../formats/file-format-examples.md).

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>tab</code> </p> </td> 
   <td colname="col2"> <p>이 매크로는 구분 문자로 사용되며 필드 사이에 탭을 삽입합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 데이터 행 매크로 {#data-row-macros}

데이터 행에 사용된 매크로입니다. 예를 들어 [파일 형식 매크로 예제를 참조하십시오](../formats/file-format-examples.md).

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>close_ para_ bracket</code> </p> </td> 
   <td colname="col2"> <p>닫는 중괄호} 문자를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>쉼표</code> </p> </td> 
   <td colname="col2"> <p>쉼표를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>dp_ uuid</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 데이터 파트너 고유 사용자 식별자 </span>. 해당 ID가 <span class="keyword"> Audience Manager </span> 장치 ID와 이미 동기화된 경우 사용자/사이트 방문자에게 할당한 ID를 반환합니다. </p> <p>dpid가 0 이면 이 매크로는 사용자의 ID 대신 <span class="keyword"> Audience Manager </span> ID를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>dp_ uuid_ list</code> </p> </td> 
   <td colname="col2"> <p>데이터 파트너의 여러 ID가 포함된 목록을 반환합니다. 이 기능은 여러 하위 분할 또는 데이터를 공유할 수 있는 기타 조직 그룹이 있는 대규모 조직이 있는 경우에 유용합니다. 이 매크로는 하위 그룹의 ID 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>Dpuuids</code> </p> </td> 
   <td colname="col2"> <p>이 매크로의 출력은 데이터 공급자 ID (dpid) 를 관련 고유 사용자 ID (dpuuid) 에 매핑합니다. 이 매크로에는 출력을 제어할 수 있는 형식 지정 문자열이 있어야 합니다. 샘플 출력은 다음과 비슷합니다. </p> <p> <code>" dpids = dpid 1, dpid 2,... dpid n | maxmappings = n | format = JSON "</code> </p> <p><code>Maxmappings</code> 설정은 매크로를 반환할 매핑 수를 결정합니다. <code>Maxmappings = 0</code>인 경우 이 매크로는 지정된 각 DPID에 대한 매핑을 반환합니다. 데이터는 타임스탬프 (가장 최근 것 먼저) 로 정렬되며 가장 큰 타임스탬프의 결과를 먼저 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>조건 <code>if</code> 및 <code>segment_ list</code> 와 <code>removed_ segment_ list</code> 매크로를 사용할 때 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if (segment_ list &amp; &amp; removed_ segment_ list) endif</code> </p> </td> 
   <td colname="col2"> <p>이 매크로 조합은 사용자가 속해 <i>있고</i> 제거된 세그먼트를 나열하는 조건문을 만듭니다. 두 조건이 모두 충족되지 않았거나 데이터가 없는 경우 빈 문자열을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud </span> ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>open_ para_ bracket</code> </p> </td> 
   <td colname="col2"> <p>여는 중괄호 {문자를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_ OUT</code> </p> </td> 
   <td colname="col2"> <p>삭제 예정. 사용하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>output_ attribute_ type</code> </p> </td> 
   <td colname="col2"> <p>삭제 예정. 사용하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>output_ attribute_ value</code> </p> </td> 
   <td colname="col2"> <p><code>1</code> 를 정적 하드코드된 값으로 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>파트너 ID (pid). PID는 관리 UI의 <span class="wintitle"> 프로필 </span> 탭 아래에 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>removed_ segment_ list</code> </p> </td> 
   <td colname="col2"> <p>제거된 세그먼트 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>segment_ list</code> </p> </td> 
   <td colname="col2"> <p>목록의 세그먼트 목록을 반환합니다. 다음 선택적 변수를 수락합니다. </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>Segmentid</code>: 기존 ID. 삭제 예정. <code>SID</code> (소문자만) 를 사용합니다. </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>Csegid</code>: 기존 ID. 삭제 예정. <code>SID</code> (소문자만) 를 사용합니다. </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>SID</code>: 세그먼트 ID. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code></code>유형: 데이터를 세그먼트 데이터로 식별하는 정적, 하드코드된 값인 <code>5</code>를 반환합니다. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>Alias</code>: 세그먼트 매핑을 참조하십시오. 삭제 예정. <code>SID</code> (소문자만) 를 사용합니다. </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>Lastupdatetime</code>: 세그먼트가 구현된 마지막 시간을 나타내는 UNIX 타임스탬프. </li> 
    </ul> <p>이러한 변수를 매크로 뒤에 중괄호로 넣습니다. 예를 들어 이 코드는|" 문자: <code>&lt; segment_ list: {seg|&lt; seg. type &gt;, &lt; seg. sid &gt;}; separator = "|" &gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>set_ attributes</code> </p> </td> 
   <td colname="col2"> <p><code>1</code> 를 정적 하드코드된 값으로 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>tab</code> </p> </td> 
   <td colname="col2"> <p>탭 구분 기호를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>trait_ list</code> </p> </td> 
   <td colname="col2"> <p>특성 목록을 반환합니다. 다음 선택적 인수를 수락합니다. </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code></code>유형: 트레이트 유형을 숫자 ID로 식별합니다. 이 변수는 다음과 같이 반환됩니다. 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>DPM</code> 트레이트 (오프라인 작업에서 온보딩된 오프라인) 를 식별하는 10. </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> 규칙을 기반으로 하는 특성 (실시간; <span class="wintitle"> DCS </span>를 통해 온보딩됩니다. </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>Traitid</code>: 특성 ID. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>래스트리스</code>: 트레이트가 실현된 마지막 시간입니다. Unix 타임스탬프. </li> 
    </ul> <p>이러한 변수를 매크로 뒤에 중괄호로 넣습니다. 예를 들어 이 코드는|" 문자: <code>trait_ list {type | traitid}; separator = "|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager </span> 사용자 ID. </p> </td> 
  </tr> 
 </tbody> 
</table>
---
description: FTP 기반 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. 일부 매크로는 모든 데이터 파일 필드 및 행에 사용할 수 있습니다. 다른 매크로는 헤더 및 데이터 행에만 적용됩니다.
seo-description: FTP 기반 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. 일부 매크로는 모든 데이터 파일 필드 및 행에 사용할 수 있습니다. 다른 매크로는 헤더 및 데이터 행에만 적용됩니다.
seo-title: 파일 형식 매크로
title: 파일 형식 매크로
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
translation-type: tm+mt
source-git-commit: 0ee7aa9c13f1b9b8fd64dddff4e52d101055e77c
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 2%

---


# 파일 형식 매크로 {#file-format-macros}

[!DNL FTP] 기반 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. 일부 매크로는 모든 데이터 파일 필드 및 행에 사용할 수 있습니다. 다른 매크로는 헤더 및 데이터 행에만 적용됩니다.

## 일반 매크로 {#common-macros}

이러한 매크로는 모든 형식 필드에서 사용할 수 있습니다. 예를 들어 [파일 형식 매크로 예](../formats/file-format-examples.md)를 참조하십시오.

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매크로 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>인쇄되지 않는 ASCII 문자입니다. 행 또는 컨텐츠 섹션의 시작을 나타냅니다. 또한 파일에서 데이터 열을 구분하는 데 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>Target 데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>사용자 ID 키 데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>주문/대상 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>주문/대상 ID에 대한 별칭입니다. </p> <p>이 별칭의 값은 대상의 <span class="wintitle"> 외래 계정 ID </span> 필드(<span class="wintitle"> 기본 설정 </span> 섹션)에서 설정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>동기화 유형을 나타냅니다. 다음 선택적 변수를 수락합니다. </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>:전체 동기화 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>:증분 동기화. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>데이터 전송 방법을 나타냅니다. 다음 선택적 변수를 수락합니다. </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>10자리, UTC, Unix 타임스탬프. </p> <p>또한 Java 날짜/타임스탬프 서식 규칙 다음에 <code>YYYYMMDDhhmmss</code> 형식을 지정할 수도 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 헤더 필드 매크로 {#header-field-macros}

헤더 필드에만 사용되는 매크로입니다. 예를 들어 [파일 형식 매크로 예](../formats/file-format-examples.md)를 참조하십시오.

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매크로 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>구분 기호로 사용되는 이 매크로는 필드 사이에 탭을 삽입합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 데이터 행 매크로 {#data-row-macros}

데이터 행에서만 사용되는 매크로입니다. 예를 들어 [파일 형식 매크로 예](../formats/file-format-examples.md)를 참조하십시오.

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매크로 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>닫힌 중괄호 <code>}</code> 문자를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>쉼표를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> 데이터 파트너 고유 사용자 식별자 </span>. 해당 ID가 이미 <span class="keyword"> Audience Manager </span> 장치 ID와 동기화된 경우 사용자/사이트 방문자에게 할당한 ID를 반환합니다. </p> <p>DPID가 0이면 이 매크로는 사용자의 ID 대신 <span class="keyword"> Audience Manager </span> ID를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>데이터 파트너의 여러 ID가 포함된 목록을 반환합니다. 이 기능은 데이터를 공유할 수 있도록 허용된 여러 하위 부문 또는 다른 조직 그룹이 있는 큰 조직이 있는 경우에 유용합니다. 이 매크로는 하위 그룹의 ID 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>이 매크로의 출력은 데이터 공급자 ID(DPID)를 관련 DPUUID(고유한 사용자 ID)에 매핑합니다. 이 매크로는 출력을 제어할 수 있는 서식 문자열이 있어야 합니다. 샘플 출력은 다음과 비슷합니다. </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p><code>maxMappings</code> 설정은 매크로를 반환할 매핑 수를 결정합니다. <code>maxMappings=0</code>이면 이 매크로는 지정된 각 DPID에 대한 모든 매핑을 반환합니다. 데이터는 타임스탬프(가장 최근 첫 번째)별로 정렬되고 가장 큰 타임스탬프가 있는 결과를 먼저 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>조건부 <code>if</code> 및 <code>SEGMENT_LIST</code> 및 <code>REMOVED_SEGMENT_LIST</code> 매크로를 사용할 때 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>이 매크로 조합을 사용하면 사용자가 속하는 세그먼트가 <i>이고</i>에서 제거된 조건문이 나열됩니다. 두 조건이 모두 충족되지 않거나 데이터가 없는 경우 빈 문자열을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Adobe Experience Cloud ID.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>열려 있는 중괄호 <code>{</code> 문자를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>삭제 예정. 사용하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>삭제 예정. 사용하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p><code>1</code>을(를) 정적 하드 코딩된 값으로 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>파트너 ID(PID). PID는 관리자 UI의 <span class="wintitle"> 프로필 </span> 탭 아래에 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>제거된 세그먼트 목록을 반환합니다(있는 경우). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>목록의 세그먼트 목록을 반환합니다. 다음 선택적 변수를 수락합니다. </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>:기존 ID. 삭제 예정. <code>sid</code>(소문자 전용)을 사용하십시오. </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>:기존 ID. 삭제 예정. <code>sid</code>(소문자 전용)을 사용하십시오. </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>:세그먼트 ID. </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>:데이터를 세그먼트 데이터 <code>5</code>로 식별하는 정적 하드 코딩된 값을 반환합니다. </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>:세그먼트 매핑을 참조하십시오. 삭제 예정. <code>sid</code>(소문자 전용)을 사용하십시오. </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>:세그먼트가 마지막으로 실현된 시간을 나타내는 Unix 타임스탬프 </li> 
    </ul> <p>이 변수를 매크로 뒤에 중괄호로 묶습니다. 예를 들어 이 코드는 파이프 "|" 문자로 결과를 구분합니다.<code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p><code>1</code>을(를) 정적 하드 코딩된 값으로 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>탭 구분 기호를 삽입합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>트레이트 목록을 반환합니다. 다음 선택적 인수를 수락합니다. </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>:숫자 ID로 식별되는 트레이트 유형. 이 변수는 다음을 반환합니다. 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code> DPM 특성(오프라인, 인바운드 작업에 의해 온보드)을 식별합니다. </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code> 규칙 기반 트레이트를 식별합니다(realtime,;DCS를 통해  <span class="wintitle"> 온보드  </span>). </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>:특성 ID. </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>:마지막으로 그 특징이 실현되었습니다. Unix 타임스탬프 </li> 
    </ul> <p>이 변수를 매크로 뒤에 중괄호로 묶습니다. 예를 들어 이 코드는 "|" 문자로 결과를 구분합니다.<code>TRAIT_LIST{type|traitId};separator="|"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword"> Audience Manager  </span> 사용자 ID. </p> </td> 
  </tr> 
 </tbody> 
</table>
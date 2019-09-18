---
description: 일반적으로 사용되는 일부 HTTP 매크로 조합의 예입니다.
seo-description: 일반적으로 사용되는 일부 HTTP 매크로 조합의 예입니다.
seo-title: ' HTTP 형식 매크로 예'
title: ' HTTP 형식 매크로 예'
uuid: a81a2e2a-de7e-4b6a-8771-fcfa0dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# HTTP 형식 매크로 예 {#http-format-macro-examples}

일반적으로 사용되는 일부 [!DNL HTTP] 매크로 조합의 예.

매크로 [및 해당](../formats/web-formats.md) 정의 목록은 HTTP 형식 매크로를 참조하십시오.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매크로 예 </th> 
   <th colname="col2" class="entry"> 출력 형식 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAIALIAS_LIST;separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|count:&lt;NUM_USERS&gt;|사용자:[&lt;USER_LIST:{user|&lt;user.aamUuid&gt;:&lt;user.dpUuid&gt;};separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>"pid_alias|count:2|users:[uuid1:dpuuid1, uuid2:dpuuid2]"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_AGENT&gt;|&lt;IP&gt;|&lt;TIMESTAMP&gt;|&lt;RANDOM&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_LIST:{u|&lt;u.userAgent&gt;|&lt;u.ip&gt;|&lt;u.timestamp&gt;|&lt;u.random&gt;};separator=", "&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;DP_UUIDS.1&gt; 및 &lt;DP_UUIDS.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid1 및 DPUUID2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>사용자:[&lt;USER_LIST:{user|&lt;user.dpUuids.1&gt; 및 &lt;user.dpUuids.2&gt;};separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>사용자:[dpuuid1 및 DPUUID2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_known_string=loremlipsum&amp;segid=&lt;TRAIALIAS_LIST;separator=","&gt;&amp;test_dpuuid_1000=&lt;DP_UUIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_known_string=loremlipsum&amp;segid=trait_1,trait_2&amp;test_dpuuid_1000=dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_dpuuids=&lt;DP_UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_dpuids=dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>"&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAIALIAS_LIST;separator=","&gt;|&lt;REMOVED_TRAITALIAS_LIST;separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"사용자": [&lt;사용자_LIST:{사용자|&lt;OPEN_BRACKET&gt; "AAM_UUID": "&lt;user.aamUuid&gt;", "DataPartner_UUID": "&lt;user.dpUuid&gt;", "세그먼트": [&lt;사용자.세그먼트:{seg|&lt;OPEN_BRACKS&gt; "세그먼트": "&lt;seg.traitAlias&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt;] "Removed_Segments": [&lt;user.removedSegments:{rseg|&lt;OPEN_BRACKETS&gt;"Segment": "&lt;rseg.alias&gt;"&lt;CLOSE_BRACKETS&gt;}; separator&gt;}; separator=","&gt; &lt;CLOSE_BRACKET&gt;}; separator=","&gt;]} </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       { "Users":[ { "AAM_UUID":"uuid1", "DataPartner_UUID":"dpuuid1", "Segments":[ { "Segment":"alias1" }, { "alias2" } ], "Removed_Segments":[ { "alias3" }, segment":"alias4" } ] } </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>
       {"사용자": [&lt;사용자_LIST:{사용자|&lt;OPEN_BRACKET&gt; "AAM_UUID": "&lt;user.aamUuid&gt;", "DataPartner_UUID": "&lt;user.dpUuid&gt;", "세그먼트": [&lt;사용자.세그먼트:{seg|&lt;OPEN_BRACKS&gt; "세그먼트": "&lt;seg.traitAlias&gt;","상태": "&lt;seg.status&gt;"&lt;CLOSE_BRACKET&gt;}; separator=","&gt;] &lt;CLOSE_BRACKETS&gt;}; separator=","&gt;]} </code> </p> </td> 
   <td colname="col2"> <p> 
     <code>
       { "Users":[ { "AAM_UUID":"uuid1", "DataPartner_UUID":"dpuuid1", "Segments":[ { "Segment":"alias1" "Status":"1" }, { "Segment":"alias2":"Status" } ] } } } } </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;세그먼트:{seg|&lt;seg.traitAlias&gt;};seg|&lt;seg.traitAlias&gt;};separator=\",\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;if(user.segments &amp;&amp; user.removedSegments)&gt;&lt;COMMA&gt;&lt;endif&gt;</code> </p> </td> 
   <td colname="col2"> <p>필드 <code>세그먼트와</code> 제거세그먼트가 <code>비어 있지 않으면</code> 쉼표를 인쇄합니다. 세그먼트 및 제거된 세그먼트에 대한 목록을 연결할 때 이 조건을 POST 요청에 사용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

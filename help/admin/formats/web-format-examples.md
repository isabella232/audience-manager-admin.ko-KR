---
description: 일반적으로 사용되는 일부 HTTP 매크로 조합의 예입니다.
seo-description: 일반적으로 사용되는 일부 HTTP 매크로 조합의 예입니다.
seo-title: HTTP 포맷 매크로 예제
title: HTTP 포맷 매크로 예제
uuid: a 81 a 2 e 2 a-de 7 e -4 b 6 a -8771-fcfa 0 dc 74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# HTTP 포맷 매크로 예제 {#http-format-macro-examples}

일반적으로 사용되는 몇 가지 [!DNL HTTP] 매크로 조합의 예입니다.

매크로 및 해당 정의 목록은 [HTTP 형식 매크로를](../formats/web-formats.md) 참조하십시오.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매크로 예제 </th> 
   <th colname="col2" class="entry"> 출력 형식 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; pid_ alias &gt;|&lt; dp_ uuid &gt;|&lt; traitalias_ list; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; pid_ alias &gt;| count: &lt; num_ users &gt;| 사용자: [&lt; user_ list: {user|&lt; user. aamuuid &gt;: &lt; user. dpuuid &gt;}; separator = "," &gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>" pid_ alias | count: 2 | 사용자: [UUID 1: DPUUID 1, UUID 2: dpuuid 2] "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; user_ agent &gt;|&lt; IP &gt;|&lt; timestamp &gt;|&lt; random &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>" Firefox | 255.255.255.255 | 1395758143 | 42341 "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; user_ list: {u|&lt; u. useragent &gt;|&lt; u. ip &gt;|&lt; u. timestamp &gt;|&lt; u. random &gt;}; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>" Firefox | 255.255.255.255 | 1395758143 | 42341 "</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; dp_ uuids .1 &gt; 및 &lt; dp_ uuids .2 &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>DPUUID 1 및 DPUUID 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>사용자: [&lt; user_ list: {user|&lt; user. dpuuids .1 &gt; 및 &lt; user. dpuuids .2 &gt;}; separator = "," &gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>사용자: [DPUUID 1 및 DPUUID 2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ known_ string = loremlipsum &amp; segid = &lt; Traitalias_ list; separator = "," &gt; &amp; test_ dpuuid_ 1000 = &lt; dp_ uuids .1000 &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ known_ string = loremlipsum &amp; segid = trait_ 1, trait_ 2 &amp; test_ dpuuid_ 1000 = dpuuid_ 1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_ dpuuids = &lt; dp_ uuids.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_ dpuuids = dpuuid 2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>" &lt; pid_ alias &gt;|&lt; dp_ uuid &gt;|&lt; traitalias_ list; separator = "," &gt;|&lt; removed_ traitalias_ list; separator = "," &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2 | trait_ 3, trait_ 4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"users": [&lt; user_ list: {user|&lt; open_ bracket &gt; 
 " aam_ uuid ": " &lt; user. aamuuid &gt; ", 
 " datapartner_ uuid ": " &lt; user. dpuuid &gt; ", 
 " 세그먼트 ": [&lt; user. segments: {seg|&lt; open_ bracket &gt; "segment": " &lt; seg. traitalias &gt; " &lt; close_ bracket &gt;}; separator = "," &gt;] 
 " removed_ segments ": [&lt; user. removedsegments: {RSEG|&lt; open_ bracket &gt; "segment": " &lt; rseg. traitalias &gt; " &lt; close_ bracket &gt;}; separator = "," &gt;] 
 &lt; close_ bracket &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{ 
 " 사용자 ": [[ 
 { 
 " aam_ uuid ": " uuid 1 ", 
 " datapartner_ uuid ": " dpuuid 1 ", 
 " 세그먼트 ": [[ 
 { 
 " 세그먼트 ": " alias 1 " 
 }, 
 { 
 " 세그먼트 ": " alias 2 " 
 } 
 ], 
 " removed_ segments ": [[ 
 { 
 " 세그먼트 ": " alias 3 " 
 }, 
 { 
 " 세그먼트 ": " alias 4 " 
 } 
 ] 
 } 
 ] 
 } </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"users": [&lt; user_ list: {user|&lt; open_ bracket &gt; 
 " aam_ uuid ": " &lt; user. aamuuid &gt; ", 
 " datapartner_ uuid ": " &lt; user. dpuuid &gt; ", 
 " 세그먼트 ": [&lt; user. segments: {seg|&lt; open_ bracket &gt; "segment": " &lt; seg. traitalias &gt; "," status ": " &lt; seg. status &gt; " &lt; close_ bracket &gt;}; separator = "," &gt;] 
 &lt; close_ bracket &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{ 
 " 사용자 ": [[ 
 { 
 " aam_ uuid ": " uuid 1 ", 
 " datapartner_ uuid ": " dpuuid 1 ", 
 " 세그먼트 ": [[ 
 { 
 " 세그먼트 ": " alias 1 " 
 " status ": " 1 " 
 }, 
 { 
 " 세그먼트 ": " alias 2 " 
 " status ": " 0 " 
 } 
 ] 
 } 
 ] 
 } </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; pid_ alias &gt;|&lt; dp_ uuid &gt;|&lt; 세그먼트: {seg|&lt; seg. traitalias &gt;}; separator =\ ",\" &gt;|&lt; removed_ segments: {seg|&lt; seg. traitalias &gt;}; separator =\ ",\" &gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_ alias | dp_ uuid | trait_ 1, trait_ 2 | trait_ 3, trait_ 4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt; if (user. segments &amp; &amp; user. removedsegments) &gt; &lt; comma &gt; &lt; endif &gt;</code> </p> </td> 
   <td colname="col2"> <p>필드 <code>세그먼트와</code> <code>Removedsegments</code> 가 비어 있지 않은 경우 쉼표를 인쇄합니다. 이 조건부 조건은 세그먼트 및 제거된 세그먼트에 대한 목록을 연결할 때 게시물 요청에 사용할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: 아웃바운드 FTP 파일 템플릿을 만드는 데 매크로를 사용하는 방법의 예.
seo-description: 아웃바운드 FTP 파일 템플릿을 만드는 데 매크로를 사용하는 방법의 예.
seo-title: 파일 포맷 매크로 예제
title: 파일 포맷 매크로 예제
uuid: F 00 D 431 D -7 E 43-457 A-B 633-C 79 CBC 4 C 8 F 10
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# 파일 포맷 매크로 예제 {#file-format-macro-examples}

매크로를 사용하여 아웃바운드 [!DNL FTP] 파일 템플릿을 만드는 방법의 예.

>[!NOTE]
>
>표에서 **굵은 글꼴** 유형은 관련 출력으로 각 매크로를 식별합니다. 형식 예제의 경우 각 매크로를 시각적으로 분리할 수 있도록 &lt; &gt; 기호가 추가되었습니다.

## 일반 매크로 {#common-macros}

이러한 매크로는 모든 형식 필드에서 사용할 수 있습니다. 전체 [목록 및 정의는 파일](../formats/file-formats.md) 형식 매크로를 참조하십시오.

<table id="table_B5073597219B470298EE614902DACAE8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 형식 및 출력 예제 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>dpid </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; sync_ type &gt;_ &lt; order_ id &gt;_ &lt; dpid &gt;_ &lt; sync_ mode &gt;_ &lt; timestamp &gt;. sync </code> </p> <p>출력: <code>ftp_ 215_ 888_ iter_ 1449756724. sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>master_ dpid </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; sync_ type &gt;_ &lt; order_ id &gt;_ &lt; dpid &gt;_ &lt; dpid &gt;_ &lt; sync_ mode &gt;_ &lt; timestamp &gt;. sync 동기화 </code> </p> <p>출력: <code>ftp_ 215_ 888_ 20915_ iter_ 1449756724. sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>order_ id </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; sync_ type &gt;_ &lt; order_ id &gt;_ &lt; dpid &gt;_ &lt; sync_ mode &gt;_ &lt; timestamp &gt;. sync </code> </p> <p>출력: <code>ftp_ 215_ 888_ iter_ 1449756724. sync </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>sync_ mode </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; sync_ type &gt;_ &lt; order_ id &gt;_ &lt; dpid &gt;_ &lt; sync_ mode &gt;_ &lt; timestamp &gt;. sync </code> </p> <p>출력: 
     <ul id="ul_F63D7B78AF1246639D6ED85C1621B17C"> 
      <li id="li_4D0D7B4D047345FE861FCBA2BD0408ED">전체: <code>ftp_ 215_ 888_ full_ 1449756724. sync </code> </li> 
      <li id="li_23F4D1F6B2784E599EDA29AA457327E6">증분: <code>ftp_ 215_ 888_ iter_ 1449756724. sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>sync_ type </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; sync_ type &gt;_ &lt; order_ id &gt;_ &lt; dpid &gt;_ &lt; sync_ mode &gt;_ &lt; timestamp &gt;. sync </code> </p> <p>출력: 
     <ul id="ul_11B14E740E40474F8302BDB809C428FE"> 
      <li id="li_54A3EAA468B44AC8B2528F855E03D04B">FTP: <code>ftp_ 215_ 888_ iter_ 1449756724. sync </code> </li> 
      <li id="li_93468C56B661463CA7F62B1F5D3A53FF">HTTPS: <code>HTTP_ 215_ 888_ ITER_ 1449756724. SYNC </code> </li> 
      <li id="li_8A204C7BEDBC41C096FE953B5F827DEC">S 3: <code>s 3_ 215_ 888_ iter_ 1449756724. sync </code> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>timestamp </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; sync_ type &gt;_ &lt; order_ id &gt;_ &lt; dpid &gt;_ &lt; sync_ mode &gt;_ &lt; timestamp &gt;. sync </code> </p> <p>출력: <code>ftp_ 215_ 888_ iter_ 1449756724. sync </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 헤더 필드 매크로 {#header-field-macros}

헤더 필드에서만 사용되는 매크로입니다. 전체 [목록 및 정의는 파일](../formats/file-formats.md) 형식 매크로를 참조하십시오.

<table id="table_ABC31B3D660D47969E111EBC734D5BBC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 형식 및 출력 예제 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>tab </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; order_ id &gt; &lt; tab &gt; &lt; sync_ type &gt; </code> </p> <p>출력: <code>888 Full. sync </code> </p> <p>출력에서 인쇄되지 않는 탭 문자는 각 요소를 분리합니다. </p> </td>
  </tr>
 </tbody>
</table>

## 데이터 행 매크로 {#data-row-macros}

헤더 필드에서만 사용되는 매크로입니다. 전체 [목록 및 정의는 파일](../formats/file-formats.md) 형식 매크로를 참조하십시오.

<table id="table_408C6DD2B9D54550B003EAC93562E64F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> macro </th> 
   <th colname="col2" class="entry"> 형식 및 출력 예제 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>dp_ uuid </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; dp_ uuid &gt; &lt; tab &gt; &lt; dp_ uuid_ list; separator = tab &gt; </code> </p> <p>출력: <code>123456 UUID 1 UUID 2 UUID 3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>dp_ uuid_ list </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; dp_ uuid &gt; &lt; tab &gt; &lt; dp_ uuid_ list; separator = tab &gt; </code> </p> <p>출력: <code>123456 UUID 1 UUID 2 UUID 3 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>segment_ list &amp; &amp; removed_ segment_ list </code> </p> </td> 
   <td colname="col2"> <p>이 예에서는 서버-서버 피드에서 제거된 세그먼트를 반환하는 형식을 만듭니다. </p> <p> 
     <code>{"Advertiserid": " &lt; Pidalias &gt; "," datacenterid ": 2, "tdid": " &lt; dp_ uuid &gt; ", 
 " 데이터 ": [&lt; segment_ list: {seg|&lt; open_ para_ bracket &gt; "name": " &lt; seg. alias &gt; " &lt; close_ para_ bracket &gt;}; 
 separator = "," &gt; &lt; if (segment_ list &amp; &amp; removed_ segment_ list) &gt; &lt; 쉼표 &gt; &lt; endif &gt; 
 &lt; removed_ segment_ list: {seg|&lt; open_ para_ bracket &gt; "name": " &lt; seg. alias &gt; ", 
 " Ttlinminutes ": 0 &lt; close_ para_ bracket &gt;}; separator = "," &gt;]} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>segment_ list </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; dp_ uuid &gt; &lt; segment_ list &gt;; separator = "" &gt; </code> </p> <p>출력: <code>123456 105955 101183 101180 101179 </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>set_ attributes </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; pid &gt; &lt; tab &gt; &lt; uuid &gt; &lt; tab &gt; &lt; dp_ uuid &gt; &lt; tab &gt; &lt; set_ attributes &gt; &lt; tab &gt; &lt; opt_ out &gt; &lt; tab &gt; &lt; segment_ list: {seg|&lt; seg. type &gt;, &lt; seg. alias &gt;, &lt; output_ attribute_ value &gt;, &lt; seg. lastupdatetime &gt; &amp;} &gt; </code> </p> <p>출력: <code>1159 000880085796836537415162975091516297500 17 T 0 AJ 01 B 120 HP 1 0 5,103714,1,1344114661000 &amp; 5,103713,1,1343250661000 </code> </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <code>tab </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; dp_ uuid &gt; &lt; tab &gt; &lt; dp_ uuid_ list; separator = tab &gt; </code> </p> <p>출력: <code>123456 UUID 1 UUID 2 UUID 3 </code> </p> <p>출력에서 인쇄되지 않는 탭 문자는 각 요소를 분리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>trait_ list </code> </p> </td> 
   <td colname="col2"> <p>형식: <code>&lt; pid &gt; &lt; tab &gt; &lt; dp_ uuid &gt; &lt; tab &gt; &lt; set_ attributes &gt; &lt; tab &gt; &lt; trait_ list; separator = «|» &gt; </code> </p> <p>출력: <code>1131 12345 1 123|456|789 </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

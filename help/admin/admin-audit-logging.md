---
description: '고객 문제를 디버깅할 때 감사 로깅을 가장 먼저 사용하십시오. '
seo-description: '고객 문제를 디버깅할 때 감사 로깅을 가장 먼저 사용하십시오. '
seo-title: 감사 로깅
title: 감사 로깅
uuid: null
translation-type: tm+mt
source-git-commit: 190ba5c1215782e46c8e544c10679d451fbed134

---


# 감사 로깅 {#audit-logging}

고객 문제를 [!UICONTROL  Audit Logging] 디버깅할 때 가장 먼저 사용할 수 있습니다.

> [!NOTE]
>
>[!UICONTROL Audit Logging] 가 현재 개발 중이며 변경될 수 있습니다. 발생한 문제를 [!DNL JIRA] ([!DNL UI] 팀)에 기록하십시오.

![감사 로깅 보기](assets/audit-logging-img.png)

감사 **유형** 드롭다운 선택기에서 다음 중 하나를 선택합니다.

* [!UICONTROL Partner]
* [!UICONTROL User]
* [!UICONTROL Group]
* [!UICONTROL Datasource Summary]
* [!UICONTROL General Datasource]
* [!UICONTROL Merge Rule Datasource]
* [!UICONTROL Data Feed]
* [!UICONTROL Data Feed Subscription]
* [!UICONTROL Trait Summary]
* [!UICONTROL Trait Rule]
* [!UICONTROL Segment Summary]
* [!UICONTROL Destination Summary]
* [!UICONTROL Server to Server Destination]
* [!UICONTROL Derived Signal]
* [!UICONTROL Model]
* [!UICONTROL Segment Test Group]

개체 **ID는** 검색 중인 항목의 ID입니다. 각 케이스의 개체 ID에 해당하는 ID는 아래 표를 참조하십시오.

| 감사 유형 | 개체 ID |
---------|----------|
| [!UICONTROL Partner] | 파트너 ID - PID |
| [!UICONTROL User] | 사용자 ID |
| [!UICONTROL Group] | B3 |
| [!UICONTROL Datasource Summary] | 데이터 소스 ID |
| [!UICONTROL General Datasource] | 데이터 소스 ID |
| [!UICONTROL Merge Rule Datasource] | 데이터 소스 ID |
| [!UICONTROL Data Feed] | 데이터 피드 ID |
| [!UICONTROL Data Feed Subscription] | 데이터 피드 ID |
| [!UICONTROL Trait Summary] | SID(트레이트) |
| [!UICONTROL Trait Rule] | SID(트레이트) |
| [!UICONTROL Segment Summary] |  |
| [!UICONTROL Destination Summary] |  |
| [!UICONTROL Server-to-Server Destination] | N/A |
| [!UICONTROL Derived Signal] | N/A |
| [!UICONTROL Model] | N/A |
| [!UICONTROL Segment Test Group] | N/A |

( [!UICONTROL Start Date] )[!DNL UTC]및 [!UICONTROL End Date] ([!DNL UTC])를 사용하여 로그의 시간 간격을 좁힙니다.
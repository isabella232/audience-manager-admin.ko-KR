---
description: 다른 파트너 또는 고객이 소유한 타겟 데이터 소스에 파일 및 데이터 온보딩이 우발되지 않도록 하기 위해 Audience Manager은 파트너 ID(PID)와 다른 파트너가 소유한 데이터 소스 간에 매핑 요구 사항을 추가했습니다.
title: 제2자 데이터에 대한 온보딩 액세스 관리
source-git-commit: 6c88979f876909bc32b5238605cb4a352e327a00
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# 제2자 데이터에 대한 온보딩 액세스 관리 {#manage-onboarding-access-for-second-party-data}

다른 파트너가 소유한 대상 데이터 소스에 파일 및 데이터 온보딩을 우발적으로 방지하기 위해 Audience Manager은 파트너 ID(PID)와 다른 파트너가 소유한 DPID(데이터 소스) 간에 매핑 요구 사항을 추가했습니다. 에서 PID 및 DPID에 대해 자세히 알아보십시오 [Audience Manager ID 색인](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html).

제2자 데이터 공유 목적의 경우, Audience Manager 파트너 또는 고객이 소유하지 않은 대상 데이터 소스에 파일을 수집하려는 경우 파트너 ID(PID)와 해당 특정 데이터 소스(DPID) 간의 매핑을 요청해야 합니다. 매핑이 없으면 인바운드 데이터 작업에 의해 파일이 처리되지 않고 데이터가 Audience Manager으로 온보딩되지 않습니다.

해당 매핑을 생성하려면 Jira 티켓을 Audience Manager 엔지니어링 팀에 제출하십시오. 샘플 Jira 티켓 보기 [여기](https://jira.corp.adobe.com/browse/AAM-60353). 기존 데이터 공유 관계에 대해 매핑을 만들 필요가 없습니다.

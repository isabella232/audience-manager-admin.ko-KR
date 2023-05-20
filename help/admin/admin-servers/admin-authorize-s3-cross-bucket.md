---
description: 일부 고객은 자신의 Amazon Simple Storage Service(Amazon S3) 액세스 또는 비밀 키를 Adobe에 제공하여 대상 데이터를 버킷에 업로드하는 것을 승인하지 않으려 할 수 있습니다.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스 권한을 부여하는 방법
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스 권한을 부여하는 방법{#authorize-cross-account-bucket-batch}

일부 고객은 오퍼를 제공하지 않을 수 있습니다. [!DNL Amazon S3] Adobe에 대한 액세스 또는 비밀 키를 사용하여 해당 버킷에 대한 대상 데이터 업로드를 승인합니다.

고객에게 제공할 수 있는 대안은 다음과 같습니다. [!UICONTROL Cross-Account Bucket Permissions] 위치: [!DNL Amazon S3]. 이 프로세스는 다음에 설명되어 있습니다. [AWS 설명서](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Audience Manager에서 이 대체 요소를 활성화하려면 아래 단계를 따르십시오.

1. 다음으로 이동 **[!UICONTROL Servers]** 및 선택 **[!UICONTROL Create Server]**.
1. 선택 **[!UICONTROL S3]** 다음에서 **[!UICONTROL Protocol/Credentials]** 드롭다운 마스크.
1. 다음 확인: **[!UICONTROL Use Internal Adobe Key]** 옵션을 선택합니다.
1. 에서 고객의 계정 및 버킷 이름 사용 [!DNL Amazon S3].
1. 고객 화이트리스트에 [!DNL Amazon S3] account `975822914085` 다음에 대한 [!DNL S3] 버킷.

>[!NOTE]
>
>아웃바운드 게시자는 권한 수준을 확인합니다 `bucket-owner-full-control` 은 고객이 해당 데이터를 소유할 수 있도록 업로드된 데이터에 대해 설정됩니다.

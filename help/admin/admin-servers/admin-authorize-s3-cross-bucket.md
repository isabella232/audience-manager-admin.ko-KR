---
description: 일부 고객은 자신의 Amazon Simple Storage Service(Amazon S3) 액세스 또는 비밀 키를 Adobe에 제공하여 대상 데이터를 자신의 버킷으로 업로드하도록 승인하지 않을 수 있습니다.
seo-description: 일부 고객은 자신의 Amazon Simple Storage Service(Amazon S3) 액세스 또는 비밀 키를 Adobe에 제공하여 대상 데이터를 자신의 버킷으로 업로드하도록 승인하지 않을 수 있습니다.
seo-title: 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스를 인증하는 방법
title: 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스를 인증하는 방법
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# How To Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations{#authorize-cross-account-bucket-batch}

일부 고객은 자신의 버킷에 대상 데이터 업로드를 인증하기 위해 Adobe에 액세스 [!DNL Amazon S3] 또는 비밀 키를 제공하지 않을 수도 있습니다.

우리가 고객에게 제공할 수 있는 대안이 [!UICONTROL Cross-Account Bucket Permissions] 있다 [!DNL Amazon S3]. 이 프로세스는 [AWS 설명서에 설명되어 있습니다](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html). Audience Manager에서 이 대체 요소를 활성화하려면 아래 단계를 수행하십시오.

1. 이동 **[!UICONTROL Servers]** 후 선택합니다 **[!UICONTROL Create Server]**.
1. 드롭다운 마스크 **[!UICONTROL S3]** 에서 **[!UICONTROL Protocol/Credentials]** 선택합니다.
1. 옵션을 **[!UICONTROL Use Internal Adobe Key]** 확인하십시오.
1. 고객 계정과 버킷 이름을 사용합니다 [!DNL Amazon S3].
1. 고객 백인이 버킷에 [!DNL Amazon S3] 계정 `975822914085` 을 나열하는지 [!DNL S3] 확인합니다.

>[!NOTE]
>
>아웃바운드 게시자는 고객이 해당 데이터를 소유할 수 있도록 권한 수준 `bucket-owner-full-control` 이 업로드된 데이터에 설정되어 있는지 확인합니다.

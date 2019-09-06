---
description: 일부 고객은 버킷에 대상 데이터 업로드를 허가하기 위해 Amazon Simple Storage Service (Amazon S 3) 액세스 또는 비밀 키를 Adobe에 제공하지 않을 수 있습니다.
seo-description: 일부 고객은 버킷에 대상 데이터 업로드를 허가하기 위해 Amazon Simple Storage Service (Amazon S 3) 액세스 또는 비밀 키를 Adobe에 제공하지 않을 수 있습니다.
seo-title: 일괄 대상에 대한 교차 계정 Amazon S 3 버킷 액세스 권한을 부여하는 방법
title: 일괄 대상에 대한 교차 계정 Amazon S 3 버킷 액세스 권한을 부여하는 방법
uuid: da 2 bcbda-a 765-437 a-bfe 9-4355383 a 4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# 일괄 대상에 대한 교차 계정 Amazon S 3 버킷 액세스 권한을 부여하는 방법{#authorize-cross-account-bucket-batch}

일부 고객은 버킷에 대상 데이터 업로드를 허가하기 위해 [!DNL Amazon S3] 액세스 또는 비밀 키를 Adobe에 제공하지 않을 수 있습니다.

[!UICONTROL Cross-Account Bucket Permissions][!DNL Amazon S3]Adobe 솔루션을 통해 얻을 수 있는 이점 이 프로세스는 [AWS 설명서에](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)설명되어 있습니다. Audience Manager에서 이 대체 항목을 활성화하려면 아래 단계를 수행하십시오.

1. Go to **[!UICONTROL Servers]** and select **[!UICONTROL Create Server]**.
1. 드롭다운 **[!UICONTROL S3]** 마스크에서 **[!UICONTROL Protocol/Credentials]** 선택합니다.
1. 옵션을 **[!UICONTROL Use Internal Adobe Key]** 확인합니다.
1. 고객의 계정 및 버킷 이름을 [!DNL Amazon S3]사용합니다.
1. 고객 흰색에 버킷에 [!DNL Amazon S3] 계정이 `975822914085` 표시되는지 [!DNL S3] 확인합니다.

>[!NOTE]
>
>아웃바운드 발행자는 업로드된 데이터에 권한 수준이 `bucket-owner-full-control` 설정되어 고객이 해당 데이터를 소유할 수 있도록 합니다.

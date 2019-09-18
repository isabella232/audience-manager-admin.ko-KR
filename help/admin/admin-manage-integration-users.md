---
description: 통합 사용자 페이지를 사용하여 Audience Manager 구성의 사용자 목록을 봅니다. 적절한 사용자 역할이 할당되어 있는 경우 기존 사용자를 편집 또는 삭제하거나 새 사용자를 만들 수 있습니다.
seo-description: 통합 사용자 페이지를 사용하여 Audience Manager 구성의 사용자 목록을 봅니다. 적절한 사용자 역할이 할당되어 있는 경우 기존 사용자를 편집 또는 삭제하거나 새 사용자를 만들 수 있습니다.
seo-title: 통합 사용자
title: 통합 사용자
uuid: 13dcb3fb-4561-40 파섹
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 통합 사용자 {#integration-users}

Audience Manager 구성의 사용자 목록을 보려면 [!UICONTROL Integration Users] 페이지를 사용합니다. 적절한 사용자 역할이 할당되어 있는 경우 기존 사용자를 편집 또는 삭제하거나 새 사용자를 만들 수 있습니다.

<!-- c_integration_users.xml -->

원하는 열의 머리글을 클릭하여 각 열을 오름차순이나 내림차순으로 정렬할 수 있습니다.
목록 아래쪽에 있는 [!UICONTROL Search] 상자 또는 페이지 매김 컨트롤을 사용하여 원하는 사용자를 찾습니다.

## 사용자 만들기 또는 편집 {#create-edit-user}

Audience Manager 도구의 [!UICONTROL Integration Users] [!UICONTROL Admin] 페이지를 사용하여 새 사용자를 만들거나 기존 사용자의 계정을 편집합니다.

<!-- t_create_user.xml -->

>[!NOTE]
>
>새 사용자를 만들려면 [!UICONTROL CREATE_USER] 역할이 있어야 합니다. 기존 사용자를 편집하려면 해당 [!UICONTROL EDIT_USER] 역할이 있어야 합니다.

1. 새 사용자를 만들려면 **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**&#x200B;을 클릭합니다. 기존 사용자를 편집하려면 **[!UICONTROL Username]** 열에서 원하는 사용자를 클릭합니다.
2. 다음 필드를 채웁니다.
   * **[!UICONTROL First Name]**:(필수) 사용자의 이름을 지정합니다.
   * **[!UICONTROL Last Name]**:(필수) 사용자의 성을 지정합니다.
   * **[!UICONTROL Username]**:(필수) 사용자의 사용자 이름을 지정합니다.
   * **[!UICONTROL Email Address]**:(필수) 사용자의 이메일 주소를 지정합니다.
   * **[!UICONTROL Phone Number]**:사용자의 전화 번호를 지정합니다.
   * **[!UICONTROL IMS ID]**:사용자의 이름을 [!UICONTROL Internet Messaging Service ID]지정합니다.
   * **[!UICONTROL User Roles]**:원하는 사용자 역할을 선택합니다.
      * **[!UICONTROL DEXADMIN]**:Audience Manager [!UICONTROL Admin] 도구에서 작업을 수행하기 위한 관리자 액세스 권한을 제공합니다. 이 옵션을 선택하지 않으면 개별 역할을 선택할 수 있습니다. 이러한 역할을 통해 사용자는 [!DNL API] 호출을 사용하여 작업을 수행할 수 있지만 관리 도구에서는 수행할 수 없습니다.
      * **[!UICONTROL CREATE_USERS]**:사용자가 [!DNL API] 호출을 사용하여 새 사용자를 만들 수 있습니다.
      * **[!UICONTROL DELETE_USERS]**:사용자가 [!DNL API] 호출을 사용하여 기존 사용자를 삭제할 수 있도록 해줍니다.
      * **[!UICONTROL EDIT_USERS]**:사용자가 [!DNL API] 호출을 사용하여 기존 사용자를 편집할 수 있도록 해줍니다.
      * **[!UICONTROL VIEW_USERS]**:사용자가 [!DNL API] 호출을 사용하여 Audience Manager 구성에서 다른 사용자를 볼 수 있도록 해줍니다.
      * **[!UICONTROL CREATE_PARTNERS]**:사용자가 [!DNL API] 전화를 사용하여 Audience Manager 파트너를 만들 수 있습니다.
      * **[!UICONTROL DELETE_PARTNERS]**:사용자가 [!DNL API] 전화를 사용하여 Audience Manager 파트너를 삭제할 수 있도록 해줍니다.
      * **[!UICONTROL EDIT_PARTNERS]**:사용자가 [!DNL API] 전화를 사용하여 Audience Manager 파트너를 편집할 수 있도록 해줍니다.
      * **[!UICONTROL VIEW_PARNTERS]**:사용자가 [!DNL API] 전화를 사용하여 Audience Manager 파트너를 볼 수 있도록 해줍니다.
   * **** 상태:이 사용자를 활성화된 Audience Manager 사용자로 **[!UICONTROL Active]** 설정하려면 선택합니다.
3. 클릭 **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

Audience Manager [!UICONTROL Integration Users] 도구의 페이지를 사용하여 기존 사용자를 [!UICONTROL Admin] 삭제합니다.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>새 사용자를 만들려면 **[!UICONTROL DELETE_USER]** 역할이 있어야 합니다.

1. 클릭 **[!UICONTROL Integration Users]**.
2. 원하는 사용자의 ![](assets/icon_delete.png) 열을 **[!UICONTROL Actions]** 클릭합니다.
3. Click **[!UICONTROL OK]** to confirm the deletion.
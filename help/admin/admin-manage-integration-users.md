---
description: 통합 사용자 페이지를 사용하여 Audience Manager 구성의 사용자 목록을 봅니다. 기존 사용자를 편집 또는 삭제하거나, 지정된 사용자 역할을 할당받았음을 제공하는 새 사용자를 만들 수 있습니다.
seo-description: 통합 사용자 페이지를 사용하여 Audience Manager 구성의 사용자 목록을 봅니다. 기존 사용자를 편집 또는 삭제하거나, 지정된 사용자 역할을 할당받았음을 제공하는 새 사용자를 만들 수 있습니다.
seo-title: 통합 사용자
title: 통합 사용자
uuid: 13 DCB 3 FB -4561-409 C -84 DA -943 D 0 D 390 CF 3
translation-type: tm+mt
source-git-commit: 10adb6b06160f5a5c4068483b407e5798fc10150

---


# 통합 사용자 {#integration-users}

이 [!UICONTROL Integration Users] 페이지를 사용하여 Audience Manager 구성의 사용자 목록을 봅니다. 기존 사용자를 편집 또는 삭제하거나, 지정된 사용자 역할을 할당받았음을 제공하는 새 사용자를 만들 수 있습니다.

<!-- c_integration_users.xml -->

원하는 열의 헤더를 클릭하여 오름차순 또는 내림차순으로 각 열을 정렬할 수 있습니다.
목록 아래쪽의 [!UICONTROL Search] 상자 또는 페이지 매김 컨트롤을 사용하여 원하는 사용자를 찾습니다.

## 사용자 만들기 또는 편집 {#create-edit-user}

Audience [!UICONTROL Integration Users] Manager [!UICONTROL Admin] 도구의 페이지를 사용하여 새 사용자를 만들거나 기존 사용자 계정을 편집합니다.

<!-- t_create_user.xml -->

>[!NOTE]
>
>새 사용자를 만들려면 [!UICONTROL CREATE_USER] 역할이 있어야 합니다. 기존 사용자를 편집하려면 [!UICONTROL EDIT_USER] 역할이 있어야 합니다.

1. 새 사용자를 만들려면 **[!UICONTROL Integration Users]** &gt; **[!UICONTROL Create a New User]**&#x200B;를 클릭합니다. 기존 사용자를 편집하려면 **[!UICONTROL Username]** 열에서 원하는 사용자를 클릭합니다.
2. 다음 필드를 채웁니다.
   * **[!UICONTROL First Name]**: (필수) 사용자의 이름을 지정합니다.
   * **[!UICONTROL Last Name]**: (필수) 사용자의 성을 지정합니다.
   * **[!UICONTROL Username]**: (필수) 사용자 이름을 지정합니다.
   * **[!UICONTROL Email Address]**: (필수) 사용자의 이메일 주소를 지정합니다.
   * **[!UICONTROL Phone Number]**: 사용자의 전화 번호를 지정합니다.
   * **[!UICONTROL IMS ID]**: 사용자를 지정합니다 [!UICONTROL Internet Messaging Service ID].
   * **[!UICONTROL User Roles]**: 원하는 사용자 역할을 선택합니다.
      * **[!UICONTROL DEXADMIN]**: Audience Manager [!UICONTROL Admin] 도구에서 작업을 수행하는 데 필요한 관리자 액세스 권한을 제공합니다. 이 옵션을 선택하지 않으면 개별 역할을 선택할 수 있습니다. 이러한 역할을 사용하면 사용자가 호출을 사용하여 [!DNL API] 작업을 수행할 수 있지만 관리 도구가 아닙니다.
      * **[!UICONTROL CREATE_USERS]**: 사용자가 호출을 사용하여 새 사용자를 만들 [!DNL API] 수 있습니다.
      * **[!UICONTROL DELETE_USERS]**: 사용자가 호출을 사용하여 기존 사용자를 삭제할 수 있도록 [!DNL API] 해줍니다.
      * **[!UICONTROL EDIT_USERS]**: 사용자가 호출을 사용하여 기존 사용자를 편집할 [!DNL API] 수 있습니다.
      * **[!UICONTROL VIEW_USERS]**: 사용자가 전화를 사용하여 Audience Manager 구성에서 다른 사용자를 볼 수 [!DNL API] 있습니다.
      * **[!UICONTROL CREATE_PARTNERS]**: 사용자가 전화를 사용하여 Audience Manager 파트너를 만들 [!DNL API] 수 있습니다.
      * **[!UICONTROL DELETE_PARTNERS]**: 사용자가 호출을 사용하여 Audience Manager 파트너를 삭제할 [!DNL API] 수 있습니다.
      * **[!UICONTROL EDIT_PARTNERS]**: 사용자가 전화를 사용하여 Audience Manager 파트너를 편집할 [!DNL API] 수 있습니다.
      * **[!UICONTROL VIEW_PARNTERS]**: 사용자가 전화를 사용하여 Audience Manager 파트너를 볼 [!DNL API] 수 있습니다.
   * **상태:** 이 사용자를 활성화된 Audience Manager 사용자로 **[!UICONTROL Active]** 만들려면 선택합니다.
3. 클릭 **[!UICONTROL Submit]**.

## Delete a User {#delete-user}

기존 [!UICONTROL Integration Users] 사용자를 삭제하려면 Audience Manager [!UICONTROL Admin] 도구의 페이지를 사용합니다.

<!-- t_delete_user.xml -->

>[!NOTE]
>
>새 사용자를 만들려면 **[!UICONTROL DELETE_USER]** 역할이 있어야 합니다.

1. 클릭 **[!UICONTROL Integration Users]**.
2. 원하는 ![](assets/icon_delete.png) 사용자의 **[!UICONTROL Actions]** 열을 클릭합니다.
3. Click **[!UICONTROL OK]** to confirm the deletion.
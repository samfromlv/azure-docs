---
title: 'Tutorial: Azure Active Directory integration with Mozy Enterprise | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Mozy Enterprise.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 11/21/2022
ms.author: jeedes
---
# Tutorial: Azure Active Directory integration with Mozy Enterprise

In this tutorial, you learn how to integrate Mozy Enterprise with Azure Active Directory (Azure AD).
Integrating Mozy Enterprise with Azure AD provides you with the following benefits:

* You can control in Azure AD who has access to Mozy Enterprise.
* You can enable your users to be automatically signed-in to Mozy Enterprise (Single Sign-On) with their Azure AD accounts.
* You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).
If you don't have an Azure subscription, [create a free account](https://azure.microsoft.com/free/) before you begin.

## Prerequisites

To configure Azure AD integration with Mozy Enterprise, you need the following items:

* An Azure AD subscription. If you don't have an Azure AD environment, you can get one-month trial [here](https://azure.microsoft.com/pricing/free-trial/)
* Mozy Enterprise single sign-on enabled subscription

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* Mozy Enterprise supports **SP** initiated SSO

## Adding Mozy Enterprise from the gallery

To configure the integration of Mozy Enterprise into Azure AD, you need to add Mozy Enterprise from the gallery to your list of managed SaaS apps.

**To add Mozy Enterprise from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon.

	![The Azure Active Directory button](common/select-azuread.png)

2. Navigate to **Enterprise Applications** and then select the **All Applications** option.

	![The Enterprise applications blade](common/enterprise-applications.png)

3. To add new application, click **New application** button on the top of dialog.

	![The New application button](common/add-new-app.png)

4. In the search box, type **Mozy Enterprise**, select **Mozy Enterprise** from result panel then click **Add** button to add the application.

	 ![Mozy Enterprise in the results list](common/search-new-app.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with Mozy Enterprise based on a test user called **Britta Simon**.
For single sign-on to work, a link relationship between an Azure AD user and the related user in Mozy Enterprise needs to be established.

To configure and test Azure AD single sign-on with Mozy Enterprise, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Configure Mozy Enterprise Single Sign-On](#configure-mozy-enterprise-single-sign-on)** - to configure the Single Sign-On settings on application side.
3. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Create Mozy Enterprise test user](#create-mozy-enterprise-test-user)** - to have a counterpart of Britta Simon in Mozy Enterprise that is linked to the Azure AD representation of user.
6. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal.

To configure Azure AD single sign-on with Mozy Enterprise, perform the following steps:

1. In the [Azure portal](https://portal.azure.com/), on the **Mozy Enterprise** application integration page, select **Single sign-on**.

    ![Configure single sign-on link](common/select-sso.png)

2. On the **Select a Single sign-on method** dialog, select **SAML/WS-Fed** mode to enable single sign-on.

    ![Single sign-on select mode](common/select-saml-option.png)

3. On the **Set up Single Sign-On with SAML** page, click **Edit** icon to open **Basic SAML Configuration** dialog.

	![Edit Basic SAML Configuration](common/edit-urls.png)

4. On the **Basic SAML Configuration** section, perform the following steps:

    ![Mozy Enterprise Domain and URLs single sign-on information](common/sp-signonurl.png)

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<tenantname>.Mozyenterprise.com`

	> [!NOTE]
	> The value is not real. Update the value with the actual Sign-On URL. Contact [Mozy Enterprise Client support team](https://www.safenames.net/about-us/contact-us) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

5. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, click **Download** to download the **Certificate (Base64)** from the given options as per your requirement and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

6. On the **Set up Mozy Enterprise** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

	a. Login URL

	b. Azure AD Identifier

	c. Logout URL

### Configure Mozy Enterprise Single Sign-On

1. In a different web browser window, log into your Mozy Enterprise company site as an administrator.

2. In the **Configuration** section, click **Authentication Policy**.
   
	![Screenshot shows Authentication Policy selected from Configuration.](./media/mozy-enterprise-tutorial/ic777314.png "Authentication policy")

3. On the **Authentication Policy** section, perform the following steps:
   
	![Screenshot shows the Authentication Policy section where you can enter the values described.](./media/mozy-enterprise-tutorial/ic777315.png "Authentication policy")
   
    a. Select **Directory Service** as **Provider**.
   
    b. Select **Use LDAP Push**.
   
    c. Click the **SAML Authentication** tab.
   
    d. Paste **Login URL**, which you have copied from the Azure portal into the **Authentication URL** textbox.
   
    e. Paste **Azure AD Identifier**, which you have copied from the Azure portal into the **SAML Endpoint** textbox.
   
    f. Open your downloaded base-64 encoded certificate in notepad, copy the content of it into your clipboard, and then paste the entire Certificate into **SAML Certificate** textbox.
   
    g. Select **Enable SSO for Admins to log in with their network credentials**.
   
    h. Click **Save Changes**.

### Create an Azure AD test user 

The objective of this section is to create a test user in the Azure portal called Britta Simon.

1. In the Azure portal, in the left pane, select **Azure Active Directory**, select **Users**, and then select **All users**.

    ![The "Users and groups" and "All users" links](common/users.png)

2. Select **New user** at the top of the screen.

    ![New user Button](common/new-user.png)

3. In the User properties, perform the following steps.

    ![The User dialog box](common/user-properties.png)

    a. In the **Name** field enter **BrittaSimon**.
  
    b. In the **User name** field type **brittasimon\@yourcompanydomain.extension**  
    For example, BrittaSimon@contoso.com

    c. Select **Show password** check box, and then write down the value that's displayed in the Password box.

    d. Click **Create**.

### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to Mozy Enterprise.

1. In the Azure portal, select **Enterprise Applications**, select **All applications**, then select **Mozy Enterprise**.

	![Enterprise applications blade](common/enterprise-applications.png)

2. In the applications list, select **Mozy Enterprise**.

	![The Mozy Enterprise link in the Applications list](common/all-applications.png)

3. In the menu on the left, select **Users and groups**.

    ![The "Users and groups" link](common/users-groups-blade.png)

4. Click the **Add user** button, then select **Users and groups** in the **Add Assignment** dialog.

    ![The Add Assignment pane](common/add-assign-user.png)

5. In the **Users and groups** dialog select **Britta Simon** in the Users list, then click the **Select** button at the bottom of the screen.

6. If you are expecting any role value in the SAML assertion then in the **Select Role** dialog select the appropriate role for the user from the list, then click the **Select** button at the bottom of the screen.

7. In the **Add Assignment** dialog click the **Assign** button.

### Create Mozy Enterprise test user

In order to enable Azure AD users to log into Mozy Enterprise, they must be provisioned into Mozy Enterprise. In the case of Mozy Enterprise, provisioning is a manual task.

>[!NOTE]
>You can use any other Mozy Enterprise user account creation tools or APIs provided by Mozy Enterprise to provision Azure AD user accounts.

**To provision a user accounts, perform the following steps:**

1. Log in to your **Mozy Enterprise** tenant.

2. Click **Users**, and then click **Add New User**.
   
	![Users](./media/mozy-enterprise-tutorial/ic777317.png "Users")
   
	>[!NOTE]
	>The **Add New User** option is only displayed only if **Mozy** is selected as the provider under **Authentication policy**. If SAML Authentication is configured, then the users are added automatically on their first login through Single sign on.
    
3. On the new user dialog, perform the following steps:
   
	![Add Users](./media/mozy-enterprise-tutorial/ic777318.png "Add Users")
   
    a. From the **Choose a Group** list, select a group.
   
    b. From the **What type of user** list, select a type.
   
    c. In the **Username** textbox, type the name of the Azure AD user.
   
    d. In the **Email** textbox, type the email address of the Azure AD user.
   
    e. Select **Send user instruction email**.
   
    f. Click **Add User(s)**.

     >[!NOTE]
     > After creating the user, an email will be sent to the Azure AD user that includes a link to confirm the account before it becomes active.

### Test single sign-on 

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the Mozy Enterprise tile in the Access Panel, you should be automatically signed in to the Mozy Enterprise for which you set up SSO. For more information about the Access Panel, see [Introduction to the Access Panel](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Additional Resources

- [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](./tutorial-list.md)

- [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)

- [What is Conditional Access in Azure Active Directory?](../conditional-access/overview.md)
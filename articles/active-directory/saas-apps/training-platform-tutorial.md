---
title: 'Tutorial: Azure AD SSO integration with Training Platform'
description: Learn how to configure single sign-on between Azure Active Directory and Training Platform.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 06/14/2022
ms.author: jeedes

---

# Tutorial: Azure AD SSO integration with Training Platform

In this tutorial, you'll learn how to integrate Training Platform with Azure Active Directory (Azure AD). When you integrate Training Platform with Azure AD, you can:

* Control in Azure AD who has access to Training Platform.
* Enable your users to be automatically signed-in to Training Platform with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Training Platform single sign-on (SSO) enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Azure AD.
For more information, see [Azure built-in roles](../roles/permissions-reference.md).

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Training Platform supports **SP** and **IDP** initiated SSO.
* Training Platform supports **Just In Time** user provisioning.

## Add Training Platform from the gallery

To configure the integration of Training Platform into Azure AD, you need to add Training Platform from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Training Platform** in the search box.
1. Select **Training Platform** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for Training Platform

Configure and test Azure AD SSO with Training Platform using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Training Platform.

To configure and test Azure AD SSO with Training Platform, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Training Platform SSO](#configure-training-platform-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Training Platform test user](#create-training-platform-test-user)** - to have a counterpart of B.Simon in Training Platform that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Training Platform** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

    ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** textbox, type a value using the following pattern:
    `urn:auth0:living-security:<ID>`

    b. In the **Reply URL** textbox, type a URL using the following pattern:
    `https://identity.livingsecurity.com/login/callback?connection=<ID>`

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:    

    In the **Sign-on URL** text box, type the URL:
    `https://app.livingsecurity.com`

    > [!Note]
    > These values are not real. Update these values with the actual Identifier and Reply URL. Contact [Training Platform support team](mailto:support@livingsecurity.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. On the **Set up single sign-on with SAML** page, In the **SAML Signing Certificate** section, click copy button to copy **App Federation Metadata Url** and save it on your computer.

	![Screenshot shows the Certificate download link.](common/copy-metadataurl.png "Certificate") 

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Training Platform.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Training Platform**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Training Platform SSO

1. Log in to your Training Platform company site as an administrator.

1. Go to **Configuration** section and select **SAML SSO Configuration** tab.

1. Make sure your application is set to **Metadata URL** Mode.

1. In the **Identity Provider Metadata Url*** textbox, paste the **App Federation Metadata Url** which you have copied from the Azure portal.

    ![Screenshot that shows the Configuration Settings.](./media/training-platform-tutorial/settings.png "Configuration")

1. Click **Save**.

### Create Training Platform test user

In this section, a user called B.Simon is created in Training Platform. Training Platform supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in Training Platform, a new one is created after authentication.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Training Platform Sign-on URL where you can initiate the login flow.  

* Go to Training Platform Sign on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Training Platform for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Training Platform tile in the My Apps, if configured in SP mode you would be redirected to the application sign-on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Training Platform for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Next steps

Once you configure Training Platform you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).

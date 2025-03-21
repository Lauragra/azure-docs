---
title: 'Tutorial: Azure Active Directory integration with ARES for Enterprise | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and ARES for Enterprise.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 06/10/2021
ms.author: jeedes
---
# Tutorial: Azure Active Directory integration with ARES for Enterprise

In this tutorial, you'll learn how to integrate ARES for Enterprise with Azure Active Directory (Azure AD). When you integrate ARES for Enterprise with Azure AD, you can:

* Control in Azure AD who has access to ARES for Enterprise.
* Enable your users to be automatically signed-in to ARES for Enterprise with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* ARES for Enterprise single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* ARES for Enterprise supports **SP** initiated SSO.

* ARES for Enterprise supports **Just In Time** user provisioning.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add ARES for Enterprise from the gallery

To configure the integration of ARES for Enterprise into Azure AD, you need to add ARES for Enterprise from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **ARES for Enterprise** in the search box.
1. Select **ARES for Enterprise** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for ARES for Enterprise

Configure and test Azure AD SSO with ARES for Enterprise using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in ARES for Enterprise.

To configure and test Azure AD SSO with ARES for Enterprise, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure ARES for Enterprise SSO](#configure-ares-for-enterprise-sso)** - to configure the single sign-on settings on application side.
    1. **[Create ARES for Enterprise test user](#create-ares-for-enterprise-test-user)** - to have a counterpart of B.Simon in ARES for Enterprise that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **ARES for Enterprise** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

4. On the **Basic SAML Configuration** section, perform the following step:

    In the **Sign on URL** text box, type the URL:
    `https://login.graebert.com`

5. On the **Set up Single Sign-On with SAML** page, In the **SAML Signing Certificate** section, click copy button to copy **App Federation Metadata Url** and save it on your computer.

    ![The Certificate download link](common/copy-metadataurl.png)

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

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to ARES for Enterprise.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **ARES for Enterprise**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure ARES for Enterprise SSO

To configure single sign-on on **ARES for Enterprise** side, you need to send the **App Federation Metadata Url** to [ARES for Enterprise support team](mailto:support@graebert.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create ARES for Enterprise test user

In this section, a user called Britta Simon is created in ARES for Enterprise. ARES for Enterprise supports **just-in-time provisioning**, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in ARES for Enterprise, a new one is created when you attempt to access ARES for Enterprise.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

* Click on **Test this application** in Azure portal. This will redirect to ARES for Enterprise Sign-on URL where you can initiate the login flow. 

* Go to ARES for Enterprise Sign-on URL directly and initiate the login flow from there.

* You can use Microsoft My Apps. When you click the ARES for Enterprise tile in the My Apps, this will redirect to ARES for Enterprise Sign-on URL. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Next steps

Once you configure ARES for Enterprise you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).

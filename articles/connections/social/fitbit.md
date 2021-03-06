---
title: Connect Apps to Fitbit
connection: Fitbit
image: /media/connections/fitbit.png
seo_alias: fitbit
index: 14
description: Learn how to add login functionality to your app with Fitbit. You will need to obtain a Client Id and Client Secret for Fitbit.
toc: true
topics:
  - connections
  - social
  - fitbit
contentType: how-to
useCase:
    - customize-connections
    - add-idp
---

# Connect Apps to Fitbit

You can add functionality to your web app that allows your users to log in with Fitbit. 

::: note
New connections with Fitbit will use OAuth 2.0. Please see the following documentation on [Using OAuth 2.0](https://dev.fitbit.com/docs/oauth2/) with Fitbit.
:::

## Prerequisites

Before you connect your Auth0 app to Fitbit, you must have a [Fitbit Developer](https://dev.fitbit.com) account.

## Steps

To connect your app to Fitbit, you will:

1. [Set up your app in Fitbit](#set-up-your-app-in-fitbit)
2. [Create and enable a connection in Auth0](#create-and-enable-a-connection-in-auth0)
3. [Test the connection](#test-the-connection)

### Set up your app in Fitbit

Set up an app in Fitbit. During this process, Fitbit will generate a **API Key** and **API Secret** for your application; make note of these.

1. Log in to [Fitbit's Developer](https://dev.fitbit.com) portal, and select **Register an App**.
2. Complete information about your app including the following:

| Field | Description
--------|------------
Application Website | `https://${account.namespace}`
OAuth 2.0 Application Type | Select **Application**
Callback URL | `https://${account.namespace}/login/callback`
Default Access Type | The type of access granted to the app

<%= include('../_find-auth0-domain-redirects') %>

3. Click **Register**.

### Create and enable a connection in Auth0

[Set up the Fitbit social connection](/dashboard/guides/connections/set-up-connections-social) in Auth0. Make sure you have the generated **API Key** and the **API Secret**.

### Test the connection

You're ready to [test your connection](/dashboard/guides/connections/test-connections-social). After logging in, you'll be prompted to allow your app access. To do so, click **Install unlisted app**.

::: note
Fitbit is a registered trademark and service mark of Fitbit, Inc. Auth0 is designed for use with the Fitbit platform. This product is not part of Fitbit, and Fitbit does not service or warrant the functionality of this product.
:::

<%= include('../_quickstart-links.md') %>

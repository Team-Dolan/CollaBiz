# CollabBiz - an initiative to collaborate small businesses

This application was devloped as a solution for Microsoft's HackOnAzure.

## Team-Dolan

- ROHAN TANEJA (<b>Leader</b>)
- Ujjawal Aggarwal
- Aaryaman Saini

## Contents

1. [Overview](#overview)
2. [Diagrams](#diagrams)
3. [Technologies](#technologies)
4. [Getting started](#getting-started)
5. [Deployment](#deployment)
6. [Usages](#usages)

## Overview

We identified two problems and came up with a solution that can help both the entities. These problems were identified from our own personal experiences when it became hard for us to get certain items in stores. While the Lockdown, has proved to be a good step, but it came with some new problem. There are many small businesses, which depend on their daily sales and in Lockdown, many people stopped buying stuff. So, they had to face huge backlashes. Also, there are many things that people need, like important medicines and electronics, but these are not available in their local stores on which they counted on normally. The reason for unavailability of such items in some stores can be because of restrictions on delivery of goods to every store. So, we can see there are two problems here.
So, the question was, how can we help small businesses to be able to keep selling products and how can people get those products for which they would normally depend on local stores? The answer is CollabBiz.

## Diagrams

![Workflow diagram](/images/workflow.png)

![Flow-chart diagram](/images/flow-chart.png)

## Technologies

## Getting started
<details>
  <summary>Click here to view!</summary>

### Prerequisites

- Register for an [IBM Cloud](https://www.ibm.com/account/reg/us-en/signup?formid=urx-42793&eventid=cfc-2020?cm_mmc=OSocial_Blog-_-Audience+Developer_Developer+Conversation-_-WW_WW-_-cfc-2020-ghub-starterkit-cooperation_ov75914&cm_mmca1=000039JL&cm_mmca2=10008917) account.
- Install and configure [IBM Cloud CLI](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#overview).
- Register for a [HERE](https://developer.here.com/ref/IBM_starterkit_Covid?create=Freemium-Basic) account.
- Install [React Native CLI dependencies](https://reactnative.dev/docs/getting-started.html).
    - [Node.js](https://nodejs.org/en/)
    - [Watchman](https://facebook.github.io/watchman/docs/install)
    - **Android only**
        - [Java Development Kit](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html)
        - [Android Studio](https://developer.android.com/studio/index.html) - add Android 9 (Pie) SDK & configure `ANDROID_HOME`
        - [Create an Android Virtual Device (AVD)](https://developer.android.com/studio/run/managing-avds.html) - with Pie image (API Level 28)
- Clone the [repository](https://github.com/Team-Dolan/CollaBiz.git).

</details>

### Steps
<details>
  <summary>Click here to view!</summary>

1. [Set up an instance of Watson Assistant](#1-set-up-an-instance-of-watson-assistant).
1. [Provision a CouchDB instance using Cloudant](#2-Provision-a-CouchDB-instance-using-Cloudant).
1. [Generate an API Key from the HERE Developer Portal](#3-generate-an-api-key-from-the-here-developer-portal).
1. [Run the server](#4-run-the-server).
1. [Run the mobile application](#5-run-the-mobile-application).

### 1. Set up an instance of Watson Assistant

Log in to IBM Cloud and provision a Watson Assistant instance.

1. Provision an instance of **Watson Assistant** from the [IBM Cloud catalog](https://cloud.ibm.com/catalog/services/watson-assistant).
1. Launch the Watson Assistant service.
1. [Create an **Assistant**](https://cloud.ibm.com/docs/assistant?topic=assistant-assistant-add).
1. [Add a dialog skill](https://cloud.ibm.com/docs/assistant?topic=assistant-skill-dialog-add) to the **Assistant** by importing the [`starter-kit-cooperation-dialog-skill.json`](./starter-kit/assistant/starter-kit-cooperation-dialog-skill.json) file.
1. Go back to All Assistants page, open **Settings** from the action menu ( **`⋮`** ) and click on **API Details**.
1. Note the **Assistant ID**, **API Key**, and **Assistant URL**. For **Assistant URL**, make note of the base URL/domain (e.g., `https://api.us-south.assistant.watson.cloud.ibm.com` or `https://api.eu-gb.assistant.watson.cloud.ibm.com`) and not the full directory/path. You will need all three of these values in Step 4 below.

1. Go to **Preview Link** to get a link to test and verify the dialog skill.

### 2: Provision a CouchDB instance using Cloudant

Log into the IBM Cloud and provision a [CouchDB instance using Cloudant](https://www.ibm.com/cloud/cloudant).

1. From the catalog, select Databases and then the Cloudant panel.
1. Once selected, you can choose your Cloudant plan -- there is a free tier for simple testing that is sufficient to run this CIR example. You should choose an appropriate region, give the service a name, and it is recommended you choose **Use only IAM** under **Available authentication methods**. You can leave the other settings with their defaults. Click the blue **Create** button when ready.
1. Once your Cloudant instance has been created, you need to create a service credential that the CIR API Server can use to communicate with it. By selecting your running Cloudant instance, you can choose **Service credentials** from the left-hand menu. Create a new service credential and give it a name (it doesn't matter what you call it).
1. Once created, you can display the credentials by selecting **view service credentials**, and then copy the credential, so you are ready to paste it into the code of the API server in Step 4.

### 3. Generate an API Key from the HERE Developer Portal

The application uses HERE Location Services for maps, searching, and routing.

To access these services, you'll need an API key. Follow the instructions outlined in the [HERE Developer Portal](https://developer.here.com/ref/IBM_starterkit_Covid?create=Freemium-Basic) to [generate a JavaScript API key](https://developer.here.com/documentation/authentication/dev_guide/topics/api-key-credentials.html).

### 4. Run the server

To set up and launch the server application:

1. Go to the `starter-kit/server-app` directory of the cloned repo.
1. Copy the `.env.example` file in the `starter-kit/server-app` directory, and create a new file named `.env`.
1. Edit the newly created `.env` file and update the `ASSISTANT_URL`, `ASSISTANT_ID`, and `ASSISTANT_IAM_APIKEY` with the values from the dialog skill's API Detail page in Watson Assistant, from Step 1. Also, update the `CLOUDANT_ID` and `CLOUDANT_IAM_APIKEY` with the values from the service credential you created in Step 2. (Note that the `username` from the credential is what should be used for the `CLOUDANT_ID`.)
1. Edit the **name** value in the `manifest.yml` file to your application name (for example, _my-app-name_).
1. From a terminal:
    1. Go to the `starter-kit/server-app` directory of the cloned repo.
    1. Install the dependencies: `npm install`.
    1. Launch the server application locally or deploy to IBM Cloud:
        - To run locally:
            1. Start the application: `npm start`.
            1. The server can be accessed at <http://localhost:3000>.
        - To deploy to IBM Cloud:
            1. Log in to your IBM Cloud account using the IBM Cloud CLI: `ibmcloud login`.
            1. Target a Cloud Foundry org and space: `ibmcloud target --cf`.
            1. Push the app to IBM Cloud: `ibmcloud app push`.
            1. The server can be accessed at a URL using the **name** given in the `manifest.yml` file (for example,  <https://my-app-name.bluemix.net>).

### 5. Run the mobile application

To run the mobile application (using the Xcode iOS Simulator or Android Studio Emulator):

1. Go to the `starter-kit/mobile-app` directory of the cloned repo.
1. Copy the `.env.example` file in the `starter-kit/mobile-app` directory, and create a file named `.env`.
1. Edit the newly created `.env` file:
    - Update the `STARTER_KIT_SERVER_URL` with the URL to the server app launched in the previous step.
        > **Note**: If you are running the server locally and testing with the Android Emulator set the `STARTER_KIT_SERVER_URL` using the local machine's URL (e.g., `http://10.0.2.2:3000`) instead of `localhost`
    - Update the `HERE_APIKEY` with the API key generated in the HERE Developer Portal.
1. From a terminal:
    1. Go to the `starter-kit/mobile-app` directory.
    1. Install the dependencies: `npm install`.
        - **Android only**: `npm run android`
            > **Note**: Your Android Studio needs to have the `Android 9 (Pie)` SDK and a `Pie API Level 28` virtual device

</details>

With the application running in the simulator/emulator, you should be able to navigate through the various screens:

<details>
  <summary>Click here to view!</summary>

  ![Home Page](/images/Home.JPG)
  ![Current Inventory](/images/curr_inv.JPG)
  ![Add Inventory](/images/add_inven.JPG)
  ![Update Inventory](/images/update_inv.JPG)
  ![Search Inventory](/images/search_inv.JPG)
  ![Chat with Watson](/images/chat_watson.JPG)
  ![User Chat Init](/images/enter_chat.JPG)
  ![User Chat Interface](/images/chat.JPG)
</details>

## Deployment

A Supplier (who may be a regular resident, a small business, a voluntary organization, etc.) that has food, supplies, resources, or other essentials they can provide opens the mobile application and fills out a brief form that indicates what they have. This information is then stored in the database.

A Recipient, who is in need of food, supplies, resources, or other essentials, opens the mobile application and can use the chat interface to locate supplies near them. For instance, they might type "Where can I find bread?" or "Can someone collect my shopping for me?" The mobile application then accesses the database (after first understanding the question) and then displays a map showing locally where they can find what they are looking for.

## Usages

The goal was to make a web-application to get businesses to collaborate. We aimed to establish a networking model for business to function, especially Pharmacies, which tend to be most frequently visited for need of sanitization and hygiene products. This helps in modelling a market to get in touch with the supply chain as closely and conviniently, and restrict the movement of community to look in search of certain products. The application can come in handy even after lockdown.

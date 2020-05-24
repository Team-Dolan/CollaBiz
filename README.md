# CollabBiz - an initiative to collaborate small businesses

This solution is based over the community cooperation model provided by technologists from IBM.

## Team-Dolan

- <b>Rohan Taneja</b> <b>TEAM LEADER</b>
- Ujjawal Aggarwal
- Aaryaman Saini

## Contents

1. [Overview](#overview)
2. [The idea](#the-idea)
3. [How it works](#how-it-works)
4. [Diagrams](#diagrams)
5. [Technology](#technology)
6. [Getting started](#getting-started)
7. [Resources](#resources)
8. [License](#license)

## Overview

### What's the problem?

We identified two problems and came up with a solution that can help both the entities. These problems were identified from our own personal experiences when it became hard for us to get certain items in stores. COVID-19 is a pandemic as declared by WHO. Initially, people took this lightly as the cases were only limited to China. Gradually, cases were being reported all over the world and people then started to panic. Governments, in all countries, started taking measures to prevent the spread of this disease. Some of the measures taken by the governments, as suggested by WHO, are Social Distancing. To implement this, Indian Government declared LOCKDOWN, so that social distancing can be ensured. This is a big step and it did indeed help to control the number of cases in India. Many people stayed at home for their own safety and only essential workers were allowed to work.
While this, the Lockdown, has proved to be a good step, but with this came a new problem. There are many small businesses, which depend on their daily sales and in Lockdown, many people stopped buying stuff. So, they had to face huge backlashes. Also, there are many things that people need like important medicines and electronics, but these are not available in their local stores on which they count normally. The reason for unavailability of such items in some stores can be because of restrictions on delivery of goods to every store. So, we can see there are two problems here.
So, the question was, how can we help small businesses to be able to keep selling products and how can people get those products for which they would normally depend on local stores? The answer is CollabBiz.

### How can technology help?

Mobile, web, and cloud services enable rapid deployment of applications that can empower cooperation in the community. [Watson Assistant](https://www.ibm.com/cloud/watson-assistant/) is a service on [IBM Cloud](https://cloud.ibm.com) that allows you to build, train, and deploy conversational interactions into any application, device, or channel.

Creating a chatbot using Watson Assistant can help you address the issues that your users may face while trying to gather the necessary information. Embedding location/routing services (like [HERE](https://developer.here.com/products/routing)) can enhance such applications, giving optimum guidance so that they are outside of their isolation location for the minimum amount of time.

## The idea

The goal is make a web-application to bring such a collaboration at vast level. Using the given kit for starters we added more form and categories to bring suitable suppliers and recipients together. For starters, the collaboration functionality as provided we added a chat functionality on top to bring the collaborators together in the chatroom. A ticketing system for order generation and logistic handling has to be added to bring a sense of security for orders to be supplied.

We aim to establish a networking model for business to function especially Pharmacies which tend to be most frequently visited for need of sanitization and hygiene products. This helps in modelling a market to get in touch with the supply chain as close and conviniently and restrict the movement of community to look in search of certain products.

## Features

- [x] Home Activity
- [x] Inventory - Add, Edit, and Delete
- [x] Location Services - HERE
- [x] Watson Assistant - Training - Covid only updates
- [x] Watson Assistant - Training - User support
- [x] Chatroom service for Collaborators - Firebase - Group Chat
- [ ] Complaint Form/ Report False Supply
- [ ] Order and Logistics Ticketing
- [ ] Sales Tracking and Review
- [ ] Transaction History
- [ ] Customer Record and many more 

## How it works


A Supplier (who may be a regular resident, a small business, a voluntary organization, etc.) that has food, supplies, resources, or other essentials they can provide opens the mobile application and fills out a brief form that indicates what they have. This information is then stored in a database in the IBM Cloud.

A Recipient, who is in need of food, supplies, resources, or other essentials, opens the mobile application and can use the chat interface to locate supplies near them. For instance, they might type "Where can I find bread?" or "Can someone collect my shopping for me?" The mobile application then accesses the database (after first understanding the question via Watson Assistant) and then displays a map showing locally where they can find what they are looking for.



## Diagrams

![Workflow diagram](/images/workflow.png)

![Flow-chart diagram](/images/flow-chart.png)





## Technology

### IBM Cloud Services
<details>
  <summary>Click here to view!</summary>

- [Bot Asset Exchange](https://developer.ibm.com/code/exchanges/bots/)
- [IBM Watson Assistant](https://www.ibm.com/cloud/watson-assistant/)
- [How-to guides for chatbots](https://www.ibm.com/watson/how-to-build-a-chatbot)
- [Learning path: Getting started with Watson Assistant](https://developer.ibm.com/series/learning-path-watson-assistant/)
- [Build a Chatbot For Your Mobile App](https://developer.ibm.com/technologies/mobile/patterns/building-a-chatbot-with-kubernetes-watson-assistant-and-elastic-search)
- [Build a cross-platform mobile app using React Native](https://developer.ibm.com/technologies/mobile/patterns/build-a-cross-platform-mobile-app-to-search-company-news-and-gain-insights)
- [Building successful mobile apps article series](https://developer.ibm.com/series/building-successful-mobile-apps/)
- [Node-RED Slack integration](https://www.ibm.com/cloud/blog/create-a-chatbot-on-ibm-cloud-and-integrate-with-slack-part-1)

### HERE Technologies

- [HERE.com API Key](https://developer.here.com/ref/IBM_starterkit_Covid?create=Freemium-Basic)
- [HERE Maps](https://developer.here.com/products/maps)
- [HERE Routing](https://developer.here.com/products/routing)
- [Integrate interactive maps and location features into your application](https://developer.here.com/documentation/)

</details>

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
<img align="left" width="320" height="530" src=/images/Home.JPG>
<img align="right"  width="320" height="530" src=/images/curr_inv.JPG>
<img align="left" width="320" height="530"  src=/images/add_inven.JPG>
<img align="right" width="320" height="530" src=/images/update_inv.JPG>
<img align="left" width="320" height="530"  src=/images/search_inv.JPG>
<img align="right" width="320" height="530" src=/images/chat_watson.JPG>
<img align="left"  width="320" height="530"  src=/images/enter_chat.JPG>
<img align="right" width="320" height="530" src=/images/chat.JPG>
</details>

## Resources

- [IBM Cloud](https://www.ibm.com/cloud)
- [Watson Assistant](https://cloud.ibm.com/docs/assistant?topic=assistant-getting-started)
- [IBM Cloudant](https://cloud.ibm.com/docs/Cloudant?topic=cloudant-overview)
- [HERE Location Services](https://developer.here.com/documentation)
- [Node.js](https://nodejs.org)
- [React Native](https://reactnative.dev/)
- [IBM Blockchain for Developers](https://developer.ibm.com/technologies/blockchain/)


## License

This solution starter is made available under the [Apache 2 License](LICENSE).

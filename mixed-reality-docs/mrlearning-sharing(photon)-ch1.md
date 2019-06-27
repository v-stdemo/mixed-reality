---
title: MR Learning Sharing Module for HoloLens 2
description: Complete this course to learn how to implement multi-user shared experiences within a HoloLens 2 application.
author: jessemcculloch
ms.author: jemccull
ms.date: 02/26/2019
ms.topic: article
keywords: mixed reality, unity, tutorial, hololens
---

# Setting up photon

In this lesson, we learn how to prepare for creating a shared experience by importing Photon Unity Networking (PUN) into your Unity project. Photon is one of several networking options available to mixed reality developers to create shared experiences. We'll learn how to create a Photon account, import Photon, and create an optional local server

Objectives:

* Learn how to create a Photon account

* Learn how to find and import Photon Unity Networking

* Set up a local Photon server

  

### Setting Up Photon

1. Set up a [Photon](https://dashboard.photonengine.com/en-US/Account/SignUp) account. Navigate to the Photon sign-up page by going [here](https://dashboard.photonengine.com/en-US/Account/SignUp). Follow the instructions on the sign-up page to create the account. 
   

![Module3Chapter1step1im](images/module3chapter1step1im.PNG)



![Module3Chapter1step6im](images/module3chapter1step6im.PNG)

2. Create an application ID by clicking Create a New App..

![Module3Chapter1step7aim](images/module3chapter1step7aim.PNG)

3. Select Photon PUN from the drop-down menu under Photon Type. Then give it a name. In this example, we named it HoloLensPhotonProject. When finished, click CREATE.

![Module3Chapter1step7bim](images/module3chapter1step7bim.PNG)

4. Once that is done, return to your application page and you will see something similar in the image below. Click on the application ID and copy it. Paste it where you can easily find it.  

![Module3Chapter1step8im](images/module3chapter1step8im.PNG)

5. Create a new Unity project, and name it HLSharingProject. For instructions on how to create a new Unity project, refer to [the Base Module's "Create Unity Project" section](https://docs.microsoft.com/en-us/windows/mixed-reality/mrlearning-base-ch1#create-new-unity-project). 

6. Once the project has loaded, click on the Assets Store tab as shown in the image below. In the search box highlighted in the image below, type in PUN, and select the "hoton PUN 2 - FREE asset from the search results. 

![Module3Chapter1step10im](images/module3chapter1step10im.PNG)

7. Download and import this asset by pressing the Download and Import buttons.

![Module3Chapter1step11im](images/module3chapter1step11im.PNG)

8. Once Photon has completed the importing process, the Pun Wizard will appear. Take the application ID, which should be in your clipboard from Step 4, and paste it into the AppID box. Press Setup Project. 
![module3chapter1step12im](images/module3chapter1step12im.PNG)

9. After successfully adding the AppID, navigate to "Photon"->"PhotonUnityNetworking" -> Resources->PhotonServerSettings in Assets. Select the Use Name Server option, and set the fixed region to US or your photon service region.

   ![module3chapter1step13im](images/module3chapter1step13im.PNG)

## Congratulations

You have successfully created a Photon account, set up a local Photon server, and imported PUN into Unity. Your next step is to set up the project and allow connections with other users so that multiple users can see your work. 

[Next Lesson: Sharing(Photon) Lesson 2](mrlearning-sharing(photon)-ch2.md)


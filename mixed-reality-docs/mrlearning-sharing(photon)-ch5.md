---
title: MR Learning Sharing Module for HoloLens 2
description: Complete this course to learn how to implement multi-user shared experiences within a HoloLens 2 application.
author: jessemcculloch
ms.author: jemccull
ms.date: 02/26/2019
ms.topic: article
keywords: mixed reality, unity, tutorial, hololens
---

# 5. Integration Azure Spatial Anchors into a shared experience

In this tutorial, we learn how to integrate Azure Spatial Anchors (ASA) into our shared experience. ASA allows multiple co-located devices to have a common reference if their physical environment is to anchor virtual experiences such that all participants see objects in the same physical place.

Before proceeding with this lesson, we'll need to complete the ASA learning module, which will cover ASA basics, Azure account and resource creation, and other fundamental buildings blocks that are required before we can integrate ASA into our shared experience.

Objectives:

- Integrate ASA into a shared experience for multi-device alignment
- Learn the fundamentals of how ASA works in the context of a local shared experience

### Instructions

1. Save the project from the previous lesson (control+S) and name it, HLSharedProjectMainPart5.unity, so that it's easier to find when you need it again.

2. Select the TableAnchor prefab underneath the MixedRealityPlayspace parent object, and delete it.

![Module3Chapter5tep2im](images/module3chapter5step2im.PNG)



3.  In the Project view go to Assets->Resources->Prefabs, and drag the TableAnchor prefab on top of the SharedPlayground object to make it a child.
4. ​	Expand the MixedRealityPlayspace parent object, TableAnchor object, and expand the Buttons object as well. 

![Module3hapter5step5im](images/module3chapter5step5im.PNG)

4. Now in the hierarchy, select ShareAzureAnchorButton, and move your attention to the Inaspector panel. Scroll down to the drop-down menu shown in the image below, and select AnchorModuleScript and click ShareAnchorNetework().

![Module3hapter5step6im](images/module3chapter5step6im.PNG)

5. Select GetAzureAnchorButton (see Step 4), and move your attention back to the Inspector panel. Scroll down to the drop-down menu shown in the image below, and select AnchorModuleScript, and click GetSharedAnchorNetwork(), and save.

![Module3hapter5step7im](images/module3chapter5step7im.PNG)




## Congratulations

In this Lesson you learned how to integrate Azure's powerful new Spatial Anchors to align co-located devices in a shared experience! This lesson also concludes the Sharing Module. We learned how to set up a new Photon account, integrate Photon and PUN into a new Unity application, configuring avatars and shared objects, and finally aligning multiple participants using ASA. 


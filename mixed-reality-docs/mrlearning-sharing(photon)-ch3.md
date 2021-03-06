---
title: Multi-user capabilities tutorials - 4. Sharing object movements with multiple users
description: Complete this course to learn how to implement multi-user shared experiences within a HoloLens 2 application.
author: jessemcculloch
ms.author: jemccull
ms.date: 02/26/2019
ms.topic: article
keywords: mixed reality, unity, tutorial, hololens
ms.localizationpriority: high
---

# 3. Sharing object movements with multiple users

In this tutorial, you will learn how to share the movements of objects so that all participants of a shared experience can collaborate and view each others' interactions.

## Objectives

* Configure your project to share the movements of objects
* Learn how to build a basic multi-user collaborative application

## Preparing the scene

In this section, you will prepare the scene by adding the tutorial prefab.

In the Project window, navigate to the **Assets** > **MRTK.Tutorials.MultiUserCapabilities** > **Prefabs** folder and drag the **TableAnchor** prefab on top of the **SharedPlayground** object in the Hierarchy window to add it to your scene as a child of the SharedPlayground object:

![mrlearning-sharing](images/mrlearning-sharing/tutorial3-section1-step1-1.png)

## Configuring PUN to instantiate the objects

In this section, you will configure the project to use the RocketLauncher_Complete_Variant prefab you created in the previous section and define where it will be instantiated.

In the Project window, navigate to the **Assets** > **MRTK.Tutorials.MultiUserCapabilities** > **Resources** folder.

In the Hierarchy window, expand the **NetworkLobby** object and select the **NetworkRoom** child object, then in the Inspector window, locate the **Photon Room (Script)** component and configure it as follows:

* To the **Photon User Prefab** field, assign the **PhotonUser** prefab from the Resources folder

![mrlearning-sharing](images/mrlearning-sharing/tutorial3-section2-step1-1.png)

With the **NetworkRoom** child object still selected, in the Hierarchy window, expand the **TableAnchor** object, then in the Inspector window, locate the **Photon Room (Script)** component and configure it as follows:

* To the **Rocket Launcher Location** field, assign the **Table** child object from the Hierarchy window

![mrlearning-sharing](images/mrlearning-sharing/tutorial3-section2-step1-2.png)

## Trying the experience with shared object movement

If you now build and deploy the Unity project to your HoloLens, and then, back in Unity, press the Play button to enter Game mode while the application is running on your HoloLens, you will see the object move in Unity when you move the object in HoloLens:

![mrlearning-sharing](images/mrlearning-sharing/tutorial3-section3-step1-1.gif)

## Congratulations

You have successfully configured your project so object movements are synchronized and users can see the objects move when other users move the objects. In the next tutorial, you will implement functionality so the shared experience is aligned in the physical world and the users see each other in their actual physical location and so the objects appear in the same physical position and rotation for all users.

[Next tutorial: 4. Integrating Azure Spatial Anchors into a shared experience](mrlearning-sharing(photon)-ch4.md)

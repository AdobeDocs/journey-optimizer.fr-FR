---
solution: Journey Optimizer
product: journey optimizer
title: Copier un parcours dans un autre sandbox
description: Découvrez comment copier un parcours dans un autre sandbox.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: sandbox, parcours, copier, environnement
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
version: Journey Orchestration
source-git-commit: 118bf89f56d26213fde71fa795fc6576ce764ef2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 100%

---

# Copier un parcours dans un autre sandbox {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

Journey Optimizer vous permet de copier un parcours complet d’un sandbox à un autre. Par exemple, vous pouvez copier un parcours de votre environnement de sandbox d’évaluation vers votre sandbox de production.

En plus du parcours lui-même, Journey Optimizer copie également la plupart des objets dont dépend le parcours : audiences, schémas, événements et actions.

Le processus de copie est réalisé via un **export et un import de package** entre les sandbox source et cible. Des informations détaillées sur l’export d’objets et leur import dans un sandbox cible sont disponibles dans cette section : [Copier des objets vers un autre sandbox](../configuration/copy-objects-to-sandbox.md).

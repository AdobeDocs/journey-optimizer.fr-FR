---
solution: Journey Optimizer
product: journey optimizer
title: Gérer le processus d’opt-out
description: Découvrez comment gérer le processus d’opt-out et la confidentialité
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: f5390bbb3bab435b21ace4d1842de0048132bc8c
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 1%

---

# Mise en oeuvre du consentement pour l’exclusion de la personnalisation {#cpes-opt-out}


## Éditeur d’expressions

Éditeur d’expressions lors de la personnalisation d’images, de texte, d’objet (Segment dans les campagnes) - IU et sans affichage

L’éditeur de personnalisation lui-même n’effectue aucune vérification ou application du consentement, car il n’est pas impliqué dans la diffusion des actions de message. L’éditeur de personnalisation adhère aux étiquettes de contrôle d’accès basées sur les droits fournies par le service de profil unifié afin d’autoriser/non l’utilisation de différents champs pour la personnalisation. Le service de prévisualisation et de rendu des messages masque les champs identifiés avec des informations sensibles.

Dans les campagnes AJO, l’application de la stratégie de consentement peut se produire à deux endroits. Les clients peuvent inclure des définitions de stratégie de consentement dans le cadre de la création de l’audience ou du segment afin de s’assurer que l’audience sélectionnée pour la campagne a déjà filtré les profils qui ne correspondent pas aux critères de consentement. Deuxièmement, le service d’exécution des messages effectuera une vérification générale du consentement au niveau du canal pour s’assurer que les profils ont choisi de recevoir des communications marketing sur le canal spécifique. Actuellement, l’objet AJO Campaign n’effectue aucune vérification supplémentaire de l’application de la stratégie de consentement.

Étapes AJO Campaign et de personnalisation pour appliquer manuellement le consentement :

L’état d’inclusion et les préférences de personnalisation d’un utilisateur doivent faire partie des règles et de la définition de l’audience avant l’activation dans une campagne Journey Optimizer. Un utilisateur marketing dans Adobe Experience Platform peut ajouter une vérification du consentement à son audience en créant une nouvelle composition d’audience ou en définissant un nouveau segment à l’aide du créateur de règles.

Si vous utilisez le compositeur d’audience, vous pouvez fractionner votre audience à l’aide d’attributs de profil. Une fois que vous avez effectué vos sélections sur les attributs de consentement appropriés que vous souhaitez vérifier, vous pouvez enregistrer les audiences obtenues pour activation dans une campagne. Gardez à l’esprit que si vous créez une audience qui n’a pas donné son consentement pour la personnalisation et que vous sélectionnez ensuite cette audience pour activation dans une campagne, les outils de personnalisation restent disponibles. Il appartient à l’utilisateur marketing de comprendre que s’il travaille avec une audience qui ne doit pas recevoir de personnalisation, il ne doit pas utiliser d’outils de personnalisation.

Pour créer une audience partagée dans la composition de l’audience, procédez comme suit :

1. Sélectionnez l’audience de départ.

1. Cliquez sur l’icône plus (+) pour créer une audience partagée.

1. Dans les propriétés de Partage, sélectionnez &quot;partage d’attribut&quot; comme type.

1. Dans le champ attribut , cliquez sur l’icône en forme de crayon pour afficher la fenêtre de sélection des attributs.

1. Saisissez la valeur Choix pour rechercher l’attribut de consentement de personnalisation (notez qu’il s’agit du chemin d’accès d’attribut profile.consentement.personalize.content.val).

1. Sélectionnez cet attribut.

1. Dans Chemin 1 : choisissez un libellé qui vous aidera à définir l’audience non personnalisée.

1. Sélectionnez la valeur appropriée dans la liste suivante : https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=en#choice-values

   Dans ce cas, nous utiliserons un &quot;n&quot; pour signifier NON comme exclusion de la personnalisation.

   Vous pouvez créer un chemin distinct pour les autres valeurs de choix ou vous pouvez choisir de supprimer les chemins restants et activer &quot;autres profils&quot; qui inclurait tous les autres profils qui n’avaient pas de valeur de choix de &quot;n&quot;.

1. Une fois que vous avez terminé, cliquez dans la zone où il est indiqué &quot;Enregistrer l’audience&quot;. Une nouvelle fenêtre de propriétés s’ouvre, vous permettant de choisir le nom que vous souhaitez utiliser pour les audiences dérivées.

1. Une fois terminé, publiez la composition de l’audience.

Si vous utilisez le créateur de règles de segment pour créer votre audience, vous pouvez sélectionner les choix de valeurs de personnalisation et de consentement comme paramètres d’exclusion dans la définition de l’audience. En ajoutant dans les paramètres d’exclusion, vous pouvez créer un segment d’audience unique de profils dans lequel les personnes qui n’ont pas donné leur consentement sont filtrées.


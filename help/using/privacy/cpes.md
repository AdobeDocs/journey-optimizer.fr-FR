---
solution: Journey Optimizer
product: journey optimizer
title: Gérer le processus d’opt-out
description: Découvrez comment gérer le processus d’opt-out et la confidentialité
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 97%

---

# Implémenter le consentement pour la désinscription de la personnalisation {#cpes-opt-out}


## Éditeur d’expression

Éditeur d’expression lors de la personnalisation d’images, de texte, d’objet (Segment dans les campagnes) – IU et découplé

L’éditeur de personnalisation lui-même n’effectue aucune vérification ou application du consentement, car il n’est pas impliqué dans la diffusion des actions de message. L’éditeur de personnalisation adhère aux libellés de contrôle d’accès basées sur les droits fournies par le service de profil unifié afin d’autoriser ou non l’utilisation de différents champs pour la personnalisation. Le service de prévisualisation et de rendu des messages masque les champs identifiés avec des informations sensibles.

Dans les campagnes AJO, l’application de la politique de consentement peut se produire à deux endroits. Les clientes et clients peuvent inclure des définitions de politique de consentement dans le cadre de la création de l’audience ou du segment afin de s’assurer que l’audience sélectionnée pour la campagne a déjà exclu du filtre les profils qui ne correspondent pas aux critères de consentement. Deuxièmement, le service d’exécution des messages effectuera une vérification générale du consentement au niveau du canal pour s’assurer que les profils ont choisi de recevoir des communications marketing sur le canal spécifique. Actuellement, l’objet de la campagne AJO n’effectue aucune vérification supplémentaire de l’application de la politique de consentement.

Étapes de campagne AJO et de personnalisation pour appliquer manuellement le consentement :

Le statut d’opt-in et les préférences de personnalisation d’un utilisateur ou d&#39;une utilisatrice doivent faire partie des règles et de la définition de l’audience avant l’activation dans une campagne Journey Optimizer. Un utilisateur ou une utilisatrice marketing dans Adobe Experience Platform peut ajouter une vérification du consentement à son audience en créant une nouvelle composition d’audience ou en définissant un nouveau segment à l’aide du créateur de règles.

Si vous utilisez le compositeur d’audience, vous pouvez répartir votre audience à l’aide d’attributs de profil. Une fois que vous avez effectué vos sélections sur les attributs de consentement appropriés que vous souhaitez vérifier, vous pouvez enregistrer les audiences obtenues pour activation dans une campagne. Gardez à l’esprit que si vous créez une audience qui n’a pas donné son consentement pour la personnalisation et que vous la sélectionnez ensuite pour activation dans une campagne, les outils de personnalisation restent disponibles. Il appartient à l’utilisateur ou à l’utilisatrice marketing de comprendre que s’il ou elle travaille avec une audience qui ne doit pas recevoir de personnalisation, les outils de personnalisation ne doivent pas être utilisés.

Pour créer une audience répartie dans la composition de l’audience, procédez comme suit :

1. Sélectionnez votre audience de départ.

1. Cliquez sur l’icône plus (+) pour créer une audience répartie.

1. Dans les propriétés de répartition, sélectionnez « répartition des attributs » comme type.

1. Dans le champ attribut, cliquez sur l’icône en forme de crayon pour afficher la fenêtre de sélection des attributs.

1. Saisissez la valeur Choix pour rechercher l’attribut de consentement de personnalisation (notez qu’il s’agit du chemin d’accès d’attribut profile.consentement.personalize.content.val).

1. Sélectionnez cet attribut.

1. Dans Chemin 1 : choisissez un libellé qui vous aidera à définir l’audience non personnalisée.

1. Sélectionnez la valeur appropriée dans cette liste : https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values

   Dans ce cas, nous utiliserons un « n » pour signifier NON comme désinscription de la personnalisation.

   Vous pouvez créer un chemin distinct pour les autres valeurs de choix ou vous pouvez choisir de supprimer les chemins restants et activer « autres profils » qui inclut tous les autres profils dont la valeur de choix n’est pas « n ».

1. Une fois que vous avez terminé, cliquez dans la zone où il est indiqué « Enregistrer l’audience ». Une nouvelle fenêtre de propriétés s’ouvre, vous permettant de choisir le nom que vous souhaitez utiliser pour les audiences dérivées.

1. Une fois terminé, publiez la composition de l’audience.

Si vous utilisez le créateur de règles de segment pour créer votre audience, vous pouvez sélectionner les choix de valeur de personnalisation et de consentement comme paramètres d’exclusion dans la définition de l’audience. En les ajoutant dans les paramètres d’exclusion, vous pouvez créer un segment ciblé unique d’audience de profils dans lequel les personnes qui n’ont pas donné leur consentement sont exclues du filtre.

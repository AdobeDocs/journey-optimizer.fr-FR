---
solution: Journey Optimizer
product: journey optimizer
title: Publier le parcours
description: Découvrez comment publier un parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publication, parcours, dynamique, validité, vérifier
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: 5bdacef2196592776c6b37708b0df0986460ca1f
workflow-type: ht
source-wordcount: '613'
ht-degree: 100%

---

# Publier votre parcours {#publishing-the-journey}

Pour activer un parcours et permettre à de nouveaux profils de le rejoindre, vous devez le publier. Suite à sa publication, le parcours devient actif et fonctionnel. Avant de le publier, vous devez vous assurer que le parcours est complet et valide, et corriger les erreurs, car un parcours ne peut pas être publié s’il contient des erreurs.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Processus de publication {#journey-publication}

Les étapes de publication d’un parcours sont présentées en détail ci-dessous :

1. Avant de publier votre parcours, assurez-vous qu’il est valide et sans erreur. Les parcours ne peuvent pas être publiés s’ils contiennent des erreurs.

   * Découvrez comment tester votre parcours sur [cette page](testing-the-journey.md).
   * Découvrez comment résoudre les erreurs présentes dans votre parcours dans [cette section](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

1. Pour publier le parcours, cliquez sur l’option **[!UICONTROL Publier]** située dans le menu déroulant qui se trouve en haut à droite.

   >[!NOTE]
   >
   > Si votre parcours est soumis à une politique d’approbation, vous devez demander une approbation avant de pouvoir le publier. [En savoir plus](../test-approve/gs-approval.md)


   ![](assets/journeyuc1_18.png)

Une fois le parcours publié, il est en **lecture seule**. Lorsqu’un parcours est en lecture seule, vous ne pouvez modifier que les libellés et les descriptions d’activité, ainsi que le nom et la description du parcours. Si vous devez apporter des modifications à un parcours publié, vous devez en créer [une nouvelle version](journey-ui.md#journey-versions).

Lorsque vous arrêtez un parcours, il est définitivement arrêté : toutes les personnes présentes dans le parcours sont définitivement arrêtées, et le parcours cesse d’autoriser de nouvelles entrées. Si vous devez réexécuter le parcours, vous devez le dupliquer et publier le nouveau parcours.


>[!IMPORTANT]
>
>Si des modifications sont apportées à une décision d’offres qui est utilisée dans le message d’un parcours, vous devez dépublier le parcours et le republier. Cela permet de s’assurer que les modifications sont intégrées au message du parcours et que le message est cohérent avec les dernières mises à jour.


## Versions de parcours {#journey-versions}

Dans la liste des parcours, toutes les versions de parcours sont accompagnées d’un numéro. Lorsque vous recherchez un parcours, les versions les plus récentes apparaissent en haut de la liste la première fois que vous ouvrez l&#39;application. Vous pouvez ensuite définir l&#39;ordre de tri souhaité ; l&#39;application le conservera en tant que préférence utilisateur. La version du parcours est également affichée en haut de l&#39;interface d&#39;édition des parcours, au-dessus de la zone de travail.

![](assets/journeyversions1.png)

>[!NOTE]
>
>En règle générale, un profil ne peut pas être présent plusieurs fois dans le même parcours et au même moment. Cela s’applique à toutes les versions actives du parcours. Si la nouvelle entrée est activée, un profil peut rejoindre à nouveau un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours. [En savoir plus](entry-management.md).

### Créer une nouvelle version d’un parcours {#journey-create-new-version}

Si vous devez apporter des modifications à un parcours publié, vous devez en créer une nouvelle version. Pour créer une nouvelle version d’un parcours existant, procédez comme suit :

1. Ouvrez la dernière version de votre parcours actif, puis cliquez sur **[!UICONTROL Créer une version]**, puis confirmez.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Vous ne pouvez créer une version qu&#39;à partir de la dernière version d&#39;un parcours.

1. Apportez vos modifications, cliquez sur **[!UICONTROL Publier]** et confirmez.

Dès la publication du parcours, les personnes vont accéder à la dernière version du parcours. Les clients qui ont déjà accédé à une version antérieure y restent jusqu&#39;à la fin du parcours. Si les personnes entrent à nouveau dans le même parcours par la suite, elles accéderont à la dernière version.

Les versions de parcours peuvent être arrêtées individuellement. Toutes les versions de parcours portent le même nom.

Lorsque vous publiez une nouvelle version d&#39;un parcours, la version précédente se termine automatiquement et passe au statut **Fermé**. Aucune entrée dans le parcours ne peut se produire. Même si vous arrêtez la dernière version, la version précédente reste fermée.


>[!NOTE]
>
>Des mécanismes de sécurisation et des limitations spécifiques s’appliquent au contrôle de version des parcours. En savoir plus sur [cette page](../start/guardrails.md#journey-versions-journey-versions-g).


## Vidéo pratique {#video}

Découvrez comment publier un parcours dans cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)
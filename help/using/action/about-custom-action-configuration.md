---
solution: Journey Optimizer
product: journey optimizer
title: Configurer une action personnalisée
description: Découvrez comment configurer une action personnalisée
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, tiers, personnalisé, parcours, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 80%

---

# Configurer une action personnalisée {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Actions personnalisées "
>abstract="Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, utilisez des actions personnalisées pour configurer la connexion de ce système aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/), Firebase, etc."

Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d’API à un système tiers, utilisez des actions personnalisées pour configurer la connexion de ce système aux parcours. Par exemple, vous pouvez vous connecter aux systèmes suivants avec des actions personnalisées : Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target="_blank"}, Firebase, etc.

Les actions personnalisées sont des actions supplémentaires définies par les utilisateurs techniques et mises à la disposition des spécialistes marketing. Une fois configurés, elles apparaissent dans la palette gauche de votre parcours, dans la catégorie **[!UICONTROL Action]**. En savoir plus sur [cette page](../building-journeys/about-journey-activities.md#action-activities).

## Limites{#custom-actions-limitations}

Les actions personnalisées sont assorties de quelques limites répertoriées dans [cette page](../start/guardrails.md).

Dans les paramètres d’action personnalisés, vous pouvez transmettre une collection simple, ainsi qu’une collection d’objets. En savoir plus au sujet de ces limites de collection sur [cette page](../building-journeys/collections.md#limitations).

Notez également qu’un format spécifique est attendu pour les paramètres d’action personnalisés (par exemple : chaîne, décimal, etc.). Vous devez veiller au respect de cette exigence. En savoir plus sur ce [cas d’utilisation](../building-journeys/collections.md).

Les actions personnalisées prennent en charge le format JSON uniquement lors de l’utilisation de [requêtes](../action/about-custom-action-configuration.md#define-the-message-parameters) ou de [payloads de réponse](../action/action-response.md).

## Bonnes pratiques{#custom-action-enhancements-best-practices}

Lorsque vous choisissez un point d’entrée à cibler à l’aide d’une action personnalisée, assurez-vous de ce qui suit :

* Ce point d’entrée peut prendre en charge le débit des parcours à l’aide de configurations de l’[API de limitation](../configuration/throttling.md) ou de l’[API de plafonnement](../configuration/capping.md) pour le limiter. Faites preuve de prudence si une configuration de limitation ne peut pas descendre sous 200 TPS. Tout point d’entrée ciblé devra prendre en charge au moins 200 TPS.
* Ce point d’entrée doit avoir un temps de réponse aussi bas que possible. Selon le débit attendu, un temps de réponse élevé peut avoir un impact sur le débit réel.

Un plafond de 300 000 appels sur une minute est défini pour toutes les actions personnalisées. En outre, la limitation par défaut est effectuée par hôte et par sandbox. Par exemple, sur un sandbox, si vous avez deux points d’entrée avec le même hôte (par exemple, `https://www.adobe.com/endpoint1` et `https://www.adobe.com/endpoint2`), la limitation s’applique à tous les points d’entrée sous l’hôte adobe.com. Le point d’entrée 1 et le point d’entrée 2 partagent la même configuration de limitation. En outre, le fait qu’un point d’entrée atteigne la limite a un impact sur l’autre point d’entrée.

Cette limite a été définie en fonction de l’utilisation de la clientèle, afin de protéger les points d’entrée externes ciblés par des actions personnalisées. Vous devez prendre cela en compte dans vos parcours basés sur l’audience en définissant un taux de lecture approprié (5 000 profils/s lors de l’utilisation d’actions personnalisées). Si nécessaire, vous pouvez remplacer ce paramètre en définissant une limitation ou un ralentissement plus élevé via nos API de limitation/ralentissement. Consultez [cette page](../configuration/external-systems.md).

Vous ne devez pas cibler les points d’entrée publics avec des actions personnalisées pour diverses raisons :

* Sans limitation ou ralentissement approprié, il existe un risque d’envoyer trop d’appels à un point d’entrée public qui ne prend pas en charge un tel volume.
* Les données de profil peuvent être envoyées par le biais d’actions personnalisées, de sorte que le ciblage d’un point d’entrée public peut entraîner le partage accidentel d’informations personnelles en externe.
* Vous n’avez aucun contrôle sur les données renvoyées par les points d’entrée publics. Si un point d’entrée modifie son API ou commence à envoyer des informations incorrectes, celles-ci seront rendues disponibles dans les communications envoyées, avec des impacts négatifs potentiels.

## Consentement et gouvernance des données {#privacy}

Dans Journey Optimizer, vous pouvez appliquer des politiques de gouvernance des données et de consentement à vos actions personnalisées, afin d’empêcher l’exportation de champs spécifiques vers des systèmes tiers ou d’exclure les clients qui n’ont pas consenti à recevoir des communications par e-mail, push ou SMS. Pour plus d’informations, consultez les pages suivantes :

* [Gouvernance des données](../action/action-privacy.md).
* [Consentement](../action/action-privacy.md).


## Étapes de configuration {#configuration-steps}

Les principales étapes nécessaires pour configurer une action personnalisée sont les suivantes :

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**. Dans la section **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Gérer]**. Cliquez sur **[!UICONTROL Créer une action]** pour créer une nouvelle action. Le volet de configuration des actions s&#39;ouvre dans la droite de l&#39;écran.

   ![](assets/custom2.png)

1. Saisissez le nom de l&#39;action.

   >[!NOTE]
   >
   >Seuls les caractères alphanumériques et les traits de soulignement sont autorisés. La longueur maximale est de 30 caractères.

1. Ajoutez une description à l&#39;action. Cette étape est facultative.
1. Le nombre de parcours qui font appel à cette action apparaît dans le champ **[!UICONTROL Utilisé(e) dans]**. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours utilisant cette action.
1. Définissez les différents paramètres de **[!UICONTROL Configuration d&#39;URL]**. Voir [cette page](../action/about-custom-action-configuration.md#url-configuration).
1. Configurez la section **[!UICONTROL Authentification]**. Cette configuration est la même que pour les sources de données.  Consultez [cette section](../datasource/external-data-sources.md#custom-authentication-mode).
1. Définissez les **[!UICONTROL paramètres d&#39;action]**. Voir [cette page](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   L&#39;action personnalisée est maintenant configurée et prête à être utilisée dans vos parcours. Voir [cette page](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Lorsqu&#39;une action personnalisée est utilisée dans un parcours, la plupart des paramètres sont en lecture seule. Vous ne pouvez modifier que les champs **[!UICONTROL Nom]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** et la section **[!UICONTROL Authentification.]**

## Configuration du point d’entrée {#url-configuration}

Lors de la configuration d’une action personnalisée, vous devez définir les paramètres de **[!UICONTROL configuration de point d’entrée]** suivants :

![](assets/action-response1bis.png){width="70%" align="left"}

1. Dans le champ **[!UICONTROL URL]**, spécifiez l&#39;URL du service externe :

   * Si l’URL est statique, saisissez l’URL dans ce champ.

   * Si l’URL comprend un chemin dynamique, saisissez uniquement la partie statique de l’URL, c’est-à-dire le schéma, l’hôte, le port et, éventuellement, une partie statique du chemin.

     Exemple : `https://xxx.yyy.com/somethingstatic/`

     Vous spécifiez le chemin dynamique de l’URL lors de l’ajout de l’action personnalisée à un parcours. [En savoir plus](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Pour des raisons de sécurité, nous vous recommandons vivement d’utiliser le schéma HTTPS pour l’URL. L&#39;utilisation des adresses Adobe qui ne sont pas publiques et des adresses IP n&#39;est pas autorisée.
   >
   >Seuls les ports par défaut sont autorisés lors de la définition d’une action personnalisée : 80 pour http et 443 pour https.

1. Sélectionnez la **[!UICONTROL Méthode]** d’appel : il peut s’agir de **[!UICONTROL POST]**, **[!UICONTROL GET]** ou **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > Le méthode **DELETE** n’est pas prise en charge. Si vous devez mettre à jour une ressource existante, sélectionnez la méthode **PUT**.

1. Définissez les en-têtes et les paramètres de requête :

   * Dans la section **[!UICONTROL En-têtes]**, cliquez sur **[!UICONTROL Ajouter un champ d’en-tête]** pour définir les en-têtes HTTP du message de requête à envoyer au service externe. Les champs d’en-tête **[!UICONTROL Type de contenu]** et **[!UICONTROL Charset]** sont définis par défaut. Vous ne pouvez pas supprimer ces champs. Seul l’en-tête **[!UICONTROL Content-Type]** peut être modifié. Sa valeur doit respecter le format JSON. Voici la valeur par défaut :

   ![](assets/content-type-header.png)

   * Dans la section **[!UICONTROL Paramètres de requête]**, cliquez sur **[!UICONTROL Ajouter un champ de paramètre de requête]** pour définir les paramètres à ajouter à l’URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Saisissez le libellé ou le nom du champ.

1. Sélectionnez le type : **[!UICONTROL Constant]** ou **[!UICONTROL Variable]**. Si vous avez sélectionné **[!UICONTROL Constant]**, saisissez la valeur constante dans le champ **[!UICONTROL Valeur]**. Si vous avez sélectionné **[!UICONTROL Variable]**, vous spécifiez cette variable lors de l’ajout de l’action personnalisée à un parcours. [En savoir plus](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Après avoir ajouté l’action personnalisée à un parcours, vous pouvez toujours y ajouter des champs d’en-tête si le parcours a le statut de brouillon. Si vous ne souhaitez pas que le parcours soit affecté par les modifications de configuration, dupliquez l’action personnalisée et ajoutez les champs d’en-tête à la nouvelle action personnalisée.
   >
   >Les en-têtes sont validés conformément à des règles d’analyse. En savoir plus dans [cette documentation](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Définir les paramètres de payload {#define-the-message-parameters}

1. Dans la section **[!UICONTROL Requête]**, collez un exemple de payload JSON à envoyer au service externe. Ce champ est facultatif et disponible uniquement pour les méthodes d’appel POST et PUT.

1. Dans la section **[!UICONTROL Réponse]**, collez un exemple de payload renvoyée par l’appel. Ce champ est facultatif et disponible pour toutes les méthodes d’appel. Pour plus d’informations sur l’utilisation des réponses d’appel API dans les actions personnalisées, reportez-vous à [cette page](../action/action-response.md).

>[!NOTE]
>
>La fonctionnalité de réponse est actuellement disponible en version Beta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>L’exemple de payload ne peut pas contenir de valeurs nulles. Les noms de champ de la payload ne peuvent pas contenir de caractère &quot;.&quot; . Ils ne peuvent pas commencer par le caractère &quot;$&quot;.

Vous aurez la possibilité de définir le type de paramètre (par exemple : string, integer, etc.).

Vous pourrez également préciser si le paramètre est une constante ou une variable :

* Le paramètre « **Constant** » signifie que la valeur du paramètre est définie dans le volet de configuration des actions par une persona ayant un rôle technique. La valeur reste identique dans tous les parcours et la personne chargée du marketing ne la voit pas lors de l’utilisation de l’action personnalisée dans le parcours. Il peut s&#39;agir, par exemple, d&#39;un identifiant attendu par le système tiers. Dans ce cas, le champ situé à droite du bouton bascule Constante/Variable correspond à la valeur transmise.
* Le paramètre « **Variable** » signifie que la valeur du paramètre varie. Le spécialiste marketing qui utilise cette action personnalisée dans un parcours sera libre de transmettre la valeur de son choix ou bien d’indiquer où récupérer la valeur de ce paramètre (à partir de l’événement, d‘Adobe Experience Platform, etc.). Dans ce cas, le champ situé à droite du bouton bascule Constante/Variable correspond au libellé que le spécialiste marketing voit dans le parcours pour nommer ce paramètre.

![](assets/customactionpayloadmessage2.png)

## Prise en charge du protocole mTLS {#mtls-protocol-support}

Vous pouvez désormais utiliser le protocole mTLS (Mutual Transport Layer Security) pour garantir une sécurité renforcée dans les connexions sortantes aux destinations d’API HTTP et aux actions personnalisées Adobe Journey Optimizer. mTLS est une méthode de sécurité de bout en bout pour l’authentification mutuelle qui garantit que les deux parties qui partagent des informations sont celles qu’elles prétendent être avant que les données ne soient partagées. mTLS inclut une étape supplémentaire par rapport à TLS, dans laquelle le serveur demande également le certificat du client et le vérifie à son bout.

Dans Adobe Journey Optimizer, mTLS est utilisé conjointement avec des actions personnalisées. Aucune configuration supplémentaire pour les actions personnalisées Adobe Journey Optimizer n’est requise de votre part pour activer mTLS. Lorsque le point de terminaison d’une action personnalisée est activé par mTLS, le système récupère le certificat du KeyStore Adobe Experience Platform et le fournit automatiquement au point de terminaison (comme requis pour les connexions mTLS).

Si vous souhaitez utiliser mTLS avec ces processus de destination d’API HTTP Adobe Journey Optimizer et Experience Platform, l’adresse du serveur que vous placez dans l’interface utilisateur d’action du client Adobe Journey Optimizer ou l’interface utilisateur des destinations doit avoir les protocoles TLS désactivés et uniquement mTLS activé. Si le protocole TLS 1.2 est toujours activé sur ce point de terminaison, aucun certificat n’est envoyé pour l’authentification du client. Cela signifie que pour utiliser mTLS avec ces workflows, votre point d’entrée de serveur &quot;récepteur&quot; doit être un mTLS. **only** point d’entrée de connexion activé.

>[!IMPORTANT]
>
>Aucune configuration supplémentaire n’est requise dans votre action personnalisée ou votre parcours Adobe Journey Optimizer pour activer mTLS ; ce processus se produit automatiquement lorsqu’un point d’entrée compatible mTLS est détecté. Les noms communs (CN) et les noms de remplacement du sujet (SAN) pour chaque certificat sont disponibles dans la documentation dans le cadre du certificat et peuvent être utilisés comme une couche supplémentaire de validation de la propriété si vous le souhaitez.
>
>La norme RFC 2818, publiée en mai 2000, rend obsolète l’utilisation du champ Nom commun (CN) dans les certificats HTTPS pour la vérification du nom du sujet. Il recommande plutôt d’utiliser l’extension SAN (Subject Alternative Name) du type &quot;dns name&quot;.

Si vous souhaitez vérifier le CN ou le SAN pour effectuer une validation tierce supplémentaire, vous pouvez télécharger les certificats pertinents ici :

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```


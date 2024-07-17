---
solution: Journey Optimizer
product: journey optimizer
title: Demandes d’accès à des informations personnelles
description: En savoir plus sur les demandes d’accès à des informations personnelles et Privacy Service.
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 100%

---

# Demandes d’accès à des informations personnelles {#track-changes}

Adobe Experience Platform **Privacy Service** fournit une API RESTful ainsi qu’une interface utilisateur vous permettant de gérer les demandes de données des clients. Grâce à Privacy Service, vous pouvez soumettre des demandes d’accès et de suppression de données personnelles des clients depuis les applications Adobe Experience Cloud. Cela facilite la mise en conformité automatique avec les réglementations légales et organisationnelles liées à la confidentialité.

Les demandes d’accès à des informations personnelles peuvent être créées et gérées à partir du menu **[!UICONTROL Demandes]**.

![](assets/requests.png)

Pour plus d’informations sur Privacy Service et sur la création et la gestion des demandes d’accès à des informations personnelles, consultez la documentation d’Adobe Experience Platform :

* [Présentation de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr)
* [Gérer les traitements relatifs à la confidentialité dans l’interface utilisateur de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr)



## Gérer les demandes individuelles d’accès à des informations personnelles que vous pouvez envoyer à Adobe Journey Optimizer {#data-privacy-requests}

Vous pouvez envoyer des demandes individuelles pour accéder aux données de la clientèle d’Adobe Journey Optimizer et les supprimer de deux manières :

* Par le biais de l’**Interface d’utilisation de Privacy Service**. Consultez la documentation [ici](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/ui/user-guide#_blank).
* Par le biais de l’**API Privacy Service**. Consultez la documentation [ici](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) et les informations sur l’API [ici](https://developer.adobe.com/experience-platform-apis/#_blank).

Privacy Service prend en charge deux types de demandes : l’**accès aux données** et la **suppression de données**.

>[!NOTE]
>
>Ce guide porte uniquement sur la manière d’effectuer des demandes d’accès à des informations personnelles pour Adobe Journey Optimizer. Si vous prévoyez également d’effectuer des demandes d’accès à des informations personnelles pour le lac de données de Platform, reportez-vous à ce [guide](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/privacy) en plus de ce tutoriel. Pour le profil client en temps réel, consultez ce [guide](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/privacy) et pour le service d’identités, reportez-vous à ce [guide](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/privacy). Pour les demandes de suppression et d’accès, vous devez appeler ces systèmes individuels afin de vous assurer que les demandes sont traitées par chacun d’entre eux. L’envoi d’une demande d’accès à des informations personnelles à Adobe Journey Optimizer ne supprimera pas les données de tous ces systèmes.

Pour les **demandes d’accès**, spécifiez « Adobe Journey Optimizer » dans l’interface d’utilisation (ou « CJM » comme code de produit dans l’API).

Pour les **demandes de suppression**, en plus de la demande « Adobe Journey Optimizer », vous devez également envoyer des demandes de suppression à trois services en amont pour empêcher Journey Optimizer de réinjecter les données supprimées. Si ces services en amont ne sont pas spécifiés, la demande « Adobe Journey Optimizer » restera à l’état « traitement » jusqu’à la création des demandes de suppression pour les services en amont.

Voici les trois services en amont :

* Profil (code produit : « profileService »)
* Lac de données AEP (code produit : « AdobeCloudPlatform »)
* Identité (code produit : « identity »)

## Créer des demandes d’accès et de suppression

### Conditions préalables

Pour envoyer des demandes d’accès et de suppression de données pour Adobe Journey Optimizer, vous devez disposer des éléments suivants :

* un ID d’organisation IMS ;
* un identifiant d’identité de la personne sur laquelle vous souhaitez agir et le ou les espaces de noms correspondants. Pour plus d’informations sur les espaces de noms d’identité dans Adobe Journey Optimizer et Experience Platform, voir [Vue d’ensemble de l’espace de noms d’identité](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces).

### Valeurs de champ requises dans Adobe Journey Optimizer pour les requêtes API

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### Exemple de demande d’accès dans le cadre du RGPD :

Depuis l’interface d’utilisation :

![](assets/accessrequest.png)

Par le biais de l’API :

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### Exemple de demande de suppression dans le cadre du RGPD :

Depuis l’interface d’utilisation :

![](assets/deleterequest.png)

Par le biais de l’API :

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

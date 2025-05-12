---
title: Déduplication des éléments de décision dans les implémentations basées sur du code
description: Cette page montre comment appliquer la déduplication à vos requêtes de prise de décision dans votre implémentation basée sur le code Journey Optimizer.
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: f9477611-b792-4b28-8ec2-6bbea2fa3328
source-git-commit: 4995bf642231248ece0211a7ecf2f38ccd846d36
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 10%

---

# Prise de décision dans les implémentations d’expérience basées sur du code

Lors de l’utilisation de Decisioning dans des expériences basées sur du code, pensez à ajouter les indicateurs suivants à votre implémentation client dans les cas décrits ci-dessous.

## Test d’expériences basées sur du code à l’aide de décisions {#code-based-test-decisions}

Actuellement, vous ne pouvez pas simuler le contenu de l’interface d’utilisation dans une campagne ou un parcours d’[expérience basée sur du code](create-code-based.md) à l’aide de décisions.

Pour pallier ce problème, vous pouvez tester la prise de décisions après la publication de votre campagne en ajoutant l’indicateur `dryRun` dans le bloc `data` d’événement XDM de votre mise en œuvre cliente :

     »
    {
    « data »: {
     »__adobe »: {
    « ajo »: {
    « dryRun »: true
    }
    }
    }
    }
     »

>[!CAUTION]
>
>L’ajout de l’indicateur `dryRun` à votre demande empêchera la capture de commentaires pour la création de rapports et l’ajout de compteurs de fréquence.

## Déduplication des éléments de décision dans les implémentations basées sur du code {#code-based-decisioning-deduplication}

Lors de l’utilisation de [politiques de décision](../experience-decisioning/create-decision.md) dans vos expériences basées sur du code, découvrez comment appliquer une déduplication à vos requêtes de prise de décision dans votre implémentation client.

Les requêtes de prise de décision (par l’intermédiaire de Konductor) acceptent l’indicateur de déduplication, qui gère l’unicité des éléments de décision dans une requête unique composée de plusieurs politiques de décision ou emplacements.

### Logique de déduplication {#deduplication-logic}

Pour toute requête de prise de décision, vous pouvez avoir une ou plusieurs politiques de décision/emplacements basés sur la configuration.

* Pour une **politique de décision unique** et un emplacement dans une requête, tous les éléments de la réponse sont uniques (par défaut). Deux éléments de décision ne peuvent pas être identiques dans une seule demande.

* Pour les **politiques/emplacements de décision multiples** dans une requête :

   * Si `allowDuplicateDecisionItems` est défini sur `false` : tous les éléments de la réponse sont uniques (quels que soient le message/la politique de décision/l’emplacement auquel l’élément est destiné).

   * Si `allowDuplicateDecisionItems` est défini sur `true` (par défaut) : les éléments de la réponse peuvent être dupliqués (si plusieurs messages/politiques de décision/emplacements sont qualifiés pour le même élément de décision pour cette requête).

### Appliquer la déduplication dans une requête {#deduplication-in-request}

Par défaut, l’indicateur de déduplication est défini sur `true` (il n’est pas transmis).

Dans une requête Konductor, vous pouvez transmettre l’indicateur de déduplication si vous souhaitez des éléments uniques dans la réponse. Dans ce cas, définissez-le sur `false`.

```
{
    "data": {
        "__adobe": {
            "ajo": {
                "allowDuplicateDecisionItems": false
            }
        }
    }
}
```

+++Exemple de requête Decisioning

```
curl --location 'https://edge-int.adobedc.net/ee/v1/interact?configId=2f21d344-b69f-4a4f-98e8-000282fc9552' \
--header 'Content-Type: application/json' \
--data-raw '{
    "events": [
        {
            "query": {
                "personalization": {
                    "schemas": [
                        "https://ns.adobe.com/personalization/html-content-item"
                    ],
                    "surfaces": [
                        "https://www.adobe.com/san/placement/header",
                        "https://www.adobe.com/san/placement/footer"
                    ]
                }
            },
            "xdm": {
                "identityMap": {
                    "Email": [
                        {
                            "id": "cmk-exd-user01-deleted@adobe.com",
                            "primary": true
                        }
                    ]
                }
            },
            "data": {
                "__adobe":{
                    "ajo":{
                        "allowDuplicateDecisionItems": false
                    }
                }       
            }
        }
    ]
}'
```

+++

### Réponse de déduplication {#deduplication-response}

Supposons que vous ayez la même politique de décision avec l’emplacement de l’en-tête et du pied de page dans une seule requête.

* Decisioning renvoie deux propositions.

* Si `itemId-X` est l’élément de décision unique qui remplit les critères pour la combinaison de politique de décision et d’emplacement :

   * Si `allowDuplicateDecisionItems` est `true` (par défaut) : `itemId-X` est renvoyée pour les deux propositions dans une seule réponse.

   * Si `allowDuplicateDecisionItems` est `false` :

      * `itemId-X` est renvoyée pour la première proposition.

      * L&#39;élément de décision de secours (également unique) ou un élément de décision vide est transmis pour la deuxième proposition.

+++Exemple de réponse Decisioning (`allowDuplicateDecisionItems` = `true`)

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }
    ]
}
```

+++

+++Exemple de réponse Decisioning (`allowDuplicateDecisionItems` = `false`)

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "3913a28e-d33b-475b-9737-9f6de3940799",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": ""
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }       
    ]
}
```

+++

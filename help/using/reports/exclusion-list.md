---
solution: Journey Optimizer
product: journey optimizer
title: Liste d’exclusions
description: En savoir plus sur les exclusions survenant lors de l’envoi
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 98%

---

# Causes d’exclusion {#exclusion-list}

| Motif d’exclusion | Code d’erreur | Canal | Explication |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Tous les canaux | Événement d’exclusion générique pour toute erreur de distribution d’exécution. |
| RuntimeRenderingError | 050302 | Tous les canaux | Événement d’exclusion générique pour toute erreur de rendu d’exécution. |
| NamespaceErrorForExperimentation | 050017 | Tous les canaux | Un événement d’exclusion est généré lorsque l’espace de nommage dans l’expérience est différent de l’espace de nommage du profil. |
| ExperimentationHoldoutExclusion | 050018 | Tous les canaux | Cet événement d’exclusion est généré lorsque le traitement qualifié pour une expérience est « Exclusion ». |
| ExcludedForControlRules | 050002 | Tous les canaux | Cet événement d’exclusion est généré lorsque la diffusion du message actuel entraîne une violation des règles de contrôle, par exemple le nombre d’e-mails autorisés en un mois. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Un événement d’exclusion est généré lorsque la variante Publipostage direct n’est pas définie. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| EmailNoConsent | 050101 | E-mail | Un événement d’exclusion est généré lorsque l’utilisateur ou l’utilisatrice s’exclut de la réception des e-mails marketing. |
| Supprimé | 050107 | E-mail | Exclusion du fait de l’un des motifs de suppression. |
| EmailSuppressed | 050102 | E-mail | Un événement d’exclusion est généré lorsque l’e-mail cible est supprimé. |
| DomainSuppressed | 050105 | E-mail | Un événement d’exclusion est généré lorsque le domaine de l’e-mail ciblé est supprimé. |
| NotAllowed | 050108 | E-mail | Un événement d’exclusion est généré lorsque la liste autorisée est activée et que l’e-mail ciblé est exclu de la liste autorisée. |
| EmailNotAllowed | 050103 | E-mail | Un événement d’exclusion est généré lorsque la liste autorisée est activée et que l’e-mail ciblé est exclu de la liste autorisée. |
| DomainNotAllowed | 050106 | E-mail | Un événement d’exclusion est généré lorsque la liste autorisée est activée et que le domaine de l’e-mail ciblé est exclu de la liste autorisée. |
| EmailNoSubscriberIdFoundInProfile | 050025 | E-mail | Un événement d’exclusion est généré lorsque la valeur subscriberId est introuvable dans le profil pour un e-mail d’abonnement. |
| EmailNoAddressFoundInProfile | 050020 | E-mail | Un événement d’exclusion est généré lorsque l’adresse électronique est introuvable dans l’adresse d’exécution. |
| EmailNoAddressDefinedInPreset | 050021 | E-mail | Un événement d’exclusion est généré lorsque l’adresse d’exécution n’est pas définie dans la configuration. |
| EmailNoVariantDefined | 050026 | E-mail | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie dans l’e-mail. |
| EmailNoMessageFoundForTreatment | 050027 | E-mail | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| EmailMalformedAddress | 050024 | E-mail | Un événement d’exclusion est généré lorsque l’e-mail contient une adresse incorrecte. |
| InAppNoVariantDefined | 050041 | InApp | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie pour le message in-app. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| PushNoTokenFoundInProfile | 050030 | Notification push | Un événement d’exclusion est généré lorsque le profil ne comporte pas de jetons push. |
| PushNoValidTokenFoundForApps | 050031 | Notification push | Un événement d’exclusion est généré lorsqu’aucun jeton valable n’est trouvé pour les applications ciblées dans la configuration. |
| PushMalformedProfile | 050034 | Notification push | Un événement d’exclusion est généré lorsque pushNotificationDetails est incorrect dans le profil. |
| PushNoConsent | 050111 | Notification push | Un événement d’exclusion est généré lorsque l’utilisateur ou l’utilisatrice s’exclut des notifications push marketing. |
| PushNoApplicationDefinedInPreset | 050033 | Notification push | Un événement d’exclusion est généré lorsque la configuration ne contient aucune application à cibler. |
| PushNoVariantDefined | 050035 | Notification push | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie. |
| PushNoMessageFoundForTreatment | 050036 | Notification push | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| SMSNoConsent | 050104 | SMS | Un événement d’exclusion est généré lorsque l’utilisateur ou l’utilisatrice s’exclut de la réception des SMS marketing. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Un événement d’exclusion est généré lorsque « FromNumber » n’est pas défini dans la configuration. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Un événement d’exclusion est généré lorsque « ToNumber » n’est pas défini dans la configuration. |
| SMSNoVariantDefined | 050154 | SMS | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| WebNoVariantDefined | 050041 | Web | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie pour un message web. |
| WebNoMessageFoundForTreatment | 050042 | Web | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |

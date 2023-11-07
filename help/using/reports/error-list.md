---
solution: Journey Optimizer
product: journey optimizer
title: Liste des erreurs
description: En savoir plus sur les erreurs qui se produisent lors de l'envoi
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: deaa72f235a64dd2cb9bfbafef3574fdb025a026
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 9%

---

# Liste des motifs d’erreur {#error-list}

| Motif d’exclusion | Code d’erreur | Canal | Explication |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Tous les canaux | Événement d’exclusion générique pour toute erreur de distribution Runtime. |
| RuntimeRenderingError | 050302 | Tous les canaux | Événement d’exclusion générique pour toute erreur de rendu Runtime. |
| NamespaceErrorForExperimentation | 050017 | Tous les canaux | Un événement d’exclusion est généré lorsque l’espace de noms dans l’expérience est différent de l’espace de noms du profil. |
| ExperienceHoldoutExclusion | 050018 | Tous les canaux | Cet événement d’exclusion est généré lorsque le traitement qualifié pour une expérience est &quot;Holdout&quot;. |
| ExcludedForControlRules | 050002 | Tous les canaux | Cet événement d’exclusion est généré lorsque la diffusion du message actuel entraîne une violation des règles de contrôle, par exemple le nombre d’emails autorisés dans un mois. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Un événement d’exclusion est généré lorsque la variante courrier n’est pas définie. |
| DirectMailNoMessageFoundForTraitement | 050061 | DirectMail | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| EmailNoConsent | 050101 | E-mail | Un événement d’exclusion est généré lorsque l’utilisateur s’est désabonné de la réception des emails marketing. |
| Supprimé | 050107 | E-mail | Exclusion pour l&#39;un des motifs de suppression. |
| EmailSuppressed | 050102 | E-mail | Un événement d’exclusion est généré lorsque l’email cible est supprimé. |
| DomainSuppressed | 050105 | E-mail | Un événement d’exclusion est généré lorsque le domaine de l’email ciblé est supprimé. |
| NotAllowed | 050108 | E-mail | Un événement d’exclusion est généré lorsque la liste autorisée est activée et que l’email ciblé est exclu de la liste autorisée. |
| EmailNotAllowed | 050103 | E-mail | Un événement d’exclusion est généré lorsque la liste autorisée est activée et que l’email ciblé est exclu de la liste autorisée. |
| DomainNotAllowed | 050106 | E-mail | Un événement d’exclusion est généré lorsque la liste autorisée est activée et que le domaine de l’email ciblé est exclu de la liste autorisée. |
| EmailNoSubscriberIdFoundInProfile | 050025 | E-mail | Un événement d’exclusion est généré lorsque la valeur subscriberId est introuvable dans le profil pour un email d’abonnement. |
| EmailNoAddressFoundInProfile | 050020 | E-mail | Un événement d’exclusion est généré lorsque l’adresse électronique est introuvable dans l’adresse d’exécution. |
| EmailNoAddressDefinedInPreset | 050021 | E-mail | Un événement d’exclusion est généré lorsque l’adresse d’exécution n’est pas définie en surface. |
| EmailNoVariantDefined | 050026 | E-mail | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie dans le message électronique. |
| EmailNoMessageFoundForTreatment | 050027 | E-mail | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| EmailMalformedAddress | 050024 | E-mail | Un événement d’exclusion est généré lorsque le courrier électronique contient une adresse incorrecte. |
| InAppNoVariantDefined | 050041 | InApp | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie pour le message InApp. |
| InAppNoMessageFoundForTraitement | 050042 | InApp | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| PushNoTokenFoundInProfile | 050030 | Notification push | Un événement d’exclusion est généré lorsque le profil ne comporte pas de jetons push. |
| PushNoValidTokenFoundForApps | 050031 | Notification push | Un événement d’exclusion est généré lorsqu’aucun jeton valide n’est trouvé pour les applications ciblées en surface. |
| PushMalformedProfile | 050034 | Notification push | Un événement d’exclusion est généré lorsque pushNotificationDetails du profil est incorrect. |
| PushNoConsent | 050111 | Notification push | Un événement d’exclusion est généré lorsque l’utilisateur s’est désabonné des notifications push marketing. |
| PushNoApplicationDefinedInPreset | 050033 | Notification push | Un événement d’exclusion est généré lorsque la surface ne contient aucune application à cibler. |
| PushNoVariantDefined | 050035 | Notification push | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie. |
| PushNoMessageFoundForTreatment | 050036 | Notification push | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| SMSNoConsent | 050104 | SMS | Un événement d’exclusion est généré lorsque l’utilisateur s’est désabonné du SMS marketing. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Un événement d’exclusion est généré lorsque &quot;FromNumber&quot; n’est pas défini en surface. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Un événement d’exclusion est généré lorsque &quot;ToNumber&quot; n’est pas défini en surface. |
| SMSNoVariantDefined | 050154 | SMS | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie. |
| SMSNoMessageFoundForTraitement | 050155 | SMS | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |
| WebNoVariantDefined | 050041 | Web | Un événement d’exclusion est généré lorsqu’aucune variante n’est définie pour un message web. |
| WebNoMessageFoundForTreatment | 050042 | Web | Un événement d’exclusion est généré lorsque l’expérience est activée pour le message et qu’aucun message n’est trouvé pour le traitement qualifié. |

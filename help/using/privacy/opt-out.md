---
solution: Journey Optimizer
product: journey optimizer
title: Gérer le processus d’opt-out
description: Découvrez comment gérer le processus d’opt-out et la confidentialité
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: ht
source-wordcount: '232'
ht-degree: 100%

---

# Gérer le processus d’opt-out {#consent}

## À propos de la gestion des désinscriptions {#about}

La possibilité pour les destinataires de se désabonner de la réception des communications d’une marque est une exigence légale. Pour en savoir plus sur la législation applicable, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=fr#regulations){target="_blank"}.

**Pourquoi est-ce important ?**

* Le fait de ne pas se conformer à ces règlements introduit des risques juridiques réglementaires pour votre marque.
* Cela vous aide à éviter d&#39;envoyer des communications non sollicitées à vos destinataires, ce qui pourrait les faire marquer vos messages comme des courriers indésirables et nuire à votre réputation.

## Gestion des désinscriptions dans Journey Optimizer {#opt-out-ajo}

Lors de l’envoi de messages à partir des parcours ou des campagnes, vous devez toujours vous assurer que les client(e)s peuvent annuler l’abonnement à de futures communications. Une fois désinscrits, les profils sont automatiquement supprimés de l’audience des futurs messages marketing.

Alors que **[!DNL Journey Optimizer]** offre des moyens permettant de gérer les désinscriptions des e-mails et des SMS, les notifications push ne nécessitent aucune action de votre part, car les destinataires peuvent annuler leur abonnement depuis leurs appareils. Par exemple, lors du téléchargement ou de l’utilisation de votre application, ils peuvent choisir d’arrêter les notifications. De même, ils peuvent modifier les paramètres de notification par le biais du système d’exploitation mobile.

Découvrez comment gérer les désinscriptions des e-mails et des SMS de Journey Optimizer dans les sections suivantes :

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Prospect" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>Gérer le processus de désinscription aux e-mails</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Peu fréquent" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>Gestion du processus de désinscription aux SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>Dans [!DNL Journey Optimizer], le consentement est géré par le [Schéma de consentement](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=fr){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=fr#choice-values){target="_blank"} d’Experience Platform.
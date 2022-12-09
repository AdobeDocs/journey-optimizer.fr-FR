---
solution: Journey Optimizer
product: journey optimizer
title: Gérer le droit d’opposition
description: Découvrez comment gérer l’exclusion et la confidentialité
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Gérer le droit d’opposition {#consent}

## A propos de la gestion des désinscriptions {#about}

Fournir aux destinataires la capacité de se désabonner de recevoir des communications d’une marque est une obligation légale. En savoir plus sur la législation applicable dans la section [Documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

**Pourquoi est-ce important ?**

* Le non-respect de ces réglementations entraîne des risques juridiques pour votre marque.
* Il permet d&#39;éviter d&#39;envoyer des communications non sollicitées à vos destinataires, ce qui pourrait les faire marquer vos messages comme du spam et nuire à votre réputation.

## Gestion des exclusions dans Journey Optimizer {#opt-out-ajo}

Lors de l’envoi de messages à partir de parcours ou de campagnes, vous devez toujours vous assurer que les clients peuvent se désabonner de futures communications. Une fois désabonnés, les profils sont automatiquement supprimés de l’audience des futurs messages marketing.

while **[!DNL Journey Optimizer]** offre des moyens de gérer l’exclusion dans les emails et les SMS, les notifications push ne nécessitent aucune action de votre côté, car les destinataires peuvent se désabonner via leurs appareils eux-mêmes. Par exemple, lors du téléchargement ou de l’utilisation de votre application, ils peuvent choisir d’arrêter les notifications. De même, ils peuvent modifier les paramètres de notification par le biais du système d’exploitation mobile.

Découvrez comment gérer l’exclusion dans les emails et SMS Journey Optimizer dans les sections suivantes :

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="prospect" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>Gestion des opt-out des emails</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Inrégulier" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>Gestion des opt-out des SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>Dans [!DNL Journey Optimizer], le consentement est géré par Experience Platform. [Schéma de consentement](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. Par défaut, la valeur du champ de consentement est vide et traitée comme un consentement pour recevoir vos communications. Vous pouvez modifier cette valeur par défaut lors de l’intégration à l’une des valeurs possibles répertoriées. [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.
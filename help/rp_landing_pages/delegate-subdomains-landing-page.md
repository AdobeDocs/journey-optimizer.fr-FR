---
solution: Journey Optimizer
product: Journey Optimizer
title: Déléguer les sous-domaines d’e-mail
description: Déléguer les sous-domaines d’e-mail
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# Déléguer les sous-domaines d’e-mail{#section-overview}

La délégation de sous-domaines d’e-mail est une étape essentielle de la [configuration des canaux](../using/configuration/get-started-configuration.md), requise avant d’envoyer des e-mails à partir de Journey Optimizer. Les sous-domaines vous permettent d’isoler les types de trafic (par exemple, marketing ou transactionnel), de protéger la réputation de votre domaine principal et d’accélérer le [préchauffage d’adresses IP](../using/configuration/ip-warmup-gs.md). Ils fonctionnent conjointement avec [configuration du canal e-mail](../using/email/get-started-email-config.md) et [surveillance de la délivrabilité](../using/reports/deliverability.md) pour garantir que les messages atteignent les boîtes de réception.

Vous pouvez choisir entre plusieurs méthodes de configuration : **délégation complète** (Adobe gère le DNS), **configuration CNAME** ou **délégation personnalisée** (vous possédez les certificats et le DNS). Si vous commencez avec CNAME, vous pouvez ensuite [migrer vers la délégation personnalisée](../using/configuration/custom-subdomain-migration.md) pour une sécurité plus stricte. Cette section couvre également les enregistrements DMARC et PTR, les enregistrements TXT Google pour Gmail et les pools d&#39;adresses IP. Pour obtenir des conseils plus généraux sur la délivrabilité, consultez [Prise en main de la délivrabilité](../using/reports/deliverability.md) et [Surveillance des adresses e-mail](monitor-reputation-landing-page.md).

## Déléguer les sous-domaines d’e-mail

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=fr)

Commencer avec la délégation de sous-domaines

Découvrez les avantages, les méthodes de configuration et les points à prendre en compte pour la délégation de sous-domaines dans Adobe Journey Optimizer.

[Commencer à déléguer des sous-domaines](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=fr)

Déléguer un sous-domaine

Cette section contient des conseils détaillés pour la délégation de sous-domaines à Adobe, y compris la délégation complète et la configuration CNAME.

[Découvrir comment déléguer](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg?lang=fr)

Configurer un sous-domaine personnalisé

Prenez pleinement possession de vos sous-domaines avec la délégation personnalisée : chargez vos propres certificats SSL et gardez le contrôle total sur la configuration des domaines.

[Configurer un sous-domaine personnalisé](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

Migration de CNAME vers la délégation personnalisée

Migrez les sous-domaines existants configurés CNAME vers la délégation personnalisée pour répondre aux politiques de sécurité et contrôler entièrement les certificats.

[Migration de votre sous-domaine](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=fr)

Configurer les enregistrements DMARC

Configurez les enregistrements DMARC pour améliorer la sécurité et la délivrabilité des e-mails pour les sous-domaines délégués.

[Configurer DMARC maintenant](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=fr)

Ajouter un enregistrement TXT Google

Vérifiez les sous-domaines pour la délivrabilité de Gmail en ajoutant des enregistrements TXT Google dans Adobe Journey Optimizer.

[Ajouter des enregistrements TXT Google](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=fr)

Accéder aux enregistrements PTR et les modifier

Gérez les enregistrements PTR pour les sous-domaines délégués, y compris la modification et la compréhension des statuts de mise à jour.

[Modifier les enregistrements PTR](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=fr)

Créer des groupes d’adresses IP

Regroupez les adresses IP pour améliorer la délivrabilité des e-mails et gérez efficacement la réputation des sous-domaines.

[Créer des groupes d’adresses IP](../using/configuration/ip-pools.md)
:::

::::

## Ressources supplémentaires

- **[Configurer des sous-domaines de page de destination](../using/landing-pages/lp-subdomains.md)** - Configurez des sous-domaines pour les pages de destination et les formulaires d’abonnement.
- **[Configurer des sous-domaines web](../using/web/web-delegated-subdomains.md)** - Déléguer des sous-domaines pour le tracking et les expériences web.
- **[Prise en main de la configuration des canaux](../using/configuration/get-started-configuration.md)** - Présentation de toutes les étapes de configuration des canaux, y compris la délégation de sous-domaines.

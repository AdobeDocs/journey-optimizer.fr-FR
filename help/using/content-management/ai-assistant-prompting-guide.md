---
solution: Journey Optimizer
product: journey optimizer
title: Guide de création de prompts de contenu avec l’assistant IA
description: Découvrez comment créer des prompts efficaces pour la génération de contenu optimisé par l’IA à l’aide du framework CO-STAR afin de créer du contenu marketing à conversion élevée et aligné sur la marque.
topic: Artificial Intelligence
role: User
level: Intermediate
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '2107'
ht-degree: 100%

---

# Bonnes pratiques relatives aux prompts de l’assistant IA {#ai-assistant-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_ai_assistant_prompt"
>title="Exemples de prompts"
>abstract="Pour découvrir comment créer des prompts efficaces qui génèrent du contenu marketing de marque à conversion élevée, consultez la documentation Journey Optimizer."

Ce guide vous permet de structurer vos requêtes, de communiquer l’intention avec clarté et de vous assurer que l’IA produit un message qui correspond aux directives de votre marque, aux besoins de l’audience et aux objectifs de votre campagne.
Découvrez comment rédiger des prompts efficaces qui permettent à l’assistant IA de générer du contenu marketing de grande qualité, conforme à la marque et adapté à vos objectifs.

## Utiliser le framework CO-STAR {#costar-framework}

Pour de meilleurs résultats avec l’assistant IA, organisez vos prompts à l’aide du framework CO-STAR. Cette approche structurée garantit que l’IA comprend exactement ce dont vous avez besoin.

| Composant | Signification | Importance de ces éléments |
|-|-|-|
| **C - Contexte** | Contexte de votre campagne, produit ou situation | Aide l’IA à comprendre la situation dans son ensemble. |
| **O - Objectif** | Votre objectif marketing spécifique | Détermine l’objectif du contenu. |
| **S - Style** | Comment vous voulez communiquer | Définit l’approche. |
| **T - Ton** | Style émotionnel et voix | Détermine comment votre message est perçu. |
| **A - Audience** | Audience ciblée | Garantit que le message trouve un écho auprès des personnes appropriées. |
| **R - Exigences** | Contraintes spécifiques ou exigences | Définit les limites et les éléments critiques. |

## Les bases des prompts d’IA {#key-takeaways}


### Conseils et erreurs à éviter


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Conseils</th>
<th>Erreurs à éviter</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Utiliser le framework CO-STAR pour la structure</p>
<p>Distinguer le nouveau contenu du contenu existant</p>
<p>Se concentrer sur l’utilisation des documents avec des directives d’extraction spécifiques</p>
<p>Utiliser les sélections de menu déroulant pour le ton, la stratégie et les paramètres régionaux</p>
<p>Adapter les objectifs marketing aux fonctionnalités de type de contenu</p>
<p>Générer plusieurs variantes pour les tests A/B</p>
</td>
<td>
<p>Demander des modifications structurelles, de style ou de modification d’image dans les prompts</p>
<p>Mentionner le ton/la stratégie dans les prompts si disponible dans les listes déroulantes</p>
<p>Utiliser des objectifs vagues comme « promouvoir notre produit »</p>
<p>Demander des sélections d’éléments conditionnels</p>
<p>S’attendre à des modifications de la disposition via des prompts</p>
</td>
</tr>
</tbody>
</table>

### Contenu non pris en charge dans les prompts

>[!TIP]
>
>Utilisez l’**éditeur d’e-mail** ou **Adobe Express** pour apporter des modifications visuelles ou d’image.

Ces requêtes ne sont pas prises en charge et doivent être traitées par d’autres outils :

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✕ modifications de la structure des e-mails</th>
<th>✕ Modifications visuelles de style</th>
<th>✕ Opérations de modification d’images</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Sélection des sections spécifiques à modifier</li>
<li>Suppression ou clonage d’éléments</li>
<li>Sélections conditionnelles</li>
<li>Ajout ou suppression de sections de disposition</li>
</ul>
</td>
<td>
<ul>
<li>Mise en forme du texte (gras, italique, taille de police)</li>
<li>Modifications de couleur</li>
<li>Style de disposition (bordures, marge intérieure, marges)</li>
<li>Effets visuels (ombres)</li>
</ul>
</td>
<td>
<ul>
<li>Modifications d’arrière-plan</li>
<li>Ajout de superpositions de texte ou de logos</li>
<li>Recadrage ou redimensionnement d’images</li>
<li>Réglages des couleurs</li>
<li>Remplacement d’image</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Liste de contrôle de qualité {#quality-checklist}

Avant de générer du contenu, vérifiez les points suivants :

&amp;check; **Objectif clair** : indique clairement l’action, le produit/service, la valeur et le contexte.

&amp;check; **Audience cible définie** : indique la démographie, le rôle ou le segment.

&amp;check; **Alignement du type de contenu** : l’objectif correspond au canal ou au format sélectionné.

&amp;check; **Sélections déroulantes configurées** : la tonalité, la stratégie et les paramètres régionaux sont sélectionnés, ne les incluez pas dans le prompt.

&amp;check; **Thème du document spécifié** : met en évidence le contenu ou les sections à référencer.

&amp;check; **Marque appliquée** : les directives de marque appropriées sont sélectionnées.

&amp;check; **Portée réaliste** : évitez les demandes de modifications de disposition, de style ou de structure.

## Rédiger des objectifs marketing efficaces {#marketing-objectives}

### Faites preuve de précision et de réactivité.

Lors de l’élaboration des objectifs marketing, assurez-vous qu’ils sont clairs, exploitables et mesurables. Évitez les énoncés vagues ou génériques.

**Exemples de bons objectifs :**

&amp;check; « Augmenter les inscriptions à notre essai gratuit de 30 jours du nouveau tableau de bord d’analyse optimisée par l’IA »

&amp;check; « Générer des lead pour notre webinaire B2B sur la réduction des coûts du cloud de 40 % qui aura lieu le 15 mars »

&amp;check; « Promouvoir notre réduction de 25 % à durée limitée pour les fêtes sur les abonnements Premium, jusqu’au 25 décembre »

**Exemples à éviter :**

✕ « Promouvoir notre produit » (trop vague)

✕ « Inciter les personnes à acheter » (valeur non précisée)

✕ « E-mail à propos des nouvelles fonctionnalités » (sans objectif)

### Structurez votre objectif.

Fournissez toujours le contexte et la proposition de valeur afin que l’IA puisse générer du contenu pertinent.
Utilisez cette formule pour vous aider à rédiger des objectifs efficaces : **Action + Produit/Service + Valeur/Avantage + Urgence/Contexte**

**Exemples de bons objectifs :**

&amp;check; « Inciter à télécharger notre nouvelle application mobile qui permet aux utilisateurs et utilisatrices de suivre des habitudes de vie durable avec des recommandations personnalisées et écologiques »

&amp;check; « Promouvoir l’inscription à notre atelier exclusif sur les techniques avancées de visualisation des données pour les responsables marketing »

&amp;check; « Augmenter la participation à notre événement de lancement de produit présentant l’assistant IA de rédaction révolutionnaire qui permet de gagner plus de 5 heures par semaine »

**Exemples à éviter :**

✕ « Annoncer une nouvelle application » (proposition de valeur et contexte manquants)

✕ « Inciter les gens à s’inscrire à l’atelier » (manque de précision concernant l’audience et les avantages)

✕ « Promouvoir l’événement » (aucune action, valeur ou urgence claire)

## Créer du contenu ou modifier du contenu existant {#new-vs-modify}

Indiquez clairement si votre demande implique la génération de nouveau contenu ou la mise à jour de contenu existant. Cette distinction est importante, car elle guide l’IA dans le choix de l’approche appropriée et garantit un résultat plus précis et pertinent.

### Création de nouveau contenu

Appliquez cette stratégie lorsque vous lancez des campagnes marketing, de nouveaux produits ou tout type de communication mise à jour ou actualisée. Cela garantit la pertinence de votre message et qu’il s’aligne sur vos objectifs.

**Quels prompts utiliser** ➤ Lors de la création d’un nouveau contenu, concentrez-vous sur votre objectif marketing sans référencer de contenu existant.

>[!BEGINSHADEBOX]

**Exemples :**

* **Essai SaaS** : « Lance notre nouveau logiciel CRM auprès des propriétaires de petites entreprises, en soulignant un gain de temps de 50 %, une qualification des leads 90 % plus rapide et en offrant un essai gratuit de 30 jours avec intégration personnalisée. »
* **Annonce des fonctionnalités** : « Annonce de nouvelles fonctionnalités d’intégration d’API qui réduisent de 60 % le temps de développement pour les entreprises clientes, en ciblant les décideurs et décideuses techniques. »
* **Promotion d’événements** : « Organise les inscriptions à notre webinaire sur les tendances du marketing numérique 2024, avec des experts de Google, Meta et Adobe, en mettant l’accent sur les informations exploitables et le nombre de places limité (500 au maximum). »

>[!ENDSHADEBOX]

### Modification du contenu existant

>[!TIP]
>
>Pour des modifications standard telles que le développement, le résumé ou la simplification, utilisez la fonctionnalité **Affiner** au lieu de rédiger des prompts personnalisés. [En savoir plus](generative-uc.md##refine)

Appliquez cette méthode lorsque vous devez mettre à jour, actualiser ou adapter vos campagnes marketing actuelles. Elle favorise les améliorations progressives, afin que vos messages restent pertinents sans avoir à repartir de zéro.

**Quels prompts utiliser** ➤ Lors de la modification d’un contenu existant, indiquez clairement ce que vous souhaitez modifier et comment le modifier.

>[!BEGINSHADEBOX]

**Exemples :**

* **Actualisation de campagne** : « Modifie l’e-mail de lancement du produit pour mettre l’accent sur les fonctionnalités de sécurité de l’entreprise plutôt que sur les avantages généraux en matière de productivité, en ciblant les décideurs et décideuses informatiques avec des certifications de conformité. »
* **Changement d’audience** : « Adapte notre invitation de démonstration de logiciel pour cibler le secteur de la santé en particulier, en remplaçant les exemples génériques par des cas d’utilisation pour le secteur de la santé et des avantages en termes de conformité HIPAA. »
* **Mise à jour pour les fêtes** : « Remplace notre campagne promotionnelle du troisième trimestre par les achats des fêtes du quatrième trimestre, en mettant l’accent sur les cadeaux des fêtes de fin d’année plutôt que sur la rentrée scolaire, et en insistant sur la rapidité de la livraison. »

>[!ENDSHADEBOX]

## Améliorer votre prompt avec les paramètres avancés {#personalize-prompt}

### Types de stratégie de communication

>[!TIP]
>
>Utilisez le menu déroulant Stratégie de communication du menu Paramètres de texte au lieu de la mentionner dans votre prompt pour un traitement spécialisé.

Votre stratégie de communication détermine la manière dont vous présentez votre message afin de maximiser l’impact. Différentes stratégies fonctionnent mieux selon les objectifs, que vous cherchiez à créer un sentiment d’urgence, à instaurer la confiance ou à déclencher une action immédiate. Choisissez la stratégie qui correspond le mieux à vos objectifs de campagne et à l’état d’esprit de votre audience.

| **Stratégie** | **Idéale pour** | **Style de message** | **Exemples** |
|--------------|--------------|------------------------|--------------|
| **Urgent** | Offres à durée limitée, échéances, action immédiate | Crée une pression immédiate avec un langage axé sur le facteur temporel. | « Agissez dès maintenant : l’offre expire à minuit. » <br> « Inscrivez-vous dès aujourd’hui avant qu’il ne reste plus de places. » <br> « La vente flash de 48 heures commence maintenant. » |
| **FOMO (peur de passer à côté)** | Offres limitées, événements, accès exclusif | Utilise des signaux d’urgence, de rareté et de pression temporelle. | « Plus que 24 heures ! 40 % de réduction sur un stock limité » <br> « Dernière chance : les tarifs avantageux se terminent demain. » <br> « Plus que 100 points bêta. » |
| **Preuve sociale** | Création de confiance, témoignages, produits populaires | Tire parti des expériences et de la validation des autres personnes. | « Rejoignez plus de 50 000 clientes et clients satisfaits. » <br> « 4,9/5 étoiles par les spécialistes du secteur » <br> « Approuvé par des entreprises du Fortune 500 » |
| **Pénurie** | Stock limité, versions exclusives, articles à forte demande | Souligne la disponibilité limitée et l’exclusivité. | « Seulement 5 pièces en stock » <br> « Édition limitée : 100 unités disponibles » <br> « Version exclusive : premier arrivé, premier servi » |
| **Avantage incitatif** | Promotions, programmes de récompenses, offres spéciales | Met en évidence les avantages et les récompenses tangibles. | « Obtenez 20 % de réduction sur votre première commande. » <br> « Multipliez par deux vos points ce week-end. » <br> « Livraison gratuite sur les commandes de plus de 50 euros. » |
| **Exclusivité** | Produits premium, expériences VIP, offres réservées aux membres | Utilise le positionnement premium et le langage mettant en avant un accès privilégié. | « Invitation exclusive à notre démonstration privée » <br> « L’abonnement Elite donne accès à l’analyse avancée. » <br> « Rejoignez des entreprises du Fortune 500 qui font déjà partie de notre clientèle. » |
| **Gamification** | Campagnes d’engagement, programmes de fidélité, contenu interactif | Utilise les mécaniques de jeu et le langage de réussite. | « Accédez à votre prochain niveau de récompense. » <br> « Relevez des défis pour gagner des badges. » <br> « Grimpez au classement pour remporter des récompenses exclusives. » |
| **Informatif** | Formation, recherche, produits complexes, expertise reconnue | Utilise des faits, des données, des informations et des explications. | « 5 informations grâce à l’analyse de plus de 10 000 interactions » <br> « Une nouvelle recherche révèle 3 approches novatrices. » <br> « Guide complet d’implémentation de l’IA dans le marketing » |
| **Formation et informations** | Contenu d’apprentissage, tendances du secteur, bonnes pratiques | Fournit des connaissances précieuses et des points à retenir exploitables. | « Maîtrisez des techniques avancées avec notre guide spécialisé. » <br> « Découvrez les 7 stratégies utilisées par les principaux responsables marketing. » <br> « Découvrez comment optimiser votre workflow en 5 étapes. » |

### Définissez le bon ton. {#tone}

>[!TIP]
>
>Utilisez la liste déroulante Ton du menu Paramètres de texte plutôt que de le spécifier dans votre prompt.

Le ton influence la perception et la réaction de votre audience face à votre message. Sélectionnez toujours un ton qui correspond à l’image de votre marque et à l’étape du parcours des profils.

Utilisez le tableau ci-dessous pour explorer chaque ton en détail, y compris les situations où il est le plus efficace et des exemples de contenu adaptés à chaque style.

| Ton | Idéal pour | Exemple de contenu |
|-|-|-|
| Professionnel | Communications B2B, annonces formelles | « Nous avons le plaisir d’annoncer notre partenariat stratégique… » |
| Empathique | Assistance clientèle, sujets sensibles | « Nous comprenons votre frustration… » |
| Humoristique | Campagnes attrayantes, contenu léger | « Avertissement : peut entraîner de sérieux gains de productivité ! » |
| Enthousiaste | Lancements de produits, promotions d’événements | « C’est le moment que vous attendiez ! » |
| Inspirant | Campagnes de motivation, objectif de la marque | « Ensemble, nous pouvons changer le monde… » |
| Persuasif | Campagnes commerciales, conversions | « Ne manquez pas cette occasion unique de… » |
| Amical | Engagement des clientes et clients, messages de bienvenue | « Quel plaisir de vous accueillir parmi nous ! » |
| Formel | Communications juridiques, notifications officielles | « Nous vous informons des modifications suivantes… » |
| D’excuse | Rétablissement du service, résolution des problèmes | « Nous vous présentons toutes nos excuses pour les désagréments causés… » |
| Affirmé | Contenu de leadership, messages faisant autorité | « Voici ce que vous devez faire maintenant… » |
| Storytelling | Narrations sur la marque, liens émotionnels | « Tout a commencé par une simple question… » |
| Conversationnel | Campagnes d’accompagnement, création de relations | « Parlons de la façon dont cela peut vous aider… » |

### Optimisez les ressources de votre marque. {#brand-assets}

>[!TIP]
>
>Si vous avez déjà chargé une ressource de marque par l’intermédiaire du menu **Ressources de marque**, vous n’avez pas besoin de la référencer dans votre prompt. Le système utilise automatiquement tous les documents sélectionnés.

Les ressources de marque fournissent des informations factuelles qui enrichissent votre contenu généré avec des détails précis et spécifiques.
Lorsque vous chargez des documents généraux tels que des brochures de produit, ajoutez à votre prompt les parties sur lesquelles vous souhaitez mettre l’accent :

* **Au lieu de** _« Utilise la brochure produit »,_ **écrivez** _« Concentre-toi sur les fonctionnalités de sécurité avancées et les certifications de conformité, en particulier la conformité à la norme SOC 2 et le chiffrement des données »_

* **Au lieu de** _« Référence les études de cas »_ **écrivez** _« Mets en évidence les résultats du retour sur investissement des clientes et clients du secteur de la santé, en particulier la réduction de 40 % des coûts au centre médical régional »_

* **Au lieu de** _« Inclus les détails techniques »_ **écrivez** _« Mets l’accent sur les fonctionnalités d’intégration d’API et les avantages pour l’équipe de développement, en te concentrant sur les points d’entrée de l’API REST et le SLA à 99,9 % de disponibilité »_

### Affinement du contenu

>[!TIP]
>
>Utilisez la fonction Affiner au lieu de rédiger des prompts pour préciser, résumer, simplifier, changer de ton ou traduire le contenu existant. [En savoir plus](generative-uc.md#refine)

Une fois le contenu généré, utilisez la fonction **Affiner** pour l’itérer et l’améliorer avec les options suivantes :

| **Action** | **Exemple d’utilisation** | **Exemple de prompt** |
|-|-|-|
| **Développer** | Ajouter de la profondeur et des détails à un contenu succinct | « Développe les avantages techniques de nos fonctions de sécurité. » |
| **Résumer** | Condenser du contenu long pour différents formats | « Résume cette présentation de produit pour une publication sur les réseaux sociaux. » |
| **Simplifier** | Rendre le contenu complexe plus accessible | « Simplifie cette explication technique pour le grand public. » |
| **Modifier le ton** | Adapter le contenu pour différentes audiences | « Adopte un ton plus décontracté pour les jeunes. » |
| **Transcréer** | Adaptation culturelle au-delà de la traduction | « Transcrée cette campagne pour le marché japonais. » |

## Exemples de prompts basés sur un scénario

### En fonction du type de contenu {#content-type-practices}

<table style="table-layout: fixed; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canal</th>
<th>Exemple</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-mail</strong></td>
<td>« Accompagne les prospects d’entreprise en présentant trois témoignages de succès client avec des mesures de retour sur investissement détaillées (IBM : réduction des coûts de 45 %, Accenture : augmentation des leads de 200 %, Microsoft : gains de temps de 60 %), ciblant les directeurs et directrices informatiques des entreprises de plus de 1 000 personnes employées. »</td>
</tr>
<tr>
<td><strong>SMS</strong></td>
<td>« Alerte les clientes et clients VIP d’une vente flash d’environ 4 heures sur des produits électroniques haut de gamme avec une remise de 40 %, limitée aux 100 premières personnes. »</td>
</tr>
<tr>
<td><strong>Notifications push</strong></td>
<td>« Réengage les utilisateurs et utilisatrices qui n’ont pas ouvert l’application depuis 7 jours avec des recommandations de contenu personnalisé basées sur leur historique de lecture. »</td>
</tr>
<tr>
<td><strong>Pages de destination</strong></td>
<td>« Convertis les visiteurs et visiteuses B2B en leads qualifiés en montrant comment notre solution de sécurité d’entreprise empêche 99,9 % des cyberattaques, grâce aux témoignages d’entreprises du Fortune 500 et à un audit de sécurité gratuit. »</td>
</tr>
</tbody>
</table>

### Basé sur des approches spécifiques au secteur {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Secteur industriel</th>
<th>Exemple de prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Technologie B2B</strong></td>
<td>« Montre le retour sur investissement et les spécifications techniques tout en répondant aux préoccupations de sécurité des décideurs et décideuses informatiques qui évaluent notre solution d’infrastructure cloud, en mettant l’accent sur le SLA à 99,9 % de disponibilité, la conformité au SOC 2 et des économies de 40 %. »</td>
</tr>
<tr>
<td><strong>Vente au détail - e-commerce</strong></td>
<td>« Crée un sentiment d’urgence autour des articles des fêtes en stock limité tout en soulignant la livraison gratuite et les retours faciles pour les acheteurs et acheteuses de dernière minute, les quantités limitées (moins de 50 unités restantes) et les délais de livraison de 24 heures. »</td>
</tr>
<tr>
<td><strong>Services financiers</strong></td>
<td>« Sensibilise les clientes et clients aux stratégies de diversification du portefeuille d’investissement tout en maintenant la conformité réglementaire, avec des conseils financiers certifiés et des avertissements sur les risques. »</td>
</tr>
<tr>
<td><strong>Santé et bien-être</strong></td>
<td>« Fais la promotion des avantages en matière de soins préventifs et des bilans de santé annuels tout en maintenant la précision médicale, avec des recommandations de médecins certifiés et des garanties de confidentialité pour les patientes et patients. »</td>
</tr>
<tr>
<td><strong>Formation</strong></td>
<td>« Mets l’accent sur les perspectives d’évolution de carrière et les certifications professionnelles, tout en mettant en valeur l’expertise des formateurs et formatrices, en soulignant un taux de placement de 92 % et un programme axé sur les projets. »</td>
</tr>
<tr>
<td><strong>Plateformes SaaS</strong></td>
<td>« Mets en avant les gains de temps et les avantages de l’automatisation grâce à des mesures spécifiques tout en répondant aux problèmes d’intégration, avec un gain de temps hebdomadaire moyen de 25 heures et une intégration à plus de 200 outils populaires. »</td>
</tr>
</tbody>
</table>

---
solution: Journey Optimizer
product: journey optimizer
title: Guide de demande de contenu de l’assistant AI
description: Découvrez comment créer des invites efficaces pour la génération de contenu optimisée par l’IA à l’aide du framework CO-STAR afin de créer du contenu marketing hautement convertissable et aligné sur la marque.
role: User
level: Intermediate
source-git-commit: 5063115c6ac93ef332044bfff43a4df817a1a4e3
workflow-type: tm+mt
source-wordcount: '2107'
ht-degree: 1%

---

# Bonnes pratiques relatives aux invites de l&#39;assistant AI {#ai-assistant-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_ai_assistant_prompt"
>title="Exemples de prompts"
>abstract="Consultez la documentation de Journey Optimizer pour savoir comment créer des invites efficaces qui génèrent du contenu marketing de marque à conversion élevée."

Ce guide vous aide à structurer vos requêtes, à communiquer l’intention avec clarté et à vous assurer que l’IA produit un message qui correspond aux directives de votre marque, aux besoins de l’audience et aux objectifs de votre campagne.
Découvrez comment écrire des invites efficaces qui permettent à l&#39;assistant AI de générer du contenu marketing sur la marque de haute qualité adapté à vos objectifs.

## Utilisation du cadre CO-STAR {#costar-framework}

Pour de meilleurs résultats avec AI Assistant, organisez vos invites à l&#39;aide du framework CO-STAR. Cette approche structurée garantit que l’IA comprend exactement ce dont vous avez besoin.

| Composant | Signification | Importance de ces éléments |
|-|-|-|
| **C - Contexte** | Informations sur votre campagne, produit ou situation | Aide l’IA à comprendre la situation dans son ensemble |
| **O - Objectif** | Votre objectif marketing spécifique | Détermine l’objectif que le contenu doit atteindre. |
| **S - Style** | Comment vous voulez communiquer | Définit l’approche |
| **T - Ton** | Style émotionnel et voix | Forme le ressenti de votre message |
| **A - Audience** | Audience ciblée | Garantit que le message trouve un écho auprès des personnes appropriées |
| **R - Conditions requises** | Contraintes spécifiques ou exigences | Définit les limites et les éléments critiques |

## L’IA demande des informations essentielles {#key-takeaways}


### À faire et à ne pas faire


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Faire</th>
<th>Ne pas</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Utiliser le framework CO-STAR pour la structure</p>
<p>Soyez explicite en ce qui concerne le contenu nouveau par rapport au contenu existant</p>
<p>Concentrez-vous sur l’utilisation des documents avec des conseils d’extraction spécifiques</p>
<p>Utiliser les sélections de menu déroulant pour le ton, la stratégie et le paramètre régional</p>
<p>Association des objectifs marketing aux fonctionnalités de type de contenu</p>
<p>Générer plusieurs variantes pour les tests A/B</p>
</td>
<td>
<p>Demander des modifications structurelles, de style ou de modification d’image dans les invites</p>
<p>Mentionnez la tonalité/la stratégie dans les invites si disponible dans les listes déroulantes</p>
<p>Utiliser des objectifs vagues comme « promouvoir notre produit »</p>
<p>Sélections d’éléments conditionnels de requête</p>
<p>Attendez-vous à des modifications de la disposition via des invites</p>
</td>
</tr>
</tbody>
</table>

### Contenu non pris en charge dans les invites

>[!TIP]
>
>Utilisez l’**éditeur d’e-mail** ou **Adobe Express** pour apporter des modifications visuelles ou d’image.

Ces requêtes ne sont pas prises en charge et doivent être traitées par d’autres outils :

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✕ modifications de la structure des e-mails</th>
<th>✕ Modifications visuelles de style</th>
<th>✕ Opérations d’édition d’images</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Sélection des sections spécifiques à modifier</li>
<li>Suppression ou clonage d'éléments</li>
<li>Sélections conditionnelles</li>
<li>Ajout ou suppression de sections de disposition</li>
</ul>
</td>
<td>
<ul>
<li>Formatage du texte (gras, italique, taille de police)</li>
<li>Modifications de couleur</li>
<li>Style de disposition (bordures, marge intérieure, marges)</li>
<li>Effets visuels (ombres)</li>
</ul>
</td>
<td>
<ul>
<li>Modifications en arrière-plan</li>
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

Avant de générer du contenu, vérifiez les points suivants :

&check; **Objectif clair** : indique clairement l’action, le produit/service, la valeur et le contexte.

&check; **Audience cible définie** : indique la population, le rôle ou le segment.

&check; **Alignement du type de contenu** : l’objectif correspond au canal ou au format sélectionné.

&check; **Les sélections déroulantes configurées** : la tonalité, la stratégie et le paramètre régional sont sélectionnés, ne les incluez pas dans l’invite.

&check; **Focus du document spécifié** : met en surbrillance le contenu ou les sections à référencer.

&check; **Marque appliquée** : les directives de marque appropriées sont sélectionnées.

&check; **Portée réaliste** : évitez les demandes de modifications de disposition, de style ou de structure.

## Rédiger des objectifs marketing efficaces {#marketing-objectives}

### Être spécifique et orienté vers l&#39;action

Lors de l’élaboration des objectifs marketing, assurez-vous qu’ils sont clairs, exploitables et mesurables. Évitez les énoncés vagues ou génériques.

**Exemples de bons objectifs :**

&check; « Augmentez les inscriptions à notre essai gratuit de 30 jours du nouveau tableau de bord d’analyse optimisé par l’IA »

&check; « Générer des pistes pour notre webinaire B2B sur la réduction des coûts du cloud de 40 % » qui aura lieu le 15 mars »

&check; « Promouvoir notre réduction de 25 % pour les vacances à durée limitée sur les abonnements Premium, jusqu’au 25 décembre »

**Exemples à éviter :**

✕ « Promouvoir notre produit » (trop vague)

✕ « Faire en sorte que les gens achètent des choses » (valeur non précisée)

✕ « E-mail à propos des nouvelles fonctionnalités » (n’a pas d’objectif)

### Structurer votre objectif

Toujours fournir le contexte et la proposition de valeur afin que l’IA puisse générer du contenu pertinent.
Utilisez cette formule pour vous aider à rédiger des objectifs efficaces : **Action + Produit/Service + Valeur/Avantage + Urgence/Contexte**

**Exemples de bons objectifs :**

&check; « Encouragez les téléchargements de notre nouvelle application mobile qui aide les utilisateurs à suivre les habitudes de vie durables avec des recommandations personnalisées et écologiques »

&check; « Promouvoir l’inscription à notre atelier exclusif sur les techniques avancées de visualisation des données pour les professionnels du marketing »

&check; « Augmentez la participation à notre événement de lancement de produit présentant l’assistant d’écriture d’IA révolutionnaire qui vous permet de gagner plus de 5 heures par semaine »

**Exemples à éviter :**

✕ « Annoncer une nouvelle application » (proposition de valeur et contexte manquants)

✕ « Inciter les gens à s’inscrire à l’atelier » (manque de précision concernant l’audience et l’avantage)

✕ « Promouvoir l’événement » (aucune action, valeur ou urgence claire)

## Créer du contenu ou modifier du contenu existant {#new-vs-modify}

Indiquez clairement si votre demande implique la génération de nouveau contenu ou la mise à jour de contenu existant. Cette distinction est importante, car elle guide l’IA dans le choix de l’approche appropriée et garantit un résultat plus précis et utile.

### Créer du contenu

Appliquez cette stratégie lorsque vous lancez des campagnes marketing, dévoilez de nouveaux produits ou lancez tout type de communication mise à jour ou actualisée. Cela garantit que votre message commence fort et s’aligne sur vos objectifs.

**Comment inviter** ➤ Lors de la création d’un nouveau contenu, concentrez-vous sur votre objectif marketing sans référencer de contenu existant.

>[!BEGINSHADEBOX]

**Exemples :**

* **Essai SaaS** : « Lancez notre nouveau logiciel CRM auprès des propriétaires de petites entreprises, en soulignant les économies de temps de 50 %, la qualification de lead 90 % plus rapide et en offrant un essai gratuit de 30 jours avec intégration personnalisée »
* **Annonce de la fonctionnalité** : « Annonce de nouvelles fonctionnalités d’intégration d’API qui réduisent de 60 % le temps de développement pour les clients d’entreprise, en ciblant les décideurs techniques »
* **Promotion d’événements** : « Organisez les inscriptions à notre webinaire sur les « Tendances du marketing numérique 2024 », avec des experts de Google, Meta et Adobe, en mettant l’accent sur les informations exploitables et les places limitées (500 max.) »

>[!ENDSHADEBOX]

### Modifier du contenu existant

>[!TIP]
>
>Pour des modifications standard telles que l’élaboration, la synthèse ou la simplification, utilisez la fonction **Affiner** au lieu d’écrire des invites personnalisées. [En savoir plus](generative-uc.md##refine)

Appliquez-la lorsque vous devez mettre à jour, actualiser ou adapter vos campagnes marketing actuelles. Cette méthode prend en charge des améliorations incrémentielles, afin que vos messages restent pertinents sans devoir repartir de zéro.

**Comment inviter** ➤ Lors de la modification d’un contenu existant, indiquez clairement ce que vous souhaitez modifier et comment le modifier.

>[!BEGINSHADEBOX]

**Exemples :**

* **Actualisation de Campaign** : « Modifiez l’e-mail de lancement du produit pour vous concentrer sur les fonctionnalités de sécurité de l’entreprise plutôt que sur les avantages généraux en matière de productivité, en ciblant les décideurs informatiques avec des certifications de conformité »
* **Audience pivot** : « Adaptez notre invitation de démonstration de logiciel pour cibler les soins de santé en particulier, en remplaçant les exemples génériques par des cas d’utilisation des soins de santé et des avantages en termes de conformité HIPAA »
* **Mise à jour saisonnière** : « Mettez à jour notre campagne promotionnelle du T3 pour les achats du T4 pour les vacances, en passant de la rentrée des classes au cadeau de vacances avec l’accent sur la livraison rapide »

>[!ENDSHADEBOX]

## Améliorez votre invite avec les paramètres avancés {#personalize-prompt}

### Types de stratégie de communication

>[!TIP]
>
>Utilisez le menu déroulant Stratégie de communication du menu Paramètres de texte au lieu de le mentionner dans votre invite pour un traitement spécialisé.

Votre stratégie de communication détermine la manière dont vous présentez votre message afin de maximiser l’impact. Différentes stratégies fonctionnent mieux pour différents objectifs, que vous construisiez l&#39;urgence, établissiez la confiance ou conduisiez à une action immédiate. Choisissez la stratégie qui correspond le mieux à vos objectifs de campagne et à l’état d’esprit de votre audience.

| **Stratégie** | **Idéal Pour** | **Style de message** | **Exemples** |
|--------------|--------------|------------------------|--------------|
| **Urgent** | Offres sensibles au facteur temps, échéances, action immédiate | Crée une pression immédiate avec un langage temporel | « Agir maintenant : l’offre expire à minuit » <br> « Inscrivez-vous aujourd’hui avant que les places ne se remplissent » <br> « La vente flash de 48 heures commence maintenant » |
| **FOMO (peur de manquer)** | Offres limitées, événements, accès exclusif | Utilise des signaux d’urgence, de rareté et de pression temporelle | « Il ne reste que 24 heures ! Stock limité à 40 % de réduction » <br> « Dernière chance : les tarifs anticipés se terminent demain » <br> « Il ne reste que 100 points bêta » |
| **Épreuve sociale** | Création de confiance, témoignages, produits populaires | Tire parti des expériences et de la validation des autres utilisateurs | « Rejoignez plus de 50 000 clients satisfaits » <br> « 4,9/5 étoiles par les professionnels du secteur » <br> « Entreprises du Fortune 500 dignes de confiance » |
| **Pénurie** | Stock limité, versions exclusives, articles à forte demande | Souligne la disponibilité limitée et l’exclusivité | « Seulement 5 restants en stock » <br> « Edition limitée : 100 unités disponibles » <br> « Version exclusive : Premier arrivé, premier servi » |
| **Incentive** | Promotions, programmes de récompenses, offres spéciales | Met en évidence les avantages et les récompenses tangibles | « Obtenez 20 % de réduction sur votre première commande » <br> « Gagnez deux points ce week-end » <br> « Livraison gratuite sur les commandes de plus de 50 $ » |
| **Exclusivité** | Produits Premium, expériences VIP, offres réservées aux membres | Utilise le positionnement Premium et le langage d’accès spécial | « Invitation exclusive à notre aperçu privé » <br> « L’adhésion Elite débloque l’analyse avancée » <br> « Rejoignez certaines entreprises du Fortune 500 qui nous utilisent déjà » |
| **Gamification** | Campagnes d’engagement, programmes de fidélité, contenu interactif | Utilise la mécanique du jeu et le langage de réalisation | « Déverrouillez votre prochain niveau de récompense » <br> « Défis complets pour gagner des badges » <br> « Grimpez au classement pour obtenir des prix exclusifs » |
| **Informatif** | Éducation, recherche, produits complexes, leadership | Utilise des faits, des données, des informations et des explications | « 5 informations à partir de l’analyse de plus de 10 000 interactions » <br> « Une nouvelle recherche révèle 3 approches novatrices » <br> « Guide complet d’implémentation de l’IA dans le marketing » |
| **Éducation et informations** | Contenu d’apprentissage, tendances du secteur, bonnes pratiques | Fournit des connaissances précieuses et des points à retenir exploitables | « Principal des techniques avancées avec notre guide d’expert » <br> « Découvrez les 7 stratégies utilisées par les principaux professionnels du marketing » <br> « Découvrez comment optimiser votre workflow en 5 étapes » |

### Donnez le bon ton {#tone}

>[!TIP]
>
>Utilisez la liste déroulante Ton du menu Paramètres Texte plutôt que de le spécifier dans votre invite.

Le ton façonne la manière dont votre audience perçoit votre message et y répond. Sélectionnez toujours un ton qui correspond à la voix de votre marque et à la scène du parcours de profil.

Utilisez le tableau ci-dessous pour explorer chaque tonalité en détail, y compris quand elle fonctionne le mieux et des exemples de contenu adaptés à chaque style.

| Tonalité | Idéal Pour | Exemple de contenu |
|-|-|-|
| Professionnel | Communications B2B, annonces formelles | « Nous sommes heureux d&#39;annoncer notre partenariat stratégique... » |
| Empathique | Assistance clientèle, sujets sensibles | « Nous comprenons à quel point cela doit être frustrant pour vous... » |
| Humoristique | Campagnes attrayantes, contenu léger | « Avertissement : peut entraîner de sérieux gains de productivité ! » |
| Excitant | Lancements de produits, promotions d’événements | « C&#39;est le moment que vous attendiez ! » |
| Inspirant | Campagnes de motivation, objectif de la marque | « Ensemble, nous pouvons faire la différence dans le monde... » |
| Persuasif | Campagnes commerciales, conversions | « Ne manquez pas cette occasion limitée de... » |
| Amical | Engagement des clients, messages de bienvenue | « Nous sommes si heureux que vous soyez ici avec nous ! » |
| Formel | Communications juridiques, avis officiels | « Nous vous informons des modifications suivantes... » |
| Pardonnable | Récupération des services, résolution des problèmes | « Nous nous excusons sincèrement pour tout désagrément causé... » |
| Assertif | Contenu de leadership, messages faisant autorité | « Voici ce que vous devez faire maintenant... » |
| Storytelling | Narrations sur la marque, liens émotionnels | « Tout a commencé par une simple question... » |
| Conversationnel | Cultiver les campagnes, créer des relations | « Parlons de la façon dont cela peut vous aider... » |

### Optimiser les ressources de votre marque {#brand-assets}

>[!TIP]
>
>Si vous avez déjà chargé une ressource de marque par l’intermédiaire du menu **Brand Assets**, vous n’avez pas besoin de la référencer dans votre invite. Le système utilise automatiquement tous les documents sélectionnés.

Les ressources de marque fournissent des informations factuelles qui enrichissent votre contenu généré avec des détails précis et spécifiques.
Lorsque vous téléchargez des documents généraux tels que des brochures de produit, ajoutez à l&#39;invite les parties sur lesquelles vous souhaitez mettre l&#39;accent :

* **Au lieu de** _« Utilisez la brochure produit »_ **vous devez utiliser** _« Concentrez-vous sur les fonctionnalités de sécurité avancées et les certifications de conformité, en particulier la conformité à la norme SOC 2 et le chiffrement des données »_

* **Au lieu de** _« Référencez les études de cas »_ **vous devriez utiliser** _« Mettez en évidence les résultats du retour sur investissement des clients du secteur de la santé, en particulier la réduction de 40 % des coûts au centre médical régional »_

* **Au lieu de** _« Inclure les détails techniques »_ **vous devez utiliser** _« Mettre l’accent sur les fonctionnalités d’intégration d’API et les avantages pour les développeurs, en vous concentrant sur les points d’entrée de l’API REST et le SLA à 99,9 % de disponibilité »_

### Raffinement du contenu

>[!TIP]
>
>Utilisez la fonction Affiner au lieu d’inviter à préciser, résumer, simplifier, changer de ton ou traduire le contenu existant. [En savoir plus](generative-uc.md#refine)

Une fois le contenu généré, utilisez la fonction **Affiner** pour l’itérer et l’améliorer avec les options suivantes :

| **Action** | **Exemple d’utilisation** | **Exemple d’invite** |
|-|-|-|
| **Développer** | Ajouter de la profondeur et des détails au contenu succinct | « Explorez en détail les avantages techniques de nos fonctions de sécurité. » |
| **Résumé** | Condenser du contenu long pour différents formats | « Résumer cette présentation de produit pour une publication sur les médias sociaux » |
| **Simplifier** | Rendre le contenu complexe plus accessible | « Simplifiez cette explication technique pour le grand public » |
| **Modifier la tonalité** | Adapter le contenu pour différentes audiences | « Changer de ton pour donner un ton plus décontracté aux jeunes » |
| **Transcréer** | Adaptation culturelle au-delà de la traduction | « Transcréer cette campagne pour le marché japonais » |

## Exemples d&#39;invites basées sur un scénario

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
<td>« Stimulez les perspectives d’entreprise en présentant trois témoignages de clients avec des mesures de retour sur investissement détaillées (IBM : réduction des coûts de 45 %, Accenture : augmentation des prospects de 200 %, Microsoft : gains de temps de 60 %), ciblant les directeurs informatiques des entreprises de plus de 1 000 employés. »</td>
</tr>
<tr>
<td><strong>SMS</strong></td>
<td>« Alertez les clients VIP sur une vente flash d’environ 4 heures sur des produits électroniques haut de gamme avec une remise de 40 %, limitée aux 100 premiers clients »</td>
</tr>
<tr>
<td><strong>Notifications push</strong></td>
<td>« Réengagez les utilisateurs qui n’ont pas ouvert l’application depuis 7 jours avec des recommandations de contenu personnalisé basées sur leur historique de lecture »</td>
</tr>
<tr>
<td><strong>Pages de destination</strong></td>
<td>« Convertissez les visiteurs B2B en prospects qualifiés en démontrant comment notre solution de sécurité d’entreprise prévient 99,9 % des cyberattaques, grâce aux témoignages Fortune 500 et à un audit de sécurité gratuit »</td>
</tr>
</tbody>
</table>

### Basé sur des approches spécifiques au secteur {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Secteur industriel</th>
<th>Exemple d'invite</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Technologie B2B</strong></td>
<td>« Démontrez le retour sur investissement et les spécifications techniques tout en répondant aux préoccupations de sécurité des décideurs informatiques qui évaluent notre solution d’infrastructure cloud, en mettant l’accent sur la disponibilité de 99,9 % de SLA, la conformité au SOC 2 et des économies de 40 %. »</td>
</tr>
<tr>
<td><strong>Commerce électronique - Vente au détail</strong></td>
<td>« Créez l’urgence autour des articles de vacances en stock limité tout en soulignant la livraison gratuite et les retours faciles pour les acheteurs de dernière minute, en soulignant les quantités limitées (moins de 50 restantes) et la limite de livraison de 24 heures. »</td>
</tr>
<tr>
<td><strong>Services financiers</strong></td>
<td>« Sensibiliser les clients aux stratégies de diversification du portefeuille d'investissement tout en maintenant la conformité réglementaire, avec des conseils financiers certifiés et des avertissements sur les risques. »</td>
</tr>
<tr>
<td><strong>Santé et Bien-être</strong></td>
<td>« Promouvoir les avantages en matière de soins préventifs et les examens médicaux annuels tout en maintenant l'exactitude médicale, avec des recommandations de médecins certifiés par le conseil d'administration et des garanties de confidentialité pour les patients. »</td>
</tr>
<tr>
<td><strong>Education &amp; Formation</strong></td>
<td>« Mettre l'accent sur les résultats d'avancement professionnel et les certifications du secteur tout en mettant en valeur l'expertise des instructeurs, en soulignant le taux de placement de 92 % et le programme axé sur les projets. »</td>
</tr>
<tr>
<td><strong>Plateformes SaaS</strong></td>
<td>« Mettez en avant les gains de temps et les avantages de l’automatisation grâce à des mesures spécifiques tout en répondant aux problèmes d’intégration, avec un gain de temps hebdomadaire moyen de 25 heures et une intégration à plus de 200 outils populaires. »</td>
</tr>
</tbody>
</table>

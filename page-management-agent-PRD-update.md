---
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 1%

---
# Mise à jour du PRD pour l’agent de gestion de page (agent de structure)

## URL de la page Wiki
https://wiki.corp.adobe.com/display/~simonetn/%3CUC-12%3E+Structure+Agent

---

# &#x200B;1. Résumé

L’**Agent de gestion de page** (anciennement « Agent de structure ») aide les auteurs à réorganiser la documentation en toute sécurité en déplaçant, supprimant ou renommant les pages, tout en gérant automatiquement tous les impacts sur l’ensemble du référentiel.

**Statut :** ✅ **IMPLÉMENTÉ** (v1.5.0 - Publiée en novembre 2025)

**Objectif :** Éliminez la refactorisation manuelle de la documentation, source d’erreurs, en fournissant une analyse d’impact automatisée, une exécution transparente et une vérification complète des déplacements, des suppressions et des renommages.

JIRA > DOCAC-13695

---

# &#x200B;2. Énoncé du problème

Les référentiels de documentation nécessitent des modifications structurelles fréquentes. Ces opérations sont actuellement **manuelles et extrêmement sources d’erreurs**, ce qui entraîne :

- **Liens internes rompus** — Le déplacement d’une page rompt toutes les références qui y sont faites
- **Liens d’ancrage non valides** — Les liens profonds (`page.md#section`) ne fonctionnent plus
- **Entrées de table des matières obsolètes** — La table des matières devient incohérente
- **Redirections manquantes** — L’optimisation pour les moteurs de recherche souffre d’URL rompues
- **Chemins d’accès aux images rompus** — Les chemins d’accès aux images relatives se rompent lorsque les pages déplacent des dossiers
- **Matière première obsolète** — Les références aux pages connexes deviennent obsolètes
- **Heures de travail manuel** — Les auteurs doivent rassembler, rechercher et mettre à jour manuellement les liens

**Exemple concret :** le déplacement d’une page de `campaigns/` vers `email/` dossier nécessite la mise à jour de plus de 20 fichiers, ce qui prend entre 2 et 3 heures et génère souvent des problèmes manquants.

L’**Agent de gestion de page** automatise l’ensemble de ce processus, en moins d’une minute et avec une précision de 100 %.

---

# &#x200B;3. Objectifs et résultats clés (OKR)

| **Objectif** | **Résultats clés** | **Statut** |
|---------------|-----------------|-----------|
| Automatiser le workflow de refactorisation complète | 100 % des impacts détectés et mis à jour | ✅ **RÉALISÉ** |
| Suppression des liens rompus | 0 lien rompu après opérations | ✅ **RÉALISÉ** |
| Préserver l’intégrité de la documentation | Cohérence de 100 % de la table des matières/redirection | ✅ **RÉALISÉ** |
| Réduire le temps de création | Réduction de 95 % (3h → 1min) | ✅ **RÉALISÉ** |
| Opérations transparentes | Pré-exécution de 100 % de visibilité | ✅ **RÉALISÉ** |

---

# &#x200B;4. Trois opérations principales

## 📦 Déplacer une page

Déplacer la page vers un autre dossier lors de la mise à jour de toutes les références :
- Met à jour les liens internes (absolus, relatifs, relatifs à la racine)
- Recalcule les chemins d’accès aux images pour la nouvelle structure de dossiers
- Met à jour le fichier TOC.md avec le nouvel emplacement.
- Ajoute la redirection dans redirections.csv
- Met à jour les références du sujet principal
- Valide tous les liens d’ancrage

## 🗑️ Supprimer une page

Supprimez la page contenant une gestion d’impact complète :
- Identifie toutes les pages liées à une page supprimée
- Configure éventuellement la redirection vers la page de remplacement
- Supprime l’entrée du fichier TOC.md
- Avertit en cas de liens rompus si aucune redirection n’a été fournie
- Nettoie les références du sujet principal

## ✏️ Renommer une page

Modifiez le nom de fichier tout en conservant le même dossier :
- Met à jour toutes les références pour utiliser le nouveau nom de fichier
- Met à jour l’entrée TOC.md
- Ajoute une redirection pour la continuité de l’optimisation du moteur de recherche (SEO)
- Conserve tous les liens d’ancrage
- Met à jour les références des pages associées

---

# &#x200B;5. Workflow (16 Étapes)

| **Étape** | **Action** | **Détails** |
|----------|-----------|-------------|
| 1. Invocation | Types d’utilisateurs `@page-management` | Chargement instantané de l’agent |
| &#x200B;2. Analyse du référentiel | Analyse de la structure | Compter les fichiers, localiser la table des matières/les redirections, créer le graphique des liens |
| &#x200B;3. Sélection des opérations | Choisir de déplacer/supprimer/renommer | Menu interactif |
| &#x200B;4. Collection de chemins d’accès | Obtenir la source et la destination | Validation des chemins d’accès |
| &#x200B;5. Analyse D&#39;Impact | Analyse complète | grep + recherche sémantique pour toutes les références |
| &#x200B;6. Rapport d&#39;impact | Détaillé avant/après | Chemins d’accès aux fichiers, numéros de ligne, modifications |
| &#x200B;7. Confirmation de l’utilisateur | Approbation explicite requise | Oui/Non/Modifier |
| &#x200B;8. Fonctionnement des fichiers | Déplacer/supprimer/renommer le fichier | Fonctionnement du système de fichiers |
| &#x200B;9. Lier les mises à jour | Mettre à jour tous les liens | Liens internes et d’ancrage |
| &#x200B;10. Mise à jour de la table des matières | Mettre à jour la table des matières | Conserver la hiérarchie |
| &#x200B;11. Gestion des redirections | Ajouter à redirections.csv | Pour l’optimisation du moteur de recherche |
| &#x200B;12. Mise À Jour Du Chemin De L’Image | Recalculer les chemins (déplacements uniquement) | Conserver la résolution de l’image |
| &#x200B;13. Mise À Jour De Front Matter | Mettre à jour les références YAML | Pages associées, prérequis |
| &#x200B;14. Vérification | Valider toutes les modifications | Rechercher les liens rompus |
| &#x200B;15. Préparation de l&#39;engagement | Générer un message de validation | Résumé détaillé avec statistiques |
| &#x200B;16. Évaluation facultative | Ajout Git si demandé | Fonctionnalité pratique |

---

# &#x200B;6. Exigences fonctionnelles

| **ID** | **Exigence** | **Priorité** | **Statut** |
|--------|----------------|-------------|-----------|
| FR-1 | Prise en charge des opérations Déplacer, Supprimer et Renommer | P1 | ✅ implémenté |
| FR-2 | Détecter tous les liens internes (absolus, relatifs, relatifs à la racine) | P1 | ✅ implémenté |
| FR-3 | Validation et mise à jour des liens d’ancrage | P1 | ✅ implémenté |
| FR-4 | Mettre automatiquement à jour le fichier TOC.md | P1 | ✅ implémenté |
| FR-5 | Gestion des redirections.csv pour l’optimisation du moteur de recherche | P1 | ✅ implémenté |
| FR-6 | Recalculer les chemins d’accès aux images lors du déplacement de pages | P1 | ✅ implémenté |
| FR-7 | Mettre à jour les références du sujet principal | P1 | ✅ implémenté |
| FR-8 | Générer un rapport d’impact complet | P1 | ✅ implémenté |
| FR-9 | Fournir un aperçu avant/après | P1 | ✅ implémenté |
| FR-10 | Exiger une confirmation explicite de l’utilisateur | P1 | ✅ implémenté |
| FR-11 | Afficher la progression transparente | P1 | ✅ implémenté |
| FR-12 | Vérifier toutes les modifications | P1 | ✅ implémenté |

---

# &#x200B;7. Mise En Œuvre Technique

## Algorithme de détection des liens

Approche multi-stratégie :
- **Modèle Regex :** `\[([^\]]+)\]\(([^)]+\.md(?:#[^)]*)?)\)`
- **Handles :** Absolus, relatifs, chemins d’accès racine-relatif + ancres
- **Outils :** grep (correspondance exacte) + codebase_search (sémantique)

## Résolution du chemin

Algorithme intelligent :
1. Obtenir le répertoire des fichiers de lien
2. Résoudre par rapport au chemin absolu
3. Normalisation des chemins d’accès (suppression de `./`, résolution de `..`)
4. Comparer avec le chemin cible
5. Calculer un nouveau chemin relatif pour la destination

## Recalcul du chemin de l&#39;image

Lors du déplacement de pages entre des dossiers, recalcule les chemins d’accès relatifs afin de conserver une résolution d’image correcte.

**Exemple :**

```
Original:  help/using/campaigns/page.md
Image:     ![](assets/image.png)
Resolves:  help/using/campaigns/assets/image.png

Moving to: help/using/email/page.md
New image: ![](../campaigns/assets/image.png)
Resolves:  help/using/campaigns/assets/image.png ✅
```

---

# &#x200B;8. Format du rapport d&#39;impact

Rapport complet présentant :

1. **Résumé des opérations** — Source, destination, type
2. **Tableau récapitulatif des impacts** — Décompte de chaque type d&#39;impact
3. **Liens internes** — Fichier, ligne, avant/après pour chaque lien
4. **Ancrer les liens** — Liens profonds avec les références de section
5. **Mises à jour de la table des matières** — Modifications de la table des matières
6. **Redirections** — Nouvelles entrées de redirection
7. **Chemins d’accès aux images** — Références d’image mises à jour (pour les déplacements)
8. **Front Matter** — Mises à jour des références de métadonnées
9. **Problèmes potentiels** — Avertissements
10. **Plan d&#39;exécution** — Aperçu détaillé

**Exemple de rapport d’impact :**
- 23 liens internes mis à jour dans 15 fichiers
- 5 liens d’ancrage mis à jour
- 1 entrée de table des matières mise à jour
- 1 redirection ajoutée
- 4 chemins d’accès aux images recalculés
- 2 références de front-issue mises à jour
- **Total : 18 fichiers modifiés en ~30 secondes**

---

# &#x200B;9. Exigences Non Fonctionnelles

| **Catégorie** | **Exigence** | **Obtenu** |
|--------------|----------------|-------------|
| **Performances** | Terminer en 60 secondes | ✅ 30 à 45 secondes |
| **Précision** | Détection à 100 % | ✅ 100 % |
| **Évolutivité** | Gérer des milliers de pages | ✅ 500+ testé |
| **Transparence** | Afficher toutes les modifications | ✅ l’aperçu complet |
| **Sécurité** | Aucune perte de données | Confirmation explicite de ✅ |
| **Vérification** | Valider les modifications | ✅ chèques automatisés |
| **Vérifiabilité** | Journal des modifications complet | ✅ validations détaillées |

---

# &#x200B;10. Mesures De Succès

## Quantitatif
- **Gain de temps :** réduction de 95 % (2-3 heures → &lt;1 minute)
- **Exactitude :** 100 % des références détectées et mises à jour
- **Fiabilité :** 0 lien rompu après la refactorisation
- **Performances :** 30 à 45 secondes pour des opérations standard
- **Couverture :** 7 types d’impacts analysés

## Qualitatif
- Les auteurs ✅ peuvent effectuer une refactorisation en toute confiance
- ✅ Transparence complète
- ✅ Contrôles de sûreté explicites
- ✅ Aucun nettoyage manuel nécessaire
- ✅ Vérifiabilité complète

---

# &#x200B;11. Risques et mesures d’atténuation

| **Risque** | **Impact** | **Réduction** |
|----------|-----------|---------------|
| Calculs de chemin incorrects | Liens rompus | ✅ Algorithme complet + vérification |
| Références manquantes | Liens rompus dans les cas de périphérie | ✅ Recherche multi-stratégie (grep + sémantique) |
| Exécution non révisée | Modifications involontaires | ✅ Confirmation obligatoire |
| Conflits de fichiers | Perte ou remplacement de données | ✅ Vérification des conflits avant le vol |
| Modifications non validées | Travail en cours perdu | ✅ Avertissement d&#39;arborescence de travail sale |
| Chemins relatifs complexes | Références d’image endommagées | ✅ Résolution du chemin testé |
| Opérations à grande échelle | Mises à jour incomplètes | ✅ algorithmes efficaces |

---

# &#x200B;12. Instructions d’utilisation

## Démarrage rapide

```
@page-management
```

## Commandes en langage naturel

```
move a page
delete a page
rename a page
refactor documentation
```

## Exemple de session

```
User: @page-management

Agent: 🔧 Page Management Agent
       [Scans repository...]
       ✅ Found 487 Markdown files
       
       What would you like to do?
       1. Move a page
       2. Delete a page
       3. Rename a page

User: 1

Agent: Which page do you want to move?

User: help/using/campaigns/setup.md

Agent: Where should it go?

User: help/using/email/setup.md

Agent: [Analyzes impacts...]
       📊 Impact Report:
       - 23 internal links → update needed
       - 5 anchor links → update needed
       - 1 TOC entry → update needed
       - 4 image paths → update needed
       Total: 18 files will be modified
       
       Proceed? (Yes/No)

User: Yes

Agent: ✅ Complete! All changes verified.
       Ready to commit.
```

---

# &#x200B;13. Améliorations futures

**Fonctionnalités prévues :**
- Opérations par lots (déplacer/renommer plusieurs pages)
- Mode Exécution d’essai (afficher les impacts sans exécution)
- Fonction d’annulation/de restauration
- Suggestions de fusion intelligente lors de la suppression
- Mises à jour du texte du lien en cas de modification du titre
- Déplacement de ressources (déplacement d’images avec une page)
- Gestion des liens entre référentiels
- Option de validation automatique
- Aperçu de la comparaison
- Exporter les rapports d’impact

---

# &#x200B;14. Documentation et ressources

- **Fichier de l’agent :** `.cursor-agents/agents/page-management-agent.md`
- **Référence rapide :** `.cursor-agents/AGENTS.md`
- **Version :** 1.5.0 (Novembre 2025)
- **Référentiel:** `git@git.corp.adobe.com:AdobeDocs/CursorAgents.git`

**Documentation supplémentaire :**
- Guide de configuration : `INSTALL.md`
- Dépannage : `TROUBLESHOOTING.md`
- Tous les agents : `AGENTS.md`

---

# &#x200B;15. Notes de mise à jour

## v1.5.0 (novembre 2025) - Version initiale
- ✅ Implémentation complète des opérations Déplacer/Supprimer/Renommer
- ✅ Analyse d&#39;impact complète (7 types de références)
- ✅ Exécution transparente avec suivi de la progression
- ✅ Vérification et validation automatisées
- ✅ génération d’un message de validation détaillé
- ✅ la vérification de version silencieuse
- ✅ la politique Nouveau démarrage (sans fond perdu)

## Limites connues
- Opérations sur une seule page uniquement (lot bientôt disponible)
- Nécessite un arbre de travail propre pour la sécurité (avertissement fourni)
- Validation manuelle requise (validation automatique bientôt disponible)

---

*Dernière mise à jour : 6 novembre 2025*


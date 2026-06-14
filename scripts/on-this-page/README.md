---
source-git-commit: a4123db7ae90552a15e6f425bce0037426053a78
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---
# Outils de boîte « Sur cette page »

Outil pour ajouter et vérifier la zone ombrée standard **« Sur cette page »** en haut de
Pages de documentation AJO. Voir la spécification dans `.cursor/rules/on-this-page-box.mdc`.
Le déploiement est suivi sous epic **DOCAC-14936** (une tâche par dossier de niveau supérieur).

## Comment se présente la boîte

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## Workflow recommandé (par dossier/tâche Jira)

Exécutez à partir de la racine du référentiel (`journey-optimizer.en/`).

1. **Insérer des cases** (amorçage d&#39;une première ébauche de phrase à partir du sujet de première page)
   `description`). Mécanique, idempotent, ne touche jamais la matière frontale :

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   Prévisualisez d’abord avec `--dry-run`.

2. **Affiner le libellé.** L’adresse est un point de départ : modifiez chaque phrase pour qu’elle
se lit comme une déclaration d’objectif (une phrase, texte brut, anglais américain). Si vous
passez `--seed-from-description`, un espace réservé `{{TODO...}}` est inséré à la place et
le programme de validation signale les éléments restants.

3. **Valider** avant d’ouvrir la requête de tirage :

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   Le code de sortie n’est pas nul en cas d’échec, il peut donc déclencher l’CI.

## Portée / exclusions

Les pages de référence et de syntaxe sont exclues par défaut (parties de chemin `api-reference`,
`expression`, `functions`). Remplacez par `--exclude ...` si nécessaire.

## Vérification de la progression dans l’ensemble du référentiel

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

Sans `--require`, les pages auxquelles il manque toujours une zone sont signalées comme `pending` (et non comme
échec), afin que vous puissiez suivre la progression du déploiement dans le guide.

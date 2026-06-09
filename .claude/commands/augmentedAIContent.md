---
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

---
# augmentedAIContent

Ajoute un accordéon Assistant d’IA généré automatiquement à la fin d’un ou de plusieurs fichiers Markdown dans le référentiel de documentation de Journey Optimizer.

## Référentiel cible

`help/using/` (relatif à la racine du référentiel)

## Syntaxe de l&#39;accordéon (Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Règles:**
- `+++Title` sur une ligne — le titre suit immédiatement `+++`
- `+++` seul sur une ligne ferme l’accordéon
- Ligne vierge avant le `+++` d&#39;ouverture et après le `+++` de fermeture

&#x200B;---

## Workflow

### Étape 1 — Demander la ou les cibles

Demandez à l’utilisateur :
> Quel fichier ou dossier voulez-vous enrichir ?
> - Fichier unique : chemin d’accès relatif à la racine du référentiel (par exemple, `help/using/email/get-started-email.md`)
> - Dossier : tous les fichiers `.md` de manière récursive (ex : `help/using/email`)
> - Liste des fichiers/dossiers

Si un dossier est indiqué, répertoriez les fichiers `.md` trouvés et confirmez-les avant de les traiter.

### Etape 2 — Pour chaque fichier : lire et générer

1. **Lire le fichier** dans son intégralité.
2. **Comprendre le sujet de la page** — quelle fonctionnalité, quel concept ou quelle tâche couvre-t-il ?
3. **Générez le contenu de l’accordéon** à l’aide des règles ci-dessous.
4. **Vérifiez** si un accordéon d’IA existe déjà à la fin (recherchez les `+++AI Assistant` près de la fin). Si oui, demandez à l’utilisateur : remplacer ou ignorer ?

### Étape 3 — Ajouter l&#39;accordéon

Ajoutez à la toute fin du fichier . Ne modifiez aucun autre contenu.

### Étape 4 — Rapport

- Fichiers modifiés ✓
- Fichiers ignorés + raison (contient déjà un accordéon / vide / page d’index)

&#x200B;---

## Règles de génération de contenu

Analysez la page et générez les sections ci-dessous **dans l’ordre** sous forme de listes à puces Markdown. Ignorer les sections où aucun contenu significatif ne peut être extrait.

### Titre de l’accordéon

`+++AI Assistant — Page context`

### 1. TL;DR

Résumé en une phrase de ce que la page enseigne ou permet.

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. Intentions

3 à 6 choses qu’un utilisateur ou une utilisatrice peut accomplir après avoir lu cette page.

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. Glossaire

Termes clés spécifiques à cette page/fonctionnalité avec des définitions courtes. Signalez les termes spécifiques au produit.

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
```

N’incluez que les termes relatifs à cette page. N’utilisez pas de termes marketing génériques.

### &#x200B;4. Mécanismes de sécurisation

Limites, conditions préalables, autorisations ou contraintes mentionnées sur la page.

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. Terminologie

Noms canoniques, acronymes, variantes acceptées, synonymes, désambiguation. Principalement pour la normalisation des pipelines d’IA.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. Questions fréquentes

3 à 6 questions qu’un utilisateur peut poser, avec des réponses courtes.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### Éléments à NE PAS inclure

- Ne **pas** réécrire ou résumer le contenu du corps (il est déjà dans la page)
- N **incluez pas** instructions détaillées
- N’inventez **pas** contenu non pris en charge par la page.

### Modèle complet

```markdown
+++AI Assistant — Page context

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## Remarques

- Traitez les fichiers un par un pour en assurer la qualité.
- Indiquez les pages très courtes ou indexées uniquement et demandez à l’utilisateur s’il doit les ignorer.
- Ne créez pas de nouveaux fichiers : modifiez uniquement les fichiers `.md` existants.

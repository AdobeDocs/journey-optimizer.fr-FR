---
name: ajo-ai-accordion
description: Enrichit les pages de documentation de Adobe Journey Optimizer avec une section en accordéon Assistant AI ajoutée à la fin de chaque fichier Markdown. Lit chaque page, génère automatiquement le contenu pertinent de l’assistant d’IA en fonction du sujet de la page et l’insère sous la forme d’un accordéon réductible. À utiliser lorsque l’utilisateur souhaite ajouter des informations d’IA aux documents AJO, enrichir les pages Markdown d’AJO avec du contenu d’IA ou traiter un fichier ou un dossier de fichiers Markdown avec des sections en accordéon d’IA.
disable-model-invocation: true
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# Enrichissement de l’accordéon d’AJO AI

Ajoute un accordéon Assistant d’IA généré automatiquement à la fin d’un ou de plusieurs fichiers Markdown dans le référentiel de documentation de Journey Optimizer.

## Référentiel cible

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## Syntaxe de l&#39;accordéon (Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Règles:**
- `+++Title` sur une ligne — le titre suit immédiatement `+++`, aucun espace entre
- `+++` seul sur une ligne ferme l’accordéon
- Ligne vierge avant le `+++` d&#39;ouverture et après le `+++` de fermeture

---

## Workflow

### Étape 1 — Demander la ou les cibles

Demandez à l’utilisateur :

> Quel fichier ou dossier voulez-vous enrichir ?
> - Fichier unique : chemin d’accès relatif à la racine du référentiel (par exemple, `help/using/email/get-started-email.md`)
> - Dossier : traite de manière récursive (ex. `help/using/email`) tous les fichiers `.md` qu’il contient
> - Liste des fichiers/dossiers

Utilisez `AskQuestion` si disponible, sinon demandez au niveau de la conversation.

Si un dossier est indiqué, répertoriez tous les fichiers `.md` trouvés et confirmez auprès de l’utilisateur avant de les traiter.

### Etape 2 — Pour chaque fichier : lire et générer

Pour chaque fichier cible :

1. **Lire le fichier** dans son intégralité.
2. **Comprendre le sujet de la page** — quelle fonctionnalité, quel concept ou quelle tâche couvre-t-il ?
3. **Générez le contenu de l’accordéon** à l’aide des règles de génération de contenu ci-dessous.
4. **Vérifiez** si un accordéon d’IA existe déjà à la fin du fichier (recherchez les `+++` près de la fin). Si c’est le cas, demandez à l’utilisateur s’il faut remplacer ou ignorer.

### Étape 3 — Ajouter l&#39;accordéon

Ajoutez à la toute fin du fichier :

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

Aucun autre contenu du fichier ne doit être modifié.

### Étape 4 — Rapport

Une fois tous les fichiers traités :
- Liste des fichiers modifiés ✓
- Liste des fichiers ignorés et motif (contient déjà un accordéon, un fichier vide, n’est pas pertinent, etc.)

---

## Règles de génération de contenu

Générez le contenu de l’accordéon en analysant la page Markdown. Générez les sections suivantes **dans l’ordre**, formatées sous forme de listes à puces Markdown. Ignorez les sections pour lesquelles aucun contenu significatif ne peut être extrait de la page.

---

### Titre de l’accordéon

Utilisation : `+++AI Assistant — Page context`

---

### Sections à générer (dans l’ordre)

**1. TL;DR**

Une phrase. Qu’enseigne ou qu’active cette page ?

```markdown
- **TL;DR:** [one sentence summary]
```

---

**2. Intentions**

Liste à puces de ce qu’un utilisateur peut accomplir après avoir lu cette page (3 à 6 éléments).

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

---

**3. Glossaire**

Termes clés spécifiques à cette page/fonctionnalité, avec une définition courte. Signalez les termes spécifiques au produit.

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

N’incluez que des termes pertinents pour le sujet de cette page. N’utilisez pas de termes marketing génériques.

---

**4. Mécanismes de sécurisation**

Limites, conditions préalables, autorisations ou contraintes mentionnées sur la page.

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

---

**5. Terminologie**

Noms de produits canoniques, acronymes, variantes acceptées, synonymes et indications de désambiguïté. Cette section traite principalement de la normalisation des pipelines d’IA.

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

N’incluez que les entrées présentes ou implicites sur la page.

---

**6. FAQ**

3 à 6 questions qu’un utilisateur peut poser sur le contenu de cette page, avec des réponses courtes.

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

---

### Éléments à NE PAS inclure

- Ne **pas** réécrivez ou résumez le corps du contenu de la page (il est déjà là).
- N **incluez pas** instructions détaillées (elles se trouvent sur la page).
- N **inventez pas** contenu qui n’est pas pris en charge par la page.

---

### Modèle d’accordéon complet

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## Remarques

- Traitez les fichiers un par un, et non en bloc, pour maintenir une qualité de génération élevée.
- Si la page est très courte ou est uniquement une page de redirection/d’index, marquez-la et demandez à l’utilisateur s’il souhaite l’ignorer.
- Ne créez pas de nouveaux fichiers : modifiez uniquement les fichiers `.md` existants.

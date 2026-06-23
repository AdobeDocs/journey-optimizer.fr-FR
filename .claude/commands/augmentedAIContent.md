---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

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

---

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
3. **Générez le contenu de l’accordéon** à l’aide des règles de génération de contenu ci-dessous.
4. **Exécutez la liste de contrôle de validation de post-génération** (voir ci-dessous) — ne la ignorez pas.
5. **Vérifiez** si un accordéon d’IA existe déjà à la fin (recherchez les `+++AI Knowledge Reference` près de la fin). Si oui, demandez à l’utilisateur : remplacer ou ignorer ?

### Étape 3 — Ajouter l&#39;accordéon

Utilisez le bloc d’ouverture fixe et le modèle complet définis dans la **Règles de génération de contenu** ci-dessous. Ajoutez à la toute fin du fichier, suivi immédiatement du commentaire de synchronisation :

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

Ce commentaire permet aux outils et aux rédacteurs à venir de détecter le moment où le corps de la page a dérivé de l’accordéon. Ne modifiez aucun autre contenu.

### Étape 4 — Rapport

- Fichiers modifiés ✓
- Fichiers ignorés + raison (contient déjà un accordéon / vide / page d’index)
- Tous les avertissements de validation générés lors de l’étape 2

---

## Règles de génération de contenu

Analysez la page et générez les sections ci-dessous **dans l’ordre** sous forme de listes à puces Markdown. Ignorer les sections où aucun contenu significatif ne peut être extrait.

### Titre de l&#39;accordéon et ouverture fixe — mot à mot, ne pas modifier

Chaque accordéon doit commencer par ce bloc exact. Copiez-le en l’état ; ne paraphrasez pas, ne condensez pas et ne réorganisez pas :

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Les sections de contenu générées suivent immédiatement après ces deux paragraphes.

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

**Règle de précision du mode de validation — obligatoire :**
Si la page couvre une forme quelconque de test, de prévisualisation ou d’exécution simulée, vous DEVEZ faire la distinction entre tous les modes que la page décrit réellement. Ne réduisez pas les modes distincts en une seule entrée abrégée :
- **Simulation** : effectue le rendu du contenu du message sans l’envoyer ; utilise des profils réels
- **Mode test** — envoie uniquement aux profils de test désignés ; utilise des profils de test AEP persistants (et non des profils synthétiques ou factices)
- **Exécution d’essai** : exécute la logique de parcours complète sans activer les actions ; utilise les données d’audience réelles.

Incluez uniquement les modes présents dans la page. Copiez le terme « produit précis » du corps de la page — ne remplacez ni « profils synthétiques », ni « fausses données », ni « sans données réelles » par l’un de ces termes.

### &#x200B;4. Mécanismes de sécurisation

Limites, conditions préalables, autorisations ou contraintes mentionnées sur la page.

```
**Guardrails:**
- [guardrail]
```

**Règles de précision du mécanisme de sécurisation — obligatoire :**

- **Qualifiez chaque limite numérique** qu’elle soit recommandée ou stricte. Exemple : « Maximum 10 recherches de jeux de données par message (limite stricte) » et non « Maximum 10 recherches de jeux de données ».
- **Qualifiez chaque chiffre de débit ou de débit** avec sa portée. Exemple : « Limite de 150 000 messages/heure TPS (par sandbox) » et non « Limite de 150 000 messages/heure ».
- **Vérifiez chaque mécanisme de sécurisation par rapport au corps de la page** avant de l’inclure. Si la page indique 10 et que l’accordéon indique 5, l’accordéon est erroné. Le corps de la page fait autorité.
- **Ne déduisez pas les mécanismes de sécurisation** qui ne sont pas indiqués sur la page. Si une contrainte existe mais n’est pas indiquée sur la page, omettez-la.

### &#x200B;5. Terminologie

Noms canoniques, acronymes, variantes acceptées, synonymes, désambiguation. Principalement pour la normalisation des pipelines d’IA.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**Règle de précision du statut et du cycle de vie :**
Lorsque la page décrit un cycle de vie (statuts de parcours, statuts de message, statuts de campagne, etc.), copiez les libellés de statut exacts à partir du corps de la page. Ne paraphrase pas. Utilisez les entrées « Ne pas confondre » pour distinguer les statuts qui partagent un mot racine mais ont une signification distincte. Exemple :

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Questions fréquentes

3 à 6 questions qu’un utilisateur peut poser, avec des réponses courtes.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

**Règle de précision des questions fréquentes :**
Les réponses doivent utiliser les mêmes choix de verbe et de substantif que le corps de la page. N’introduisez pas de verbes tels que « rétablir », « réinitialiser » ou « restaurer », sauf si la page les utilise. Si une transition met fin à une session (par exemple, quitter le mode test revient à l’état précédent du parcours), dites exactement cela - ne dites pas que « le parcours revient au mode Brouillon ».

### Éléments à NE PAS inclure

- Ne **pas** réécrire ou résumer le contenu du corps (il est déjà dans la page)
- N **incluez pas** instructions détaillées
- N’inventez **pas** contenu non pris en charge par la page.
- N’utilisez **pas** les termes imprécis suivants, sauf s’ils apparaissent mot pour mot dans le corps de la page : « synthétique », « fausses données », « sans données réelles », « inversé », « restauration » (lors de la description des transitions d’état de produit)

---

## Liste de contrôle de validation de post-génération

Exécutez cette liste de contrôle sur chaque accordéon avant de l’ajouter. Signalez tout échec à l’utilisateur avant de continuer.

### Vérification du mécanisme de sécurisation
- [ ] Chaque valeur numérique de l’accordéon existe mot pour mot ou peut être dérivée du corps de la page
- [ ] Chaque limite est qualifiée comme recommandée ou stricte
- [ ] Chaque chiffre de débit inclut sa portée (sandbox/organisation/instance)

### Vérification terminologique
- [ ] Tous les modes de validation (Simulation, Mode Test, Exécution d’essai) présents dans la page sont inclus et nommés avec des termes adaptés à la page
- [ ] Tous les statuts de cycle de vie utilisent les libellés exacts du corps de la page
- [ ] Pas de verbes imprécis dans les réponses aux questions fréquentes (« revert », « synthétique », « fausses données », « sans données réelles ») sauf s&#39;ils sont présents mot pour mot dans la page

### Vérification de la portée
- [ ] glossaire ne contient pas de termes marketing génériques sans rapport avec la page
- [ ] réponses aux questions fréquentes n’introduisent pas d’informations absentes de la page

Si une vérification échoue, corrigez l’accordéon avant de l’ajouter. Enregistrez la correction dans le rapport Étape 4.

---

## Responsabilité de synchronisation

L’accordéon est une dérivée du corps de la page à un moment donné. Il doit être traité comme faisant partie de la page.

**Lorsque le corps de la page est mis à jour (PR de version, corrections, etc.) :**
- Si la mise à jour modifie un mécanisme de sécurisation, une limite, un libellé d’état ou un mode de validation décrit dans l’accordéon, → régénérer ou mettre à jour manuellement l’accordéon dans la même requête de tirage.
- Si la mise à jour n’est pas liée au contenu de l’accordéon (par exemple, les étapes de la procédure, les mises à jour des captures d’écran), → l’accordéon peut rester inchangé, mais passez-le brièvement en revue.

Le commentaire de synchronisation ajouté après l’accordéon (`<!-- ai-accordion-version -->`) est le signal : si le contenu du fichier précédant l’accordéon a changé depuis que ce hachage a été écrit, l’accordéon est candidat à la révision.

---

## Modèle complet

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
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

---

## Remarques

- Traitez les fichiers un par un pour en assurer la qualité.
- Indiquez les pages très courtes ou indexées uniquement et demandez à l’utilisateur s’il doit les ignorer.
- Ne créez pas de nouveaux fichiers : modifiez uniquement les fichiers `.md` existants.
- La liste de contrôle de validation de post-génération n’est pas facultative. Exécutez-le pour chaque fichier, y compris les opérations en bloc.

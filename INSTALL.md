---
source-git-commit: 80d5f294491b35dcdbfe4976cb3ec4cf14384858
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 4%

---
# 🚀 Installation des agents de curseur

Les agents curseur sont des outils partagés qui vous permettent de créer et de gérer plus efficacement la documentation.

## Première configuration

Vous n’avez à effectuer cette opération qu’une **fois** par référentiel.

### Option 1 : Utilisation Du Curseur (⭐ Recommandé)

1. Ouvrir la conversation avec le curseur (`Cmd+L` ou `Ctrl+L`)
2. Type :

   ```
   @setup-agents
   ```

3. Suivre les invites
4. Terminé ! ✨

### Option 2 : Utilisation du terminal

1. Ouvrez votre terminal dans la racine du référentiel.
2. Exécuter :

   ```bash
   ./setup-agents.sh
   ```

   Ou manuellement :

   ```bash
   git submodule update --init --recursive
   ```

3. Terminé ! ✨

## Vérification

Après la configuration, vérifiez l’installation :

```bash
ls .cursor-agents/agents/
```

Vous devriez voir :
- `draft-page-generator.md`
- `fix-grammar.md`
- etc.

## Utilisation

Une fois installés, vous pouvez utiliser des agents dans le curseur :

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

Voir `.cursor-agents/AGENTS.md` pour obtenir la liste complète des agents disponibles.

## Mise à jour des agents

Pour obtenir la dernière version de tous les agents :

### Option 1 : Utilisation Du Curseur

```
@update-agents
```

### Option 2 : Utilisation du terminal

```bash
git submodule update --remote
```

## Résolution des problèmes

### Erreur « Agent introuvable »

Si cette erreur s’affiche, les agents ne sont pas encore installés. Exécuter :

```
@setup-agents
```

### Le sous-module est vide

Si `.cursor-agents/` existe mais est vide :

```bash
git submodule update --init --recursive --remote
```

### Autorisation refusée

Assurez-vous que le script de configuration est exécutable :

```bash
chmod +x setup-agents.sh
```

### Problèmes réseau/VPN

- Vérifiez que vous êtes connecté à un VPN Adobe
- Vérifier la connectivité réseau
- Vérifier l’accès Git :

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## Fonctionnement

Les agents de curseur sont distribués sous la forme d’un **sous-module Git** :

```
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

Le sous-module pointe vers :
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Cela garantit que tout le monde utilise les mêmes agents, qui sont à jour.

**Besoin d’aide ?** Contactez le responsable de votre équipe de documentation ou vérifiez le wiki interne.


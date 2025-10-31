---
source-git-commit: 7e2ed972b85255ccd64cd04d306f7de602b41165
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 2%

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

3. L’agent va automatiquement :
   - Tester l’accès SSH et HTTPS
   - Utilisation de la méthode de travail
   - Vous guider tout au long de la configuration si nécessaire
4. Terminé ! ✨

**Remarque :** l’agent détecte automatiquement si vous avez un accès SSH ou HTTPS à `git.corp.adobe.com` et utilise la méthode appropriée. Si aucun d’eux ne fonctionne, il fournit une configuration guidée.

### Option 2 : Utilisation du terminal

1. Ouvrez votre terminal dans la racine du référentiel.
2. Exécuter :

   ```bash
   ./setup-agents.sh
   ```

   Le script va automatiquement :
   - Tester l’accès SSH et HTTPS
   - Utilisation de la méthode de travail
   - Afficher les instructions de configuration si nécessaire

   Ou manuellement (si vous savez que votre Git est configuré) :

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

Voir [AGENTS.md](AGENTS.md) pour obtenir la liste complète des agents disponibles.

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
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

Le sous-module pointe vers :
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Cela garantit que tout le monde utilise les mêmes agents, qui sont à jour.

## Pour les responsables

### Ajout à un nouveau référentiel

1. Ajoutez le sous-module :

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. Copiez les fichiers de configuration :
   - `setup-agents.sh`
   - `setup-agent.md` (place dans le root, pas dans le sous-module)
   - `INSTALL.md`

3. Valider :

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### Mise à jour du référentiel central

Les modifications apportées aux agents doivent l’être dans :
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Tous les référentiels recevront des mises à jour via `git submodule update --remote`.

---

**Besoin d’aide ?** Contactez le responsable de votre équipe de documentation ou vérifiez le wiki interne.

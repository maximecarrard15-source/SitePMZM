# SitePMZM

Projet de site web partagé utilisant GitHub.

Ce guide explique simplement comment travailler sur le projet à plusieurs sans écraser accidentellement le travail des autres.

---

# 1. Comment fonctionne le projet

Le projet utilise les **branches GitHub**.

La branche principale s'appelle :

```text
main
```

`main` doit contenir la version stable du site.

Chaque personne travaille sur sa propre branche.

Par exemple :

```text
main
│
├── Maxime
├── Zephyr
├── Matthieu
└── Paul
```

Chacun travaille sur sa branche, puis envoie ses modifications vers `main` grâce à une **Pull Request**.

### Règle importante

**Ne travaillez pas directement sur `main`**, sauf si toute l'équipe est d'accord.

Utilisez votre propre branche.

---

# 2. Le fonctionnement général

Le fonctionnement normal est :

```text
1. Récupérer la dernière version de main
2. Travailler sur sa propre branche
3. Enregistrer ses modifications
4. Faire un commit
5. Faire un push de sa branche vers GitHub
6. Créer une Pull Request
7. Vérifier les modifications
8. Faire un merge de la Pull Request dans main
```

---

# 3. Avant de commencer

Il faut avoir :

* Un compte GitHub
* L'accès au repository `SitePMZM`
* Les permissions nécessaires sur le repository
* Sa propre branche

Pour utiliser VS Code, il faut également avoir :

* VS Code
* Git

---

# 4. UTILISATEURS VS CODE

## A. Première installation

Si vous n'avez jamais téléchargé le projet sur votre ordinateur :

### Étape 1 : ouvrir VS Code

Ouvrez VS Code.

Sur l'écran d'accueil, sélectionnez :

**Clone Git Repository**

### Étape 2 : entrer le repository

Utilisez :

```text
https://github.com/maximecarrard15-source/SitePMZM.git
```

Choisissez l'endroit où vous voulez enregistrer le projet.

Par exemple :

```text
Downloads/
```

### Étape 3 : ouvrir le projet

Lorsque VS Code demande :

> Would you like to open the cloned repository?

Cliquez sur :

**Open**

Vous devriez voir les fichiers du projet :

```text
Hacker_logo.jpg
index1.html
indexCarte.html
style1.css
```

---

# 5. Passer sur sa branche

Regardez dans le **coin inférieur gauche de VS Code**.

Vous devriez voir la branche actuelle, par exemple :

```text
main
```

Cliquez dessus.

Sélectionnez votre branche.

Par exemple :

```text
Maxime
```

Vous devriez maintenant voir :

```text
Maxime
```

dans le coin inférieur gauche.

Vous travaillez maintenant sur la branche `Maxime`.

---

# 6. Avant de commencer à travailler

Il faut toujours vérifier que vous avez la dernière version de `main`.

Ouvrez :

**Terminal → New Terminal**

Lancez :

```bash
git switch main
```

Puis :

```bash
git pull
```

Ensuite, retournez sur votre branche :

```bash
git switch Maxime
```

Remplacez `Maxime` par le nom de votre branche.

### Pourquoi ?

Quelqu'un peut avoir ajouté de nouvelles modifications à `main`.

Vous voulez commencer votre travail à partir de la version la plus récente du projet.

---

# 7. Travailler sur sa branche

Modifiez maintenant les fichiers normalement dans VS Code.

Par exemple :

```text
index1.html
indexCarte.html
style1.css
```

Enregistrez vos modifications avec :

```text
⌘ + S
```

sur Mac.

---

# 8. Vérifier ses modifications

Dans le terminal, lancez :

```bash
git status
```

Vous pourriez voir :

```text
On branch Maxime

Changes not staged for commit:
    modified: index1.html
```

Cela signifie que Git a détecté vos modifications.

---

# 9. Faire un commit

Commencez par :

```bash
git add .
```

Puis :

```bash
git commit -m "Describe what you changed"
```

Par exemple :

```bash
git commit -m "Updated homepage design"
```

Un **commit** est une sauvegarde de vos modifications dans l'historique Git.

Utilisez des messages courts et compréhensibles.

### Bons exemples

```text
Added map section
Updated homepage
Fixed navigation
Changed CSS layout
```

### À éviter

```text
stuff
changes
lol
final
final2
final_final
```

Git a déjà suffisamment de problèmes sans devoir comprendre ce que signifie `final_final`.

---

# 10. Faire un push

Après le commit, envoyez votre branche vers GitHub :

```bash
git push
```

Vos modifications sont maintenant sur GitHub.

Elles sont toujours sur **votre branche**, et pas sur `main`.

Par exemple :

```text
main
│
└── Maxime
     └── Vos modifications
```

---

# 11. Créer une Pull Request

Allez sur le repository GitHub.

Vous devriez avoir la possibilité de créer une :

**Pull Request**

La Pull Request doit être :

```text
Maxime → main
```

Cela signifie :

> « Je veux ajouter les modifications de ma branche au projet principal. »

Donnez un titre clair à la Pull Request.

Par exemple :

```text
Updated homepage design
```

Expliquez brièvement ce que vous avez modifié.

Puis créez la Pull Request.

---

# 12. Vérifier et faire le merge

Avant de faire le merge, vérifiez les modifications.

Si tout est correct :

**Merge Pull Request**

Les modifications feront alors partie de :

```text
main
```

Une fois le travail terminé, votre branche peut être supprimée si elle ne sert plus.

---

# 13. UTILISATEURS GITHUB UNIQUEMENT

Il est également possible de travailler directement sur GitHub sans utiliser VS Code.

C'est surtout pratique pour les petites modifications.

## A. Ouvrir le repository

Allez sur :

```text
https://github.com/maximecarrard15-source/SitePMZM
```

---

# 14. Passer sur sa branche

En haut de la liste des fichiers, trouvez le sélecteur de branche.

Il devrait probablement afficher :

```text
main
```

Cliquez dessus.

Sélectionnez votre branche.

Par exemple :

```text
Maxime
```

Vous êtes maintenant sur la version `Maxime` du projet.

---

# 15. Modifier un fichier

Ouvrez le fichier que vous voulez modifier.

Par exemple :

```text
index1.html
```

Cliquez sur le bouton **pencil/edit**.

Faites vos modifications.

Puis descendez en bas de la page.

---

# 16. Faire un commit directement sur GitHub

GitHub vous demandera un message de commit.

Par exemple :

```text
Updated homepage
```

Vérifiez que vous faites le commit sur votre branche.

Vous voulez :

```text
Commit directly to the Maxime branch
```

et PAS :

```text
Commit directly to main
```

Cliquez ensuite sur :

**Commit changes**

---

# 17. Créer une Pull Request

Une fois vos modifications terminées, allez dans :

**Pull requests → New pull request**

Vérifiez que les branches sont :

```text
base: main
compare: Maxime
```

Autrement dit :

```text
Maxime → main
```

Vérifiez les modifications.

Si tout est correct, créez la Pull Request.

---

# 18. Faire le merge dans main

Une fois que l'équipe a vérifié la Pull Request :

**Merge Pull Request**

Les modifications seront ajoutées à :

```text
main
```

---

# 19. Créer une nouvelle branche

Les branches peuvent être créées directement sur GitHub.

Allez sur le repository.

Cliquez sur le sélecteur de branche :

```text
main
```

Entrez le nom de la nouvelle branche.

Par exemple :

```text
Maxime
```

GitHub proposera :

**Create branch: Maxime from main**

Cliquez dessus.

La branche existe maintenant.

---

# 20. Nommer les branches

Utilisez des noms qui permettent de comprendre facilement à quoi elles servent.

### Par personne

```text
Maxime
Zephyr
Matthieu
Paul
```

### Par fonctionnalité

```text
homepage
map
navigation
login-page
new-design
```

Pour ce projet, utiliser le prénom de chaque personne est parfaitement acceptable :

```text
Maxime
Zephyr
Matthieu
Paul
```

---

# 21. Ce qu'il NE faut PAS faire

### Ne travaillez pas directement sur `main`

Sauf si toute l'équipe est d'accord.

### Ne supprimez pas la branche de quelqu'un d'autre

Sauf si vous savez qu'elle n'est plus nécessaire.

### N'utilisez pas `force push`

Évitez :

```bash
git push --force
```

surtout sur les branches partagées.

### Ne mettez jamais de mots de passe ou de clés secrètes

Ne mettez jamais dans le repository :

```text
password
API keys
private keys
tokens
```

---

# 22. Si Git signale des modifications que vous ne reconnaissez pas

Ne supprimez pas immédiatement les fichiers et ne lancez pas des commandes Git au hasard.

Commencez par :

```bash
git status
```

Puis regardez ce qui a changé.

---

# 23. En cas de conflit

Un **conflict** arrive lorsque deux personnes modifient la même partie d'un même fichier.

Par exemple :

```text
Maxime modifie la ligne 20
        +
Zephyr modifie la ligne 20
        =
Git ne sait pas quelle version garder
```

Git vous demandera de résoudre le conflit.

**Ne paniquez pas et ne supprimez pas simplement une des deux versions.**

Ouvrez le fichier et décidez quelles modifications doivent être conservées.

Puis :

```bash
git add .
git commit -m "Resolved merge conflict"
git push
```

Si vous n'êtes pas sûr de ce qu'il faut garder, demandez à un autre membre de l'équipe avant de résoudre le conflit.

---

# 24. Commandes VS Code utiles

### Voir sa branche actuelle

```bash
git branch
```

### Changer de branche

```bash
git switch branch-name
```

Exemple :

```bash
git switch Maxime
```

### Récupérer les dernières modifications

```bash
git pull
```

### Voir les modifications

```bash
git status
```

### Préparer les modifications

```bash
git add .
```

### Sauvegarder une version

```bash
git commit -m "Description of changes"
```

### Envoyer les modifications sur GitHub

```bash
git push
```

---

# 25. Workflow VS Code rapide

Pour travailler normalement, retenez :

```bash
git switch main
git pull
git switch YOUR-BRANCH
```

Travaillez ensuite sur vos fichiers.

Quand vous avez terminé :

```bash
git add .
git commit -m "What I changed"
git push
```

Puis créez une Pull Request :

```text
YOUR-BRANCH → main
```

---

# 26. Workflow GitHub rapide

Si vous travaillez directement sur GitHub :

```text
1. Select your branch
2. Edit your files
3. Commit to your branch
4. Create Pull Request
5. Check the changes
6. Merge into main
```

---

# 27. Le concept le plus important

Retenez ceci :

```text
MAIN
│
│   Version stable
│
├───────────────┐
│               │
▼               ▼
VOTRE BRANCHE   BRANCHE D'UN AMI
│               │
│ Travail       │ Travail
│               │
└───────┬───────┘
        │
        ▼
   PULL REQUEST
        │
        ▼
       MAIN
```

**`main` = le projet stable partagé**

**Votre branche = votre espace de travail**

**Commit = enregistrer votre travail dans Git**

**Push = envoyer votre travail vers GitHub**

**Pull = récupérer les dernières modifications**

**Pull Request = demander à ajouter votre travail à `main`**

**Merge = ajouter réellement les modifications à `main`**

---

# 28. Règle recommandée pour l'équipe

Pour chaque nouvelle fonctionnalité :

```text
1. Partir de la dernière version de main
2. Créer/utiliser sa propre branche
3. Travailler sur la fonctionnalité
4. Faire régulièrement des commits
5. Faire un push de la branche
6. Créer une Pull Request
7. Vérifier les modifications
8. Faire le merge dans main
```

Cela permet de garder le projet organisé et réduit fortement le risque qu'une modification accidentelle détruise le site entier.

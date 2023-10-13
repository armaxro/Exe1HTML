
# creation d'un depot GIT 
## Création d'un dépôt GIT en local

Dans la console, initialisation du dépôt:

```bash 
git init
```
## visualisation de l'état de GIT
```bash
git status
```
### Pour voir les fichiers et dossiers unix

```bash
ls -a
```
## Pour ajouter un fiechier à la future sauvegarde
```bash
git add README.md
```

## Pour effectuer la sauvegarde
les fichiers en attentes s-de sauvegarde sont en vert 
les fichiers non suivi sont en rouge

seul les fichiers en **staging** seront sauvés
```bash
git commit -m"Message du commit"

un commit est une sauvegarde, on peut y accéder avec un 'git log'
(affichage des identifiants des sauvegardes et 'git show' (sans paramètre, affichage 
du dernier commit)


## Pour ajouter tous les fichiers
```bash
git add . 
```

## Ajout d'un serveur

Nous allons utiliser un dépôt que l'on va créer sur Github.com
après connexion. Comme c'est un travail personnel, son URL sera 
de ce type https://github.com/VOTRE_USERNAME/le nom du projet

Nos créons un new repository, puis nous copions la clefs SSH

git@github.com:armaxro/Exe1HTML.git

Nous retournons dans notre console:

```bash
git remote add origin git@github.com:armaxro/Exe1HTML.git
```

Pour voir si ça a fonctionné
```bash
git remote -v
```

## Envoi du projet
```bash
git push origin master
```

#Récupération du projet

Si on sohaite récupérer que le `.git`(donc l'historique sans le fichiers)

```bash
git fetch origin master
```

Si on souhaite récupérer toute la branche `main`

```bash
git pull origin master
```

Si on a effectué des modifications en local non voulues empèchant
la recuperation des fichiers (`merge error`)


On peut utiliser un `git stash` pour faire une pseudo sauvegarde et revenir au dernier commit
avant de refaire un `git pull`


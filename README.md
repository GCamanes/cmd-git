![alt text](https://cdn-images-1.medium.com/max/2000/1*yGFvyglXcEt-ZOV3IWQTdw.jpeg "Logo Bandeau Git")

# Git & commandes pratiques
Petite page sympa pour se rappeler des commandes les plus utilisées dans les bonnes pratiques de Git ! 

## init
```bash
git init
```
Permet d'initialiser le suivi de version avec Git d'un projet.

## status
```bash
git status
```
Permet de connaitre l'état/le status du dossier local git.
Par exemple, sur quelle branche on se trouve, si on est à jour avec la branche master, s'il y a des choses à commit, etc.

## add
```bash
git add <FICHIER>
```
Permet d'ajouter un fichier à l'index (stage) pour que les modifications de ce fichier soient prises en compte dans le prochain commit.

## commit 
```bash
git commit -a -m "MESSAGE"
```
Permet de réaliser un commit avec les dernières modifications indexées.
L'option "-a" permet dd'ajouter tous les fichiers (déjà suivis) sans passer par un add.
L'option "-m" d'ajouter tous les fichiers (déjà suivis) sans passer par un add


## config

Permet de configurer les informations utilisées par le dépôt git.
```bash
git config --global user.name NAME user.email MAIL
```
configuration pour tous les projets

```bash
--local
```
configuration pour le dossier courant uniquement
```bash
--system
```
configuration niveau machine

## log
```bash
git log -N
```
permet de consulter l'historique des N derniers commit du dossier git.

## checkout

permet de récupérer la dernière version d'un élément du dépôt git.

``` bash
git checkout FICHIER
```
dernière version du fichier

``` bash
git checkout -- FICHIER
```
dernière version indexée du fichier
``` bash
git checkout BRANCHE
```
déplacement sur la branche BRANCHE.

Marche aussi avec les versions (TAG).

## fichier .gitignore

Ce fichier permet de spécifier l'ensemble des fichiers (ou type de fichier) qui ne seront jamais indexés et de les ignorer.

- *.a. : pas de fichier .a dans tous le projet
- !lib.a.      : suivi du fichier malgré la règle précédente
- /TODO  : ignorer le fichier TODO à la racine du projet
- build/     : ignorer tous les fichiers dans le répertoire build
- doc/*.txt   : ignorer doc/notes.txt, mais pas doc/server/arch.txt
- doc/**/*.txt : ignorer tous les fichiers .txt sous le répertoire doc/

## fetch
```bash
git fetch REMOTE
```
Consulter les changements survenus sur le REMOTE

## branch
```bash
git branch BRANCHE
```
Permet de créer une branche.
```bash
git branch
```
Permet de lister les branches existantes et savoir sur laquelle on se trouve.

## merge
```bash
git merge BRANCHE
```
permet de récupérer les modifications de la branche BRANCHE sur la branche courante.

## stash
```bash
git stash
```
permet de créer une sauvegarde temporaire sans passer par un commit.

# Compte rendu — TP01 Git

## Partie 0
La version installé est la 2.43.0


## Partie 1
https://github.com/Rebistoukette


## Partie 2

1. ```
    user.name=Rémi Bertranda
    user.email=remi.bertranda@gmail.com
    init.defaultbranch=main
    core.editor=nano
    ```
2. Il sert à faire la config pour toute la session
    Les réglages sont enregistrés dans .git/congif

    
## Partie 3
### 3.1
Il répond une erreur qui dit que ce repertoire n'est pas un repo car on n'a rien initialisé

### 3.2
1. Il a créé le dossier .git

    On ne le voyais pas car il est caché

2. Il répond qu'il n'y a aucun commit

### 3.3
git status range README.md dans le répertoire de travail

### 3.4
Le README.md est passé dans la zone de préparation

### 3.5
1. ```
    commit ceee8e85c74635e36868cf36e36a5ef895ac00e8 (HEAD -> main)
    Author: Rémi Bertranda <remi.bertranda@gmail.com>
    Date:   Tue Sep 29 16:18:22 2026 +0200

    Création du README
    ```
2. hash : ceee8e85c74635e36868cf36e36a5ef895ac00e8

    auteur : Rémi Bertranda <remi.bertranda@gmail.com>

    date : Tue Sep 29 16:18:22 2026 +0200

3. Il s'écrit avec 40 caractères d'hexadécimal soit 160 bits au total

### 3.7
1. `git status` décrit README.md comme élément modifié.

2. `git diff` montre les différences entre le fichier local et celui envoyé sur le commit. Le `+` montre ce qu'il y a sur la machine.

Ligne supplémentaire pour le 3.8.


### 3.8
1. ```
    89dec09 (HEAD -> main) Ajout de la ligne supplémentaire pour le 3.8.
    7ffa632 Création de l'aide-mémoire Git
    d286cab Question 3.7 complété avec la seconde question de la 3.7
    897dcf9 Question 3.7 (réponse 1 et 2)
    0feb3f9 Ajout du compte rendu (questions 0 à 3.5)
    fabd5c6 Ajout du compte rendu (questions 0 à 3.5)
    ceee8e8 Création du README
    ```

2. ça permet de pouvoir revenir à une ancienne sauvegarde d'un seul fichier en cas de problème au lieu de récupéré les anciennes sauvegarde de tous les fichiers

## Partie 4

### 4.1
Le `git show` montre les modifications ajouté depuis la version précédente du fichier correspondant au hash choisi. On retrouve donc tout les ajouts et suppressions.

### 4.2
Le `git restore` permet d'annuler la dernière modification d'un fichier.

### 4.3
Après le `git restore`, le fichier `test.txt` se retrouve à nouveau dans le répèrtoire de travail.
Le fichier est toujours présent sur le disque, il a seulement été changé de zone.

### 4.4
1. Les fichiers qui ont disparu du `git status` sont tout les fichiers ajouté dans le `gitignore`. 
<br>
`*.log` désigne tout les fichier qui finissent en `.log`

2. Le fichier qui apparait est `.gitignore` et il ne faut pas le committer.

### 4.5
Le fichier `README.md` contenait lors du permier commit :
```
# TP01 — Découverte de Git

Dépôt réalisé par Prénom Nom, 1CIEL-IR.

Ce dépôt contient mon compte rendu du TP01.

```

Ce qui a changé depuis c'est ajout de la ligne de l'année.

## Partie 5

### 5.2
1. Les fichiers créés sont `id_ed25519.pub` (la clé publique) et `id_ed25519` (la clé privé)
2. Ils sont tout les deux en 700 car seul le propriétaire des clé dois pouvoir les voir et en faire ce qu'il veut.

### 5.4
1. `Hi Rebistoukette! You've successfully authenticated, but GitHub does not provide shell access.`

2. Avec notre clé privé, GitHub pourrait usurper notre identité ou quelqu'un qui récupère des information depuis github pourrait également, alors qu'avec la clé prublique c'est impossible.
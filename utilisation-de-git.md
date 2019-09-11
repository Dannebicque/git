# Utilisation de GIT

{% hint style="info" %}
Cette partie s'applique essentiellement si c'est un projet que vous avez créé \(git init\). Si vous avez récupéré un projet, les fichiers à surveiller seront probablement déjà définis. Mais vous pourrez en ajouter.
{% endhint %}

GIT est configuré et activé sur un dossier. Cependant, GIT ne surveille rien, et ne fait rien pour le moment. Plusieurs étapes sont nécessaires :

* Surveiller votre projet
* Ajouter des fichiers ou des répertoires
* Sauvegarder des modifications \(commit\)
* Utiliser des repository/remote

## Surveiller votre projet

A tout moment vous pouvez executer la commande suivante :

```text
git status
```

Cette commande va vous indiquer l'activité de votre projet. Ce qui est modifié, ajouté et ignoré par GIT.

A tout moment vous pouvez regarder les différences en executant la commande suivante :

```text
git diff
```

Cette commande va vous indiquer toutes les différences entre la dernière version sauvegardée et l'actuelle, pour l'ensemble des fichiers.

L'affichage précédent peut être difficile à lire, il est donc possible de regarder les différentes pour un fichier précis, en executant la commande suivante :

```text
git diff /chemin/du/fichier
```

Cette commande va vous indiquer toutes les différences entre la dernière version sauvegardée et l'actuelle, pour le fichier spécifié.

## Ajouter des fichiers ou des répertoires

Certains fichiers sont définis comme "untracked" par GIT, c'est à dire qu'il ne suit pas les modifications. Il faut donc les ajouter, si on souhaite les versionner.

```text
git add nomfichier1 nomfichier2
```

Cette commande permet de versionner le fichier nomfichier1 et nomfichier2.

Il est aussi possible d'ajouter directement un répertoire.

```text
git add repertoire/
```

Cette commande permet de versionner tous les fichiers contenus dans repertoire.

{% hint style="danger" %}
`git add *` **tu ne feras jamais !!**
{% endhint %}

l ne faut ajouter les fichiers qu'une seule fois. Ils seront ensuite toujours suivi par GIT.

Par contre il est nécessaire d'ajouter chaque nouveau fichier créé.

## Sauvegarder les modifications \(commit\)

Maintenant que les fichiers sont suivis, on peut sauvegarder les modifications

```text
git commit
```

Cette commande va sauvegarder tous les fichiers suivis et modifiés. En executant cette commande vous devrez **OBLIGATOIREMENT** indiquer un message pour permettre de comprendre les modifications.



Il peut parfois être intéressant de ne sauvegarder qu'une partie des modifications. Dans ce cas on peut préciser les fichiers

```text
git commit nomfichier1 nomfichier2
```



On peut également inclure le message directment dans la ligne de commande

```text
git commit -m "Mon message de suivi de modification"
```

## Utiliser des repository/remote \(push/pull\)

On vient de voir l'intérêt d'utiliser Git. Mais pour le moment tout le suivi de version est stocké sur notre machine. Ce qui limite l'intérêt et ne permet donc pas une réelle sauvegarde de notre travail, ni même un travail collaboratif.

Pour cela, il faut passer par un remote. On peut installer son propre remote assez facilement sur un serveur, ou utiliser une solution existante : GitHub, GitLab, BitBucket, Mercurial, ...



Cette solution n'est pas la seule, mais elle est la plus simple et rapide, car n'implique pas de configuration.

* Pour cela il faut se rendre sur la solution choisie \(GitHub par exemple\) et créer grâce à l'interface votre repository.
* Remplissez les informations et laissez le fichier readme.md
* Ensuite il faut cloner ce repository sur votre machine.

Marquer solution pour ajouter le serveur + création sur github


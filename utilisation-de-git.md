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

```bash
git status
```

Cette commande va vous indiquer l'activité de votre projet. Ce qui est modifié, ajouté et ignoré par GIT.

A tout moment vous pouvez regarder les différences en executant la commande suivante :

```bash
git diff
```

Cette commande va vous indiquer toutes les différences entre la dernière version sauvegardée et l'actuelle, pour l'ensemble des fichiers.

L'affichage précédent peut être difficile à lire, il est donc possible de regarder les différentes pour un fichier précis, en executant la commande suivante :

```bash
git diff /chemin/du/fichier
```

Cette commande va vous indiquer toutes les différences entre la dernière version sauvegardée et l'actuelle, pour le fichier spécifié.

## Ajouter des fichiers ou des répertoires

Certains fichiers sont définis comme "untracked" par GIT, c'est à dire qu'il ne suit pas les modifications. Il faut donc les ajouter, si on souhaite les versionner.

```bash
git add nomfichier1 nomfichier2
```

Cette commande permet de versionner le fichier nomfichier1 et nomfichier2.

Il est aussi possible d'ajouter directement un répertoire.

```bash
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

```bash
git commit
```

Cette commande va sauvegarder tous les fichiers suivis et modifiés. En executant cette commande vous devrez **OBLIGATOIREMENT** indiquer un message pour permettre de comprendre les modifications.



Il peut parfois être intéressant de ne sauvegarder qu'une partie des modifications. Dans ce cas on peut préciser les fichiers

```bash
git commit nomfichier1 nomfichier2
```



On peut également inclure le message directment dans la ligne de commande

```bash
git commit -m "Mon message de suivi de modification"
```

## Utiliser des repository/remote \(push/pull\)

On vient de voir l'intérêt d'utiliser Git. Mais pour le moment tout le suivi de version est stocké sur notre machine. Ce qui limite l'intérêt et ne permet donc pas une réelle sauvegarde de notre travail, ni même un travail collaboratif.

Pour cela, il faut passer par un remote. On peut installer son propre remote assez facilement sur un serveur, ou utiliser une solution existante : GitHub, GitLab, BitBucket, Mercurial, ...

1. Il faut créer un compte sur un gestionnaire de remote \(GitHub par exemple\)
2. Créer son premier dépôt
3. Associer ce dépôt à notre projet local en exécutant la commande ci-dessous :

```bash
git remote add origin https://github.com/user/repo.git
```

La commande ci-dessus est à adapter à votre dépôt. Lors de la création d'un nouveau dépôt sur les remotes, vous avez généralement toutes les instructions.

* `origin` correspond au nom que vous donnez à votre dépôt. C'est le nom par défaut lorsque l'on a qu'un seul dépôt associé.

Il est possible d'associer plusieurs dépôts pour un projet. Il faudra choisir à chaque fois vers lequel vous souhaitez envoyer vos informations.

Pour lister les remotes accessibles vous pouvez exécuter la commande suivante.

```bash
git remote -v
```


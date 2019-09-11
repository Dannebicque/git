# Installation et configuration

## Installation

Pour fonctionner, GIT nécessite la présence d'un petit logiciel sur votre machine.

Il est tout à fait possible d'utiliser GIT sur sa machine, simplement pour le versionning.

[Télécharger GIT : https://git-scm.com/](https://git-scm.com/)

## Configuration

### Configuration de l'utilisateur

Configuration de votre pseudo \(ou nom\), afin de tracer les modifications.

```bash
git config --global user.name "votre_pseudo"
```

Configuration de votre email, également pour tracer les modifications

```bash
git config --global user.email moi@email.com
```

### Configuration "esthétique"



```bash
git config --global color.diff auto
git config --global color.status auto
git config --global color.branch auto
```

Ces instructions permettent de rendre l'usage de la console plus agréable, en ajoutant les couleurs.

## Initialisation dans un nouveau projet

Il faut maintenant activer GIT dans un projet et lui expliquer les éléments qu'il doit surveiller. En effet, il est tout à fait possible de dire à GIT de ne surveiller que certains fichiers. Il est même très souvent nécessaire d'exclure des fichiers de la surveillance \(des fichiers contenant des mots de passe par exemple, ou des éléments téléchargés par les utilisateurs\)

Pour cela placez vous dans un projet et exécutez la commande suivante pour initialiser GIT

```bash
git init
```

Cette commande va créer un répertoire \(`.git`\) et des fichiers cachés qui contiendront l'historique de votre projet.

## Récupérer un projet déjà existant

Lorsque l'on souhaite repartir d'un projet déjà existant et versionné, il est possible de cloner un dépôt depuis un repository \(distant ou local\).

```bash
git clone http://github.com/symfony/symfony.git
```

Cette commande télécharger, depuis un repository sur GitHub \(dans cet exemple\), les sources d'un projet nommé Symfony. Un nouveau repertoire sera créé à l'emplacement ou vous exécutez la commande.


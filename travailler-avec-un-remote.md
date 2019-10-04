# Travailler avec un remote

## Envoyer

Un remote permet de sauvegarder \(et de partager\) des commits avec l'ensemble des développeurs d'un projet.

```bash
git push origin master
```

* Origin désigne le remote par défaut sur lequel sera envoyé le code. Il correspond au clone fait précédemment. 
* Master représente la "Branch" sur laquelle le code est envoyé.

## Récupérer

Pour récupérer toutes les mises à jour depuis le remote :

```bash
git pull origin master
```

* Origin désigne le remote par défaut sur lequel sera envoyé le code. Il correspond au clone fait précédemment. 
* Master représente la "Branch" sur laquelle le code est envoyé.

## Résolution de conflit

L'envoi ou la récupération des modifications peuvent provoquer des conflits entre votre code et le code distant ou inversement. Dans ce cas il faut régler les conflits en fusionnant les deux sources \(distant et local\), et en choisissant pour chaque fichier problématique lequel garder. Cela ne se produit que si les développeurs ont modifier des endroits similaire d'un fichier.


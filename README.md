# Outil de génération et de vérification d'une phrase ménomique BIP39 avec des dés

Ce dépôt contient une application Web hors ligne pour générer et vérifier une phrase ménomique BIP39 à partir de lancers de dés. Les phrases BIP39 sont utilisées pour représenter de manière lisible une entropie cryptographique, notamment pour les portefeuilles Bitcoin. Cet outil propose une approche manuelle où chaque bit de l'entropie est déterminé par un lancer de dé physique.

## Avertissement de sécurité

⚠️ Ce dépôt **n’a pas encore fait l’objet d’un audit de sécurité indépendant**.
N’utilisez pas cet outil pour la conservation de longue durée ni pour protéger de grosses sommes tant qu’un audit n’a pas été réalisé.

## Fonctionnement

L'application affiche une interface minimaliste permettant de :

* Choisir la longueur de la phrase (12, 15, 18, 21 ou 24 mots).
* Lancer un dé et saisir les résultats en cliquant sur les boutons 1 à 6 : les lancers 1, 3 et 5 sont interprétés comme **1**, les lancers 2, 4 et 6 comme **0**.
* Chaque groupe de 11 bits est converti en un mot de la liste BIP39 anglaise.
* Pour le dernier mot, l'outil calcule automatiquement le bit de somme de contrôle via SHA ‑26 conformément à la spécification BIP39.
* Construire une phrase complète en enchaînant les mots et copier la phrase finale en un clic.

Toutes les opérations se font localement dans le navigateur, sans dépendances externes ni envoi de données.

## Utilisation

1. Clonez ou téléchargez ce dépôt.
2. Ouvrez le fichier **index.html** dans un navigateur moderne.
3. Sélectionnez le nombre de mots souhaité.
4. Utilisez les boutons pour saisir vos lancers de dés successifs.
5. Ajoutez chaque mot généré à la phrase jusqu'à atteindre la longueur souhaitée.
6. Copiez la phrase finale et conservez‑la en lieu sûr.

## Déploiement sur GitHub Pages

Le site peut être publié via GitHub Pages pour un accès plus simple :
1. Allez dans *Settings > Pages* de ce dépôt.
2. Choisissez la branche `main` et le dossier racine (`/`) comme source.
3. Enregistrez. GitHub générera une URL publique du type `https://<utilisateur>.github.io/bip39-dice-tool/`.

## Licence

Ce projet est diffusé sous licence MIT. Consultez le fichier **LICENSE** pour plus de détails.

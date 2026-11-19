# Dragon Quest IV, V et VI (Android) : patch français

`DQ_Patch_FR.exe` est un outil pour Windows qui met en français les versions Android (Google Play) de Dragon Quest IV, V et VI.

Il lit le français officiel dans la ROM DS européenne de chaque jeu. Les textes propres à la version mobile sont traduits par le patch. Le jeu patché est ensuite installé sur le téléphone par USB.

## Contenu

| Élément | Rôle |
|---|---|
| `DQ_Patch_FR.exe` | L'outil |
| `readme.txt` | Mode d'emploi complet |
| `roms/` | Dossier prévu pour vos ROM DS (`.nds`, ou `.zip` qui les contient) |
| `dépendances/` | Rempli par l'outil : l'outil installé, les réglages, le journal et les programmes téléchargés |
| `jeux/DQ4/`, `jeux/DQ5/`, `jeux/DQ6/` | Remplis par l'outil, un dossier par jeu : `apks`, `textes`, `fabrication`, `patched_apks`, `ecran_titre`, `signes`, `saves` |

Les dossiers vides contiennent seulement un fichier `.gitkeep`, qui sert à les garder dans le dépôt.

## Ce qu'il faut

- Le jeu (IV, V ou VI), installé depuis le Google Play Store sur un téléphone Android.
- La ROM DS européenne du même jeu, copiée depuis votre propre cartouche :

| Jeu | ROM DS européenne | Code |
|---|---|---|
| Dragon Quest IV | Dragon Quest : L'Épopée des Élus | NTR-YIVP-EUR |
| Dragon Quest V | Dragon Quest : La Fiancée céleste | NTR-YV5P-EUR |
| Dragon Quest VI | Dragon Quest VI : Le Royaume des songes | NTR-YVIP-EUR |

- Un PC sous Windows 10 ou 11, avec environ 3 Go d'espace libre.
- Un câble USB qui transfère les données, et le débogage USB activé sur le téléphone.
- Une connexion Internet au premier lancement, pour télécharger les programmes nécessaires (adb, Java portable, uber-apk-signer). Rien n'est installé dans Windows.

## Utilisation

1. Téléchargez le dépôt (bouton **Code**, puis **Download ZIP**) et décompressez-le dans un dossier à vous, pas dans « Program Files ».
2. Copiez vos ROM DS dans `roms`.
3. Lancez `DQ_Patch_FR.exe`. Au premier lancement, il s'installe dans `dépendances`, puis il propose de télécharger les programmes qui manquent.
4. Cliquez sur « Choisir le dossier des ROM... » et choisissez `roms`.
5. Suivez les étapes de l'onglet du jeu : 1 (copie du jeu depuis le téléphone), 2 (création des textes), 3 (fabrication), 4 (installation).

Le détail de chaque étape, les options et le dépannage sont dans `readme.txt` et dans le menu Aide de l'outil.

## Mise à jour

Fermez l'outil, remplacez `DQ_Patch_FR.exe` par la nouvelle version dans le même dossier, puis relancez-le. Les réglages, les programmes téléchargés et le dossier `jeux` sont gardés.

## Ce que l'outil ne contient pas

L'outil ne contient aucune ROM, aucun fichier du jeu et aucun texte officiel : tout est lu sur votre ordinateur, dans votre ROM et votre jeu. Ne partagez pas vos ROM, les APK fabriqués ni le fichier des textes créé par l'outil.

## Mentions

Projet non officiel, sans lien avec Square Enix, Armor Project, Bird Studio, ArtePiazza, Nintendo ni Google. DRAGON QUEST est une marque de Square Enix.

L'outil est fourni tel quel, sans garantie, pour un usage personnel, avec des jeux et des cartouches que vous possédez légalement.

Programmes téléchargés par l'outil, chacun sous sa propre licence : SDK Platform-Tools (Google), Java Temurin (Eclipse Adoptium), uber-apk-signer (licence Apache 2.0).

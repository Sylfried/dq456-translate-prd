=====================================================================
  DRAGON QUEST IV, V et VI (Android)
  PATCH FRANCAIS NON OFFICIEL - outil DQ_Patch_FR.exe, version 1.26
=====================================================================

SOMMAIRE
   1. Presentation
   2. Ce qu'il vous faut
   3. Installer l'outil
   4. La langue de l'outil
   5. Preparer le telephone
   6. Mettre le jeu en francais, pas a pas
   7. Vos sauvegardes
   8. L'option "Ecran titre FR"
   9. Modifier les textes du jeu (facultatif)
  10. Les dossiers crees par l'outil
  11. Mettre a jour l'outil
  12. Contribuer : traduire l'outil
  13. Contribuer : proposer vos traductions des jeux
  14. Bon a savoir
  15. Depannage
  16. Limites connues et reste a faire
  17. Contact
  18. Mentions


1. PRESENTATION
---------------
Les versions Android (Google Play) de Dragon Quest IV, V et VI n'existent pas en francais. DQ_Patch_FR.exe les
met en francais :
 - la tres grande majorite des textes (dialogues, objets, monstres, sorts, lieux, personnages...) est le francais
   OFFICIEL des versions DS europeennes, lu dans VOTRE ROM DS ;
 - les textes propres a la version mobile (menus tactiles, sauvegarde, ajouts) sont traduits par le patch ;
 - le clavier de saisie des noms est traduit (Maj. / Suppr. / OK) et, en option, le logo et l'ecran titre.

L'outil ne contient aucune ROM, aucun fichier du jeu et aucun texte officiel : tout est lu sur VOTRE ordinateur,
dans VOTRE ROM et VOTRE jeu. Ne partagez jamais votre ROM, les APK fabriques ni le fichier des textes cree par
l'outil (il contient le texte de votre ROM).

L'interface de l'outil existe en plusieurs langues (section 4). Le jeu, lui, est mis en francais.

Un seul fichier, un onglet par jeu :
  Dragon Quest IV   ROM DS europeenne "Dragon Quest : L'Epopee des Elus"            (code NTR-YIVP-EUR)
  Dragon Quest V    ROM DS europeenne "Dragon Quest : La Fiancee celeste"           (code NTR-YV5P-EUR)
  Dragon Quest VI   ROM DS europeenne "Dragon Quest VI : Le Royaume des songes"     (code NTR-YVIP-EUR)
La ROM europeenne est la meme dans tous les pays d'Europe : elle contient l'anglais, le francais, l'allemand,
l'espagnol et l'italien.

C'est une version beta : merci de signaler tout probleme (section 17).


2. CE QU'IL VOUS FAUT
---------------------
 - Le jeu (IV, V ou VI) installe depuis le Google Play Store sur votre telephone Android.
 - La ROM DS EUROPEENNE du meme jeu (fichier .nds, ou .zip qui le contient), copiee depuis votre propre
   cartouche. Seule la version europeenne convient : c'est elle qui contient le francais.
 - Un PC sous Windows 10 ou 11 avec environ 3 Go d'espace libre (et 1 a 2 Go de memoire libre pour l'option
   "Ecran titre FR").
 - Un cable USB qui transfere les donnees (pas seulement la charge).
 - Une connexion Internet au premier lancement, pour telecharger les programmes necessaires (section 3).


3. INSTALLER L'OUTIL
--------------------
 1. Placez DQ_Patch_FR.exe dans un dossier a vous (par exemple Documents\DQ_Patch_FR), pas dans "Program Files".
    L'outil range tout a cote de lui (section 10).
 2. Lancez-le (un seul double-clic suffit : s'il est deja ouvert, sa fenetre est simplement remise devant).
    Au premier lancement (et apres chaque nouvelle version), une petite fenetre "installation de l'outil" s'affiche
    quelques secondes : l'outil s'installe dans le dossier "dependances" a cote de lui. Ensuite, il s'ouvre aussitot.
    - Si Windows affiche "Windows a protege votre ordinateur" : "Informations complementaires" puis "Executer quand
      meme" (l'outil n'est pas signe numeriquement).
    - Si votre antivirus le bloque, le supprime ou l'empeche de s'ouvrir : c'est un faux positif frequent des
      programmes de ce type ; ajoutez une exclusion pour son dossier (Avast : Menu > Parametres > General >
      Exceptions ; Windows : Securite Windows > Protection contre les virus et menaces > Gerer les parametres >
      Exclusions).
 3. Au premier lancement, l'outil verifie les programmes dont il a besoin. S'il en manque, une fenetre vous demande
    une seule fois l'autorisation de les telecharger, puis il les telecharge tous automatiquement :
      SDK Platform-Tools (adb)    dialogue avec le telephone par USB (Google, environ 10 Mo)      indispensable
      Java portable (Temurin)     fait fonctionner l'outil de signature (environ 45 Mo)           indispensable
                                  (le Java deja installe sur le PC est utilise s'il est assez recent)
      uber-apk-signer             signe le jeu en francais pour pouvoir l'installer (1 Mo)        indispensable
      Modules de l'ecran titre    seulement pour l'option "Ecran titre FR" (environ 25 Mo)        facultatif
                                  (deja integres dans la plupart des cas)
    Ce sont des versions portables, rangees dans le dossier "dependances" de l'outil : RIEN n'est installe dans
    Windows. Le menu "Dependances" les liste avec leur etat (a quoi sert chacun, ou il est range) et permet de les
    telecharger plus tard si vous avez refuse, ou de les reinstaller ("Tout reinstaller...").
 4. Dans la zone "Verifications", cliquez sur "Choisir le dossier des ROM..." et choisissez le dossier qui contient
    vos ROM DS. Le meme dossier sert pour les 3 jeux : l'outil y trouve tout seul la ROM de chaque jeu.


4. LA LANGUE DE L'OUTIL
-----------------------
Le menu "Langue (Language)" choisit la langue des fenetres, des messages, du journal et de l'aide de l'outil :
 - "Langue du systeme" (choix par defaut) : la langue de Windows si l'outil la connait, sinon l'anglais ;
 - Francais, English, Deutsch, Espanol, Italiano, japonais, chinois simplifie, chinois traditionnel, coreen ;
 - les langues que vous avez ajoutees vous-meme (section 12) ;
 - "Autre" : interface en anglais.
Apres un changement, l'outil propose de redemarrer. Le choix est garde dans dependances\dq_patch_outil.json.
Le menu donne aussi acces au classeur Excel de tous les textes de l'outil (section 12).
Attention : la langue choisie ici ne change que l'outil. Le jeu, lui, est mis en francais.


5. PREPARER LE TELEPHONE
------------------------
 1. Activez les options pour les developpeurs : Parametres > A propos du telephone > touchez 7 fois "Numero de build"
    (l'emplacement exact varie selon les marques).
 2. Dans Parametres > Options pour les developpeurs, activez "Debogage USB".
 3. Branchez le telephone au PC. Sur le telephone, acceptez la demande "Autoriser le debogage USB ?" (cochez
    "Toujours autoriser depuis cet ordinateur"). Si on vous le demande, choisissez le mode "Transfert de fichiers".
 4. Dans le Play Store, desactivez les mises a jour automatiques du jeu : une mise a jour remplacerait la version
    francaise (section 14).
La ligne "Telephone" de la zone "Verifications" devient verte quand tout est pret.


6. METTRE LE JEU EN FRANCAIS, PAS A PAS
---------------------------------------
Choisissez l'onglet du jeu. A gauche, la zone "Verifications" montre ce qui est pret (point vert) ou a regler
(point rouge), et la ligne "A faire ensuite" dit ce qu'il faut lancer maintenant. A droite, les 4 etapes se lancent
a la main, dans l'ordre. Un bouton reste grise tant que l'etape n'est pas possible (survolez-le : une bulle explique
pourquoi). L'icone a droite de chaque bouton indique si l'etape est faite (coche verte), pas encore faite ou a
relancer (croix rouge), ou a verifier (triangle orange). Le "Journal", en bas, raconte tout ce que fait l'outil.

  Etape 1 - Extraire les APK d'origine            (telephone branche, jeu d'origine installe)
            Copie le jeu installe sur le telephone vers le PC (dossier "apks"). A faire une seule fois.
  Etape 2 - Preparer les textes                   (ROM choisie ; le telephone n'est pas necessaire)
            Lit votre ROM et le jeu, applique toutes les regles du patch et ecrit TOUS les textes du jeu dans le
            fichier "textes\DQx_textes_du_jeu.json". Dure plusieurs minutes.
  Etape 3 - Patcher les APK                       (le telephone n'est pas necessaire)
            Fabrique la version francaise avec les textes de ce fichier (dossier "patched_apks"). Rapide.
            A relancer apres chaque modification du fichier des textes. A droite du bouton : l'option
            "Ecran titre FR" (section 8).
  Sauvegardes - "Extraire les sauvegardes"        (recommande AVANT l'etape 4)
            L'etape 4 desinstalle le jeu d'origine, ce qui efface ses sauvegardes locales : extrayez-les avant
            (section 7).
  Etape 4 - Signer et installer                   (telephone branche)
            Signe la version francaise, desinstalle le jeu d'origine (apres confirmation) puis installe la version
            francaise. Si vous n'avez jamais extrait vos sauvegardes, l'outil propose de le faire ; sinon, il vous
            rappelle la date de votre dernier backup avant de continuer.
            PENDANT L'INSTALLATION, REGARDEZ LE TELEPHONE : si Google Play Protect propose d'envoyer l'application
            pour analyse, touchez "Ne pas envoyer". S'il la bloque : "Plus de details" puis "Installer quand meme".
  Sauvegardes - "Restaurer les sauvegardes"        (APRES l'etape 4)
            Lancez une fois le jeu en francais, fermez-le completement, puis cliquez sur ce bouton pour remettre
            vos sauvegardes. Elles apparaissent ensuite dans "Poursuivre votre aventure".

C'est fini : le jeu est en francais. Pour un autre jeu, passez a son onglet et recommencez.


7. VOS SAUVEGARDES
------------------
 - Le jeu en francais porte une autre signature que celui du Play Store : Android oblige a desinstaller l'original,
   ce qui efface ses sauvegardes LOCALES (fichiers data*.dat).
 - "Extraire les sauvegardes" les copie dans "jeux\DQx\saves\AAAAMMJJ_HHMMSS" (un "backup" par extraction, avec
   verification de la taille des fichiers). Gardez ce dossier precieusement.
 - "Restaurer les sauvegardes" remet sur le telephone le backup de votre choix (le plus recent est preselectionne).
   Les sauvegardes deja presentes sur le telephone sont remplacees par celles du backup choisi.
 - La "Sauvegarde cloud" du jeu NE FONCTIONNE PAS avec la version francaise (elle est liee a la signature du Play
   Store). Utilisez ces deux boutons a la place.


8. L'OPTION "ECRAN TITRE FR"
----------------------------
 - C'est la case a cocher "Ecran titre FR", a droite du bouton de l'etape 3 : cochee = activee, decochee =
   desactivee. Elle est grisee tant que l'etape 3 n'est pas disponible.
 - Activee, elle traduit aussi le sous-titre du logo (par exemple "La Fiancee celeste" a la place de "Hand of the
   Heavenly Bride") et "Tap to Start" ("Touchez l'ecran"), avec des images redessinees en haute definition,
   integrees a l'outil.
 - La premiere etape 3 avec l'option dure plusieurs minutes et demande 1 a 2 Go de memoire ; le resultat est garde
   dans "jeux\DQx\ecran_titre", les fois suivantes sont rapides.
 - Apres un changement de l'option, relancez les etapes 3 et 4.
 - Si le jeu plante au demarrage, desactivez-la et relancez les etapes 3 et 4.


9. MODIFIER LES TEXTES DU JEU (FACULTATIF)
------------------------------------------
L'etape 2 ecrit TOUS les textes du jeu, tels que le patch les met, dans "jeux\DQx\textes\DQx_textes_du_jeu.json"
(menu Fichier > "Ouvrir le dossier des textes de DQx"). Vous pouvez y corriger un texte puis relancer les etapes 3
et 4. Le detail complet est aussi dans l'outil : menu Aide > "Comment modifier les textes".

  Avant de modifier
   - Faites une COPIE du fichier : c'est votre retour en arriere.
   - Ouvrez-le avec Notepad++ ou VS Code (gratuits), jamais avec Word ou WordPad, et enregistrez-le en UTF-8.
   - Ne modifiez QUE les lignes "texte" ("anglais" et "origine" sont la pour vous aider). Ne supprimez aucune entree
     et ne changez pas les numeros.
  Trouver le bon texte
   - Les textes sont ranges par fichier puis par numero, dans l'ordre du jeu, avec l'anglais en face.
   - Cherchez (Ctrl+F) 3 ou 4 mots qui se suivent, SANS la ponctuation (il y a une espace insecable avant ! ? : ;).
   - Les noms et nombres qui changent (nom du heros, somme d'or...) sont des codes "%a" suivis de 6 chiffres : ne
     les tapez pas dans la recherche.
   - Si la meme replique existe plusieurs fois (deux moments de l'histoire...), corrigez-les toutes.
  Les regles du fichier
   - Le texte est entre guillemets droits : n'appuyez JAMAIS sur Entree a l'interieur, ne supprimez ni ces
     guillemets ni la virgule qui suit. Un guillemet droit dans un texte s'ecrit \" (preferez les guillemets
     francais, que le jeu affiche).
   - Si l'etape 3 signale une erreur "ligne X, colonne Y", allez a cette ligne (Ctrl+G dans Notepad++) : c'est
     presque toujours un guillemet ou une virgule.
  Les codes du jeu : a garder tels quels
   - "%a" + 6 chiffres : nom ou nombre variable (vous pouvez le deplacer dans la phrase).
   - "%H...%X forme 1 %Y forme 2 %Z" (et %A, %B, %G...) : variantes choisies par le jeu (masculin / feminin,
     singulier / pluriel) ; changez les mots entre les codes, jamais les codes.
   - Les lettres russes de certains personnages (accent russe) sont voulues : gardez-les.
  Retours a la ligne et bulles
   - "\n" force un retour a la ligne. La plupart des dialogues n'en ont pas : le jeu les coupe tout seul.
   - Une bulle affiche environ 3 lignes ; un caractere special (a copier depuis un autre texte) passe a une
     nouvelle bulle, un autre marque une courte pause : gardez-les.
   - Dans les menus, ";" marque l'endroit ou le libelle peut passer a la ligne : ne le supprimez pas.
  Apres chaque modification
   - Enregistrez, relancez l'etape 3 puis l'etape 4, et verifiez dans le jeu.
   - Lisez "textes\rapport_etape3.txt" : modifications refusees (le texte d'origine est garde), lignes plus larges
     qu'avant, caracteres absents de la police du jeu.
   - Relancer l'etape 2 propose de garder votre fichier ; s'il est recree, l'ancien est d'abord copie dans
     "textes\anciens".
   - Pour faire profiter tout le monde de vos corrections : section 13.


10. LES DOSSIERS CREES PAR L'OUTIL
----------------------------------
Tout est range a cote de DQ_Patch_FR.exe, dans deux dossiers, nulle part ailleurs :
(le dossier s'appelle "dependances" avec un accent sur le e ; ce fichier est ecrit sans accents)
  dependances\         l'outil lui-meme (installe par DQ_Patch_FR.exe, recree s'il est efface), avec :
      platform-tools\, java\, uber-apk-signer.jar   les programmes telecharges (adb, Java, signature)
      langues\          les textes de l'outil charges depuis un classeur Excel (section 12)
      dq_patch_outil.json   vos reglages (langue, dossier des ROM, option de l'ecran titre)
      journal.txt       le journal de l'outil, commun aux 3 jeux
  jeux\                un dossier par jeu, DQ4\, DQ5\ et DQ6\, qui contient :
      apks\           les APK d'origine copies du telephone (etape 1)
      textes\         DQx_textes_du_jeu.json (etape 2), rapport_etape3.txt, anciens\
      fabrication\    la version francaise de base (etape 2)
      patched_apks\   la version francaise avec vos textes (etape 3)
      ecran_titre\    le logo et "Touchez l'ecran" en francais (option de l'etape 3)
      signes\         les APK prets a installer (etape 4)
      saves\          vos backups de sauvegardes, un dossier par date
Pour desinstaller l'outil, supprimez simplement ce dossier (gardez "jeux\DQx\saves" si vous voulez conserver vos
backups). En se fermant, l'outil arrete tout ce qu'il a lance lui-meme (adb compris) : rien ne reste en
arriere-plan.


11. METTRE A JOUR L'OUTIL
-------------------------
 1. Fermez l'outil.
 2. Remplacez DQ_Patch_FR.exe par la nouvelle version, dans le MEME dossier.
 3. Lancez-le : il s'installe de nouveau dans "dependances" (quelques secondes), puis s'ouvre.
Vos reglages, vos langues ajoutees (dependances\langues), les programmes telecharges et tout le dossier "jeux"
(APK, textes, sauvegardes) sont gardes.
Une nouvelle version contient souvent un nouveau patch des jeux : relancez alors l'etape 2 (gardez votre fichier
des textes si vous l'avez modifie), puis les etapes 3 et 4. "A faire ensuite" vous le rappelle.
Les anciennes versions de l'outil rangeaient tout a cote de l'exe (ou dans "programme") : au premier lancement,
l'outil deplace tout seul ces dossiers dans "dependances" et "jeux".


12. CONTRIBUER : TRADUIRE L'OUTIL
---------------------------------
Tous les textes de l'outil (pas ceux des jeux) tiennent dans un classeur Excel, un onglet par langue.
 1. Menu Langue > "Exporter les textes de l'outil (Excel)..." : l'outil enregistre le classeur avec la derniere
    version de chaque langue (langues integrees et langues que vous avez chargees). Chaque onglet porte le nom
    d'une langue : colonne A = cle de chaque texte, colonne B = texte dans cette langue.
 2. Ouvrez-le avec Excel, Excel Online ou LibreOffice.
    - Ne modifiez pas la colonne A et ne triez pas les lignes.
    - Pour AJOUTER une langue : dupliquez un onglet (l'anglais, par exemple), renommez-le avec le nom de la langue,
      tel qu'il doit apparaitre dans le menu (par exemple Portugues), puis traduisez sa colonne B.
    - Pour CORRIGER une langue (le francais compris) : modifiez les cases de son onglet.
    - Gardez tels quels les {0}, {1}... (ils sont remplaces par un nom, un nombre, une date...), les "\n" (retour a
      la ligne), les ** (texte en gras dans l'aide) et les noms de dossiers ("jeux", "dependances", "saves"...).
    - Une case vide garde l'anglais.
 3. Menu Langue > "Charger les textes de l'outil (Excel)..." : l'outil lit tous les onglets, enregistre chaque
    langue dans dependances\langues et propose de redemarrer. Une nouvelle langue apparait dans le menu Langue.
    Un texte dont les {0}, {1}... ne correspondent pas au francais est refuse (le journal le signale).
Recommencer est sans risque : chaque nouvel export repart de la derniere version chargee.
Pour faire integrer votre traduction a l'outil pour tout le monde, envoyez le classeur (section 17).


13. CONTRIBUER : PROPOSER VOS TRADUCTIONS DES JEUX
-------------------------------------------------
 - Une correction ou une meilleure traduction d'un texte du jeu : corrigez-la dans votre fichier des textes et
   verifiez-la en jeu (section 9), puis envoyez-la (section 17) avec le jeu, la cle du texte (le fichier et le
   numero, par exemple b0502000.mpt, 615) et le texte corrige. Une capture d'ecran aide beaucoup.
 - Ne partagez jamais le fichier des textes lui-meme : il contient le texte de votre ROM.
 - Les plus gros chantiers ouverts (discussions de groupe de DQ IV, descriptions des objets...) sont listes dans
   l'outil : menu Aide > "Reste a faire" (section 16).
 - Patch des jeux dans d'autres langues que le francais : prevu dans une prochaine version (la ROM europeenne
   contient deja l'allemand, l'espagnol et l'italien).


14. BON A SAVOIR
----------------
 - Mises a jour du jeu : desactivez-les dans le Play Store. Une mise a jour remplacerait la version francaise, et une
   nouvelle version du jeu peut demander une nouvelle version du patch.
 - Le patch ajuste aussi deux details du moteur du jeu : un monstre suivi d'une lettre garde son article ("Le Gluant A
   attaque !") et les initiales accentuees passent en majuscule ("Epee de cuivre"). Chaque ajustement n'est fait que
   si le jeu correspond exactement a la version attendue.
 - Au premier lancement, le jeu peut demander de choisir un compte Google (surtout s'il y a plusieurs comptes sur le
   telephone). Ce n'est pas obligatoire : passez l'ecran en touchant a cote, ou avec "Annuler" ou "Continuer".
 - Certains personnages parlent avec un accent russe ecrit avec des lettres speciales (comme sur DS) : c'est voulu.
 - Aide integree : menu Aide (presentation, dossiers et depannage, modifier les textes, reste a faire). En survolant
   un bouton, une zone ou une ligne, une bulle explique ce que c'est.


15. DEPANNAGE
-------------
 - Telephone non detecte ou "non autorise" : cable qui transfere les donnees, mode "Transfert de fichiers", Debogage
   USB active ; debranchez, rebranchez et acceptez l'autorisation sur l'ecran du telephone.
 - ROM introuvable ou "ROM d'une autre region" : seule la ROM europeenne du jeu convient (codes en section 1) ; elle
   doit etre dans le dossier des ROM choisi ou dans un de ses sous-dossiers directs.
 - "APK deja patches" a l'etape 1 : le jeu du telephone est deja en francais. Pour repartir de l'original,
   desinstallez-le, reinstallez-le depuis le Play Store et relancez l'etape 1.
 - Play Protect bloque l'installation : "Plus de details" puis "Installer quand meme".
 - Echec "INSTALL_FAILED_..." a l'etape 4 : copiez le journal (bouton "Copier le journal") et envoyez-le (section 17).
 - Le jeu plante au demarrage avec l'option "Ecran titre FR" : desactivez-la, relancez les etapes 3 et 4.
 - Le jeu s'ouvre en japonais : choisissez l'anglais dans les options du jeu (le francais remplace l'anglais).
 - Erreur "ligne X, colonne Y" a l'etape 3 : le fichier des textes est mal forme a cet endroit (section 9).
 - Un texte deborde d'une fenetre : corrigez-le (section 9) ou signalez-le (section 17).
 - L'outil est dans une langue que vous ne lisez pas : menu "Langue (Language)", le 3e en partant de la gauche.
 - Une langue chargee depuis un classeur pose probleme : supprimez son fichier dans dependances\langues, puis
   relancez l'outil (les textes integres reviennent).
 - Verification de l'outil : lancez "DQ_Patch_FR.exe --selftest" depuis une invite de commandes ; le resultat est
   ecrit dans dependances\selftest.txt.
 - Une etape echoue sans explication claire : bouton "Copier le journal", puis collez-le dans votre message
   (section 17).


16. LIMITES CONNUES ET RESTE A FAIRE
------------------------------------
 - Dragon Quest IV : la version mobile ajoute environ 7 800 repliques de "discussion de groupe" qui n'existent pas
   sur DS. Elles n'ont donc pas de traduction officielle : le patch en contient une premiere traduction, non
   officielle, a reprendre.
 - Quelques messages restent en anglais : ecrans de telechargement et de fermeture de l'application, onomatopees
   identiques en francais (Zzzz, Grrr...).
 - Descriptions des objets : ce sont celles de la DS, souvent vagues et presque identiques entre les objets d'un
   meme type. Des descriptions propres a chaque objet sont recherchees.
 - Interface de l'outil dans une autre langue que le francais : quelques messages techniques restent en francais
   (messages du script de fabrication dans le journal, par exemple).
 - Toutes les remarques sur les textes sont bienvenues : textes qui depassent ou collent aux bords des fenetres,
   fautes de frappe ou d'orthographe, accords faux (il / elle, singulier / pluriel), traductions manquantes ou a
   ameliorer, objet sans la bonne description, dialogue au mauvais endroit (replique qui ne va pas avec la scene
   ou le personnage, repliques dans le desordre), meme texte different d'un jeu a l'autre (description, menu, nom
   d'objet, de sort ou de monstre), meme nom ecrit de deux facons, personnage qui change de facon de parler
   (tutoiement / vouvoiement, accent), mauvais nom affiche, texte qui parle encore de la DS (stylet, boutons...).
La liste a jour est dans l'outil : menu Aide > "Reste a faire".


17. CONTACT
-----------
Remarques, corrections, propositions de traduction (des jeux ou de l'outil), problemes avec l'outil : l'adresse
est dans l'outil, menu Aide > "Reste a faire" (bouton "Copier l'adresse e-mail").
Pour un probleme de texte, indiquez si possible : le jeu, l'endroit (ville, scene, menu), le texte tel qu'il
s'affiche, une capture d'ecran et votre proposition (et, si vous l'avez trouve dans le fichier des textes, son
fichier et son numero). Pour un probleme avec l'outil : bouton "Copier le journal", puis collez-le dans votre message.


18. MENTIONS
------------
Projet de fans, non officiel, sans lien avec Square Enix, Armor Project, Bird Studio, ArtePiazza, Nintendo ni Google.
DRAGON QUEST est une marque de Square Enix. Ce patch est fourni tel quel, sans garantie, pour un usage strictement
personnel, avec des jeux et des cartouches que vous possedez legalement. Les traductions propres au patch et les
traductions de l'interface de l'outil ont ete redigees avec l'aide d'une intelligence artificielle (Claude,
d'Anthropic) et meritent une relecture.
Programmes utilises (telecharges depuis leur site officiel, chacun sous sa propre licence) : SDK Platform-Tools
(Google), Java Temurin (Eclipse Adoptium), uber-apk-signer (Patrick Favre, licence Apache 2.0), UnityPy, Pillow et
numpy (logiciels libres).

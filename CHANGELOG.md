# Journal des versions

Numérotation : X.Y (par exemple 2.0).

## 4.2
- Onglet Soudure : visualisation seulement (pouces à souder et poids total du projet, par ISO, avec répartition atelier/chantier).
- Suivi par spool (avancement par phase, pouces soudés, reste, tout soudé) déplacé dans l'onglet Soudure atelier (SW) et, séparément, dans l'onglet Soudure chantier (FW, avec poids à poser).
- Excel : une page « Atelier (SW) » et une page « Chantier (FW) » (joints, pouces à souder / soudés / reste, avancement, poids du spool).

## 4.1
- Onglets Soudure atelier (SW) / chantier (FW) : choix SW ou FW sur chaque soudure ; passer en FW la fait disparaître de l'onglet SW et l'affiche dans l'onglet FW (et inversement). Bouton « Recopier les joints de l'onglet Soudure » dans l'onglet SW (l'onglet Soudure reste inchangé).

## 4.0
- Lecture du cartouche élargie : le numéro de ligne (ex. 100-V-31-133-6C1-PP, sous « LIGNE N° ») et le numéro de document sont cherchés sur toute la largeur du bas de page, puis en secours sur la page entière.

## 3.9
- Numéro d'iso lu comme DN-SERVICE-…-CLASSE-SYS (ex. 250-SHS-31-130-6C1-HC ou 100-V-31-133-6C1-PP) : service, pipe/class et SYS remplis automatiquement (scan, liste, exports Excel, projets existants). Le numéro de document (AR327-23-06-IS-000x) va dans « Document N° ». Nouveau champ SYS dans le scan ; service sur 1 à 4 lettres.

## 3.8
- Pouces à souder (diamètre-pouces) : estimation par page d'après la liste de matériel (coude 2 soudures, té 3, bride WN/SO 1, olet 1, fond 1, réduction 2, vanne à souder 2 ; bride pleine et pièces filetées 0). Utile pour les isométriques sans repères de spool.

## 3.7
Regroupe tous les changements depuis 3.6 (versions internes ci-dessous). Prochaine version : 3.8.

### 4.2
- Nouveau style d'isométrique : repères de spool SP01, SP02… (cadre rouge, texte vert, flèche rouge), points noirs = soudures atelier (SW), croix orange = soudures chantier (FW). Détection automatique, rattachement des soudures à leur spool (FW douteuse : spool le plus petit), numérotation des soudures par spool.
- Numérotation des versions : 3.6, 3.7, 3.8…

### 4.1.1
- ND lu automatiquement dans la colonne ND de la liste en DN (20, 150, 150x20 → 3/4", 6", 6"x3/4"). Si illisible : ND de la ligne (début du nom de ligne, ex. 150-CS-…), signalé à vérifier.
- Les supports de tuyauterie (PIPE SUPPORTS) sont ignorés : sans effet sur les poids.

### 4.1.0
- Suppression du bouton IA de calcul des spools (non disponible sur GitHub). Méthode sans IA : règles de calcul (cotes à l'axe, encombrements) appliquées par l'application.

### 4.0.2
- Leçon corrigée : cotes à l'axe du coude/té, à la face de la bride WN ; exemples SP01 et SP02 (page 3/7).

### 4.0.1
- Leçon spool SP01 (page 3/7) intégrée à l'IA : points = SW, croix X = FW (limites), té et bride WN déduits.

### 4.0.0
- Bouton « ✦ Calculer les spools automatiquement (IA) » par page : l'IA lit le dessin (liste, cotes, extrémités), répartit pièces et tubes par spool, avec cotes en expression et extrémités (bride SO, coude SW, piquage…). Résultat à vérifier ligne par ligne. Disponible uniquement dans la version ouverte depuis claude.ai (pas sur GitHub).

### 3.9.0
- Poids et peinture par spool : bouton « Répartir par spool » sur chaque ligne de la liste (tube ou accessoire) : une ligne par spool de la page, avec rappel du total de la liste, du réparti et du reste. Avertissement avant d'ajouter des lignes sans spool.

### 3.8.0
- Revue du scan : tampons triés par numéro de soudure (SW1, SW2, FW3, SW4…), spools en tête.
- Liste de matériel : classe de bride lue correctement (3000# n'était plus pris pour 300#), vanne XV (type boisseau), boulonnerie (tiges + écrous → jeux de boulons selon la bride).
- Bouton ✦ « Commande » : demande en langage courant (ex. « ne pas calculer la peinture des inox », « pas de peinture pour ISO-003 »). Règles de peinture sauvegardées avec le projet. Avec l'IA Claude (version publiée sur claude.ai) : aussi schedule, classe, matériau ; hors ligne / GitHub : règles locales (peinture).

### 3.7.1
- Spools : un tronçon de tuyau séparé du reste par un trou du dessin (cartouche, repère) reprend le spool du tronçon voisin le plus proche (≤ 60 px), signalé en orange. Corrige SW4 sans spool (ISO 14/40). Soudure FW douteuse : repère du spool inférieur.

### 3.7.0
- Lecture des numéros manuscrits réentraînée sur 27 pages relues à l'œil (≈360 tampons) : chiffres décrits sur 14×14 au lieu de 6×6, nouveau réseau, nouveau classement SW/FW. Numéros justes sur des pages jamais vues : 72 % → 85 %. Données d'apprentissage et scripts dans le dossier apprentissage/.

### 3.6.6
- Icône et en-tête en rouge pour distinguer cette version (avec scan) de l'application sans scan.

### 3.6.5
- Soudure FW située entre plusieurs spools : le scan retient le repère du spool inférieur (entre 2, 3 et 4 → 2), signalé en orange.

### 3.6.4
- Longueur des tubes par spool : cotes en expression (=125+125), répartition d'un tube sur plusieurs spools, extrémités Bride SO (épaisseur), Coude forgé SW (cote A de la base B16.11) et Piquage sur tube (demi-Ø du ND principal), longueur nette affichée.

### 3.6.3
- Les pastilles de joints (S1, S2…) deviennent J1, J2… pour ne plus être confondues avec les spools. Scan : si l'isométrique ne porte qu'un seul tampon Spool, toutes ses lignes reçoivent ce numéro. Champ spool vide affiché « — ».

### 3.6.2
- Nouvelle icône (scanner + coude). Confirmation avant toute suppression (soudure, ligne, liste, projet). Repères de spool dans les onglets SW/FW (regroupement par spool, champ Spool à l'ajout). Paramètres isométrique : révision et code lus sur le cartouche, bouton pour copier vers les autres ISO.

### 3.7 (version sans scan, autre dépôt)
- Le scanner devient une application indépendante (« Scanner isométrique »). Ici : l'icône 📷 importe le fichier .json exporté par le scanner (lignes → Assemblage, soudures → onglets SW / FW). Code de lecture retiré (application plus légère).

## 3.6.1 (scan + spools)
- Rattachement des soudures aux spools par la géométrie du dessin ; champ Spool modifiable par soudure, colonne Spool dans l'Excel et le .json.

## 3.6
- Scanner : le type SW/FW ne dépend plus de la forme du tampon (estimation à vérifier) ; boutons « + Spool / + SW / + FW » pour les marques écrites à la main ; aperçu de la page scannée.

## 3.5
- Scanner : lecture des tampons du dessin (cases Spool, soudures SW atelier et FW chantier) avec vignette, numéro manuscrit lu et contrôle de numérotation.
- Nouveaux onglets « Soudure atelier (SW) » et « Soudure chantier (FW) » : suivi réalisées / à souder, diamètres, pouces ; export Excel.

## 3.4
- Nouveau : icône « Scanner un isométrique » (PDF scanné ou photo). Lecture du cartouche (document, ligne, service, pipe class) et de la liste de matériel (désignation, ND, quantité), écran de contrôle modifiable, ajout au projet. Les numéros de spool manuscrits se saisissent à la main. Nécessite internet (OCR chargé à la demande).

## 3.3
- Filigrane Excel horizontal (plus en diagonale) et répété 2 fois pour couvrir toute la largeur du tableau.

## 3.2
- Filigrane Excel placé sous le tableau (plus jamais au-dessus des chiffres), pour garder les valeurs lisibles.

## 3.1
- Filigrane Excel plus discret : plus petit et plus transparent.

## 3.0
- Excel : la ligne de signature est remplacée par un filigrane en diagonale (« Créé par KAMEL NASRALLI », normes ASME et numéro de version) sur chaque feuille. Le filigrane est verrouillé par la protection des feuilles et s'imprime. Le pied de page d'impression est conservé.

## 2.9
- Excel : la ligne de signature est verrouillée (feuilles protégées par mot de passe). Toutes les autres cellules restent modifiables (saisie, tri, filtres, insertion de lignes et de colonnes).

## 2.8
- Excel : la signature « Créé par KAMEL NASRALLI · ASME B36.10M / B36.19M · ASME B16.9 · B16.5 · kg · Version X.Y » est imprimée en bas de chaque feuille et dans le pied de page d'impression (avec le numéro de page).

## 2.7
- Onglet Assemblage : chaque ligne affiche en couleur vive les repères de soudure qu'elle génère (S1, S2… ou S1 à S9), avec leur nombre et leur diamètre, dans la même numérotation que l'onglet Soudure.

## 2.6
- Pouces à souder d'un spool = somme des diamètres de chaque soudure (ex. 10 + 10 + 10 + 0,5 + 0,5 = 31 po), au lieu de diamètre principal × joints. Répercuté dans Soudure, Rapport par spool, Excel et CSV.

## 2.5
- Soudure, détail des soudures : chaque soudure prend le diamètre de la pièce correspondante dans Assemblage (par exemple 0,75 po pour un piquage ¾" sur un tube de 10"), au lieu du seul diamètre principal. Les pouces soudés sont la somme des diamètres cochés ; tout coché = 100 %.

## 2.4
- Onglet Soudure : détail des soudures par spool (S1, S2, S3… selon le nombre de joints), chacune avec son diamètre ; cocher une soudure = terminée à 100 %. Les pouces soudés, l'avancement et l'Excel suivent automatiquement. La saisie manuelle et « Tout soudé » restent disponibles.

## 2.3
- Aide : l'onglet Information a sa propre rubrique (titre bleu), placée juste après « Principe » ; rubriques renumérotées.

## 2.2
- Aide, « Démarrer » : le réglage des paramètres isométrique passe en étape 2, avant l'ajout des pièces.

## 2.1
- Aide : nouvelle rubrique « Un problème ? Une erreur ? » (décrire l'erreur, joindre une capture d'écran) avec un bouton « Écrire un email » vers ktopnet@gmail.com, objet et corps pré-remplis.

## 2.0
- Numérotation des versions simplifiée : un seul chiffre après le point (2.0, 2.1…). Regroupe les évolutions 1.20.x : thème moderne, anneau de répartition, FR / EN, aide, thème clair / sombre, onglets Assemblage et Information, schémas réalistes.

## 1.20.9
- Icône soleil / lune dans l'en-tête pour basculer entre thème clair et sombre (choix mémorisé ; par défaut le thème de l'appareil).

## 1.20.8
- Onglet Information : le tableau « Schedules disponibles » n'affiche plus la colonne des poids (kg/m) pour les accessoires ; elle reste pour les tubes.

## 1.20.7
- Schémas des accessoires (coudes, tés, réductions, fonds, brides, raccords forgés, piquages, boulonnerie) : même rendu réaliste que les vannes, clair et sombre ; cotes inchangées.

## 1.20.6
- Schémas de vannes : rendu réaliste (corps métallique dégradé, volant rouge, ombres, fond clair) ; les cotes restent calculées par DN et classe.

## 1.20.5
- L'onglet « Fiche » devient « Information » ; ses champs Quantité, ISO, N° spool, poids unitaire imposé, surface imposée et joints imposés sont supprimés (ils se saisissent dans Assemblage).

## 1.20.4
- Aide : on commence par l'onglet Assemblage ; la Fiche est présentée comme information.

## 1.20.3
- Les paramètres isométrique ne sont plus dans l'onglet Fiche ; ils se renseignent uniquement dans l'onglet Assemblage.

## 1.20.2
- Icône d'aide « ? » dans l'en-tête : guide d'utilisation en français et en anglais (fenêtre, fermeture par × ou Échap).

## 1.20.1
- L'onglet « Liste » est renommé « Assemblage » (« Assembly » en anglais).

## 1.20.0
- Thème plus moderne : bandeau d'en-tête dégradé, onglets en pastilles, cartes arrondies avec ombres, boutons et totaux en dégradé.
- Nouveaux graphiques : anneau (tubes / accessoires / brides) avec légende et pourcentages, barres empilées par ISO.
- Bouton globe FR / EN dans l'en-tête : interface, messages et en-têtes / noms de feuilles / statuts de l'Excel traduits (les données saisies ne sont jamais traduites). Langue mémorisée.

## 1.19.1
- Zones de filtres (Liste, Rapport par spool, Soudure) : fond bleu et bordure marquée, avec cases plus foncées, pour les repérer d'un coup d'œil (clair et sombre).

## 1.19.0
- Onglet « Liste » : filtres par ISO, spool, catégorie et recherche libre (désignation, ISO, spool, matériau), avec compteur « n lignes sur N » et bouton « Tout afficher ». Les totaux suivent le filtre ; les exports restent complets.

## 1.18.1
- Onglet « Soudure » : les pouces soudés ne peuvent plus dépasser les pouces à souder du spool (la valeur est ramenée au maximum, avec un message).
- Onglet « Rapport par spool » : filtre par isométrique (spools et totaux filtrés ; les exports restent complets).

## 1.18.0
- Onglet « Soudure » : avancement des autres tâches par spool (sortie matériel, débitage / assemblage, NDT, inspection, peinture / passivation, livraison site) en paliers 0 / 25 / 50 / 75 / 100 %, avec l'avancement global du spool. Sortie matériel et débitage passent à 100 % (verrouillés) au-delà de 10 % de soudage.
- Excel « Suivi des travaux » et « Tableau d'avancement » : ces avancements sont repris dans les colonnes correspondantes.
- Barre d'onglets plus compacte sur téléphone.

## 1.17.1
- Excel : dès que « Pointage / Soudage » dépasse 10 %, « Sortie matériel » et « Débitage / Assemblage » passent automatiquement à 100 % (feuilles « Suivi des travaux » et « Tableau d'avancement »).

## 1.17.0
- Nouvel onglet « Soudure » : liste des spools avec filtres (ISO, recherche de spool, état À souder / En cours / Soudés), pouces à souder de chaque spool et case « Pouces soudés » à saisir à la main (bouton « Tout soudé »), reste et totaux. Les valeurs sont enregistrées avec le projet et reprises dans le Tableau de Bord Excel (colonne « Pouces soudés » ; pointage / soudage = soudés ÷ à souder).

## 1.16.8
- Excel « Suivi des travaux » : formules rendues compatibles avec les anciens tableurs (LibreOffice Android, etc.) : plus de IFERROR ni de SUBTOTAL(109), ce qui supprimait les erreurs #NOM? et Err:502.

## 1.16.7
- Excel : les paramètres isométrique (code artc, document N°, rev iso, soumission, service, pipe / class, SYS) sont aussi ajoutés aux feuilles « Par ISO » et « Détail », juste après l'ISO (ils figuraient déjà dans « Suivi des travaux » et « Tableau d'avancement »).

## 1.16.6
- Correction : les paramètres isométrique saisis avant le nom de l'ISO (dans une ligne de la liste) disparaissaient dès qu'on modifiait un autre champ. Ils suivent maintenant le nom de l'ISO au fur et à mesure de la saisie.

## 1.16.5
- Paramètres isométrique : le bloc reste ouvert quand on remplit le reste du formulaire (il se refermait à chaque changement de liste déroulante). Dans la fiche, les champs se remplissent avec les valeurs déjà connues dès qu'on saisit un ISO existant.

## 1.16.4
- Suppression d'une ligne : confirmation en deux temps (le bouton devient « Confirmer la suppression » pendant 4 secondes), comme pour « Vider la liste ».

## 1.16.3
- Extrémités de tube : ajout de « Té (passage) » (encombrement = cote C ASME B16.9) et « Réduction » (encombrement = longueur H ASME B16.9). Chaque extrémité raccordée compte toujours 1 joint à souder ; l'encombrement imposé reste possible.

## 1.16.2
- Paramètres isométrique : bloc placé en premier (avant ISO et N° spool) dans la liste et dans la fiche de saisie, avec des cases au fond plus foncé (clair et sombre). Dans la fiche, les valeurs saisies avant le nom de l'ISO sont enregistrées avec la ligne ajoutée.

## 1.16.1
- Liste : les paramètres isométrique (code artc, document N°, rev iso, soumission, service, pipe / class, SYS) passent en haut de chaque ligne, dans un bloc repliable fermé par défaut, pour gagner de la place. Le titre du bloc rappelle les valeurs déjà saisies.

## 1.16.0
- Onglet « Suivi » supprimé de l'application.
- Feuille Excel « Suivi des travaux » avec formules : « Pouces soudés » et les phases se saisissent dans Excel ; Pointage / Soudage = pouces soudés ÷ pouces à souder (100 % quand ils sont égaux) ; Avancement = somme des phases × pondérations (ligne modifiable) ; Poids fabriqué = avancement × poids ; Statut automatique (Non commencé / En cours / Terminé) ; indicateurs et totaux recalculés. Barres de progression et couleurs de statut conservées.

## 1.15.2
- Feuille Excel « Suivi des travaux » : ajout des colonnes Code artc, Document N°, Rev iso, Soumission, Service, Pipe / class et SYS, dans l'ordre exact du Tableau de Bord (Code artc, Document N°, ISO, Rev iso, … , DN, joints, pouces à souder, spool, …). Les trois premières colonnes restent figées.

## 1.15.1
- Code artc, Document N°, Rev iso, Soumission, Service, Pipe / class et SYS ajoutés directement dans chaque ligne de la liste et dans chaque carte de l'onglet Suivi (« Données ISO »). Ils sont partagés par toutes les lignes du même ISO.

## 1.15.0
- « Joints à souder imposés » : valeur par défaut 1 pour toute nouvelle ligne (vider la case pour revenir au calcul automatique).
- Données par ISO dans l'application (code artc, document N°, rev iso, soumission, service, pipe / class, SYS), dans l'ordre des colonnes du Tableau de Bord ; une case vide reprend la valeur d'en-tête. Elles sont enregistrées avec le projet et reprises ligne par ligne dans le Tableau de Bord Excel.
- Pouces à souder d'un spool = diamètre principal × nombre de joints, calculé automatiquement (appli, Suivi, Excel).

## 1.14.2
- Feuille « Suivi des travaux » : ajout des colonnes « Longueur axe-axe (mm) » et « Surface peinture (m²) » juste après « Poids (kg) », avec leurs totaux.

## 1.14.1
- Feuille « Suivi des travaux » : colonnes réordonnées selon l'ordre du Tableau de Bord (ISO, DN, joints à souder, pouces à souder, spool, pouces soudés, poids, phases dans l'ordre chronologique, avancement, poids fabriqué, statut).

## 1.14.0
- Nouvel onglet « Suivi » : tableau de suivi de travaux moderne par spool, avec indicateurs (avancement global, spools terminés / en cours / à démarrer, pouces soudés, poids fabriqué), 7 phases pondérées (sortie matériel, débitage/assemblage, pointage/soudage, NDT, inspection, peinture/passivation, livraison), filtres, recherche et « Tout à 100 % » / « Remettre à 0 ». Données enregistrées avec le projet.
- Export Excel : nouvelle feuille « Suivi des travaux » (indicateurs, barres de progression, statuts colorés, totaux) ; « Tableau d'avancement » rempli avec les valeurs du suivi.

## 1.13.2
- Fichier Tableau de Bord : suppression de toutes les formules de calcul (totaux, sous-totaux, avancement, cumul) ; les valeurs sont écrites telles quelles et la mise en forme (couleurs, en-têtes, bordures, couleurs de statut) est conservée. Les colonnes d'avancement restent à remplir dans Excel.

## 1.13.1
- Le matériau est la première cellule de la fiche et de chaque ligne, avec « Acier carbone » par défaut pour toute nouvelle ligne (le choix est conservé d'une ligne à l'autre).

## 1.13.0
- Matériau par ligne : liste déroulante (acier carbone, basse température, P11/P22, inox 304/316/321/347, duplex, super duplex, Inconel, Monel, cuivre, cupronickel, titane, aluminium) dans la fiche et dans chaque ligne ; le matériau du projet reste la valeur par défaut.
- Poids calculés avec la masse volumique de chaque matériau ; répartition des kg par matériau dans les totaux ; colonne Nuance (Excel Détail) et colonne « Matériau (code) » dans le CSV (import compatible).

## 1.12.2
- Import corrigé : sélecteur de fichier sans filtre de type (les fichiers CSV/JSON ne sont plus grisés sur Android), bouton en libellé, lecture UTF-8 ou Windows-1252, message clair si un fichier Excel est choisi.

## 1.12.1
- Schémas de piquages corrigés : suppression des bouts de ligne parasites, lignes de fermeture ajoutées en haut et en bas de l'alésage.

## 1.12.0
- Piquages : schémas en coupe du weldolet, du sockolet et du threadolet avec cotes MSS SP-97 taille sur taille (hauteur A, largeur de base B, alésage D).

## 1.11.2
- Allègement de l'interface d'export : suppression de la liste des noms de fichiers, des notes de dossier et des boutons « Ouvrir » en double (reste « Ouvrir le Tableau de Bord »).

## 1.11.1
- Bouton « Ouvrir le Tableau de Bord » : génère et ouvre le fichier en un seul geste (feuille de partage), sans exporter d'abord ; repli sur l'enregistrement si l'appareil ne le permet pas.

## 1.11.0
- Bouton « Ouvrir » après un export : ouvre le dernier fichier (feuille de partage de l'appareil pour choisir Excel, ou nouvel onglet).

## 1.10.1
- Le fichier Excel du récap s'appelle maintenant « Tableau-de-Bord_<projet>_<date>.xlsx ».

## 1.10.0
- Récap Excel : nouvelle feuille « Tableau d'avancement » au modèle du tableau de bord de fabrication tuyauterie (ISO, DN, nombre de soudures, pouces, spool, poids théorique et axe-axe, longueur, peinture, colonnes d'avancement pondérées, totaux, sous-totaux filtrables, couleurs de statut).
- Informations d'en-tête du tableau (projet, code, document, rev, service, classe, SYS) saisies dans l'onglet Rapport par spool et enregistrées avec le projet.
- Feuille Détail : colonne Nuance.

## 1.9.1
- Récap Excel : colonne « Diamètre des pipes » en B (Récap, Par ISO, Détail) ; poids, surface de peinture et soudures décalés à droite.

## 1.9.0
- Soudures : nombre de joints à souder (1 par extrémité raccordée d'un tube, ou valeur imposée), diamètre principal et pouces-diamètre (joints × NPS × quantité) par ligne, par spool, par ISO et au total.
- Récap Excel : colonnes Joints à souder / Pouces à souder dans Récap, Par ISO et Détail. Colonnes ajoutées aux CSV (liste et spools), import compatible.

## 1.8.1
- Schémas de vannes redessinés d'après Pipedata : opercule, soupape, clapet, boisseau (vue de bout + face), papillon wafer.
- Nouvelle vanne papillon à oreilles.

## 1.8.0
- Tableaux SW/TH remplacés par les valeurs réelles de l'ASME B16.11-2021 (B, C, D, G, J, A, K ; 3000/6000 SW, 2000/3000/6000 TH).
- Nouveaux schémas en coupe (style Pipedata) : coude SW 45°, té SW, bouchon SW, coude 90°/45° fileté, té fileté.
- Les poids des raccords forgés SW peuvent varier légèrement (recalibrage sur Pipedata conservé).

## 1.7.4 - 2026-10-26

- Schéma du fond corrigé : demi-vue extérieure et demi-coupe hachurée comme dans Pipedata, biseau de soudure, axe central. Le dessin ne se déforme plus sur les petits diamètres à forte épaisseur (par exemple 1/2" SCH XXS).

## 1.7.3 - 2026-10-26

- Schémas de brides conformes au dessin technique : ligne continue de la face d'étanchéité à travers l'alésage, extrémité du moyeu fermée, arêtes de la bride tracées à travers les trous de boulons, coupure du tube sur les brides SO, SW et filetée.

## 1.7.2 - 2026-10-26

- Brides : schémas en coupe ajoutés pour la bride pleine, à emboîtement glissant (SO), filetée et à souder (SW), avec le diamètre d'alésage SO et la profondeur d'emboîtement SW. La hauteur du moyeu de ces types est estimée et non cotée.

## 1.7.1 - 2026-10-26

- Schémas redessinés à l'échelle dans le style Pipedata : coupes hachurées et cotes à flèches (coudes, tés, réductions, fonds, brides à collerette, coudes et manchons forgés, vannes, goujons, tube).
- Brides : ajout du cercle de boulons, du diamètre de ressaut et du diamètre de moyeu (ASME B16.5), des cotes Y et de la hauteur totale.
- Vannes : face à face par classe selon ASME B16.10 (remplace le coefficient forfaitaire), ce qui affine la surface de peinture.
- Le schéma en coupe des brides n'est donné que pour la bride à collerette ; les autres types affichent leurs cotes.

## 1.7.0 - 2026-10-26

- Fiche de calcul : bloc « Encombrement et schéma » pour chaque catégorie, avec un schéma côté et les dimensions : coudes (R, A, O), tés (C, M), réductions (H), fonds (E), brides (Ø, longueur Y, épaisseur, boulons), vannes (face à face L), raccords forgés B16.11 (A, J, L), boulonnerie et piquages.
- Tube : schéma de la longueur mesurée, des encombrements d'extrémité et du tube net.
- Les dimensions sont indicatives ; la hauteur de vanne et la hauteur de piquage dépendent du fabricant et ne sont pas incluses.

## 1.6.0 - 2026-10-26

- Gestion de plusieurs projets : chaque projet garde ses lignes et ses paramètres (créer, renommer, dupliquer, supprimer, ouvrir).
- Les données de la version 1.5 sont reprises automatiquement dans « Projet 1 ».
- Corbeille : les 5 derniers projets supprimés peuvent être restaurés.
- Sauvegarde d'un projet ou de tous les projets (.json) ; import d'un fichier comme nouveau projet.
- Le nom du projet figure dans les noms de fichiers exportés.
- Demande de stockage persistant au navigateur.

## 1.5.0 - 2026-10-26

- Export « Récap Excel (.xlsx) » : feuilles Récap (ISO, spool, poids, surface de peinture), Par ISO et Détail, avec totaux en formules.
- Génération du fichier Excel dans le navigateur, sans bibliothèque externe, donc utilisable hors connexion.

## 1.4.0 - 2026-10-26

- Nouvelle catégorie « Piquage (olet) » : weldolet (STD, XS, XXS), sockolet (3000#, 6000#) et threadolet, avec poids et surface de peinture.
- Raccords forgés : demi-manchons et manchons, à souder et filetés (3000#, 6000#).
- Une série XS de weldolet n'est jamais plus légère que la STD.
- Le changement de schedule ou de classe ne modifie plus la taille choisie.
- Format de fichier : version 5 (les versions 1 à 4 restent importables).

## 1.3.2 - 2026-10-26

- Icône du raccourci : tous les fichiers sont à la racine du dépôt (plus de dossier `icons/`), car l'envoi par l'interface web de GitHub aplatit les dossiers et cassait les chemins du manifeste.
- Nouvel identifiant d'application dans le manifeste, pour forcer Chrome à réinstaller avec la bonne icône.
- Service worker : un fichier manquant n'empêche plus l'installation.

## 1.3.1 - 2026-10-26

- Boulonnerie : longueur de goujon = 2 × épaisseur de bride + 2,5 × diamètre, calée sur Pipedata (12" classe 300 : 170 mm, 21,77 kg).
- Icône du raccourci : copie intégrée dans `index.html` en secours, au cas où le dossier `icons` n'est pas envoyé avec la page.
- Cache hors connexion : version 1.3.1.
- README : vérifications de l'icône et valeurs Pipedata de référence.

## 1.3.0 - 2026-10-25

- Raccords forgés ASME B16.11 : coudes 90° et 45°, tés, fonds, à souder (3000#, 6000#) et filetés (2000#, 3000#, 6000#), NPS 1/2 à 4, avec poids et surface de peinture.
- Boulonnerie des brides : goujons et écrous, par classe et NPS (ASME B16.5).
- Bride WN 12" classe 300 calée sur Pipedata (64,02 kg).
- Raccourci sur l'écran d'accueil : service worker, identifiant du manifeste, icône SVG, `.nojekyll`.
- Format de fichier : version 4 (les versions 1 à 3 restent importables).

## 1.2.0 - 2026-10-25

- Surface de peinture (m²) pour chaque ligne : tubes, raccords, brides, vannes. Surface imposée possible.
- Totaux de surface par catégorie, par ISO et par spool, et dans la Fiche.
- Export CSV : colonnes `Surface peinture (m²)` et `Surface imposée (m²)`, et surface par spool.
- Format de fichier : version 3 (les versions 1 et 2 restent importables).

## 1.1.0 - 2026-10-25

- Extrémités des tubes : bride, coude ou fond à chaque bout. L'encombrement est retiré automatiquement de la longueur mesurée (longueur nette).
- Encombrement imposé (mm) pour remplacer le calcul.
- Export CSV : colonnes de longueur mesurée, longueur nette et extrémités. Le réimport relit ces colonnes.
- Format de fichier : version 2 (les fichiers de la version 1 restent importables).

## 1.0.0 - 2026-10-25

Première version publiée.

- Calcul du poids des tubes (ASME B36.10M / B36.19M), coudes, tés, réductions, fonds, brides, vannes et pièces libres.
- Fiche de calcul avec coupe du tube à l'échelle et tableau des schedules par NPS.
- Liste de calcul modifiable ligne par ligne, avec isométrique (ISO) et numéro de spool.
- Total général et total par ISO.
- Rapport par ISO et par spool.
- Matériaux, contenu et isolation (paramètres de la fiche).
- Import et export : CSV (Excel), sauvegarde projet `.json`.
- Format de fichier : version 1.
- Icône de l'application et manifeste pour le raccourci sur l'écran d'accueil.

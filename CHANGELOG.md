# Journal des versions

Numérotation : X.Y (par exemple 2.0).

## 8.9
- Scanner : bouton « Déplacer les repères » (glisser chaque repère à sa place exacte sur le dessin, valable pour chaque isométrique).

## 8.8
- Scanner : suivi du tracé plus robuste pour numéroter les repères dans l'ordre (comble les petits trous, autres résolutions) ; avertissement si un scan restauré vient d'une ancienne version de la détection.

## 8.7
- Scanner : repères numérotés dans l'ordre du tracé ; 2e passe plus sensible s'il manque des points ; points isolés écartés en premier en cas de surplus ; un long tuyau vertical n'est plus pris pour le cadre ; repères parfaitement alignés sur l'image agrandie.

## 8.6
- Détection des points de soudure refaite pour les PDF vectoriels (cahier d'isométriques PIRECO) : un point de soudure est un renflement net sur le trait épais de la tuyauterie, mesuré par rapport à l'épaisseur du trait voisin. Les pointes de flèche (sens d'écoulement), vannes, brides, cadre, cartouche et texte posé sur le trait sont écartés.

## 8.5
- Scanner : aucun repère de soudure n'est ajouté sur une page sans liste de matériel (page de garde, plan seul…). Cette page reçoit seulement un numéro « Page n° N », n'est pas prise en charge et n'est pas archivée.
- Les repères automatiques ne dépassent jamais le nombre de joints de la liste de matériel (coude 2, té 3, réduction 2, fond 1, bride 1, WOL 1, vanne à souder 2 ; fileté = 0). Un contrôle « joints selon la liste / repères actifs » s'affiche sous l'aperçu de la page.

## 8.4
- La barre d'onglets reste toujours affichée en haut de l'écran pendant le défilement.

## 8.3
- Scanner : si un isométrique ne porte aucun repère de soudure, les points noirs pleins sur la ligne (soudures atelier) sont détectés et numérotés automatiquement. Ils s'affichent sur l'image de la page : toucher un repère pour le masquer, « + Ajouter un repère », « Renuméroter ».

## 8.2
- Supprimer un projet efface maintenant toutes ses données pour libérer l'espace : lignes, soudures, dernier scan, archives du scanner et images. La confirmation prévient que c'est définitif (plus de passage par la corbeille).
- Corbeille (projets supprimés avant cette version) : nouveaux boutons « Supprimer définitivement » et « Vider la corbeille » qui effacent aussi les données du scanner.

## 8.1
- Nouvel onglet « Scanner (archives) » : chaque page d'isométrique lue par le scanner est conservée automatiquement dans le projet (lignes, spools, soudures, image de la page), même si un autre dessin est scanné ensuite. Pour chaque page : miniature, date, nombre de lignes, spools et soudures ; boutons Ouvrir dans le scanner, Aperçu de la page, Supprimer ; recherche par ISO, document ou service. Stockage dans la mémoire du navigateur (IndexedDB), par projet.

## 8.0
- Correction : le pied de page affichait « Version 6.2 » en dur alors que l'en-tête indiquait la version réelle ; il suit maintenant automatiquement la version de l'application (FR et EN).

## 7.9
- Vannes : 12 nouveaux points Pipedata. Boisseau sphérique cl.300 : 2" = 20, 4" = 76, 8" = 367 kg ; cl.600 : 4" = 98, 8" = 577 kg (le pattern court 8" cl.300 = 294 kg est retrouvé). Clapet à battant cl.150 : 2" = 19, 8" = 133, 12" = 347 kg ; cl.300 : 2" = 21, 8" = 213 kg. Poids du boisseau maintenant interpolé par classe à partir de ses propres points Pipedata.
- Face RTJ disponible aussi en classe 150 : face à face RF + 13 mm (Pipedata, clapet 12").

## 7.8
- Vannes à opercule : 20 nouveaux points Pipedata (SLB). Classe 150 : 1" = 10, 1½" = 18, 2" = 18, 2½" = 28, 3" = 34, 4" = 52, 5" = 71, 6" = 88, 8" = 144, 10" = 197, 12" = 298, 14" = 406, 16" = 524, 24" = 1466 kg. Classe 600 : ½" = 5, ¾" = 10, 1" = 15, 1½" = 27, 4" = 120, 5" = 190 kg. Les tailles intermédiaires (1¼", 18", 20", ½" et ¾" en cl.150/300) sont interpolées entre les points mesurés.

## 7.7
- Vannes à brides : nouveau choix « Face de bride » RF / RTJ (RTJ à partir de la classe 300). Le face à face RTJ = RF + 16 mm (cl.300 et 1500) ou + 3 mm (cl.600 et 900), relevé dans Pipedata ; le poids reste identique. Visible dans la désignation, la fiche et le dessin.
- 14 nouveaux points Pipedata (SLB) : opercule cl.300 (2" = 24, 3" = 52, 4" = 76, 8" = 218, 10" = 352, 12" = 472 kg), opercule 12" cl.600 = 981 / cl.900 = 1550 / cl.1500 = 3244 kg, clapet à battant 6" cl.600 = 227 kg, boisseau sphérique cl.150 (6" = 227, 8" = 321, 14" = 1020 kg). Coefficients de classe 900/1500 recalés (1,58 / 3,31).

## 7.6
- Vannes : 12 nouveaux points Pipedata (SLB) : globe cl.600 (2" = 57, 3" = 89, 4" = 149, 6" = 417, 8" = 542, 12" = 900 kg) ; boisseau sphérique 12" (cl.150 = 781, cl.300 = 873, cl.600 = 1339, cl.900 = 1523 kg). Coefficients de classe du boisseau recalés (1,12 / 1,71 / 1,95) ; pattern court = 80 % du pattern long (Pipedata : 698,4 kg pour 873 kg).

## 7.5
- Vannes : 12 points Pipedata (SLB) repris exactement : boisseau sphérique 4" = 55 kg et 10" = 519 kg (cl.150), opercule 4" = 52 kg et 10" = 197 kg (cl.150), globe 10" cl.150 = 308 kg, globe cl.300 4" = 86 / 10" = 527 / 12" = 608 kg, clapet à battant 4" cl.150 = 48 kg, 4" cl.300 = 61 kg, 12" cl.300 = 449 kg. Les autres tailles sont recalées sur ces points.

## 7.4
- VANNES à brides refondues (ASME B16.10) : le face à face dépend maintenant du type de vanne (opercule, globe, clapet à battant, clapet à piston, boisseau sphérique pattern long ou court, robinet à boisseau conique) et de la classe. Ex. boisseau sphérique 10" cl.150 : 533 mm (avant : 330 mm de la vanne à opercule), identique à Pipedata.
- Poids : tableaux par taille et classe (opercule, globe, clapet cl.150/300/600, valeurs indicatives wermac) au lieu d'un coefficient unique ; boisseau sphérique calé sur Pipedata 10" cl.150 = 519 kg (avant : 156,75 kg). Valeurs non tabulées (petites tailles, classes 900/1500, autres types) estimées, avec avertissement.
- Nouveaux types : clapet à piston (lift), boisseau sphérique pattern court, robinet à boisseau conique (plug). Corrigé : face à face de l'opercule cl.300 de 14" à 24" (valeurs de l'opercule à coin, pas du conduit).

## 7.3
- Poids des raccords calés sur le catalogue Trouvay Cauvin (ASME B16.9, SCH STD) : tés égaux (+13 à +45 % selon la taille, écart désormais 0 %), coudes 90° GR, 45° GR et retours 180° (écart 0 %). Les tés réduits utilisent le même coefficient du gros diamètre. Autres schedules : même coefficient appliqué.

## 7.2
- Réductions et tés réduits : la liste « NPS réduit » ne contient plus que les combinaisons ASME B16.9 (suppression du groupe « Hors liste »). Une valeur déjà saisie hors liste reste affichée avec un avertissement.

## 7.1
- CORRECTION IMPORTANTE réductions : le poids était sous-estimé (24"×16" : 59,5 kg au lieu de 72,00 kg Pipedata ; 10"×4" : 6,8 kg au lieu de 10,70 kg). Nouveau calcul : coque conique avec la paroi du gros bout, coefficient calé sur Pipedata et sur les tableaux fabricants (écart ≤ 5 % : 10×8 = 11,87 kg, 12×6 = 15,36 kg, 6×4 = 4,15 kg) ; les deux valeurs Pipedata vérifiées (SCH STD) sont reprises exactement.
- Tailles : les listes « NPS réduit » des réductions et des tés réduits ne proposent plus que les combinaisons existantes ASME B16.9 (ex. 24" : 20, 18, 16 pour les réductions ; 24"×1/2" n'existe plus). Les autres tailles restent accessibles dans un groupe « Hors liste ASME B16.9 (à confirmer) » avec un avertissement. Changer le gros diamètre ramène automatiquement le petit à la taille existante la plus proche.
- Tés réduits : la longueur de branche utilise la cote M du tableau ASME B16.9 (corps C et piquage M) au lieu d'une moyenne.

## 7.0
- Joints à diamètres différents : une réduction 10"×8" compte 1 joint Ø10 + 1 joint Ø8 (18 po-diam. au lieu de 20) ; un té réduit compte 2 joints sur la ligne + 1 sur la branche. Pris en compte dans la fiche pièce (« 10 + 8 po »), les soudures créées par spool (Ø de chaque joint), le rapport par spool et les exports.

## 6.9
- Onglet Assemblage : nouvelle « Vue rapide » (par défaut, bouton « Cartes » pour l'ancienne vue). Une ligne compacte par pièce, groupée par ISO puis par spool avec poids, surface, joints et pouces à souder de chaque spool ; quantité / longueur et n° de spool modifiables directement dans la ligne ; sélection multiple (case de la ligne ou du spool entier) puis affectation du spool en un geste (puces SP existants, « Nouveau SPnn », autre n°), dupliquer ou supprimer en lot ; « + Pièce » ajoute une pièce directement dans un spool ; toucher le nom ouvre la fiche complète.

## 6.8
- Joints de soudure : weldolet et sockolet comptent 2 joints (soudure sur le tube + sur la branche), threadolet 1 ; les vannes à souder (SW/BW dans la désignation) comptent 2 joints quel que soit le diamètre ; manchons SW 2 joints.
- Scanner : il ne disparaît plus jamais sans ordre. Il se rouvre automatiquement avec le dernier scan s'il disparaît (rechargement de la page, retour de l'appareil photo ou du sélecteur de fichier, manque de mémoire) ; seule la croix × le ferme. Le scan est sauvegardé après chaque page lue.

## 6.7
- Correction : le scanner affichait « Erreur de lecture : Cannot read properties of undefined (reading 'then') » depuis la 6.6 (la nouvelle fonction de rétablissement du scan portait le même nom que le chargeur d'outils de lecture). Renommée.

## 6.6
- Scanner : il ne se ferme plus tout seul (ni en touchant à côté, ni avec Échap, ni après « Ajouter ») : seule la croix le ferme.
- Scan enregistré et lié au projet : le dernier scan est sauvegardé (IndexedDB) et rétabli à la réouverture, même après rechargement. Les lignes et soudures ajoutées (🔗) restent liées : les modifications faites dans les autres onglets (quantité, spool, numéro de soudure, suppression) sont reprises dans le scanner à chaque ouverture, et le bouton « Mettre à jour le projet » met à jour sans créer de doublons.
- Plan des soudures : le zoom fonctionne maintenant sur téléphone (le plan n'était plus agrandi).

## 6.5
- Vannes de diamètre ≤ 2" (à souder) : 2 joints de soudure comptés automatiquement (comme la vanne BW), donc 2 soudures créées par vanne 3/4" dans l'onglet Soudure. Repères du plan plus petits.

## 6.4
- Scanner : chaque soudure affiche maintenant son spool (bandeau et liseré de la couleur du spool, cartes triées par spool) et un nouveau « Plan : soudures par spool » repère sur le dessin chaque soudure avec son numéro, dans la couleur de son spool (zoom + / −), pour valider l'appartenance au spool.

## 6.3
- Scanner : lecture automatique des cotes. Les chiffres des cotes (police italique) sont détectés, redressés et lus par OCR chiffres seuls avec vote sur plusieurs inclinaisons. Chaque cote s'affiche avec sa vignette redressée, sa valeur (mm, modifiable), un ⚠ si la lecture est incertaine et le spool voisin ; « Créer les tubes » crée un tube par cote cochée avec le bon spool, à compléter avec les raccords d'extrémité (bloc « Cotes du spool »).

## 6.2
- Rapport par spool : nouveau bloc « Cotes du spool » sur chaque spool : on saisit chaque cote (mm) et les raccords aux deux extrémités (coude, té, bride WN, fond, réduction, piquage…) ; la longueur de coupe = cote − encombrement est calculée et alimente directement le poids, la peinture et les totaux. Exemple : 5926 − té 143 − coude 228 = 5555 mm (DN 150).

## 6.1
- Scanner : la répartition automatique des lignes par longueur dessinée (v5.9) est retirée : les isométriques ne sont pas à l'échelle (ex. cote 5926 dessinée plus courte que 623), elle donnait des longueurs de spool fausses. Les repères de spool et les soudures restent détectés ; les longueurs doivent venir des cotes.

## 6.0
- Scanner : les vignettes des repères de spool à texte noir montrent maintenant le cadre « SP nn » entier (cadre rouge détecté directement), au lieu d'un coin agrandi ou d'un texte coupé.

## 5.9
- Scanner : repères de spool à texte noir dans un cadre rouge (« SP 01 »), croix orange de grande taille, traits fins et pâles (capture d'écran, photo JPEG), marges noires de capture rognées, images petites agrandies à 3300 px.
- Scanner : un tuyau interrompu par une cote forme un seul groupe qui prend le spool de son repère ; une soudure chantier (croix) sépare deux spools : le tronçon non relié au tuyau connu passe à l'autre spool.
- Scanner : répartition automatique des lignes de la liste entre les spools lus : tubes au prorata de la longueur dessinée de chaque spool, raccords au plus fort reste (estimation signalée sur chaque ligne, à vérifier).

## 5.8
- Joints à souder : calcul automatique par pièce (chaque pièce compte ses extrémités soudées) : coude 2, té 3, réduction 2, fond 1, bride WN/SO/SW/LJ 1 (pleine et filetée 0), vanne à souder BW 2, forgé SW 2 (té 3, fond et demi-manchon 1), piquage 1 (fileté 0) ; tubes, vannes à brides et boulonnerie 0, pour ne pas compter deux fois le joint tube-raccord. La valeur « 1 joint imposé » mise par défaut sur les anciennes lignes est remplacée une fois par le calcul automatique ; les autres valeurs imposées sont conservées.

## 5.7
- Onglet Soudure atelier (SW) : chaque joint calculé reçoit automatiquement une soudure numérotée (SW1, SW2… numéros uniques par isométrique, spool et diamètre repris du calcul), sans commande à lancer. Les numéros apparaissent dans la liste, modifiables avec la case N°. Une soudure supprimée à la main n'est pas recréée.

## 5.6
- Onglets SW et FW : un numéro de soudure ne peut plus se répéter dans le même isométrique (SW et FW confondus) : refusé à l'ajout et à la modification du N° ; en cas de changement SW/FW, une soudure en conflit reçoit automatiquement le prochain numéro libre.

## 5.5
- Onglets SW et FW : une case « N° » à côté du choix SW/FW de chaque soudure pour modifier son numéro (refusé si le numéro existe déjà pour cet ISO).

## 5.4
- Onglets SW et FW : le bouton « Recopier les joints de l'onglet Soudure » est supprimé. Nouveau bouton « Annuler la dernière action » (jusqu'à 40 actions : ajout, suppression, case réalisée, type SW/FW, diamètre, spool, pouces soudés, phases d'avancement).

## 5.3
- Onglets SW et FW : une soudure ajoutée à la main (formulaire « Ajouter une soudure ») est maintenant calculée : elle compte comme joint supplémentaire de son spool (pouces à souder, soudés, reste, avancement, poids), même si l'ISO ou le spool n'existe pas dans le Détail (le spool est alors créé automatiquement).

## 5.2
- Onglets SW et FW : un seul tableau de soudures. La grille « Détail des soudures » (S1, S2…) du suivi par spool est supprimée ; on garde la liste lisible (FW1, FW2… avec Ø, spool, case « Réalisée »). Cocher une soudure met à jour automatiquement les pouces soudés et l'avancement du spool.

## 5.1
- Onglets SW et FW : la grille « Détail des soudures » (suivi par spool) et la liste des soudures (FW1, FW2…) sont liées : cocher une soudure à un endroit la coche à l'autre (y compris « Tout soudé », « Tout marquer réalisé » et la saisie des pouces soudés). La liste détaillée par ISO est repliée par défaut.

## 5.0
- Suivi par spool (onglets SW et FW) : cartes de soudure plus grandes et plus espacées (2 colonnes sur téléphone) ; le numéro et le diamètre sur une ligne, le choix SW/FW et une grande case « terminée » sur l'autre. Plus de chevauchement.

## 4.9
- Excel : les onglets « Suivi avancement atelier » et « Suivi avancement chantier » reprennent le modèle de l'onglet « Suivi des travaux » (bandeau d'indicateurs, pondération des phases, formules, barres de progression, statut). Atelier = spools SW, chantier = joints FW (poids posé).

## 4.8
- Les isométriques sont triées par numéro de page (P3, P4, P5 … P11, P12) dans les résultats, les spools, les soudures et le suivi, au lieu de l'ordre alphabétique du numéro de ligne.

## 4.7
- Excel : suppression des onglets « Atelier (SW) » et « Chantier (FW) » (les onglets de suivi d'avancement et les listes de soudures restent).

## 4.6
- Base de données : nouvelle vanne « Vanne à boisseau sphérique à souder BW (B16.10) » (poids de vannes SLB, Pipedata). Points relevés en classe 300 : 4" = 53 kg (face à face 305, hauteur 200) et 10" = 396 kg (559, 300) ; autres tailles et classes interpolées, avec avertissement.
- La boulonnerie n'est plus comptée dans les joints et les pouces à souder.
- Le scan reconnaît « BW / butt weld » sur une vanne à boisseau.

## 4.5
- Excel : deux onglets « Suivi avancement atelier » et « Suivi avancement chantier » (remplace « Avancement chantier »).
- Un joint déplacé de SW vers FW garde son repère (S2 reste S2) ; il disparaît de l'atelier et s'affiche au chantier sous le même numéro.

## 4.4
- Excel : nouvel onglet « Avancement chantier » (par spool : joints FW, pouces à souder / soudés / reste, avancement par phase, avancement global, poids à poser et poids posé, statut).

## 4.3
- Suivi par spool (onglets SW et FW) : chaque joint (S1, S2…) a un choix SW / FW. Passer un joint en FW le retire de l'atelier et l'ajoute au chantier (et inversement), avec le diamètre du joint.
- Isométrique de plusieurs pages : chaque page est calculée séparément (suffixe -P3, -P4… quand le numéro de feuille n'est pas lu ou que deux pages ont le même nom).

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

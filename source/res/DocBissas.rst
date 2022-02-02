Annexe - Documentation technique des bissas
===========================================

:Type: Documentation technique
:Organisateur: ABI
:Auteur: CDS
:Objectif: Documenter le fonctionnement logiciel des bissas


INSTALLATION
------------


#. A la lecture d'un badge sur une de ses faces, le driver de Bissas appelle la méthode contrôlerBissas(face,bCode) où face est la face (A ou B) sur laquelle la lecture a été faite et bCode est le bCode du badge lu. Cette méthode va gérer le passage dans le bissas.
#. DRIVERS de bissas
#. Les bissas sont fournis avec des drivers dont l'API est composée des fonctions essentielles suivants
#. lancer(port entier, numSérie entier, refContrôleur Contrôleur)
#.  lance une instance du driver avec
#.   port : le numéro du port de connexion au panneau de brassage du bissas
#.   numSérie : le numéro de série du bissas
#.   refContrôleur la référence (un oid) du contrôleur de bissas qui va le commander
#. allumerLedLecteur(f face, c couleur, t entier)
#.  allume la LED du lecteur de badge sur la face f avec la couleur c pendant t secondes. Les valeurs de couleur possibles sont vert, orange, rouge. Quand c=0 la LED est allumée jusqu'à la prochaine commande de changement.
#. clignoterLedLecteur(f face, c couleur, t entier)
#.  fait clignoter la LED du lecteur de badge sur la face f avec la couleur c pendant t secondes. Les valeurs de couleur possibles sont vert, orange, rouge. Quand c=0 la LED clignote jusqu'à la prochaine commande de changement. 
#. ouvrirPorte(face:caractère) : chaîne
#.  ouvre la porte de la face du bissas passée en paramètre et renvoie OK en cas de réussite et KO en cas d'échec (impossible d'ouvrir la porte complètement)
#. fermerPorte(face:caractère) : chaîne
#.  ferme la porte de la face du bissas passée en paramètre et renvoie OK en cas de réussite, KO en cas d'échec (impossible de fermer la porte complètement)
#. détecterPrésence(t:entier) : chaîne
#.  détecte la présence d'un personne à l'intérieur du bissas et renvoie Full si quelqu'un est présent, Piggypacking si plus d'une personne est présente et Void si personne n'est détecté a bout de t secondes
#. #########
#. Les fonctions suivantes sont spécifiques aux bissas Xtra
#. scannerQRCode() : qrcode
#.  lance le scan d'un QRCode sur le lecteur externe face A
#. #########
#. Les fonctions suivantes sont spécifiques aux bissas Xtra+
#. scannerEmpreinte(face) : empreinte
#.  lance le scan d'une empreinte digitale sur le lecteur interne de la face passée en paramètre
#. #########
#. Les fonctions suivantes sont spécifiques aux bissas Metra
#.  prendreTempérature() : décimal
#. Prend la température d'une personne présente à l'intérieur du bissas

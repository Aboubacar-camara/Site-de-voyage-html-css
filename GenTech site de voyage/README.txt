==========================================================
TRAVEL EXPLORER - Site vitrine d'une agence de voyage
==========================================================


1. PRÉSENTATION DU PROJET
----------------------------------------------------------
Travel Explorer est un site vitrine d'une seule page pour une agence de voyage
basée à Dakar. Il présente les destinations, les tarifs, les services et
l'agence, et propose un formulaire de contact.

Le site est écrit uniquement en HTML5 et CSS3 : pas de JavaScript, pas de
Bootstrap, pas de Tailwind. C'est un projet d'apprentissage pour débutants.
La seule ressource externe est la police Google Fonts « Poppins ». Sans
Internet, le site s'affiche quand même, avec la police Arial.


2. ARBORESCENCE
----------------------------------------------------------
travel-explorer/
├── index.html          La page du site
├── css/
│   └── style.css       Toute la mise en forme
├── images/
│   ├── logo.png        Logo (icône de l'onglet du navigateur)
│   ├── accueil.jpg     Photo de fond du hero
│   ├── destination1.jpg    Carte Saly
│   ├── destination2.jpg    Carte Marrakech
│   ├── destination3.jpg    Carte Zanzibar
│   └── whatsapp.svg        Icône WhatsApp (provisoire, voir partie 6)
└── README.txt          Ce fichier


3. COMMENT OUVRIR LE SITE
----------------------------------------------------------
Double-cliquez sur index.html : le site s'ouvre dans votre navigateur.
Aucune installation n'est nécessaire.


4. REMPLACER LES TEXTES ENTRE [CROCHETS]
----------------------------------------------------------
Ouvrez index.html dans un éditeur de texte (par exemple VS Code), puis utilisez
la recherche (Ctrl + F) pour trouver chaque texte à remplacer :

    [PRIX]        6 fois : 3 dans les cartes, 3 dans le tableau des tarifs
    [ANNÉE]       Année de création, dans la section À propos
    [NOM]         3 fois : les membres de l'équipe, dans la section À propos
    [ADRESSE]     Adresse de l'agence, dans la section Contact
    [TÉLÉPHONE]   Numéro de l'agence, dans la section Contact
    [DOMAINE]     Nom de domaine de l'e-mail, dans la section Contact

Pensez aussi à remplacer les adresses des réseaux sociaux, en bas de
index.html : elles mènent pour l'instant aux pages d'accueil de Facebook,
Instagram et LinkedIn.


5. REMPLACER LES IMAGES
----------------------------------------------------------
Pour changer une image, le plus simple est de garder le même nom de fichier :

    1. Téléchargez une photo libre de droits sur https://unsplash.com
       ou https://www.pexels.com
    2. Renommez-la avec le nom de l'image à remplacer (ex. destination1.jpg).
    3. Copiez-la dans le dossier images/ en écrasant l'ancienne.
    4. Dans index.html, mettez à jour l'attribut alt pour qu'il décrive
       la nouvelle photo.

Conseil : choisissez des photos horizontales d'environ 1200 px de large
(1920 px pour accueil.jpg), et de moins de 500 Ko.

Attention, deux images sont à remplacer avant une vraie mise en ligne :

    - La photo de l'équipe (section À propos) : la maquette ne prévoit pas de
      fichier pour cette image. Elle utilise donc accueil.jpg comme image de
      remplacement. Pour mettre une vraie photo, ajoutez images/equipe.jpg,
      puis changez le src et le alt de l'image dans index.html.
    - La carte Saly : la photo est une plage d'illustration, qui n'a pas été
      prise à Saly (aucune photo libre de la plage de Saly n'a été trouvée).

Origine des photos actuelles (photos libres de droits) :

    accueil.jpg       Pexels  - https://www.pexels.com/photo/boats-near-the-shore-3954351/
    destination1.jpg  Unsplash - https://images.unsplash.com/photo-1507525428034-b723cf961d3e
    destination2.jpg  Pexels  - https://www.pexels.com/photo/bazaar-in-marrakech-morocco-22711558/
    destination3.jpg  Pexels  - https://www.pexels.com/photo/aerial-view-of-zanzibar-beachfront-paradise-30125136/
                      (photo recadrée à l'horizontale)

logo.png a été dessiné pour ce projet.


6. LE BOUTON WHATSAPP
----------------------------------------------------------
WhatsApp est accessible à deux endroits : le bouton rond flottant en bas à
droite de l'écran, et la 4e icône du footer. Les deux utilisent le même lien.

Le numéro : dans index.html, remplacez 221XXXXXXXXX aux 2 endroits par le
numéro WhatsApp de l'entreprise.
    - Format international, SANS le « + »
    - Sans espaces et sans zéros devant
    - Exemple : +221 77 123 45 67 s'écrit 221771234567

Le format du lien :

    https://wa.me/221XXXXXXXXX?text=Bonjour%20Travel%20Explorer

    wa.me/...     Le numéro à contacter
    ?text=        Le message déjà écrit quand la discussion s'ouvre
    %20           Un espace (une adresse web ne peut pas contenir d'espace)
    %2C           Une virgule

L'icône : le fichier images/whatsapp.svg actuel est une icône PROVISOIRE (une
bulle avec un combiné), dessinée pour ce projet. Remplacez-la par le logo
officiel :
    1. Ouvrez la page officielle « Brand resources » de WhatsApp :
       https://about.meta.com/brand/resources/whatsapp/whatsapp-brand/
    2. Lisez et acceptez les conditions d'utilisation, puis téléchargez le logo.
    3. Choisissez la version BLANCHE, faite pour un fond vert.
    4. Renommez le fichier whatsapp.svg et copiez-le dans images/ en écrasant
       l'ancien. Si le logo est fourni en PNG, gardez le nom whatsapp.png et
       changez le src des 2 images dans index.html.
Les règles de WhatsApp interdisent de modifier le logo ou ses couleurs : ne le
téléchargez pas sur un autre site et ne le redessinez pas.


7. LE FORMULAIRE
----------------------------------------------------------
Le formulaire vérifie les champs obligatoires et le format de l'e-mail, mais
il n'envoie aucun message : le HTML et le CSS seuls ne peuvent pas envoyer de
mail. Le bouton « Envoyer le message » recharge simplement la page.
Pour recevoir de vrais messages, il faudra plus tard relier le formulaire à un
programme côté serveur ou à un service de formulaires en ligne.


8. NOTIONS HTML UTILISÉES
----------------------------------------------------------
html, head, body     Structure de base de index.html
title, meta, link    Dans le <head>
h1                   Grand titre du hero
h2                   Titre de chaque section
h3                   Cartes, « Tableau des tarifs », services
h4                   « Notre mission », « Notre vision »
h5                   « L'équipe », « Réserver en 3 étapes »
h6                   « Travel Explorer » dans le footer
p                    Tous les paragraphes
div                  Conteneurs de mise en page (.conteneur, .carte-corps...)
span                 Mot « Explorer », badges, prix
header, nav          Haut de la page et menu
main                 Regroupe toutes les sections
section              Accueil, Destinations, Services, À propos, Contact
article              Les 3 cartes de destinations
footer               Bas de la page
a (liens internes)   Menu, bouton du hero, boutons « En savoir plus »
a (liens externes)   Réseaux sociaux du footer, bouton WhatsApp flottant
img                  Cartes, section À propos, icônes WhatsApp
ul, li               Menu, liste « L'équipe »
ol, li               Liste « Réserver en 3 étapes »
table, tr, th, td    Tableau des tarifs
form, label, input   Section Contact
textarea, select     Section Contact (message et destination)
option               Choix de la liste des destinations
button               Bouton « Envoyer le message »
strong               Prix, année, nom de l'agence
em                   « simples, sûrs et inoubliables » dans la section À propos


9. NOTIONS CSS UTILISÉES
----------------------------------------------------------
Les numéros renvoient aux blocs de css/style.css.

Sélecteur *                 Bloc 1 (réinitialisation)
Sélecteur d'élément         Bloc 1 (body, h1, p, a, img...)
Sélecteur .classe           Partout (.conteneur, .carte-destination...)
Sélecteur #id               #accueil, #destinations, #services, #a-propos,
                            #contact (blocs 3 à 7)
color, background-color     Partout
width, height               .logo-cercle, .icone, .carte-image img
max-width                   .conteneur, .entete-section, .hero-texte
font-size, font-family      Bloc 1 (body et titres)
font-weight, text-align     Bloc 1, .entete-section, .bloc-service
margin, padding             Partout (box-sizing: border-box dans *)
border, border-radius       Cartes, boutons, champs du formulaire
box-shadow                  Cartes, tableau, formulaire, bouton du hero
background-image            #accueil (bloc 3)
object-fit                  .carte-image img, .apropos-image img
position, top, left         .badge (absolute), .carte-image (relative),
                            header (sticky)
position: fixed             .bouton-whatsapp (bloc 9), avec bottom, right
                            et z-index
transform                   Survol des cartes (translateY) et du bouton
                            WhatsApp (scale), bloc 9
display: flex               Header, hero, services, À propos, Contact, footer
justify-content             .entete-ligne, .pied-ligne, .carte-pied
align-items, gap            .entete-ligne, .apropos-ligne, .contact-ligne
display: grid               .grille-destinations, .formulaire
grid-template-columns       .grille-destinations, .formulaire
:hover                      Bloc 9
transition                  Bloc 9
@media                      Bloc 10


10. LES 10 EXERCICES DE RÉVISION
----------------------------------------------------------
 1. Menu horizontal      .menu dans le header (bloc 2 : display: flex)
 2. Titre centré         .entete-section (bloc 1 : text-align: center)
 3. 3 cartes en Grid     .grille-destinations (bloc 4)
 4. Image de fond        #accueil (bloc 3 : background-image)
 5. Images arrondies     .apropos-image img (bloc 6), et les images des cartes
                         grâce à overflow: hidden sur .carte-destination (bloc 4)
 6. Ombre des cartes     .carte-destination (bloc 4 : box-shadow)
 7. Bouton au survol     .bouton-orange:hover, .bouton-contour:hover (bloc 9)
 8. Formulaire           <form class="formulaire"> dans la section Contact (bloc 7)
 9. Menu sur téléphone   @media (max-width: 768px) : .entete-ligne, .menu (bloc 10)
10. Tableau de tarifs    <table> dans la section Destinations (bloc 4)

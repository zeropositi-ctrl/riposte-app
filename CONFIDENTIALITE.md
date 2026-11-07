# Confidentialité de Riposte

Mise à jour : 7 novembre 2026, version 2.0.

Riposte sert à prévenir tes proches. Elle n'affiche pas de publicité, ne revend rien et ne mesure pas ton usage. Cette page dit ce qui sort de ton téléphone, et où.

## Tes alertes

Une alerte part par SMS, directement de ton téléphone vers ceux de tes proches. Elle ne passe par aucun serveur de Riposte.

Ces SMS sont chiffrés (AES-256-GCM), avec une clé différente pour chaque proche, créée au moment où vous vous associez. Ils contiennent ta position, ton adresse approximative, le niveau de ta batterie, ton réseau, le modèle de ton téléphone, ta fiche médicale et ton message.

Un SMS n'est pas chiffré dans deux cas seulement :

- le proche n'a pas Riposte, ou il est sur iPhone ;
- un proche n'a pas accusé réception au bout de 3 minutes. Tu peux couper ce repli dans les réglages.

Ce SMS lisible contient ton nom, la cause de l'alerte, ton message, ton adresse et un lien vers ta position. Jamais ta fiche médicale.

Ton opérateur voit qu'un SMS part et vers quel numéro. Ton appli Messages garde une copie de ce qui est envoyé et reçu.

## Ce qui passe par un serveur

Le serveur de Riposte est hébergé chez Supabase. Voici tout ce qu'il reçoit.

| Quoi | Contenu | Durée |
| --- | --- | --- |
| Vérification des nouveautés | Rien de personnel : l'app demande la dernière version, les annonces et les options | Non conservé |
| Photo et son d'une alerte | Chiffrés sur ton téléphone, illisibles pour le serveur | Effacés après 30 jours |
| Compte, si tu en crées un | Une empreinte de ton identifiant, une preuve de mot de passe, et une sauvegarde chiffrée sur ton téléphone | Jusqu'à ce que tu l'effaces |
| Signalement de zone | Une catégorie, un lieu arrondi sur ton téléphone à environ 250 m, l'heure, l'empreinte d'un jeton aléatoire et une empreinte de ta connexion | Auteur, connexion et lieu effacés après 30 jours |
| Affichage des signalements | Un grand secteur d'environ 60 km de côté, jamais ta position exacte | Non conservé |
| Rapport de bug, si tu l'envoies | Ton message, la version, le modèle du téléphone, et un journal technique si tu l'acceptes | Jusqu'à son traitement |

Comme tout site, le serveur voit l'adresse IP de la connexion. Elle n'est pas stockée en clair : une empreinte qui change régulièrement sert à limiter les abus.

## Le compte

Le compte est facultatif. Riposte marche sans lui.

Ta sauvegarde (proches, réglages, fiche médicale) est chiffrée sur ton téléphone avant l'envoi, avec une clé tirée de ton mot de passe. Ton mot de passe ne quitte jamais ton téléphone. Personne d'autre que toi ne peut lire cette sauvegarde, nous non plus.

La contrepartie : si tu perds ton mot de passe et ton code de secours, ta sauvegarde est perdue. Nous ne pouvons pas la récupérer.

Ta position et tes alertes ne sont jamais sauvegardées.

## Ce qui reste sur ton téléphone

Tes proches, tes réglages, ta fiche médicale, ta position pendant l'usage de la carte et l'historique de tes alertes restent sur ton téléphone, chiffrés avec une clé gardée par sa puce de sécurité. Les alertes terminées s'effacent au bout de 90 jours.

## Les autres services

- **Ton opérateur** transporte les SMS.
- **Google Play Services** fournit la position, les alertes de zone et le scan de QR.
- **OpenFreeMap** fournit le fond de carte et reçoit donc le secteur affiché.
- **GitHub** héberge le téléchargement de l'app.

## Tes droits

Tu peux effacer ton compte et ta sauvegarde depuis l'app, à tout moment. Retirer Riposte efface ce qui est sur ton téléphone.

Un signalement ne comporte pas d'identité. Si un signalement te concerne, écris-nous : il sera retiré.

Pour toute demande : la page du projet, https://github.com/zeropositi-ctrl/riposte-app

## Limites

Riposte est fournie sans garantie. Elle ne remplace pas les secours. En danger immédiat, appelle le 17 ou le 112.

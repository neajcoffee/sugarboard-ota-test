# Banc de test OTA — Sugarboard

**Ce dépôt ne contient aucun firmware.** Les assets de release sont des octets
**aléatoires**.

Il sert uniquement à éprouver le *chemin* de téléchargement OTA réel :

- la chaîne de redirections de GitHub vers `release-assets.githubusercontent.com` ;
- l'autorité de certification réelle de cet hôte ;
- un transfert de 1,5 Mo avec la vérification TLS active sur la carte.

Rien de tout cela ne dépend du contenu du fichier, d'où le bruit : le test porte
sur le transport, pas sur la charge utile. L'activation de l'image échoue à la
fin, ce qui est attendu — une suite d'octets aléatoires n'est pas une image ESP32
valide.

Le dépôt de production, lui, reste privé.

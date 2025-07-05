Projet: Mise en place d'un serveur FTP sécurisé avec vsftpd

Objectif du projet

Ce projet a pour but de concevoir, configurer et sécuriser un serveur FTP fonctionnel basé sur le logiciel **vsftpd (Very Secure FTP Daemon)**. Dans un contexte où l’échange de fichiers entre machines doit être fiable et sécurisé, notre objectif est de proposer une solution simple, performante et adaptée aux environnements LAN ou WAN.


Technologies et outils utilisés

1 Système d’exploitation Linux (Ubuntu)
2 Serveur FTP: vsftpd
3 Éditeur de texte: nano 
4 Client FTP: FileZilla / lftp
5 Réseau local via VirtualBox (mode accès par pont)

Sécurité mise en place

Afin de garantir la confidentialité et l'intégrité des échanges, nous avons configuré le serveur avec:

• **Accès utilisateur local uniquement** (pas d’anonymes)
• **Chiffrement SSL/TLS** activé pour sécuriser l’authentification et les transferts
• **Certificat auto-signé** généré pour les connexions FTPS
• **Configuration du mode passif avec plage de ports dédiée**
• **Isolation des utilisateurs via chroot**
• **Contrôle d’accès via fichiers user_list et banned_users**


Structure du repository GitHub

Le repository contient:

- `rapport.pdf`: Le document détaillé du projet, incluant les étapes de configuration, les tests effectués, les captures d’écran et les résultats obtenus.
- `diapositive.pptx`: Une présentation synthétique du projet (max. 15 slides), pour accompagner une éventuelle soutenance orale.
- `README.md`: Ce fichier explicatif, donnant une vue d’ensemble du projet et de son fonctionnement.


Étapes clés de mise en œuvre

1. Installation de `vsftpd` via `apt`
2. Configuration du fichier `/etc/vsftpd.conf` selon les bonnes pratiques
3. Génération du certificat SSL auto-signé avec OpenSSL
4. Création des comptes utilisateurs FTP avec restriction de répertoire

5. Tests de connexion via FileZilla et `lftp` (avec prise en compte du certificat auto-signé)


Pourquoi vsftpd?

Nous avons opté pour vsftpd pour sa réputation en matière de sécurité, sa légèreté et sa stabilité en environnement Linux. Il est également largement documenté, ce qui facilite sa mise en œuvre dans un cadre pédagogique.


Conclusion

Ce projet nous a permis de comprendre les enjeux liés aux transferts de fichiers en réseau, et d'apprendre à sécuriser un service réseau en prenant en compte les contraintes techniques et les bonnes pratiques de cybersécurité. Le serveur FTP mis en place fonctionne comme attendu et peut être réutilisé dans d'autres environnements.

````

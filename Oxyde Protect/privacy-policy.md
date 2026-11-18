# Politique de Confidentialité – OXYDE Protect

**Dernière mise à jour : 18 Novembre 2026.**

Cette politique explique quelles données personnelles sont traitées par le bot Discord **OXYDE Protect** (et ses déclinaisons : bot personnalisé, etc.), pourquoi, où elles sont stockées, combien de temps, et comment exercer vos droits.

Elle couvre le bot lui-même ainsi que les services web qui lui sont directement rattachés : pages de transcripts de tickets, page de vérification captcha, stockage des preuves de signalements et envoi des alertes e-mail. Le site oxyde-bots.xyz en tant que tel (dashboard, connexion Discord, cookies de session, chat de support) fait l'objet de sa propre politique de confidentialité. Le bot musical est un service distinct de OXYDE Protect : il n'est pas couvert par ce document.

## Sommaire

1. [Responsable du traitement et rôles](#1-responsable-du-traitement-et-rôles)
2. [Données traitées](#2-données-traitées)
3. [Messages : lecture et conservation](#3-messages--lecture-et-conservation)
4. [Finalités et bases légales](#4-finalités-et-bases-légales)
5. [Destinataires, sous-traitants et transferts hors UE](#5-destinataires-sous-traitants-et-transferts-hors-ue)
6. [Durées de conservation](#6-durées-de-conservation)
7. [Sécurité](#7-sécurité)
8. [Décisions automatisées](#8-décisions-automatisées)
9. [Vos droits](#9-vos-droits)
10. [Mineurs](#10-mineurs)
11. [Modifications](#11-modifications)
12. [Contact et réclamation](#12-contact-et-réclamation)

***

## 1. Responsable du traitement et rôles

OXYDE Protect est édité par **Oxyde™ Groupe Bot's** (« **nous** »). Le projet est actuellement développé et exploité par plusieurs personnes physiques, sans structure juridique propre à ce jour. Les membres de l'équipe ont des situations personnelles et professionnelles différentes. Dans l'attente de la création éventuelle d'une structure juridique, les obligations relatives aux traitements de données sont assumées par les personnes qui déterminent effectivement leurs finalités et leurs moyens. Lorsque plusieurs personnes déterminent conjointement les finalités et les moyens d'un traitement, leur responsabilité conjointe est appréciée conformément à l'article 26 du RGPD ; elle ne découle pas automatiquement du fait de participer au développement ou à l'exploitation du projet.

* **Contact unique** pour toute question ou exercice de droits : [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz). Ce contact est relevé par l'équipe.
* **Identité** : pour éviter l'exposition de personnes privées, leurs noms ne sont pas publiés ici. Leur identité peut être communiquée aux autorités compétentes dans le cadre de leurs missions. Les demandes relatives à l'identité du responsable du traitement peuvent être adressées au contact indiqué ci-dessus ; nous y répondons dans le cadre de l'exercice de vos droits.
* Si une structure juridique est créée, cette politique sera mise à jour pour l'identifier.

Nous attirons votre attention sur le fait que l'absence de publication des noms ne dispense pas du respect de l'article 13 du RGPD. L'adresse privacy@oxyde-bots.xyz permet à toute personne concernée d'obtenir les informations requises sur le responsable du traitement.

Le bot est utilisé par des administrateurs de serveurs Discord pour protéger leur communauté. Nos rôles au sens du RGPD dépendent donc du traitement :

| Situation | Qui décide des finalités ? | Notre rôle |
| - | - | - |
| Traitement des membres d'un serveur pour faire tourner les fonctions que l'administrateur configure (modération, sanctions, logs, tickets, bienvenue, captcha, anti-raid…) | L'administrateur / propriétaire du serveur | **Sous-traitant** |
| Alertes e-mail, blacklist communautaire, gestion des serveurs qui utilisent le bot, supervision technique, prévention des abus du service | Nous | **Responsable du traitement** |

Les administrateurs de serveurs restent responsables d'informer leurs membres de l'usage d'un bot de sécurité (voir les [Conditions d'Utilisation](https://docs.oxyde-bots.xyz/tos.md)).

***

## 2. Données traitées

### 2.1 Identifiants et configuration

| Donnée | Utilité |
| - | - |
| Identifiants Discord : serveurs, salons, rôles, utilisateurs, messages | Cibler les sanctions, appliquer les permissions et les configurations. |
| Configuration du serveur : modules activés, préfixe, salons de logs, messages de bienvenue et d'au revoir, autorôles, rôles protégés, listes blanches (utilisateurs, rôles, salons), mots interdits AutoMod | Faire fonctionner le bot comme configuré. |
| Textes libres saisis par les administrateurs (messages personnalisés, embeds, questions de tickets, etc.) | Afficher vos contenus personnalisés. |

La configuration d'un serveur est partagée entre le bot public OXYDE Protect et un éventuel bot personnalisé du même serveur.

### 2.2 Modération et protection

| Donnée | Précisions |
| - | - |
| Sanctions et avertissements | ID du membre, ID du modérateur, serveur, motif, date, type |
| Logs d'infraction et actions du bot | Historique des détections et sanctions (kick, ban, timeout…), avec des extraits de messages et leur contexte lorsque nécessaire pour justifier une sanction |
| Logs du serveur (si activés par l'administrateur) | Membres (arrivées, départs, pseudos, rôles), messages (modifiés, supprimés), vocal, invitations, salons, rôles, etc. Ces logs sont **publiés dans les salons Discord choisis par l'administrateur** ; ils ne sont pas copiés dans notre base |
| Anti-raid / anti-spam | Compteurs et historiques d'actions **conservés en mémoire** le temps de la détection (voir [section 3](#3-messages--lecture-et-conservation)) |
| Anti-scam (si activé) | Liens et images publiés peuvent être analysés (comparaison avec des modèles d'arnaques connus, reconnaissance de texte, empreintes d'images). Les images analysées ne sont pas conservées ; seules des empreintes d'arnaques confirmées servent de référence |
| Anti-token | Les messages et les fichiers texte joints (moins de 1 Mo) sont analysés **en mémoire** pour détecter des jetons d'accès Discord. Rien n'est écrit sur le disque ni conservé ; seuls le nom du fichier et le nombre de jetons trouvés apparaissent dans les logs du serveur |
| Restriction par ancienneté de compte | Âge du compte Discord comparé au seuil configuré par l'administrateur |

### 2.3 Captcha

Lorsqu'un serveur active le captcha, l'ID du membre et l'ID du serveur sont transmis à notre API à l'arrivée du membre, qui est invité à se vérifier via une page web hébergée sur notre site.

Pour détecter les bots, les comportements suspects et les **comptes alternatifs**, la vérification enregistre, en plus de votre ID Discord, de l'ID du serveur et de la date de création de votre compte Discord :

| Catégorie | Données |
| - | - |
| Identifiants d'appareil | Empreinte du navigateur (FingerprintJS) ; identifiant de suivi d'appareil (cookie `_oxyde_tid`) |
| Réseau | Adresse IP (transmise au service de détection **proxycheck.io**, voir section 5) ; détection de VPN ou de proxy et nom du fournisseur ; fuseau horaire déduit de l'IP |
| Indices complémentaires | Fuseau horaire du navigateur ; User-Agent |

Les requêtes vers proxycheck.io sont effectuées depuis nos serveurs situés en Belgique et sont traitées par les serveurs européens de ce prestataire (Royaume-Uni, Allemagne, Finlande, Pologne). Les données sont stockées dans la région où elles sont générées et chiffrées avec chiffrement intégral du disque. Aucun transfert vers le Canada ou Singapour n'est effectué dans le cadre de notre utilisation. Nous désactivons la journalisation des adresses chez ce prestataire : l'adresse IP n'y est pas conservée.

L'adresse IP, l'empreinte du navigateur, l'identifiant du cookie et le User-Agent sont **pseudonymisés** avant d'être enregistrés (hachage HMAC-SHA256 avec une clé secrète) : nous ne les stockons pas en clair. Les autres indices (fuseau horaire, fournisseur de VPN détecté) sont enregistrés tels quels. Ils servent à calculer un **score de suspicion**, à marquer un compte comme suspect et à repérer les comptes qui partagent les mêmes identifiants techniques (l'ID des autres comptes concernés est alors enregistré). Ils ne sont utilisés à aucune autre fin : ni publicité, ni revente, ni suivi en dehors de la vérification captcha.

**Le cookie `_oxyde_tid`** n'est déposé que sur la page de vérification captcha, **et seulement après que vous avez cliqué sur « Accepter et continuer »** : avant cet accord, ni le cookie, ni l'empreinte du navigateur ne sont déposés ou enregistrés. Si vous refusez, aucune donnée n'est collectée, mais la vérification automatique ne peut pas aboutir (le staff du serveur peut alors vous vérifier manuellement). Ce cookie ne sert pas de confort : il sert uniquement à la sécurité anti-raid. Il expire après un an et vous pouvez le supprimer à tout moment depuis votre navigateur. Supprimer le cookie ne supprime pas, à lui seul, les données déjà enregistrées en base (effacées automatiquement après 30 jours, ou sur demande, voir section 9).

**Base légale et opposition** : le dépôt du cookie `_oxyde_tid` et la lecture de l'empreinte du navigateur reposent sur votre **consentement** (clic sur « Accepter et continuer »). Le reste du traitement captcha (adresse IP, score de suspicion, détection de VPN ou de proxy, rapprochement des comptes) repose sur notre **intérêt légitime** de protéger les serveurs contre les raids et les comptes malveillants (voir section 4). Vous pouvez vous opposer à ce traitement et demander l'effacement de vos données captcha à tout moment (section 9). Retirer l'application de votre compte Discord n'efface pas ces données ; passez par une demande à [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz).

Ces données sont **supprimées automatiquement au bout de 30 jours**.

### 2.4 Bienvenue et au revoir

Pour générer les bannières d'accueil, le pseudo, l'avatar et le nombre de membres sont envoyés à notre API interne de génération d'images, qui renvoie l'image au bot. Ces données ne servent qu'à cette génération.

### 2.5 Tickets et transcripts

| Donnée | Précisions |
| - | - |
| Configuration des systèmes de tickets | Salons, catégories, rôles staff, questions, embeds |
| Contenu du ticket | Messages, pièces jointes, réponses aux formulaires, ID du créateur (stocké dans le sujet du salon), participants |
| **Transcript HTML** | Généré à la fermeture d'un ticket. Il est envoyé dans le salon de logs du serveur **et hébergé sur notre site**, à une adresse de la forme `oxyde-bots.xyz/ticket/<id-serveur>/<fichier>.html` dont le nom de fichier contient un jeton aléatoire de 128 bits non devinable. **L'accès exige une authentification Discord (OAuth2)**. Chaque accès est journalisé et notifié au propriétaire du serveur dans son salon de logs. Aucune copie n'est conservée sur le serveur du bot (fichier temporaire supprimé juste après l'envoi) |
| **Transcript HTML en message privé** | À la demande d'un membre, le bot génère un transcript HTML du ticket et l'envoie directement en message privé à l'utilisateur concerné via Discord. Le fichier n'est hébergé ni sur notre site ni sur un service tiers : il transite uniquement par l'infrastructure Discord. L'utilisateur est seul responsable de la conservation et du partage de ce fichier |
| Durée | **30 jours** après la génération, suppression automatique sur le site. Le propriétaire du serveur peut demander la suppression anticipée à tout moment |

Deux canaux de transcript existent : (a) l'hébergement sur notre site avec accès authentifié et suppression automatique à 30 jours ; (b) l'envoi direct en message privé à l'utilisateur, sans conservation de notre côté.

### 2.6 Temps vocal (optionnel)

Si l'administrateur active le suivi du temps vocal : ID du serveur, ID du membre, temps cumulé et dernière connexion vocale. Il peut être réinitialisé par les administrateurs.

### 2.7 Alertes anti-raid par e-mail (optionnel)

Lié à votre compte Discord (et non à un serveur) et **seulement si vous l'ajoutez vous-même** :

* votre **adresse e-mail**, **chiffrée (AES-256-GCM)** dans notre base ;
* un **code de vérification** à 6 chiffres envoyé par e-mail ;
* votre ID Discord et l'état de vérification.

Quand une attaque est bloquée sur un serveur dont vous êtes propriétaire, un e-mail d'alerte est envoyé. Il contient : nom du serveur, heure, motif, action effectuée, et des informations sur **l'utilisateur sanctionné** (pseudo, ID, avatar).

L'envoi passe par le relais SMTP de **Brevo** (sous-traitant, France) : votre adresse transite par ce service au moment de l'envoi et peut apparaître dans ses journaux d'envoi, conservés selon sa propre politique. **Nous n'y enregistrons aucun contact** et nous n'utilisons pas votre adresse à des fins commerciales. Une adresse que vous n'avez pas confirmée avec le code reçu est supprimée automatiquement après 24 heures.

### 2.8 Blacklist communautaire et signalements

Un administrateur peut signaler un utilisateur avec la commande `/report`. Sont alors traités :

* l'ID de la personne **signalée** et l'ID du **signalant** ;
* le **motif** et **1 à 3 images de preuve** ;
* le statut du dossier (en attente, accepté, refusé).

Fonctionnement :

1. Le signalement est examiné par le staff d'OXYDE Protect. Pendant l'examen, les preuves sont dans un espace de stockage **privé** que seul le staff habilité peut consulter.
2. Si le signalement est **accepté**, les preuves sont déplacées vers un espace de stockage **public** (`cdn.oxyde-bots.xyz`) : **toute personne disposant du lien peut les ouvrir**. Les liens contiennent un identifiant aléatoire (UUID) non devinable et le listing du stockage est désactivé : les preuves ne peuvent pas être retrouvées sans le lien. Une fois les preuves publiées, nous ne pouvons pas garantir qu'elles ne seront pas recopiées ou indexées par des tiers ; elles restent toutefois accessibles uniquement via un lien non devinable et le listing est désactivé. Le signalant et la personne signalée reçoivent un message privé avec le motif et les liens.
3. Les serveurs qui ont **activé** la blacklist reçoivent une alerte (motif et preuves) lorsqu'un utilisateur blacklisté les rejoint, et le bot peut **le bannir automatiquement** ou seulement l'alerter, selon le réglage du serveur.

La personne signalée est informée par message privé au moment où le signalement est accepté, en même temps que la publication des preuves : aucun délai de contestation préalable n'est prévu, car la mesure vise à protéger rapidement les serveurs contre des comportements nuisibles (raids, arnaques). Elle peut contester ensuite à tout moment et obtenir le réexamen de son dossier ou le retrait des preuves (voir ci-dessous et section 9).

Si vous êtes blacklisté et estimez que c'est une erreur, contestez via le [serveur de support](https://discord.gg/uJC8QR9Yky) ou par e-mail : chaque contestation est réexaminée par un membre du staff. Vous pouvez aussi demander la suppression des preuves publiques (section 9).

Un mécanisme séparé permet aussi d'empêcher certains utilisateurs ou serveurs d'utiliser le bot (liste d'interdits d'accès, comprenant l'ID concerné).

### 2.9 Liaison de serveurs

Si deux serveurs sont liés : ID des serveurs, ID de leurs propriétaires, date d'ajout, et état des demandes de liaison (en attente, acceptée, refusée).

### 2.10 Informations sur les serveurs qui utilisent le bot

Lorsque le bot est ajouté à un serveur ou en est retiré, une notification est envoyée dans un salon **interne** de notre équipe : nom et ID du serveur, propriétaire (mention et ID), date de création, nombre de membres, langue, options (partenaire, vérifié).

À l'ajout, **une invitation permanente** vers un salon textuel du serveur peut être créée et transmise à ce salon interne, afin que nous puissions intervenir **à la demande du propriétaire** (raid, assistance). Les administrateurs peuvent la supprimer à tout moment depuis les paramètres d'invitations de leur serveur.

Certaines détections graves (par exemple un spam massif) déclenchent aussi une alerte interne comprenant le nom et l'ID du serveur et de l'utilisateur concerné.

### 2.11 Commandes d'information

Les commandes de type `userinfo` ou `invites` envoient l'ID (ou le code d'invitation) demandé à notre API interne pour renvoyer des informations **publiques** Discord.

### 2.12 Données techniques et supervision

| Donnée | Précisions |
| - | - |
| Métriques d'exploitation (ClickHouse) | Pour chaque appel à l'API Discord : méthode, route (pouvant contenir des ID de serveur et de salon), code de statut, latence, limites de débit, messages d'erreur. **Pas de contenu de messages**. Conservées **30 jours** |
| Compteurs globaux | Nombre de commandes, de messages traités, de tickets et d'alertes anti-raid (chiffres agrégés) |
| Journaux d'erreurs | Fichiers d'erreurs techniques (message d'erreur et trace) sur nos serveurs. Conservés **7 à 30 jours** |
| Journaux d'exploitation | Événements d'exploitation (par exemple sanctions et détections), pouvant mentionner des pseudos et des ID. Ils apparaissent dans la console du bot, qui ne garde qu'un historique glissant : conservés environ **2 jours** selon l'activité, et effacés au plus tard au redémarrage |

### 2.13 Notifications internes de l'équipe

Pour l'exploitation du service et la prévention des abus, des notifications sont envoyées dans un **salon privé Discord de l'équipe** :

* **À chaque connexion au dashboard** : pseudo, ID Discord, nom affiché, serveur concerné, adresse IP dont la fin est masquée, date et heure.
* **Quand le captcha détecte un double compte ou un VPN/proxy** : ID du membre, ID du serveur, score de suspicion, ID du compte en conflit et signaux concordants, fournisseur de VPN détecté.

Ces notifications servent aux mêmes finalités de sécurité que le captcha. Elles sont conservées **90 jours au maximum**, puis supprimées.

***

## 3. Messages : lecture et conservation

Le bot reçoit le contenu des messages de votre serveur (accès « Message Content » de Discord) pour exécuter les commandes à préfixe et les protections (spam, liens, mentions de masse, mots interdits…). Ce contenu est **analysé en mémoire** et **n'est pas enregistré dans notre base de données**, sauf dans les cas suivants :

| Cas | Ce qui est conservé ou republié | Où | Durée |
| - | - | - | - |
| Anti-spam : détection d'un spammeur | Extraits des derniers messages du salon (jusqu'à 7), pouvant inclure des messages d'autres membres | Envoyés uniquement dans le salon de logs anti-spam du serveur (créé automatiquement si absent). **Aucune copie n'est hébergée sur notre site** | Selon le serveur |
| Anti-ghostping (si activé) | Contenu du message supprimé contenant une mention | Republié dans le salon concerné | Selon le serveur |
| Commande `snipe` | Derniers messages supprimés (10 max par salon), avec auteur, avatar et première pièce jointe | **Mémoire vive** uniquement | 1 heure maximum, effacé au redémarrage |
| Signalements anti-lien | Données de détection de liens | Base de données | **Supprimées chaque jour à 1 h (Europe/Paris)** |
| Logs de messages (si activés) | Messages modifiés ou supprimés | Salon Discord choisi par l'administrateur | Selon le serveur |
| Logs d'infraction | Extrait du message avec contexte | Logs du serveur | Selon le serveur |
| Tickets | Voir section 2.5 | Salon de logs, notre site | 30 jours côté site |

***

## 4. Finalités et bases légales

| Finalité | Base légale |
| - | - |
| Fournir les fonctions du bot configurées par les administrateurs (modération, tickets, logs, bienvenue…) | Exécution du contrat ou du service demandé par l'administrateur (art. 6.1.b) pour les données nécessaires au fonctionnement ; intérêt légitime (art. 6.1.f) pour les fonctionnalités de sécurité configurées par l'administrateur |
| Protéger les serveurs contre les raids, spams, arnaques et comptes malveillants | Intérêt légitime (sécurité des communautés et des membres), avec droit d'opposition (section 9) |
| Captcha : dépôt du cookie `_oxyde_tid` et lecture de l'empreinte du navigateur | **Consentement** (clic sur « Accepter et continuer »), retirable à tout moment |
| Captcha : reste du traitement (adresse IP, score de suspicion, détection de VPN ou de proxy, rapprochement de comptes) | **Intérêt légitime** (sécurité des communautés et des membres), avec droit d'opposition (section 9) |
| Blacklist communautaire | Intérêt légitime, avec validation manuelle par le staff et droit de contestation |
| Alertes anti-raid par e-mail | Consentement (vous l'ajoutez et le vérifiez vous-même ; retirable à tout moment) |
| Supervision technique, correction des erreurs, prévention des abus du service | Intérêt légitime |
| Notifications internes de l'équipe (section 2.13) | Intérêt légitime (sécurité du service et prévention des abus) |
| Répondre aux demandes de support et exercer vos droits | Obligation légale et intérêt légitime |

Nous **ne vendons aucune donnée** et ne les utilisons **ni pour de la publicité, ni à des fins commerciales**.

***

## 5. Destinataires, sous-traitants et transferts hors UE

| Destinataire | Rôle | Pays | Données concernées |
| - | - | - | - |
| [Discord Inc.](https://discord.com/privacy) | Plateforme sur laquelle fonctionne le bot | États-Unis (hors UE) | Toutes les données échangées via Discord |
| [MiridiaHost SASU](https://miridiahost.fr/) | Hébergement du bot musical (service distinct) | France | Hors périmètre de cette politique |
| [UpCloud Oy](https://upcloud.com/) | Hébergement d'OXYDE Protect (bot et base de données) ; société établie en Finlande | États-Unis (hors UE) | Serveurs qui font fonctionner le bot et stockent la base de données |
| Infrastructure privée (serveur Dell PowerEdge R630, réseau Proximus) | Hébergement auto-géré, notamment pour l'échange de fichiers avec le site | Belgique | Fichiers de transcripts et services associés |
| [Cloudflare Inc.](https://www.cloudflare.com/) | Protection réseau et anti-DDoS | États-Unis (hors UE) | Trafic vers nos services web (dont adresses IP) |
| [Brevo](https://www.brevo.com/fr/) | Envoi des e-mails par relais SMTP (sous-traitant) | France | Adresse e-mail, contenu de l'alerte (aucun contact enregistré) |
| [proxycheck.io](https://proxycheck.io/privacy/) | Détection de VPN et de proxy lors du captcha (sous-traitant) | Royaume-Uni, Allemagne, Finlande, Pologne (Europe) | Adresse IP du membre qui se vérifie |
| Administrateurs du serveur | Responsables de leur communauté | | Logs, sanctions, transcripts de leur serveur |
| Équipe et staff habilité d'OXYDE Protect | Exploitation, support, modération des signalements | | Accès limité au strict nécessaire |

**proxycheck.io** : ce service exploite son propre matériel physique et ne fait appel à aucun sous-traitant pour la gestion de ses serveurs. Les données sont stockées dans la région où elles sont générées : nos requêtes étant effectuées depuis la Belgique, elles sont traitées et stockées uniquement sur les serveurs européens de ce prestataire (Royaume-Uni, Allemagne, Finlande, Pologne). Les données sont chiffrées avec chiffrement intégral du disque. Aucun transfert vers le Canada ou Singapour n'est effectué dans le cadre de notre utilisation.

Les transcripts HTML envoyés en message privé transitent par Discord Inc. (États-Unis), déjà listé ci-dessus. Aucun autre tiers n'intervient dans ce processus.

Pour chaque sous-traitant hors UE, nous vérifions l'existence d'un mécanisme de transfert conforme au chapitre V du RGPD (décision d'adéquation ou clauses contractuelles types).

**Base de données** : notre base MongoDB est un logiciel **auto-hébergé sur notre propre infrastructure** : celle d'OXYDE Protect est hébergée chez UpCloud, aux États-Unis. Nous n'utilisons pas de service de base de données hébergé par MongoDB Inc. ; cette société n'a donc pas accès à vos données.

**Transferts hors Union européenne** : Discord Inc. et Cloudflare Inc. sont établies aux États-Unis, et les serveurs d'OXYDE Protect (bot et base de données) sont hébergés aux États-Unis chez UpCloud. Les données transmises à ces services ou stockées sur ces serveurs sortent donc de l'UE. Pour UpCloud, dont le contrat de traitement des données (DPA) est intégré à ses conditions, les transferts internationaux reposent, selon le pays, sur des clauses contractuelles types conclues entre les sociétés de son groupe ou sur une décision d'adéquation. Pour les autres prestataires, ces transferts reposent sur les mécanismes prévus par le chapitre V du RGPD (décision d'adéquation du cadre de protection des données UE–États-Unis pour les entreprises certifiées, ou clauses contractuelles types), tels que décrits dans leurs propres politiques. Pour Discord, le transfert est inhérent au fonctionnement d'un bot Discord.

Nous n'autorisons pas ces prestataires à utiliser vos données pour leurs propres finalités, dans la limite de ce que nous pouvons contrôler.

***

## 6. Durées de conservation

| Donnée | Durée |
| - | - |
| Configuration du bot, listes blanches, messages de bienvenue et d'au revoir | Tant que le bot est présent sur le serveur, puis 90 jours après son retrait, ou immédiatement sur demande du propriétaire |
| **Configuration captcha et tickets** | **Supprimées automatiquement quand le bot est retiré du serveur** |
| Autres données du serveur (sanctions, temps vocal, configuration générale…) | Supprimées automatiquement **90 jours après le retrait du bot**, ou immédiatement sur demande du propriétaire du serveur |
| Avertissements et sanctions | Jusqu'à leur suppression par un modérateur ou sur demande, et au plus tard 90 jours après le retrait du bot |
| Temps vocal | Jusqu'à réinitialisation par un administrateur ou suppression sur demande |
| Transcripts de tickets (site) | **30 jours**, suppression automatique ; suppression anticipée sur demande |
| Transcripts HTML envoyés en MP | Aucune copie n'est conservée par nos soins ; la durée de conservation dépend de l'utilisateur et de Discord |
| Adresse IP envoyée à proxycheck.io | Non conservée par ce prestataire (journalisation désactivée) |
| Données de vérification captcha (base de données) | 30 jours, suppression automatique. Le cookie `_oxyde_tid` peut rester dans votre navigateur jusqu'à un an |
| Signalements anti-lien | Supprimés chaque jour |
| Messages supprimés (`snipe`) | 1 heure maximum, en mémoire vive |
| E-mail d'alerte (base de données) | Jusqu'à ce que vous le supprimiez vous-même ou nous le demandiez |
| Adresse e-mail non vérifiée | 24 heures |
| Blacklist : dossiers acceptés | Tant que la mesure reste justifiée, avec réexamen sur demande et revue au plus tard tous les 12 mois |
| Blacklist : dossiers en attente ou refusés | Jusqu'à suppression sur demande |
| Métriques d'exploitation (ClickHouse) | 30 jours |
| Journaux d'erreurs | 7 à 30 jours |
| Journaux d'exploitation (console du bot) | Environ 2 jours selon l'activité, effacés au plus tard au redémarrage |

La conservation d'un dossier blacklisté accepté est réexaminée au moins tous les 12 mois ; la personne concernée peut demander un réexamen ou la suppression à tout moment (section 9).

Pour demander une suppression, voir la section 9.

***

## 7. Sécurité

* Les adresses e-mail sont **chiffrées** (AES-256-GCM) dans notre base de données ; les données captcha sensibles (IP, empreinte, cookie, User-Agent) sont **pseudonymisées** par hachage HMAC-SHA256.
* Les jetons d'accès des bots personnalisés sont **chiffrés** (AES-256-GCM) dans notre base de données.
* La base de données est auto-hébergée et **n'est pas accessible depuis Internet** : elle n'est joignable que par un réseau privé (Tailscale), depuis certains de nos hébergements en Europe et par l'équipe de développement. Le staff de modération n'a accès qu'aux preuves des signalements, via un espace protégé par identifiant.
* Les transcripts de tickets sont protégés par une authentification Discord (OAuth2), des adresses non devinables et un journal d'accès notifié au propriétaire du serveur.
* Nos services sont protégés par des systèmes de détection et de prévention d'intrusion et par des services de protection réseau.
* Les preuves d'un signalement en attente sont stockées dans un espace privé.
* En cas de violation de données susceptible d'engendrer un risque élevé pour vos droits et libertés, nous vous informerons dans les meilleurs délais, conformément à l'article 34 du RGPD, ainsi que l'autorité de contrôle compétente (art. 33).

Aucun système n'est infaillible : nous ne pouvons pas garantir une sécurité absolue.

***

## 8. Décisions automatisées

Certaines protections agissent **automatiquement** : bannissement, expulsion, mise en sourdine ou suppression de messages en cas de spam, de raid, de lien interdit ou d'utilisateur blacklisté. Ce sont les administrateurs qui choisissent les modules à activer, leur sévérité et les exceptions (listes blanches).

Si vous pensez avoir été sanctionné à tort, contactez d'abord les modérateurs du serveur concerné. Vous pouvez aussi nous écrire pour demander un réexamen par une personne.

Le captcha calcule en outre un **score de suspicion** et peut marquer un compte comme suspect ou lié à un autre compte (voir section 2.3). Lorsque ce score est élevé, le rôle d'accès au serveur n'est pas attribué automatiquement et les administrateurs sont notifiés ; ils peuvent alors vérifier la personne manuellement et lui accorder l'accès. Cette décision se limite à ne pas accorder automatiquement l'accès à un serveur Discord déterminé. Le score n'est ni publié, ni partagé avec d'autres services, ni utilisé pour une autre finalité. Vous pouvez demander un réexamen humain à tout moment (section 9).

***

## 9. Vos droits

Conformément au RGPD, vous pouvez demander : **l'accès** à vos données, leur **rectification**, leur **effacement**, la **limitation** ou l'**opposition** au traitement, ainsi que la **portabilité** lorsqu'elle s'applique. Pour les traitements fondés sur le consentement (alertes e-mail, cookie `_oxyde_tid` et empreinte du navigateur), vous pouvez le retirer à tout moment.

Cas particuliers :

* **Propriétaire d'un serveur** : vous pouvez demander la purge des configurations, logs, sanctions et transcripts de votre serveur.
* **E-mail** : vous pouvez le supprimer vous-même depuis l'interface e-mail du bot ; la suppression retire l'adresse de notre base.
* **Personne blacklistée ou signalée** : vous pouvez demander l'accès à votre dossier, sa rectification, son réexamen ou sa suppression, y compris le retrait des preuves du stockage public.
* **Données captcha** : vous pouvez vous opposer au traitement et demander l'effacement de vos données de vérification avant les 30 jours.
* **Cookie et empreinte (captcha)** : pour le cookie `_oxyde_tid` et l'empreinte du navigateur, vous pouvez retirer votre consentement à tout moment en supprimant le cookie et en nous écrivant pour demander l'effacement des données déjà enregistrées.
* **Membre d'un serveur** : pour les données traitées pour le compte d'un serveur, adressez-vous d'abord à ses administrateurs, qui sont responsables du traitement ; nous les aidons à répondre.

**Comment faire** : écrivez à [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz) ou ouvrez un ticket sur notre [serveur de support](https://discord.gg/uJC8QR9Yky), en indiquant l'ID Discord (et l'ID du serveur) concerné. Nous pouvons vous demander de prouver que vous êtes bien la personne concernée. Nous répondons dans un délai d'**un mois**, prorogeable de deux mois en cas de demande complexe (art. 12.3 RGPD). Vous pouvez à tout moment introduire une réclamation auprès de l'autorité de contrôle (voir section 12).

***

## 10. Mineurs

Le bot s'adresse aux utilisateurs qui ont l'âge minimum requis par Discord pour utiliser la plateforme. Nous ne cherchons pas à collecter sciemment des données de personnes n'ayant pas cet âge. Si vous pensez qu'une telle donnée nous a été transmise, contactez-nous pour la faire supprimer. Si vous êtes mineur, nous vous invitons à ne pas nous transmettre de données personnelles sans l'accord de votre représentant légal.

***

## 11. Modifications

Nous pouvons mettre à jour cette politique. La date de dernière mise à jour figure en haut du document. Les modifications importantes sont annoncées sur notre serveur de support. En cas de modification substantielle, nous vous informerons par un moyen approprié (annonce sur le serveur de support, notification dans le bot).

***

## 12. Contact et réclamation

* **E-mail (données personnelles)** : [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz)
* **Discord** : [serveur de support](https://discord.gg/uJC8QR9Yky)

Si vous estimez que vos droits ne sont pas respectés, vous pouvez introduire une réclamation auprès de l'autorité de protection des données de votre pays. En Belgique : l'[Autorité de protection des données](https://www.autoriteprotectiondonnees.be). En France : la [CNIL](https://www.cnil.fr). Vous pouvez introduire une réclamation auprès de l'autorité de contrôle de votre lieu de résidence habituel, de votre lieu de travail ou du lieu de la violation présumée.

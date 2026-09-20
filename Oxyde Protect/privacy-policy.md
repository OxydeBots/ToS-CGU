# Politique de Confidentialité – OXYDE Protect

**Dernière mise à jour : 20 septembre 2026**

Cette politique explique quelles données personnelles sont traitées par le bot Discord **OXYDE Protect** (et ses déclinaisons : bot personnalisé, etc.), pourquoi, où elles sont stockées, combien de temps, et comment exercer vos droits.

Elle couvre le bot lui-même ainsi que les services web qui lui sont directement rattachés : pages de transcripts de tickets, page de vérification captcha, stockage des preuves de signalements et envoi des alertes e-mail. Le site oxyde-bots.xyz en tant que tel (dashboard, connexion Discord, cookies de session, chat de support) fait l'objet de sa propre politique de confidentialité.

## Sommaire

1. [Responsable du traitement et rôles](#1-responsable-du-traitement-et-rôles)
2. [Données traitées](#2-données-traitées)
3. [Messages : lecture et conservation](#3-messages--lecture-et-conservation)
4. [Finalités et bases légales](#4-finalités-et-bases-légales)
5. [Destinataires et sous-traitants](#5-destinataires-et-sous-traitants)
6. [Durées de conservation](#6-durées-de-conservation)
7. [Sécurité](#7-sécurité)
8. [Décisions automatisées](#8-décisions-automatisées)
9. [Vos droits](#9-vos-droits)
10. [Mineurs](#10-mineurs)
11. [Modifications](#11-modifications)
12. [Contact et réclamation](#12-contact-et-réclamation)

---

## 1. Responsable du traitement et rôles

OXYDE Protect est édité par **Oxyde™ Groupe Bot's** (« **nous** »), un projet qui **n'a pour l'instant pas de personnalité juridique** (ni société, ni association). Les deux personnes qui l'éditent et l'exploitent, l'une résidant en Belgique et l'autre en France, agissent donc elles-mêmes en tant que **responsables conjoints du traitement**. Vous pouvez exercer vos droits auprès de l'une ou de l'autre en passant par le contact ci-dessous. Contact : [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz). Si une structure juridique est créée, cette politique sera mise à jour pour l'identifier.

Le bot est utilisé par des administrateurs de serveurs Discord pour protéger leur communauté. Nos rôles au sens du RGPD dépendent donc du traitement :

| Situation | Qui décide des finalités ? | Notre rôle |
|---|---|---|
| Traitement des membres d'un serveur pour faire tourner les fonctions que l'administrateur configure (modération, sanctions, logs, tickets, bienvenue, captcha, anti-raid…) | L'administrateur / propriétaire du serveur | **Sous-traitant** |
| Alertes e-mail, blacklist communautaire, gestion des serveurs qui utilisent le bot, supervision technique, prévention des abus du service | Nous | **Responsable du traitement** |

Les administrateurs de serveurs restent responsables d'informer leurs membres de l'usage d'un bot de sécurité (voir les [Conditions d'Utilisation](CGU.md)).

---

## 2. Données traitées

### 2.1 Identifiants et configuration

| Donnée | Utilité |
|---|---|
| Identifiants Discord : serveurs, salons, rôles, utilisateurs, messages | Cibler les sanctions, appliquer les permissions et les configurations |
| Configuration du serveur : modules activés, préfixe, salons de logs, messages de bienvenue et d'au revoir, autorôles, rôles protégés, listes blanches (utilisateurs, rôles, salons), mots interdits AutoMod | Faire fonctionner le bot comme configuré |
| Textes libres saisis par les administrateurs (messages personnalisés, embeds, questions de tickets, etc.) | Afficher vos contenus personnalisés |

La configuration d'un serveur est partagée entre le bot public OXYDE Protect et un éventuel bot personnalisé du même serveur.

### 2.2 Modération et protection

| Donnée | Précisions |
|---|---|
| Sanctions et avertissements | ID du membre, ID du modérateur, serveur, motif, date, type |
| Logs d'infraction et actions du bot | Historique des détections et sanctions (kick, ban, timeout…), avec des extraits de messages et leur contexte lorsque nécessaire pour justifier une sanction |
| Logs du serveur (si activés par l'administrateur) | Membres (arrivées, départs, pseudos, rôles), messages (modifiés, supprimés), vocal, invitations, salons, rôles, etc. Ces logs sont **publiés dans les salons Discord choisis par l'administrateur** ; ils ne sont pas copiés dans notre base |
| Anti-raid / anti-spam | Compteurs et historiques d'actions **conservés en mémoire** le temps de la détection (voir [section 3](#3-messages--lecture-et-conservation)) |
| Anti-scam (si activé) | Liens et images publiés peuvent être analysés (comparaison avec des modèles d'arnaques connus, reconnaissance de texte, empreintes d'images). Les images analysées ne sont pas conservées ; seules des empreintes d'arnaques confirmées servent de référence |
| Restriction par ancienneté de compte | Âge du compte Discord comparé au seuil configuré par l'administrateur |

### 2.3 Captcha

Lorsqu'un serveur active le captcha, l'ID du membre et l'ID du serveur sont transmis à notre API à l'arrivée du membre, qui est invité à se vérifier via une page web hébergée sur notre site.

Pour détecter les bots, les comportements suspects et les **comptes alternatifs**, la vérification enregistre, en plus de votre ID Discord, de l'ID du serveur et de la date de création de votre compte Discord :

| Catégorie | Données |
|---|---|
| Identifiants d'appareil | Empreinte du navigateur (FingerprintJS) ; identifiant de suivi d'appareil (cookie `_oxyde_tid`) |
| Réseau | Adresse IP ; détection de VPN ou de proxy et nom du fournisseur ; fuseau horaire déduit de l'IP |
| Indices complémentaires | Fuseau horaire du navigateur ; User-Agent |

Ces éléments sont **chiffrés** dans notre base de données. Ils servent à calculer un **score de suspicion**, à marquer un compte comme suspect et à repérer les comptes qui partagent les mêmes identifiants techniques (l'ID des autres comptes concernés est alors enregistré). Ils ne sont utilisés à aucune autre fin.

Ces données sont **supprimées automatiquement au bout de 30 jours**. Le cookie `_oxyde_tid` reste dans votre navigateur jusqu'à un an ; vous pouvez le supprimer à tout moment.

### 2.4 Bienvenue et au revoir

Pour générer les bannières d'accueil, le pseudo, l'avatar et le nombre de membres sont envoyés à notre API interne de génération d'images, qui renvoie l'image au bot. Ces données ne servent qu'à cette génération.

### 2.5 Tickets et transcripts

| Donnée | Précisions |
|---|---|
| Configuration des systèmes de tickets | Salons, catégories, rôles staff, questions, embeds |
| Contenu du ticket | Messages, pièces jointes, réponses aux formulaires, ID du créateur (stocké dans le sujet du salon), participants |
| **Transcript HTML** | Généré à la fermeture d'un ticket. Il est envoyé dans le salon de logs du serveur **et hébergé sur notre site** à une adresse de la forme `oxyde-bots.xyz/ticket/<id-serveur>/<fichier>.html`. **Toute personne disposant du lien peut ouvrir la page.** Une copie est aussi présente sur le serveur du bot |
| Transcript texte via Sourcebin | Si un membre clique sur le bouton de transcript en message privé, le texte du ticket (pseudos, IDs, contenus) est publié sur le service tiers **Sourcebin** ; un lien vous est ensuite envoyé |

Ne partagez pas un lien de transcript avec des tiers si le ticket contient des informations personnelles.

### 2.6 Temps vocal (optionnel)

Si l'administrateur active le suivi du temps vocal : ID du serveur, ID du membre, temps cumulé et dernière connexion vocale. Il peut être réinitialisé par les administrateurs.

### 2.7 Alertes anti-raid par e-mail (optionnel)

Lié à votre compte Discord (et non à un serveur) et **seulement si vous l'ajoutez vous-même** :

- votre **adresse e-mail**, **chiffrée (AES-256-GCM)** dans notre base ;
- un **code de vérification** à 6 chiffres envoyé par e-mail ;
- votre ID Discord et l'état de vérification.

Quand une attaque est bloquée sur un serveur dont vous êtes propriétaire, un e-mail d'alerte est envoyé. Il contient : nom du serveur, heure, motif, action effectuée, et des informations sur **l'utilisateur sanctionné** (pseudo, ID, avatar).

L'envoi passe par **Brevo** : votre adresse y est enregistrée comme contact pour permettre l'envoi (le chiffrement AES-256-GCM concerne notre base de données, pas ce compte). **Supprimer votre e-mail dans le bot supprime aussi ce contact chez Brevo.** Nous n'utilisons pas ces contacts à des fins commerciales.

### 2.8 Blacklist communautaire et signalements

Un administrateur peut signaler un utilisateur avec la commande `/report`. Sont alors traités :

- l'ID de la personne **signalée** et l'ID du **signalant** ;
- le **motif** et **1 à 3 images de preuve** ;
- le statut du dossier (en attente, accepté, refusé).

Fonctionnement :

1. Le signalement est examiné par le staff d'OXYDE Protect. Pendant l'examen, les preuves sont dans un espace de stockage **privé** que seul le staff habilité peut consulter.
2. Si le signalement est **accepté**, les preuves sont déplacées vers un espace de stockage **public** (`cdn.oxyde-bots.xyz`) : **toute personne disposant du lien peut les ouvrir**. Le signalant et la personne signalée reçoivent un message privé avec le motif et les liens.
3. Les serveurs qui ont **activé** la blacklist reçoivent une alerte (motif et preuves) lorsqu'un utilisateur blacklisté les rejoint, et le bot peut **le bannir automatiquement** ou seulement l'alerter, selon le réglage du serveur.

Si vous êtes blacklisté et estimez que c'est une erreur, contestez via le [serveur de support](https://discord.gg/uJC8QR9Yky) ou par e-mail : chaque contestation est réexaminée par un membre du staff.

Un mécanisme séparé permet aussi d'empêcher certains utilisateurs ou serveurs d'utiliser le bot (liste d'interdits d'accès, comprenant l'ID concerné).

### 2.9 Liaison de serveurs

Si deux serveurs sont liés : ID des serveurs, ID de leurs propriétaires, date d'ajout, et état des demandes de liaison (en attente, acceptée, refusée).

### 2.10 Informations sur les serveurs qui utilisent le bot

Lorsque le bot est ajouté à un serveur ou en est retiré, une notification est envoyée dans un salon **interne** de notre équipe : nom et ID du serveur, propriétaire (mention et ID), date de création, nombre de membres, langue, options (partenaire, vérifié).

À l'ajout, **une invitation permanente** vers un salon textuel du serveur peut être créée et transmise à ce salon interne, afin que nous puissions intervenir en cas de raid ou d'assistance. Les administrateurs peuvent la supprimer à tout moment depuis les paramètres d'invitations de leur serveur.

Certaines détections graves (par exemple un spam massif) déclenchent aussi une alerte interne comprenant le nom et l'ID du serveur et de l'utilisateur concerné.

### 2.11 Commandes d'information

Les commandes de type `userinfo` ou `invites` envoient l'ID (ou le code d'invitation) demandé à notre API interne pour renvoyer des informations **publiques** Discord.

### 2.12 Données techniques et supervision

| Donnée | Précisions |
|---|---|
| Métriques d'exploitation (ClickHouse) | Pour chaque appel à l'API Discord : méthode, route (pouvant contenir des ID de serveur et de salon), code de statut, latence, limites de débit, messages d'erreur. **Pas de contenu de messages** |
| Compteurs globaux | Nombre de commandes, de messages traités, de tickets et d'alertes anti-raid (chiffres agrégés) |
| Journaux d'erreurs | Fichiers d'erreurs techniques (message d'erreur et trace) sur nos serveurs |
| Journaux d'exploitation | Événements d'exploitation (par exemple sanctions et détections), pouvant mentionner des pseudos et des ID |

---

## 3. Messages : lecture et conservation

Le bot reçoit le contenu des messages de votre serveur (accès « Message Content » de Discord) pour exécuter les commandes à préfixe et les protections (spam, liens, mentions de masse, mots interdits…). Ce contenu est **analysé en mémoire** et **n'est pas enregistré dans notre base de données**, sauf dans les cas suivants :

| Cas | Ce qui est conservé ou republié | Où | Durée |
|---|---|---|---|
| Anti-spam : détection d'un spammeur | Transcript des derniers messages du salon (jusqu'à 7), pouvant inclure des messages d'autres membres | Salon de logs anti-spam du serveur (créé automatiquement si absent), et copie sur notre site accessible par lien | Jusqu'à suppression |
| Anti-ghostping (si activé) | Contenu du message supprimé contenant une mention | Republié dans le salon concerné | Selon le serveur |
| Commande `snipe` | Derniers messages supprimés (10 max par salon), avec auteur, avatar et première pièce jointe | **Mémoire vive** uniquement | 1 heure maximum, effacé au redémarrage |
| Signalements anti-lien | Données de détection de liens | Base de données | **Supprimées chaque jour à 1 h (Europe/Paris)** |
| Logs de messages (si activés) | Messages modifiés ou supprimés | Salon Discord choisi par l'administrateur | Selon le serveur |
| Logs d'infraction | Extrait du message avec contexte | Logs du serveur | Selon le serveur |
| Tickets | Voir [section 2.5](#25-tickets-et-transcripts) | Salon de logs, notre site, copie serveur | Voir [section 6](#6-durées-de-conservation) |

---

## 4. Finalités et bases légales

| Finalité | Base légale |
|---|---|
| Fournir les fonctions du bot configurées par les administrateurs (modération, tickets, logs, bienvenue…) | Exécution du service demandé par l'administrateur ; intérêt légitime des communautés |
| Protéger les serveurs contre les raids, spams, arnaques et comptes malveillants | Intérêt légitime (sécurité des communautés et des membres) |
| Blacklist communautaire | Intérêt légitime, avec validation manuelle par le staff et droit de contestation |
| Alertes anti-raid par e-mail | Consentement (vous l'ajoutez et le vérifiez vous-même ; retirable à tout moment) |
| Supervision technique, correction des erreurs, prévention des abus du service | Intérêt légitime |
| Répondre aux demandes de support et exercer vos droits | Obligation légale et intérêt légitime |

Nous **ne vendons aucune donnée** et ne les utilisons **ni pour de la publicité, ni à des fins commerciales**.

---

## 5. Destinataires et sous-traitants

| Destinataire | Rôle | Données concernées |
|---|---|---|
| [Discord Inc.](https://discord.com/privacy) | Plateforme sur laquelle fonctionne le bot | Toutes les données échangées via Discord |
| [MiridiaHost SASU](https://miridiahost.fr/) | Hébergement | Serveurs qui font fonctionner le bot et ses services |
| [UpCloud SA](https://upcloud.com/) | Hébergement | Serveurs qui font fonctionner le bot et ses services |
| Infrastructure privée (serveur Dell PowerEdge R630, réseau Proximus, Belgique) | Hébergement auto-géré, notamment pour l'échange de fichiers avec le site | Fichiers de transcripts et services associés |
| [Cloudflare Inc.](https://www.cloudflare.com/) | Protection réseau et anti-DDoS | Trafic vers nos services web |
| [MongoDB Inc.](https://www.mongodb.com/) | Hébergement de la base de données | Configurations, sanctions, e-mails chiffrés, signalements, etc. |
| [Brevo](https://www.brevo.com/fr/) | Envoi des e-mails (sous-traitant conforme au RGPD) | Adresse e-mail, contenu de l'alerte |
| Sourcebin | Publication d'un transcript texte, sur demande du membre | Texte du ticket |
| Administrateurs du serveur | Responsables de leur communauté | Logs, sanctions, transcripts de leur serveur |
| Équipe et staff habilité d'OXYDE Protect | Exploitation, support, modération des signalements | Accès limité au strict nécessaire |

Nous n'autorisons pas ces prestataires à utiliser vos données pour leurs propres finalités, dans la limite de ce que nous pouvons contrôler.

---

## 6. Durées de conservation

| Donnée | Durée |
|---|---|
| Configuration du bot, listes blanches, messages de bienvenue et d'au revoir | Tant que le bot est présent sur le serveur |
| **Configuration captcha et tickets** | **Supprimées automatiquement quand le bot est retiré du serveur** |
| Autres données du serveur (sanctions, temps vocal, configuration générale…) | Conservées **jusqu'à demande de suppression** par le propriétaire du serveur, y compris après retrait du bot |
| Avertissements et sanctions | Jusqu'à leur suppression par un modérateur ou sur demande |
| Temps vocal | Jusqu'à réinitialisation par un administrateur ou suppression sur demande |
| Transcripts de tickets (site et copie serveur) | Sans durée fixe ; suppression à tout moment sur demande du propriétaire du serveur |
| Données de vérification captcha (base de données) | 30 jours, suppression automatique. Le cookie `_oxyde_tid` peut rester dans votre navigateur jusqu'à un an |
| Signalements anti-lien | Supprimés chaque jour |
| Messages supprimés (`snipe`) | 1 heure maximum, en mémoire vive |
| E-mail d'alerte (base de données) | Jusqu'à ce que vous le supprimiez vous-même ou nous le demandiez |
| Contact Brevo | Jusqu'à ce que vous supprimiez votre e-mail dans le bot |
| Blacklist : dossiers acceptés | Tant que la mesure reste justifiée, avec réexamen sur demande |
| Blacklist : dossiers en attente ou refusés | Jusqu'à suppression sur demande |
| Métriques et journaux techniques | Le temps nécessaire au suivi technique et au débogage |

Pour demander une suppression, voir la [section 9](#9-vos-droits).

---

## 7. Sécurité

- Les adresses e-mail sont **chiffrées (AES-256-GCM)** dans notre base de données.
- L'accès à la base de données est réservé à l'équipe de développement. Le staff de modération n'a accès qu'aux preuves des signalements, via un espace protégé par identifiant.
- Nos services sont protégés par des systèmes de détection et de prévention d'intrusion et par des services de protection réseau.
- Les preuves d'un signalement en attente sont stockées dans un espace privé.
- En cas de faille de sécurité affectant vos données, nous vous informerons dans les meilleurs délais, ainsi que l'autorité de contrôle lorsque la loi l'exige.

Aucun système n'est infaillible : nous ne pouvons pas garantir une sécurité absolue.

---

## 8. Décisions automatisées

Certaines protections agissent **automatiquement** : bannissement, expulsion, mise en sourdine ou suppression de messages en cas de spam, de raid, de lien interdit ou d'utilisateur blacklisté. Ce sont les administrateurs qui choisissent les modules à activer, leur sévérité et les exceptions (listes blanches).

Si vous pensez avoir été sanctionné à tort, contactez d'abord les modérateurs du serveur concerné. Vous pouvez aussi nous écrire pour demander un réexamen.

Le captcha calcule en outre un **score de suspicion** et peut marquer un compte comme suspect ou lié à un autre compte (voir [section 2.3](#23-captcha)).

---

## 9. Vos droits

Conformément au RGPD, vous pouvez demander : **l'accès** à vos données, leur **rectification**, leur **effacement**, la **limitation** ou l'**opposition** au traitement, ainsi que la **portabilité** lorsqu'elle s'applique.

Cas particuliers :

- **Propriétaire d'un serveur** : vous pouvez demander la purge des configurations, logs, sanctions et transcripts de votre serveur.
- **E-mail** : vous pouvez le supprimer vous-même depuis l'interface e-mail du bot ; la suppression efface aussi le contact chez Brevo.
- **Personne blacklistée ou signalée** : vous pouvez demander l'accès à votre dossier, sa rectification, son réexamen ou sa suppression.
- **Membre d'un serveur** : pour les données traitées pour le compte d'un serveur, adressez-vous d'abord à ses administrateurs, qui sont responsables du traitement ; nous les aidons à répondre.

**Comment faire** : écrivez à [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz) ou ouvrez un ticket sur notre [serveur de support](https://discord.gg/uJC8QR9Yky), en indiquant l'ID Discord (et l'ID du serveur) concerné. Nous pouvons vous demander de prouver que vous êtes bien la personne concernée. Nous répondons dans un délai d'**un mois**.

---

## 10. Mineurs

Le bot s'adresse aux utilisateurs qui ont l'âge minimum requis par Discord pour utiliser la plateforme. Nous ne cherchons pas à collecter sciemment des données de personnes n'ayant pas cet âge. Si vous pensez qu'une telle donnée nous a été transmise, contactez-nous pour la faire supprimer.

---

## 11. Modifications

Nous pouvons mettre à jour cette politique. La date de dernière mise à jour figure en haut du document. Les modifications importantes sont annoncées sur notre serveur de support. Continuer à utiliser le bot après une mise à jour vaut prise de connaissance de la nouvelle version.

---

## 12. Contact et réclamation

- **E-mail (données personnelles)** : [privacy@oxyde-bots.xyz](mailto:privacy@oxyde-bots.xyz)
- **Discord** : [serveur de support](https://discord.gg/uJC8QR9Yky)

Si vous estimez que vos droits ne sont pas respectés, vous pouvez introduire une réclamation auprès de l'autorité de protection des données de votre pays. En Belgique : l'[Autorité de protection des données](https://www.autoriteprotectiondonnees.be). En France : la [CNIL](https://www.cnil.fr).

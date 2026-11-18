## Politique de Confidentialité oxyde-bots.xyz

Dernière mise à jour : 18 Novembre 2026

Chez **Oxyde Groupe Bot's**, accessible à l'adresse [https://oxyde-bots.xyz](https://oxyde-bots.xyz), la confidentialité et la sécurité des données de nos utilisateurs sont nos priorités. Cette politique détaille quelles données sont collectées sur le site web, le dashboard et l'API, comment elles sont utilisées et sécurisées, et quels sont vos droits.

Le bot musical et son panel font l'objet d'une politique distincte. Les traitements propres au bot Discord OXYDE Protect (tickets, transcripts, captcha, signalements, e-mails d'alerte, musique) sont décrits dans la [Politique de Confidentialité du bot](https://docs.oxyde-bots.xyz/policy).

---

### 1. Responsables du traitement

Le site est édité par plusieurs personnes physiques, sans structure juridique propre à ce jour. Les obligations relatives aux traitements de données sont assumées par les personnes qui en déterminent effectivement les finalités et les moyens (voir la [politique du bot](https://docs.oxyde-bots.xyz/policy), section 1). Contact unique : **privacy@oxyde-bots.xyz**. Leur identité peut être communiquée aux autorités compétentes dans le cadre de leurs missions ; les demandes relatives à l'identité du responsable du traitement peuvent être adressées à ce contact (voir aussi les [Mentions légales](./legal.md)).

---

### 2. Données collectées

#### A. Données liées au Bot Discord et aux Serveurs
Pour que nos bots (Oxyde Protect, bots personnalisés) fonctionnent sur vos serveurs, nous stockons :
- **Identifiants Discord (IDs)** : serveurs (Guild IDs), salons (Channel IDs), rôles (Role IDs) et utilisateurs (User IDs).
- **Configurations et paramètres** : règles d'anti-raid, messages de bienvenue personnalisés, logs de modération, configurations de tickets et toutes les options définies depuis le dashboard.
- **Contenu des messages** : pour les fonctionnalités de sécurité (anti-spam, anti-lien, automod), le contenu des messages est analysé en temps réel (en mémoire) par le bot. Les messages ne sont **pas** stockés de manière persistante dans nos bases de données, à l'exception des logs de modération explicites activés par les administrateurs du serveur (système de logs, tickets de support). Le détail figure dans la politique du bot.

#### B. Données d'infrastructure et Reverse Proxy
Notre infrastructure (reverse proxy, pare-feux applicatifs) enregistre automatiquement des **journaux d'accès** lors de chaque requête vers nos services :
- **Données enregistrées** : adresse IP complète, horodatage, méthode HTTP, URL demandée, code de statut, temps de réponse, *User-Agent*.
- **Utilité** : analyse des performances, détection d'attaques (bruteforce, déni de service), débogage technique et limitation de taux (Rate Limiting).

#### C. Données d'authentification au Dashboard
- Lors de votre connexion via OAuth2, nous recevons de Discord : votre ID utilisateur, pseudonyme, avatar, adresse e-mail (si autorisée) et la liste de tous vos serveurs. Discord nous transmet toute la liste et ne permet pas de la filtrer avant l'envoi : le tri des serveurs que vous pouvez gérer est fait sur nos serveurs. Cette liste sert uniquement à ce tri et n'est pas conservée dans notre base de données.

#### D. Empreinte d'appareil (Fingerprinting) et Anti-Raid
- Uniquement sur la **page de vérification captcha** d'un serveur qui l'a activée, et **après votre acceptation explicite sur cette page**, nous collectons via *FingerprintJS* des données techniques sur votre appareil (empreinte du navigateur, fuseau horaire, capacités de rendu), ainsi que votre adresse IP et un identifiant d'appareil (cookie `_oxyde_tid`). Cela permet de différencier un utilisateur d'un bot malveillant et de repérer des comptes alternatifs lors d'un raid. Le détail, la base légale et les durées figurent dans la [politique du bot](https://docs.oxyde-bots.xyz/policy), section 2.3.

#### E. Données de support client
- Si vous utilisez le widget de chat en direct (Crisp), les informations que vous fournissez (e-mail, messages, fichiers joints) sont stockées pour le suivi de vos requêtes.

---

### 3. Cookies et stockage local

Nous n'utilisons **aucun cookie de ciblage publicitaire ni traceur comportemental** (pas de Google Analytics, ni Pixel Facebook).

- **Cookies de session sécurisés** : maintiennent votre connexion au dashboard (`session`, `session_player`) via un jeton chiffré (JWT). Leur durée de validité est de **7 jours**.
- **Cookie anti-CSRF** : `oauth_state`, temporaire, utilisé pendant la connexion pour prévenir les falsifications de requête.
- **Cookie de sécurité anti-raid** : `_oxyde_tid`, déposé uniquement sur la page de vérification captcha, après votre acceptation explicite, durée d'un an. Il identifie l'appareil lors de la vérification. Ce n'est pas un cookie strictement nécessaire à la fourniture du site : vous pouvez le supprimer à tout moment depuis votre navigateur.
- **Cookies Crisp** : maintiennent l'état de votre session de discussion avec notre support entre vos visites.

---

### 4. Finalités et bases légales

| Finalité | Base légale |
|---|---|
| Fournir le dashboard et maintenir votre session | Exécution du service demandé |
| Cybersécurité : bloquer les IP malveillantes, stopper les raids, limiter les abus d'API | Intérêt légitime |
| Captcha et détection de comptes alternatifs | Intérêt légitime, avec droit d'opposition |
| Améliorer nos outils (logs d'erreurs techniques) | Intérêt légitime |
| Support client | Intérêt légitime / exécution du service |

Nous **ne vendons aucune donnée** et ne les utilisons ni pour de la publicité, ni à des fins commerciales.

---

### 5. Outils tiers, hébergement et transferts hors UE

| Destinataire | Rôle | Pays |
|---|---|---|
| **UpCloud Oy** | Hébergement d'OXYDE Protect (bot et base de données) ; société établie en Finlande | États-Unis (hors UE) |
| **MIRIDIA SASU** | Hébergement du bot musical | France |
| **Infrastructure privée** (réseau Proximus) | Hébergement auto-géré | Belgique |
| **Base de données MongoDB** | Logiciel **auto-hébergé** sur notre infrastructure (OXYDE Protect : UpCloud, États-Unis) ; aucun service de MongoDB Inc. n'est utilisé. Non accessible depuis Internet, uniquement via un réseau privé (Tailscale). **Redis** (cache et rate-limiting) | Sur notre infrastructure |
| **Discord Inc.** | API du bot et authentification OAuth2 | États-Unis (hors UE) |
| **Cloudflare, Inc.** | Bouclier réseau et anti-DDoS ; peut traiter les adresses IP | États-Unis (hors UE) |
| **Crisp** | Chat de support | France / UE |
| **proxycheck.io** | Détection de VPN/proxy lors du captcha (adresse IP transmise) | Non précisé par nous : voir [leur politique](https://proxycheck.io/privacy/) |

Les serveurs d'OXYDE Protect étant hébergés aux États-Unis chez UpCloud, les transferts vers UpCloud, Discord Inc. et Cloudflare, Inc. reposent sur les mécanismes prévus par le chapitre V du RGPD (décision d'adéquation du cadre de protection des données UE–États-Unis pour les entreprises certifiées, ou clauses contractuelles types), tels que décrits dans leurs politiques : [Discord](https://discord.com/privacy), [Cloudflare](https://www.cloudflare.com/privacypolicy/), [Crisp](https://crisp.chat/fr/privacy/). Pour UpCloud, dont le contrat de traitement des données (DPA) est intégré à ses conditions, ils reposent, selon le pays, sur des clauses contractuelles types conclues entre les sociétés de son groupe ou sur une décision d'adéquation.

---

### 6. Durée de conservation des données

- **Configurations des serveurs** : conservées tant que le bot est présent sur votre serveur Discord, puis purgées automatiquement 90 jours après son retrait, ou immédiatement sur demande.
- **Logs du Reverse Proxy et d'infrastructure** : rotation automatique, 14 à 30 jours, sauf investigation liée à un incident de sécurité.
- **Logs de modération Discord** : selon les paramètres définis par les administrateurs du serveur.
- **Données captcha en base** : 30 jours.
- **Cookie `_oxyde_tid`** : expire après un an.
- **Support Crisp** : conservé le temps du suivi de votre demande, supprimable sur demande.

---

### 7. Sécurité des données

- **Chiffrement** : toutes les communications entre votre navigateur, Discord et nos serveurs sont chiffrées (HTTPS/TLS). Les jetons d'accès sont hachés ou signés cryptographiquement.
- **Architecture protégée** : nos bases de données ne sont pas exposées publiquement sur Internet. L'accès est réservé à notre réseau interne et protégé par un pare-feu.
- **Limitation de taux** : nos APIs utilisent Redis pour bloquer les requêtes abusives.

---

### 8. Vos droits

Conformément au RGPD, vous disposez des droits suivants :
- **Accès et portabilité** : accéder aux paramètres liés à votre compte via le dashboard.
- **Rectification et effacement** : demander la suppression de l'historique de votre serveur, de vos sessions web ou de vos conversations de support.
- **Opposition et limitation** : vous opposer à un traitement fondé sur notre intérêt légitime (par exemple le captcha) ou en demander la limitation.
- **Révocation d'accès** : à tout moment dans votre compte Discord (Paramètres > Applications autorisées).

Pour exercer ces droits ou pour toute question :
- Via le **widget de chat en direct** sur le site.
- Par e-mail à : **privacy@oxyde-bots.xyz**.

Nous répondons dans un délai d'un mois. Si vous estimez que vos droits ne sont pas respectés, vous pouvez introduire une réclamation auprès de l'[Autorité de protection des données](https://www.autoriteprotectiondonnees.be) (Belgique) ou de la [CNIL](https://www.cnil.fr) (France).

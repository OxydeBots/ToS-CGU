## Politique de Confidentialité oxyde-bots.xyz

Dernière mise à jour : 100 Août 2026

Chez **Oxyde Groupe Bot's**, accessible à l’adresse [https://oxyde-bots.xyz](https://oxyde-bots.xyz), la confidentialité et la sécurité des données de nos utilisateurs sont nos priorités absolues. Cette politique de confidentialité détaille de manière exhaustive quelles données sont collectées, comment elles sont utilisées, sécurisées, et quels sont vos droits lorsque vous utilisez notre écosystème (site web, dashboard, API et bots Discord).

---

### 1. Données collectées par nos Services

Nous collectons différents types de données selon que vous interagissez avec notre site web, notre panel de contrôle ou directement avec nos bots sur Discord.

#### A. Données liées au Bot Discord et aux Serveurs
Pour que nos bots (Oxyde Protect, bots musicaux, bots personnalisés) puissent fonctionner correctement sur vos serveurs, nous devons stocker certaines données :
- **Identifiants Discord (IDs)** : Identifiants uniques de serveurs (Guild IDs), de salons (Channel IDs), de rôles (Role IDs) et d'utilisateurs (User IDs).
- **Configurations et paramètres** : Les règles d'anti-raid, les messages de bienvenue personnalisés, les logs de modération, les configurations de tickets et toutes les options définies depuis le dashboard.
- **Contenu des messages** : Pour les fonctionnalités de sécurité (anti-spam, anti-lien, automod), le contenu des messages est analysé en temps réel (en mémoire) par le bot. Les messages ne sont **pas** stockés dans nos bases de données de manière persistante, à l'exception des logs de modération explicites activés par les administrateurs du serveur (système de logs, tickets de support).

#### B. Données d'infrastructure et Reverse Proxy
Afin de garantir la stabilité et la sécurité de notre réseau, notre infrastructure (qui inclut notre reverse proxy et nos pare-feux applicatifs) enregistre automatiquement des **journaux d'accès (logs)** lors de chaque requête vers nos services :
- **Données enregistrées** : Votre adresse IP complète, l'horodatage exact de la requête, la méthode HTTP (GET, POST, etc.), l'URL demandée, le code de statut de la réponse, le temps de réponse, ainsi que votre *User-Agent* (type de navigateur et système d'exploitation).
- **Utilité** : Ces logs d'infrastructure sont strictement utilisés pour l'analyse des performances, la détection d'attaques (bruteforce, déni de service), le débogage technique et l'application de limitations de taux (Rate Limiting).

#### C. Données d'authentification au Dashboard
- Lors de votre connexion au dashboard via OAuth2, nous recevons de Discord des informations de profil basiques : votre ID utilisateur, pseudonyme, avatar, adresse email (si autorisée) et la liste des serveurs où vous possédez les permissions nécessaires pour gérer les bots.

#### D. Empreinte d'appareil (Fingerprinting) et Anti-Raid
- Dans le cadre de notre système de vérification CAPTCHA et Anti-Raid, nous collectons des données techniques avancées sur votre appareil via *FingerprintJS* : empreinte unique du navigateur, fuseau horaire, et capacités de rendu. Cela permet de différencier un véritable utilisateur d'un bot malveillant.

#### E. Données de support client
- Si vous utilisez notre widget de chat en direct (Crisp), les informations que vous fournissez (email, messages, fichiers joints) sont stockées pour le suivi de vos requêtes.

---

### 2. Cookies et stockage local

Notre infrastructure utilise des cookies principalement pour des raisons de fonctionnalité et de sécurité. **Nous n'utilisons aucun cookie de ciblage publicitaire ni aucun traceur comportemental (pas de Google Analytics, ni Pixel Facebook).**

- **Cookies de session sécurisés** : Utilisés pour maintenir votre connexion au dashboard (`session`, `session_player`, etc.) en stockant un jeton crypté (JWT).
- **Cookies Anti-CSRF** : Un cookie temporaire (`oauth_state`) est utilisé pendant la phase de connexion pour prévenir les attaques par falsification de requête.
- **Cookies de sécurité (Anti-Raid)** : Un identifiant de suivi d'appareil (`_oxyde_tid`) est généré et stocké (durée de vie d'un an) pour identifier les appareils suspects ou mémoriser si vous avez déjà résolu un CAPTCHA avec succès.
- **Cookies Crisp** : Maintiennent l'état de votre session de discussion avec notre support client entre vos différentes visites.

---

### 3. Finalité et utilisation des données

Nous n'utilisons vos données que pour :
1. **Fournir nos services** : Appliquer les paramètres de modération sur vos serveurs Discord et rendre le dashboard fonctionnel.
2. **Assurer la cybersécurité** : Bloquer les adresses IP malveillantes via Cloudflare et notre Reverse Proxy, stopper les raids sur Discord, et limiter les abus d'API.
3. **Améliorer nos outils** : Analyser les erreurs techniques via nos logs pour déployer des correctifs.

---

### 4. Outils tiers et Partenaires

- **Hébergement et Bases de données** : Nos serveurs (incluant le Reverse Proxy, MongoDB pour les configurations, et Redis pour le cache/rate-limiting) sont hébergés sur des infrastructures robustes.
- **Discord** : Fournisseur de l'API permettant l'interaction du bot et l'authentification OAuth2.
- **Cloudflare** : Bouclier réseau situé en amont de nos serveurs. Il masque notre véritable infrastructure et peut traiter vos requêtes IP pour filtrer le trafic malveillant. (Voir la [politique de Cloudflare](https://www.cloudflare.com/privacypolicy/)).
- **Crisp** : Solution de support client intégrée au site. (Voir la [politique de Crisp](https://crisp.chat/fr/privacy/)).

---

### 5. Durée de conservation des données

- **Configurations des serveurs et profils** : Conservées tant que le bot est présent sur votre serveur Discord. Si le bot est expulsé, les données liées au serveur peuvent être automatiquement purgées après une période d'inactivité, ou immédiatement sur demande.
- **Logs du Reverse Proxy et d'infrastructure** : Conservés sur nos serveurs de manière rotative pour une durée limitée (généralement 14 à 30 jours) avant d'être définitivement effacés, sauf en cas d'investigation liée à un incident de sécurité.
- **Logs de modération Discord** : Conservés selon les paramètres définis par les administrateurs du serveur.
- **Cookies de sécurité** : L'identifiant `_oxyde_tid` expire techniquement après un an.

---

### 6. Sécurité des données

L'ensemble de l'écosystème Oxyde Bots repose sur des normes de sécurité strictes :
- **Chiffrement** : Toutes les communications entre votre navigateur, Discord et nos serveurs sont chiffrées (HTTPS/TLS). Les jetons d'accès (Tokens) sont hachés ou signés cryptographiquement.
- **Architecture protégée** : Nos bases de données ne sont pas exposées publiquement sur Internet. L'accès est strictement réservé à notre réseau interne et protégé par un pare-feu.
- **Limitation de taux (Rate Limiting)** : Nos APIs utilisent Redis pour bloquer les requêtes abusives et éviter la surcharge de l'infrastructure.

---

### 7. Vos droits

Conformément au Règlement Général sur la Protection des Données (RGPD) et aux réglementations applicables, vous disposez des droits suivants :
- **Droit d'accès et de portabilité** : Accéder aux paramètres liés à votre compte via le dashboard.
- **Droit de rectification et d'effacement (Droit à l'oubli)** : Demander la suppression totale de l'historique de votre serveur, de vos sessions web, ou de vos conversations de support. 
- **Révocation d'accès** : Vous pouvez à tout moment vous rendre dans les paramètres de votre compte Discord (Paramètres > Applications autorisées) pour révoquer l'accès de notre Dashboard à votre profil.

Pour exercer l'un de ces droits, obtenir une copie de vos données, ou pour toute question concernant cette politique, contactez-nous :
- Via le **widget de chat en direct** sur le site.
- Par e-mail à : **contact@oxyde-bots.xyz**.

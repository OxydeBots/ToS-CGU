## Mentions Légales

Dernière mise à jour : 10 Août 2026

Le présent document constitue les mentions légales du site **oxyde-bots.xyz** (ci-après « le Site »), conformément à la législation belge en vigueur et au Règlement Général sur la Protection des Données (RGPD — Règlement UE 2016/679).

---

### 1. Éditeur du site

Le Site est édité et exploité à titre **personnel et non commercial** par un particulier, sans forme juridique enregistrée (pas de société, pas d'auto-entreprise).

| Champ | Information |
|---|---|
| **Responsable de publication** | Administrateur d'Oxyde Bot's |
| **Site web** | https://oxyde-bots.xyz |
| **Contact e-mail** | contact@oxyde-bots.xyz |
| **Support Discord** | discord.gg/84fzyNYTpn |
| **Pays** | Belgique |

> Le site est exploité sur le réseau de l'opérateur **Proximus** depuis le domicile de l'éditeur. Il ne fait l'objet d'aucun enregistrement auprès d'un registre du commerce ou d'une chambre de métiers.

---

### 2. Hébergement

Le Site et ses services fonctionnent sur une infrastructure mixte :

#### A. Serveur VPS OXYDE Protect
- **Hetzner Online GmbH** — Industriestr. 25, 91710 Gunzenhausen, Allemagne
- Site : https://www.hetzner.com

#### B. Serveur VPS principal
- **MIRIDIA SASU** — 200 rue de la Croix-Nivert, 75015 Paris
- Site : https://miridiahost.fr/
  
#### C. Réseau & protection anti-DDoS
- **Cloudflare, Inc.** — 101 Townsend St, San Francisco, CA 94107, USA
- Site : https://www.cloudflare.com
- Cloudflare agit comme bouclier réseau en amont de nos serveurs et peut traiter les adresses IP des visiteurs pour filtrer le trafic malveillant.

#### D. Auto-hébergement partiel
- Serveurs physiques situés au **domicile de l'éditeur**, en Belgique, connectés via le réseau **Proximus PLC** (Boulevard du Roi Albert II 27, 1030 Bruxelles).

> Toutes les communications entre votre navigateur et nos serveurs sont chiffrées via **HTTPS/TLS**.

---

### 3. Propriété intellectuelle

L'ensemble des éléments du Site (textes, graphismes, logos, code source, structure) est la propriété exclusive de l'éditeur ou fait l'objet d'une autorisation d'utilisation.

- ✅ **Autorisé** : Consultation à titre personnel et non commercial.
- ❌ **Interdit** : Toute reproduction, copie ou diffusion sans autorisation écrite préalable.
- ❌ **Interdit** : Reverse engineering, décompilation ou désassemblage des bots et du dashboard.
- ℹ️ Les marques **Discord™**, **Cloudflare™**, **Hetzner™** restent la propriété de leurs détenteurs respectifs.

---

### 4. Limitation de responsabilité

Les services sont fournis **« en l'état »**, sans garantie d'aucune sorte. L'éditeur ne peut être tenu responsable :

- De toute **interruption de service** (maintenance, mise à jour, incident technique).
- De tout **dommage direct ou indirect** résultant de l'utilisation ou de l'impossibilité d'utiliser le Site.
- Du **contenu de sites tiers** accessibles via des liens présents sur le Site.
- Des configurations appliquées par les **administrateurs de serveurs Discord**, dont ils sont seuls responsables.

---

### 5. Liens hypertextes

Tout lien hypertexte pointant vers une page du Site est autorisé à condition de **ne pas utiliser de techniques de framing** et de ne pas laisser croire à un partenariat officiel avec l'éditeur sans accord préalable.

Le Site contient des liens vers des services tiers (Discord, Cloudflare, Hetzner, Crisp, AbuseIPDB…). L'éditeur n'exerce aucun contrôle sur ces services et décline toute responsabilité quant à leur contenu.

---

### 6. Données personnelles & RGPD

Le Site traite des données à caractère personnel conformément au **Règlement (UE) 2016/679** (RGPD) et à la **loi belge du 30 juillet 2018** relative à la protection des personnes physiques à l'égard des traitements de données.

#### Données collectées
- Identifiants Discord (Guild ID, User ID, Channel ID, Role ID)
- Configurations de serveurs (paramètres anti-raid, messages de bienvenue, logs…)
- Adresses IP et journaux d'accès (logs d'infrastructure)
- Données de session (jeton JWT chiffré)
- Empreinte de navigateur pour le système de captcha (FingerprintJS)

#### Finalité du traitement
- Fourniture des services de sécurité Discord
- Maintien de la session de connexion au dashboard
- Protection contre les attaques DDoS, raids et abus d'API

#### Durée de conservation
- **Configurations de serveurs** : durée de présence du bot sur le serveur, puis purge sur demande ou après inactivité.
- **Logs d'infrastructure** : 14 à 30 jours (rotation automatique).
- **Cookies de session** : durée de la session navigateur.
- **Cookie captcha `_oxyde_tid`** : 1 an.

#### Vos droits RGPD
Conformément au RGPD, vous disposez des droits suivants :
- **Droit d'accès** : consulter les données vous concernant.
- **Droit de rectification** : corriger des données inexactes.
- **Droit à l'effacement** (droit à l'oubli) : demander la suppression de vos données.
- **Droit d'opposition** : vous opposer au traitement de vos données.
- **Droit à la portabilité** : recevoir vos données dans un format structuré.
- **Révocation OAuth2** : révoquer à tout moment l'accès du dashboard via vos paramètres Discord (*Paramètres > Applications autorisées*).

Pour exercer ces droits :
- Via le **widget de chat en direct** sur le site.
- Par e-mail à : **privacy@oxyde-bots.xyz**.

> Pour toute information complémentaire, consultez notre [Politique de Confidentialité complète](./privacy-policy.md).

---

### 7. Cookies

Le Site utilise uniquement des cookies strictement nécessaires à son fonctionnement. **Aucun cookie publicitaire ni traceur comportemental** (Google Analytics, Meta Pixel, etc.) n'est utilisé.

| Cookie | Type | Durée | Finalité |
|---|---|---|---|
| `session` | Essentiel | Session | Connexion au dashboard (JWT chiffré) |
| `session_player` | Essentiel | Session | Session du panel musique |
| `oauth_state` | Sécurité | Temporaire | Protection anti-CSRF lors du login OAuth2 |
| `_oxyde_tid` | Captcha | 1 an | Identification de l'appareil pour le CAPTCHA |
| `crisp-*` | Tiers (Crisp) | Variable | Session du chat support |

---

### 8. Droit applicable & juridiction

Les présentes mentions légales sont régies par le **droit belge**.

En cas de litige, et à défaut de résolution amiable, les **tribunaux compétents de Belgique** seront seuls compétents.

En cas de litige relatif à la protection de vos données personnelles, vous disposez du droit d'introduire une réclamation auprès de l'autorité de contrôle belge :

**Autorité de Protection des Données (APD)**
Rue de la Presse 35 — 1000 Bruxelles, Belgique
https://www.autoriteprotectiondonnees.be

---

### 9. Contact

| Moyen | Coordonnées |
|---|---|
| **E-mail** | privacy@oxyde-bots.xyz |
| **Discord** | discord.gg/84fzyNYTpn |
| **Chat en direct** | Widget Crisp disponible sur le site |

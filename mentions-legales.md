## Mentions Légales

Dernière mise à jour : 18 Novembre 2026

Le présent document constitue les mentions légales du site **oxyde-bots.xyz** (ci-après « le Site »), conformément à la législation belge en vigueur et au Règlement Général sur la Protection des Données (RGPD — Règlement UE 2016/679).

---

### 1. Éditeur du site

Le Site est édité et exploité à titre **personnel et non commercial** par **plusieurs personnes physiques**, sans forme juridique enregistrée (pas de société, pas d'association, pas d'auto-entreprise).

| Champ | Information |
|---|---|
| **Responsables de publication** | Les administrateurs d'Oxyde Bot's |
| **Site web** | https://oxyde-bots.xyz |
| **Contact e-mail** | contact@oxyde-bots.xyz |
| **Contact données personnelles** | privacy@oxyde-bots.xyz |
| **Support Discord** | discord.gg/84fzyNYTpn |
| **Droit applicable** | Droit belge |

> Afin d'éviter l'exposition de personnes privées, les noms des éditeurs ne sont pas publiés. Leur identité peut être communiquée aux autorités compétentes dans le cadre de leurs missions ; les demandes relatives à l'identité des responsables peuvent être adressées à privacy@oxyde-bots.xyz.
>
> Une partie de l'infrastructure est exploitée sur le réseau de l'opérateur **Proximus**, sur une infrastructure privée en Belgique. Le Site ne fait l'objet d'aucun enregistrement auprès d'un registre du commerce ou d'une chambre de métiers.

---

### 2. Hébergement

Le Site et ses services fonctionnent sur une infrastructure mixte :

#### A. Serveurs OXYDE Protect
- **UpCloud Oy** — Aleksanterinkatu 15 B, 7th floor, 00100 Helsinki, Finlande (siège social). Les serveurs d'OXYDE Protect (bot et base de données) sont situés aux **États-Unis**.
- Site : https://upcloud.com

#### B. Serveur VPS du bot musical
- **MIRIDIA SASU** — 200 rue de la Croix-Nivert, 75015 Paris, France — hébergement du bot musical
- Site : https://miridiahost.fr/

#### C. Réseau & protection anti-DDoS
- **Cloudflare, Inc.** — 101 Townsend St, San Francisco, CA 94107, USA (hors UE)
- Site : https://www.cloudflare.com
- Cloudflare agit comme bouclier réseau en amont de nos serveurs et peut traiter les adresses IP des visiteurs pour filtrer le trafic malveillant.

#### D. Auto-hébergement partiel
- Serveurs physiques situés sur une **infrastructure privée**, en Belgique, connectés via le réseau **Proximus PLC** (Boulevard du Roi Albert II 27, 1030 Bruxelles).
- Notre base de données MongoDB est un logiciel **auto-hébergé** sur notre propre infrastructure (OXYDE Protect : UpCloud, États-Unis). Elle n'est pas accessible depuis Internet, uniquement via un réseau privé (Tailscale).

> Toutes les communications entre votre navigateur et nos serveurs sont chiffrées via **HTTPS/TLS**.

---

### 3. Propriété intellectuelle

L'ensemble des éléments du Site (textes, graphismes, logos, code source, structure) est la propriété exclusive de l'éditeur ou fait l'objet d'une autorisation d'utilisation.

- ✅ **Autorisé** : Consultation à titre personnel et non commercial.
- ❌ **Interdit** : Toute reproduction, copie ou diffusion sans autorisation écrite préalable.
- ❌ **Interdit** : Reverse engineering, décompilation ou désassemblage des bots et du dashboard.
- ℹ️ Les marques **Discord™** et **Cloudflare™** restent la propriété de leurs détenteurs respectifs.

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

Le Site contient des liens vers des services tiers (Discord, Cloudflare, Crisp, AbuseIPDB…). L'éditeur n'exerce aucun contrôle sur ces services et décline toute responsabilité quant à leur contenu.

---

### 6. Données personnelles & RGPD

Le Site traite des données à caractère personnel conformément au **Règlement (UE) 2016/679** (RGPD) et à la **loi belge du 30 juillet 2018** relative à la protection des personnes physiques à l'égard des traitements de données.

#### Données collectées
- Identifiants Discord (Guild ID, User ID, Channel ID, Role ID)
- Configurations de serveurs (paramètres anti-raid, messages de bienvenue, logs…)
- Adresses IP et journaux d'accès (logs d'infrastructure)
- Données de session (jeton JWT chiffré)
- Sur la page de vérification captcha uniquement : empreinte de navigateur (FingerprintJS), adresse IP et identifiant d'appareil (cookie `_oxyde_tid`)

#### Finalité du traitement
- Fourniture des services de sécurité Discord
- Maintien de la session de connexion au dashboard
- Protection contre les attaques DDoS, raids et abus d'API

#### Durée de conservation
- **Configurations de serveurs** : durée de présence du bot sur le serveur, puis purge automatique 90 jours après le retrait du bot, ou immédiatement sur demande.
- **Logs d'infrastructure** : 14 à 30 jours (rotation automatique).
- **Cookies de session** : 7 jours.
- **Données captcha en base** : 30 jours.
- **Cookie captcha `_oxyde_tid`** : 1 an.

#### Transferts hors UE
UpCloud (serveurs d'OXYDE Protect), Cloudflare, Inc. et Discord Inc. sont situés ou établis aux États-Unis. Le détail de ces transferts figure dans les politiques de confidentialité du site et du bot.

#### Vos droits RGPD
Conformément au RGPD, vous disposez des droits suivants :
- **Droit d'accès** : consulter les données vous concernant.
- **Droit de rectification** : corriger des données inexactes.
- **Droit à l'effacement** (droit à l'oubli) : demander la suppression de vos données.
- **Droit d'opposition et de limitation** : vous opposer au traitement de vos données ou en demander la limitation.
- **Droit à la portabilité** : recevoir vos données dans un format structuré.
- **Révocation OAuth2** : révoquer à tout moment l'accès du dashboard via vos paramètres Discord (*Paramètres > Applications autorisées*).

Pour exercer ces droits :
- Via le **widget de chat en direct** sur le site.
- Par e-mail à : **privacy@oxyde-bots.xyz**.

> Pour toute information complémentaire, consultez notre [Politique de Confidentialité du site](./privacy-policy.md) et la [Politique de Confidentialité du bot OXYDE Protect](https://docs.oxyde-bots.xyz/policy).

---

### 7. Cookies

Le Site utilise des cookies de session et de sécurité nécessaires à son fonctionnement, ainsi qu'un cookie de sécurité anti-raid (`_oxyde_tid`) déposé uniquement sur la page de vérification captcha, après acceptation explicite. **Aucun cookie publicitaire ni traceur comportemental** (Google Analytics, Meta Pixel, etc.) n'est utilisé.

| Cookie | Type | Durée | Finalité |
|---|---|---|---|
| `session` | Essentiel | 7 jours | Connexion au dashboard (JWT chiffré) |
| `session_player` | Essentiel | 7 jours | Session du panel musique |
| `oauth_state` | Sécurité | Temporaire | Protection anti-CSRF lors du login OAuth2 |
| `_oxyde_tid` | Sécurité anti-raid (non essentiel au sens strict) | 1 an | Identification de l'appareil lors de la vérification captcha, déposé après acceptation. Supprimable à tout moment depuis votre navigateur |
| `crisp-*` | Tiers (Crisp) | Variable | Session du chat support |

---

### 8. Droit applicable & juridiction

Les présentes mentions légales sont régies par le **droit belge**.

En cas de litige, et à défaut de résolution amiable, les **tribunaux compétents de Belgique** seront seuls compétents.

En cas de litige relatif à la protection de vos données personnelles, vous disposez du droit d'introduire une réclamation auprès de l'autorité de contrôle belge :

**Autorité de Protection des Données (APD)**
Rue de la Presse 35 — 1000 Bruxelles, Belgique
https://www.autoriteprotectiondonnees.be

(ou, si vous résidez en France, auprès de la **CNIL** : https://www.cnil.fr)

---

### 9. Contact

| Moyen | Coordonnées |
|---|---|
| **E-mail (général)** | contact@oxyde-bots.xyz |
| **E-mail (données personnelles)** | privacy@oxyde-bots.xyz |
| **Discord** | discord.gg/84fzyNYTpn |
| **Chat en direct** | Widget Crisp disponible sur le site |

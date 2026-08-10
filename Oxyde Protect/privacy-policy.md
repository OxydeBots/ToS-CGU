# Politique de Confidentialité - OXYDE Protect

**Dernière mise à jour : 10 Août 2026**

La confidentialité et la sécurité de vos données sont nos priorités absolues. Cette politique de confidentialité explique de manière transparente quelles données sont collectées par le bot Oxyde Protect, pourquoi nous les collectons, et comment nous les protégeons. Ce document concerne **exclusivement l'utilisation du bot sur Discord**.

## 1. Quelles données sont collectées par le bot ?

Pour que les systèmes de sécurité, d'anti-raid et de modération puissent fonctionner, le bot collecte et traite les informations suivantes :

- **Identifiants Discord (IDs)** : Les IDs uniques des serveurs (Guild IDs), des salons (Channel IDs), des rôles (Role IDs) et des utilisateurs (User IDs). Ces IDs sont nécessaires pour cibler les sanctions, gérer les permissions et appliquer les configurations.
- **Configurations de serveur** : Vos règles d'anti-raid personnalisées, vos messages de bienvenue, la configuration de vos systèmes de logs et de tickets, paramétrées via les commandes du bot.
- **Logs d'infraction et modération** : L'historique des infractions aux règles de votre serveur, les actions de modération effectuées par le bot ou votre équipe (kick, ban, mute), ainsi que des extraits de messages avec leur contexte (stockés uniquement dans les logs pour justifier une sanction).
- **Adresses Email (Optionnel)** : Si vous activez les alertes d'Anti-Raid par e-mail, votre adresse est collectée. Elle est chiffrée de manière sécurisée (AES-256-GCM) dans notre base de données.
- **Analyse des messages en temps réel** : Les messages envoyés sur votre serveur sont scannés **en mémoire** pour détecter le spam, les liens malveillants ou les mots interdits (Automod). **Le contenu de ces messages n'est pas sauvegardé de manière persistante**, à l'exception des cas où un message déclenche une infraction qui doit être loggée.

## 2. Comment utilisons-nous ces données ?

Les données collectées sont utilisées strictement pour faire fonctionner les services du bot :
- Sécuriser votre serveur contre les raids, le spam et les menaces.
- Fournir un historique de modération fiable aux administrateurs.
- Envoyer des notifications de sécurité par e-mail (via notre prestataire de confiance, Brevo).
- Améliorer l'efficacité de nos systèmes de détection d'attaques.

**Nous ne vendons aucune donnée à des tiers et nous n'utilisons aucune de vos données à des fins publicitaires ou commerciales.**

## 3. Stockage et Sécurité

Nous prenons la sécurité très au sérieux :
- Vos configurations et données sont stockées sur des bases de données sécurisées (MongoDB).
- Les données sensibles, telles que les adresses e-mail, sont hachées ou chiffrées cryptographiquement.
- L'accès à la base de données est restreint à l'équipe de développement. Aucun membre du support n'y a accès.

## 4. Durée de conservation des données

- **Configurations et profils** : Les données sont conservées tant que le bot est présent sur votre serveur.
- **Tickets de support** : Les données liées aux tickets fermés sont conservées afin de vous permettre de les consulter ultérieurement. 

## 5. Vos droits et contrôle de vos données

En tant qu'utilisateur et administrateur de serveur, vous gardez le contrôle total sur vos données :
- **Droit de suppression** : Vous pouvez à tout moment demander la purge complète des configurations, des logs ou de l'historique de votre serveur en nous contactant directement sur le serveur de support.
- **Contact** : Pour toute demande de suppression, d'accès à vos données, ou question concernant cette politique, veuillez ouvrir un ticket sur notre serveur de support officiel : [https://discord.gg/uJC8QR9Yky](https://discord.gg/uJC8QR9Yky)

# Politique de Confidentialité

*Dernière mise à jour : 15/08/2026*

Nous accordons une importance fondamentale au respect de la vie privée et à la protection des données à caractère personnel des utilisateurs de notre application mobile **AirTourer**.

La présente Politique de Confidentialité détaille la manière dont vos données sont traitées, conformément au Règlement Général sur la Protection des Données (RGPD - Règlement UE 2016/679), à la Loi Informatique et Libertés du 6 janvier 1978 modifiée, ainsi qu'aux directives de confidentialité des plateformes **Apple App Store** et **Google Play Store**.

---

## 1. Responsable du Traitement des Données

Le traitement des données personnelles dans le cadre de l'application est effectué sous la responsabilité de :

- **Éditeur / Développeur** : `AirTourer`
- **Localisation** : `Lille, France`
- **Email de contact / DPO** : `airtourer.app@gmail.com`

---

## 2. Traitement des Données de Géolocalisation & Requêtes Serveur (Traitement éphémère)

L'accès à la position géographique de votre appareil est encadré par des règles techniques et juridiques de confidentialité strictes et transparentes :

- **Traitement local en temps réel (RAM de l'appareil)** : Le suivi continu de votre position (affichage du point bleu sur la carte interactive, calculs de distance en direct pour le guidage pas-à-pas, boussole d'orientation) s'exécute exclusivement dans la mémoire vive (RAM) de votre smartphone.
- **Requêtes de recherche éphémères (HTTPS / TLS)** : Lorsque vous recherchez les points d'intérêt (POI) autour de vous ou que vous déplacez la carte, les coordonnées géographiques du centre de la zone visualisée et le rayon de recherche sont transmis de manière strictement éphémère via une connexion sécurisée et chiffrée (HTTPS / TLS) à notre base de données hébergée (**Supabase / PostgreSQL PostGIS**). Cette transmission a pour unique finalité d'interroger l'index spatial pour renvoyer la liste des monuments et audioguides correspondants.
- **Aucune conservation / Aucun historique / Suppression immédiate** : Ces coordonnées ne sont **JAMAIS enregistrées sur le serveur**, ni journalisées dans des fichiers de logs, ni associées à un compte utilisateur (aucun compte n'existe dans l'application), ni cédées ou revendues à des tiers. Dès que la requête SQL est exécutée et le résultat renvoyé, les coordonnées sont immédiatement supprimées de la mémoire serveur. Ce traitement répond pleinement à la définition d'un traitement « éphémère » (*ephemeral processing*) au sens de la fiche de sécurité des données Google Play (*Data Safety*).
- **Aucune localisation en arrière-plan** : L'application n'utilise pas et ne demande pas la permission d'accès à la position en arrière-plan (`ACCESS_BACKGROUND_LOCATION`). Dès que l'application est en arrière-plan ou fermée, toute lecture du signal GPS s'arrête immédiatement.
- **Contrôle et liberté de l'utilisateur** : Vous pouvez autoriser ou refuser l'accès à la position GPS lors du lancement de l'application ou à tout moment dans les réglages système de votre smartphone. Le refus de la géolocalisation n'empêche pas l'accès aux fiches des POI et aux audioguides.

---

## 3. Absence de Compte & Stockage Local Sécurisé (SecureStore)

AirTourer applique une approche stricte de protection de la vie privée dès la conception (*Privacy by Design*) :

- **Zéro inscription / Zéro compte requis** : Aucun compte utilisateur, email, identifiant ou mot de passe n'est demandé pour accéder aux fonctionnalités de l'application.
- **Stockage chiffré sur l'appareil (SecureStore)** : Les données d'état nécessaires au fonctionnement de l'application sont stockées exclusivement en local sur votre terminal dans un stockage sécurisé et chiffré (*SecureStore*). Ces données comprennent :
  - Le solde de jetons / crédits d'écoute audio gratuits ;
  - Les identifiants (IDs) des points d'intérêt (POI) débloqués ;
  - Vos préférences de langue (interface et audio).
- Ces données restent entièrement sur votre terminal et ne sont jamais transmises à des serveurs distants.

---

## 4. Publicité & Gestion du Consentement (Google AdMob & Google UMP)

L'application intègre un modèle de monétisation respectueux via des vidéos récompensées :

- **Annonces vidéo récompensées AdMob** : Les utilisateurs peuvent choisir de visionner une courte vidéo publicitaire fournie par Google AdMob afin d'obtenir **5 crédits d'écoute gratuits** par vidéo.
- **Consentement RGPD via Google UMP (CMP)** : Pour les utilisateurs situés dans l'Union Européenne (UE), le Royaume-Uni (UK) et l'Espace Économique Européen (EEE), le consentement est recueilli et géré via la plateforme **Google UMP (User Messaging Platform)**, une CMP certifiée conforme aux exigences du RGPD et au standard IAB TCF.
- **Modification et révocation à tout moment** : Vous pouvez à tout moment revoir, modifier ou révoquer vos choix de consentement publicitaire directement dans l'application depuis l'écran **« Paramètres » (Settings)**.

---

## 5. Lecture Audio en Arrière-plan (Foreground Service)

- **Autorisation `FOREGROUND_SERVICE_MEDIA_PLAYBACK`** : L'application utilise cette autorisation Android strictement pour la lecture multimédia.
- **Finalité** : Permettre aux utilisateurs de continuer à écouter leurs guides audio lorsque l'écran de leur smartphone est éteint/verrouillé ou lorsque l'application est réduite en arrière-plan pendant la visite.
- Ce service d'avant-plan ne réalise aucun traçage GPS ni aucune collecte de données personnelles.

---

## 6. Destinataires et Sous-traitants

Vos données personnelles ne sont **jamais vendues, louées ou cédées** à des tiers à des fins commerciales.

Les prestataires techniques intervenant pour le fonctionnement du service sont :
- **Supabase Inc.** : Pour l'hébergement de la base de données (PostgreSQL / PostGIS) distribuant le catalogue des points d'intérêt et traitant de manière éphémère les requêtes spatiales de recherche de POI via HTTPS/TLS.
- **Google Ireland Limited** : Pour la diffusion des publicités vidéo récompensées (Google AdMob) et la gestion du consentement réglementaire (Google UMP).
- **GitHub Pages** (GitHub, Inc.) : Pour l'hébergement du site statique d'information légale.

---

## 7. Durée de Conservation des Données

- **Données de géolocalisation & requêtes de recherche de POI** : **0 seconde** (traitement en temps réel volatil en mémoire RAM sur le smartphone et traitement éphémère en mémoire vive sur le serveur PostgreSQL uniquement pendant l'exécution de la requête spatiale ; aucune conservation sur disque, aucun historique, aucune journalisation).
- **Données locales (SecureStore)** : Conservées sur votre appareil jusqu'à la réinitialisation des données de l'application ou sa désinstallation.

---

## 8. Vos Droits (Conformité RGPD)

Conformément à la réglementation européenne sur la protection des données, vous disposez des droits suivants :

- **Droit d'accès et d'information** (Art. 15 RGPD) : Connaître les traitements appliqués.
- **Droit à l'effacement** (Art. 17 RGPD) : Supprimer définitivement vos données locales par simple réinitialisation ou désinstallation de l'application.
- **Droit de retrait du consentement** (Art. 21 RGPD) : Modifier vos préférences GPS dans les réglages système de votre téléphone et vos choix de consentement publicitaire dans l'écran Paramètres de l'application.

### Exercer vos droits
Pour toute question ou demande concernant vos données personnelles :  
👉 **`airtourer.app@gmail.com`**

Délai légal de réponse maximal : **30 jours**.

Si vous estimez que vos droits n'ont pas été respectés, vous pouvez déposer une réclamation auprès de l'autorité compétente :  
**CNIL (Commission Nationale de l'Informatique et des Libertés)**  
Site internet : [https://www.cnil.fr](https://www.cnil.fr)

---

## 9. Conformité aux Guides des Stores (Apple App Store & Google Play Store)

Cette Politique de Confidentialité répond intégralement aux exigences des magasins d'applications :
- **Apple App Store Privacy Guidelines** : Usage transparent du GPS en direct sans tracking IDFA, absence de profilage, respect strict de la vie privée.
- **Google Play User Data Policy** : Déclaration transparente de la localisation éphémère (*Ephemeral Processing* sans stockage ni journalisation dans la section Sécurité des données / *Data Safety*), déclaration de la permission *Foreground Service Media Playback*, conformité Google UMP / CMP pour la publicité, absence de géolocalisation en arrière-plan (`ACCESS_BACKGROUND_LOCATION`).

---

## 10. Modifications de la Politique

Nous nous réservons le droit de mettre à jour la présente Politique de Confidentialité pour refléter l'évolution des réglementations ou des fonctionnalités de l'application. La date de dernière mise à jour sera ajustée en conséquence.

# AirTourer - Site de Mentions Légales, Politique de Confidentialité & Transparence IA

Ce dépôt contient le site web vitrine statique et les documents juridiques et réglementaires (conformes RGPD, Google Play Data Safety, Apple App Store, AI Act UE 2024/1689 et Google UMP CMP) pour l'application mobile **AirTourer** (v1.0.28 / Build 29).

---

## 📁 Structure du projet

- **`index.html`** : Site web responsive hébergé sur GitHub Pages avec navigation par onglets, basculement mode sombre/clair, boutons d'impression et copie Markdown instantanée pour Notion / Google Play Console / App Store.
- **`MENTIONS_LEGALES.md`** : Mentions Légales complètes au format Markdown (Éditeur, GitHub Pages, base de données Supabase / PostgreSQL PostGIS, Google AdMob/UMP et conformité AI Act).
- **`POLITIQUE_DE_CONFIDENTIALITE.md`** : Politique de Confidentialité complète détaillant :
  - **Géolocalisation éphémère** : Suivi local en mémoire vive (RAM), requêtes de recherche de POI et circuits sécurisées (HTTPS/TLS) vers Supabase PostgreSQL PostGIS sans aucune conservation ni journalisation (0 seconde), aucune localisation en arrière-plan (`ACCESS_BACKGROUND_LOCATION` non demandée).
  - **Zéro compte & Stockage local sécurisé** : Aucun compte requis, stockage chiffré sur l'appareil (*SecureStore*) pour le solde de jetons d'écoute, les POIs débloqués, les badges d'exploration et les préférences de langue.
  - **Transparence IA & AI Act (UE 2024/1689)** : Information claire sur les descriptifs et voix synthétiques assistés par IA, avec bouton de signalement d'erreurs sur chaque lieu et traitement anonyme des retours.
  - **Parcours guidés & Gamification** : Découverte d'itinéraires pas-à-pas et système de badges récompensant l'exploration du patrimoine.
  - **Publicité & Consentement** : Vidéos récompensées AdMob (5 crédits par vidéo), fichier de transparence officiel `app-ads.txt` et gestion du consentement RGPD via Google UMP CMP.
  - **Lecture audio en arrière-plan** : Service d'avant-plan `FOREGROUND_SERVICE_MEDIA_PLAYBACK` strictement réservé à la lecture multimédia.
- **`app-ads.txt`** : Fichier IAB certifiant la propriété du compte Google AdMob (`google.com, pub-7121802546087832, DIRECT, f08c47fec0942fa0`).

---

## 📬 Contact & Support
- **Éditeur** : AirTourer
- **Email officiel** : `airtourer.app@gmail.com`
- **URL officielle** : [https://riff4.github.io](https://riff4.github.io)

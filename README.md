# AirTourer - Site de Mentions Légales & Politique de Confidentialité

Ce dépôt contient le site web statique et les documents juridiques (conformes RGPD, Google Play Data Safety, Apple App Store et Google UMP CMP) pour l'application mobile **AirTourer**.

---

## 📁 Structure du projet

- **`index.html`** : Site web responsive hébergeable sur GitHub Pages avec navigation par onglets, basculement mode sombre/clair, boutons d'impression et copie Markdown instantanée.
- **`MENTIONS_LEGALES.md`** : Mentions Légales complètes au format Markdown (Éditeur, GitHub Pages, base de données Supabase / PostgreSQL PostGIS, Google AdMob/UMP).
- **`POLITIQUE_DE_CONFIDENTIALITE.md`** : Politique de Confidentialité complète détaillant :
  - **Géolocalisation éphémère** : Suivi local en mémoire vive (RAM), requêtes de recherche de POI sécurisées (HTTPS/TLS) vers Supabase PostgreSQL PostGIS sans aucune conservation ni journalisation (0 seconde), aucune localisation en arrière-plan (`ACCESS_BACKGROUND_LOCATION` non utilisée).
  - **Zéro compte & Stockage local sécurisé** : Aucun compte requis, stockage chiffré sur l'appareil (*SecureStore*) pour le solde de jetons d'écoute, les POIs débloqués et les préférences de langue.
  - **Publicité & Consentement** : Vidéos récompensées AdMob (5 crédits par vidéo) et gestion du consentement RGPD via Google UMP CMP (modifiable à tout moment dans les Paramètres).
  - **Lecture audio en arrière-plan** : Service d'avant-plan `FOREGROUND_SERVICE_MEDIA_PLAYBACK` strictement réservé à la lecture multimédia.

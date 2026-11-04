# TIA COFFRE

Coffre numérique pour vos documents administratifs (carte d'identité, extrait de naissance, diplômes…).

- Interface « Portefeuille » : documents empilés comme des cartes de wallet
- Scan : photo → détection des bords → redressement automatique (réglable avec 4 points)
- Amélioration « IA » 100 % hors ligne : suppression des ombres, balance des blancs, couleurs justes, netteté
  (modes Auto / Document / Couleur fidèle / N&B / Original, comparaison avant/après)
- Recto + verso en un seul ajout (guidé)
- Documents regroupés par catégorie, navigation par slides (glisser gauche/droite)
- Paramètres : code, empreinte digitale, verrouillage auto, thème, mode d'amélioration, import/sauvegarde/restauration
- Agrandissement plein écran (pincer, glisser, double-toucher)
- Partage en image JPEG ou en PDF
- Suppression avec confirmation
- Code de verrouillage à 4 chiffres (optionnel)
- Données stockées uniquement sur le téléphone

## Compiler l'APK sur GitHub

1. Créez un dépôt GitHub (ex. `tia-coffre`) et envoyez-y **tout le contenu de ce dossier**
   (y compris le dossier `.github`).
2. Onglet **Actions** → workflow **Build TIA COFFRE APK** (il démarre à chaque push ; ou « Run workflow »).
3. À la fin (~5 min), ouvrez l'exécution → section **Artifacts** → téléchargez **TIA-COFFRE-APK** (`TIA-COFFRE.apk`).
4. Copiez l'APK sur le téléphone et installez-le (autoriser les sources inconnues).

Release automatique : `git tag v1.0.0 && git push origin v1.0.0` → l'APK est joint à la release GitHub.

## Mise à jour sans perdre ses documents

- `signing/debug.keystore` est une **clé de signature fixe** : toutes les versions compilées à partir de ce dépôt
  portent la même signature, donc Android les installe *par-dessus* la précédente en gardant les données.
  **Ne supprimez pas ce fichier** (et gardez le dépôt privé).
- L'identifiant de l'application est `com.tiacoffre.app`. La toute première version (signée avec une clé temporaire)
  ne peut pas être mise à jour : installez celle-ci à côté, transférez vos documents (Paramètres → Importer des photos),
  puis désinstallez l'ancienne.
- Pensez à **Paramètres → Sauvegarder mes documents** de temps en temps.

## Structure

- `www/index.html` : toute l'application (interface + moteur d'amélioration)
- `assets/icon-only.png`, `icon-foreground.png`, `icon-background.png` : icône de l’application (monogramme TIA orange)
- `.github/workflows/build-apk.yml` : compilation (Capacitor + Gradle)

© 2026 TIA COFFRE — Tous droits réservés.

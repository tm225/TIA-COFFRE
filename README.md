# TIA COFFRE

Coffre numérique pour vos documents administratifs (carte d'identité, extrait de naissance, diplômes…).

- Interface « Portefeuille » : documents empilés comme des cartes de wallet
- Scan : photo → détection des bords → redressement automatique (réglable avec 4 points)
- Amélioration « IA » 100 % hors ligne : suppression des ombres, balance des blancs, couleurs justes, netteté
  (modes Auto / Document / Couleur fidèle / N&B / Original, comparaison avant/après)
- Recto + verso, numéros associés à chaque face (copie d'un simple toucher)
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

## Structure

- `www/index.html` : toute l'application (interface + moteur d'amélioration)
- `assets/icon-only.png` : icône de l'application
- `.github/workflows/build-apk.yml` : compilation (Capacitor + Gradle)

© 2026 TIA COFFRE — Tous droits réservés.

# Auto-évaluation des MSP — dispositif NeuroParcours

Formulaire en ligne d'auto-évaluation des Maisons de Santé Pluriprofessionnelles engagées dans le dispositif **NeuroParcours** (troubles du neurodéveloppement), porté par la **FEMAS Hauts-de-France** avec le soutien de l'ARS Hauts-de-France.

**Accès :** https://femashdf.github.io/Autoevaluation-NeuroParcours/

## Fonctionnement
- 11 critères répartis en 3 axes (Pilotage et engagement · Formation et sensibilisation · Actions de prévention et communication), notés de 0 à 3.
- Calcul automatique du score /33 et du niveau : 0–13 initial (Bronze), 14–29 intermédiaire (Argent), 30+ avancé (Or).
- Points forts, axes d'amélioration et 3 priorités du plan d'action générés automatiquement.
- Indicateurs d'impact : enfants repérés, orientations, satisfaction des familles.
- Sauvegarde automatique dans le navigateur, sauvegarde/reprise par fichier, export Word et PDF, envoi à la FEMAS.

## Configuration de l'envoi
Dans `index.html`, bloc `const FEMAS = {...}` :
- `submitUrl` vide → le bouton « Envoyer à la FEMAS » télécharge la synthèse Word et ouvre un e-mail pré-rempli vers `contactEmail`.
- `submitUrl` = `https://submit.jotform.com/submit/<ID_DU_FORMULAIRE>/` + noms techniques des champs dans `fields` → envoi direct dans Jotform FEMAS+.

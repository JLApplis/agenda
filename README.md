# 📅 Monagenda

**Monagenda — agenda personnel** : vues Mois (défilement continu) et Liste, événements répétés, rappels, catégories colorées, impression. Synchronisé entre le téléphone et l'ordinateur. Remplace Google Agenda.

**[▶️ Ouvrir l'appli](https://jlapplis.github.io/monagenda/)**

![Licence](https://img.shields.io/badge/licence-GPL_v3-blue)

## Fonctionnement

- Connexion par e-mail et mot de passe (Firebase Authentication) — même compte et même projet Firebase que [Courses](https://jlapplis.github.io/courses/).
- Données stockées dans Firebase Firestore sous `users/{uid}/agenda_…` ; chaque compte ne voit que ses propres données (règles communes avec Courses, voir `firestore.rules`).
- Un document par année (`agenda_annees/{AAAA}`) : peu de lectures à chaque ouverture.
- Fonctionne aussi sans réseau : les changements sont envoyés au retour de la connexion.
- Rappels : affichés quand l'agenda est ouvert (pas de serveur d'envoi).
- Sauvegarde / restauration en fichier JSON (menu ▸ Sauvegarde).
- Sur Android : Chrome ▸ ⋮ ▸ « Ajouter à l'écran d'accueil » pour l'ouvrir comme une appli.

## Licence

© 2026 Jluc — JLApplis. Distribué sous licence **GNU GPL v3** (voir `LICENSE.txt`).

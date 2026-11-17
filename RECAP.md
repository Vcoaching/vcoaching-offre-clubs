# Récap du projet — Page vitrine « Offre clubs » VESTIAIRES coaching

État au 17 novembre 2026. À lire pour reprendre le projet sur un nouvel ordinateur ou dans une nouvelle conversation.

## Où est quoi

| Élément | Emplacement |
|---|---|
| Code (page unique) | `index.html` — HTML, CSS et JS dans un seul fichier, seule dépendance : Google Fonts (Roboto, Roboto Condensed) |
| Visuels | `assets/` (logos, photos, poster VESTIAIRES LIVE) |
| Dépôt GitHub | https://github.com/Vcoaching/vcoaching-offre-clubs (public, branche `main`) |
| Page en ligne | https://vcoaching.github.io/vcoaching-offre-clubs/ (GitHub Pages, mise à jour 1–2 min après chaque `git push`) |
| Miroir Cloudflare | https://clubs-vcoaching.pages.dev/ (Cloudflare Pages relié au dépôt, se met à jour tout seul) |
| Aperçu local | `python3 -m http.server 8770` dans le dossier, puis http://localhost:8770 |

## Ce que contient la page (de haut en bas)

1. **En-tête plein écran** — ornement 3 barres rouges, titre « Faites grandir / tout votre / club » + « avec » logo VESTIAIRES coaching, texte d'intro, boutons « Découvrir l'offre » et « Échanger 30 min en visio », prix « 990 € / an (paiement en une fois) ou 99 € / mois (engagement 12 mois) ». Le premier écran s'arrête sous les prix sur tous les formats ; agrandi automatiquement sur les très grands écrans.
2. **4 tuiles de résumé** à icônes rouges (V, micro, presse-papier, mégaphone).
3. **Menus** : menu latéral à ancres en desktop (apparaît après les tuiles) ; barre fixe en bas sur mobile (4 onglets icône + mot).
4. **Accès vcoaching** — « Un accès illimité à vcoaching pour tous vos éducateurs », pastilles (100 éducateurs max, accès illimité, web & mobile), carte VESTIAIRES LIVE (photo studio, vidéo à venir), « Nos contenus phares » : carrousel de 4 vidéos YouTube (Tableaux noirs, Conférences, Exo de…, Sur la route de l'entraînement) avec défilement auto toutes les 2 s, flèches, glissement tactile, pause pendant la lecture ; bandeau « 7 jours d'essai gratuit ».
5. **Conférence** — « Une conférence thématisée pour vos coachs », photo de causerie fournie, mention en italique visio / présentiel (frais de déplacement à la charge du club), infos Durée 2 h / Format visio ou présentiel / Date à définir, 2 thèmes au choix (gestion des parents, causerie).
6. **Consulting** — « Une demi-journée de conseil offerte », photo club-house fournie, 3 étapes : Travail préalable (enquête & résultats), Analyse de l'existant (échanges téléphoniques avec 2 membres), Livrable final (document de recommandations).
7. **Communication** — « Le club mis en avant sur vcoaching », 2 contenus consacrés au club sur la durée de l'abonnement, photo de tournage fournie, icônes réseaux, formats par canal (Plateforme / Newsletter / Réseaux sociaux), mention éditoriale.
8. **Tarifs** — annuel 990 € / mensuel 99 €, liste de ce qui est inclus.
9. **Rendez-vous** — « Parlons de votre club », calendrier de réservation (voir plus bas).

Charte : fond noir, rouge #E00815, dégradé #A30C14 → #E20714, pas de Rockwell.

## Ce qui reste à faire

| Sujet | Détail | Où le brancher |
|---|---|---|
| **Réservation de RDV** | Le calendrier affiché est un **aperçu non fonctionnel** (mardis 14 h–17 h, créneaux de 30 min). En attente du passage de Ionos à Google Workspace, puis création d'un **agenda de réservation Google** (mardi 14:00–17:00, 30 min, Google Meet, agenda vérifié pour les disponibilités, champ « Nom du club »). | Coller le lien de la page de réservation dans `data-booking="…"` sur `<div id="booking">` : le vrai module Google remplace alors l'aperçu automatiquement. |
| Vidéo VESTIAIRES LIVE | Photo studio en attendant le 1er épisode. | `data-youtube="ID"` sur la carte VESTIAIRES LIVE (vidéo YouTube **non répertoriée**, pas privée). |
| Lien « Essai gratuit » | Pointe vers https://www.vcoaching.com | Bouton du bandeau 7 jours. |
| Réseaux sociaux | Instagram, Facebook, LinkedIn, YouTube affichés — à ajuster selon les comptes actifs. | Bloc Communication. |
| Photo de l'en-tête | Photo Unsplash provisoire (`assets/photo-hero.jpg`). | `data-img` du bloc `.ph` de l'en-tête. |
| Mentions « TTC » | Encore présentes dans le bloc Tarifs, le pied de page et sous le bouton « Prendre RDV » du menu latéral (« À partir de 82,50 € TTC / mois »). | À retirer si souhaité. |
| Option | Ne pas faire indexer la page par Google (balise `noindex`), domaine perso (ex. clubs.vcoaching.com via un CNAME chez Cloudflare). | — |

## Reprendre le travail sur un nouvel ordinateur

1. Avoir le dossier `vcoaching-offre-clubs` (avec son dossier caché `.git`) — ou le récupérer : `gh repo clone Vcoaching/vcoaching-offre-clubs`.
2. Être connecté à GitHub : `gh auth login` (compte **Vcoaching**).
3. Modifier `index.html`, vérifier en local, puis `git add -A && git commit -m "…" && git push` : les deux sites se mettent à jour.

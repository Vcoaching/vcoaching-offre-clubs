# Offre Clubs — VESTIAIRES coaching

Page vitrine unique : `index.html` (HTML/CSS/JS autonomes, aucune dépendance hors Google Fonts).

## Aperçu local

```bash
python3 -m http.server 8770
```
puis ouvrir http://localhost:8770

## Intégrer une vidéo (bloc 01 — contenus phares)

Chaque encart vidéo est un `<div class="video" …>`. Renseigner **un** des attributs :

| Attribut | Effet |
|---|---|
| `data-youtube="ID"` | Lecteur YouTube au clic (miniature récupérée automatiquement) |
| `data-vimeo="ID"` | Lecteur Vimeo au clic |
| `data-src="assets/video.mp4"` | Vidéo hébergée avec la page |
| `data-poster="assets/miniature.jpg"` | Miniature personnalisée (optionnel) |

## Intégrer une photo

Ajouter `data-img="assets/ma-photo.jpg"` (et `data-alt="description"`) sur le bloc `.ph` correspondant.
Le visuel d'attente (terrain stylisé) disparaît automatiquement.

| `data-photo` | Emplacement | Format conseillé |
|---|---|---|
| `hero` | En-tête | 4:5 portrait |
| `intervention` | Bloc 02 | 4:5 portrait |
| `consulting` | Bloc 03 | 4:5 portrait |
| `tournage` | Bloc 04 | 21:9 panoramique |

## Prompts pour générer les photos IA

Style commun à ajouter à chaque prompt : *photographie éditoriale sportive, lumière dramatique, tons sombres avec accents rouges (#E00815), grain léger, profondeur de champ réduite, réaliste, pas de texte ni de logo.*

- **hero** — « Un éducateur de football amateur accroupi face à un groupe de jeunes joueurs (U13) en cercle sur un terrain synthétique, le soir sous les projecteurs, il leur parle avec énergie, vue de trois-quarts, format portrait 4:5. »
- **intervention** — « Un intervenant debout devant une dizaine d'éducateurs de football assis dans le club-house d'un club amateur, écran avec un schéma tactique derrière lui, ambiance chaleureuse et studieuse, format portrait 4:5. »
- **consulting** — « Trois dirigeants de club de football amateur autour d'une table, ordinateur portable, documents et paperboard couvert de post-it, maillots du club accrochés au mur, lumière de fin de journée, format portrait 4:5. »
- **tournage** — « Tournage vidéo sur un terrain de football : un cadreur avec caméra sur l'épaule filme un éducateur qui anime un exercice avec des plots et des jeunes joueurs, perche micro visible, format panoramique 21:9. »

## Liens à compléter (`TODO` dans le code)

- Bouton **Essai gratuit** (bloc 01) → actuellement `https://www.vcoaching.com`
- Calendrier de **réservation** (bloc 06) → renseigner `data-booking="…"` sur `<div id="booking">` avec le lien de l'agenda de réservation Google (mardis 14h–17h, 30 min, Google Meet). Tant qu'il est vide, un aperçu non fonctionnel est affiché.
- Icônes réseaux sociaux (bloc 04) : Instagram, Facebook, LinkedIn, YouTube — à ajuster selon les comptes actifs.

## Photos provisoires (Unsplash, licence gratuite)

| Emplacement | Fichier | Source |
|---|---|---|
| hero | `assets/photo-hero.jpg` | https://unsplash.com/photos/LIhB1_mAGhY |
| conférence | `assets/photo-conference.webp` | Visuel fourni par VESTIAIRES coaching |
| consulting | `assets/photo-consulting.jpg` | images.unsplash.com/photo-1603202662747-00e33e7d1468 |
| tournage | `assets/photo-tournage.webp` | Visuel fourni par VESTIAIRES coaching |

Pour remplacer une photo : changer `data-img` sur le bloc `.ph` correspondant (`data-pos` règle le cadrage).
